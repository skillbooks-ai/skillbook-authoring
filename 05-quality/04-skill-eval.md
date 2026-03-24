# Skill Eval — Proving Your Skillbook's Value

A Skill Eval is an automated A/B test that measures the difference your skillbook makes. Same model, same questions, one variable: access to your skillbook. The result is a structured report that proves value to operators deciding whether to add your book to their agents.

## File Layout

Eval artifacts live in an `eval/` directory at the root of your skillbook:

```
my-book/
├── SKILL.md
├── README.md
├── package.json
├── eval/                          ← eval results directory
│   ├── EVAL.md                    ← human/agent-readable report (served free)
│   ├── eval-report.json           ← machine-readable report
│   └── raw/                       ← raw model responses (optional, not served)
│       ├── sonnet-baseline.json
│       ├── sonnet-skillbook.json
│       ├── gemini-baseline.json
│       └── gemini-skillbook.json
├── 01-section/
│   └── ...
```

### What's served vs. what's stored

- `eval/EVAL.md` — **served free** (like SKILL.md). Agents and humans can read the eval report without authentication. This is your proof of value.
- `eval/eval-report.json` — **served free**. Machine-readable version for programmatic access (dashboards, catalog listings, comparison tools).
- `eval/raw/` — **not served**. Raw model responses are stored locally for auditability and re-scoring but are not published to the platform. Keep them in git.

## EVAL.md Structure

The eval report follows a standard structure so agents and humans can parse it consistently:

```markdown
# Skill Eval Report

**Book:** EPA 608 Certification
**Version:** 2.0.0
**Eval Date:** 2026-03-22
**Questions:** 15
**Archetype:** Reference

## Models Tested

| Model | Provider |
|-------|----------|
| Claude Sonnet 4 | Anthropic |
| Gemini 3.1 Pro | Google |

## Results

| Condition | Model | Mean Accuracy (0-3) | Perfect Answers | Confident-Wrong |
|-----------|-------|---------------------|-----------------|-----------------|
| Baseline | Sonnet | 1.93 | 53% | 20% |
| Baseline | Gemini | 1.60 | 40% | 33% |
| Skillbook | Sonnet | 3.00 | 100% | 0% |
| Skillbook | Gemini | 3.00 | 100% | 0% |

## Key Findings

[Narrative summary of the most significant gaps and improvements]

## Per-Question Breakdown

[Table or list showing each question, category, and scores by condition]

## Methodology

Questions designed per the Skill Eval methodology (Reference archetype).
Scoring: Accuracy 0-3 scale, Citation Quality 0-2 scale.
See: https://skillbooks.ai/building-skillbooks/11-skill-eval/
```

### Required fields

- Book name, version, eval date
- At least one model tested
- Results table with baseline vs. skillbook conditions
- Mean accuracy and perfect answer rate per condition

### Optional but recommended

- Multiple models (strengthens the evidence)
- Key findings narrative (more persuasive than raw numbers)
- Per-question breakdown (transparency)
- Web search as a third condition (shows skillbook vs. free alternatives)

## eval-report.json Schema

```json
{
  "book": "epa-608",
  "version": "2.0.0",
  "evalDate": "2026-03-22",
  "archetype": "reference",
  "questionCount": 15,
  "models": [
    {
      "id": "anthropic/claude-sonnet-4-6",
      "label": "Sonnet",
      "baseline": {
        "meanAccuracy": 1.93,
        "perfectRate": 0.53,
        "confidentWrongRate": 0.20
      },
      "skillbook": {
        "meanAccuracy": 3.0,
        "perfectRate": 1.0,
        "confidentWrongRate": 0.0,
        "citationRate": 1.0
      },
      "delta": 1.07
    }
  ],
  "questions": [
    {
      "id": "epa608-001",
      "category": "factual-recall",
      "question": "...",
      "groundTruth": "...",
      "sourcePages": ["05-type-ii/02-recovery-evacuation-levels.md"],
      "scores": {
        "anthropic/claude-sonnet-4-6": {
          "baseline": {"accuracy": 3, "confidence": "high"},
          "skillbook": {"accuracy": 3, "citation": 2, "confidence": "high"}
        }
      }
    }
  ]
}
```

## Raw Results Files

Each raw file stores one model × one condition. Structure:

```json
{
  "model": "anthropic/claude-sonnet-4-6",
  "condition": "baseline",
  "timestamp": "2026-03-22T22:00:00Z",
  "answers": [
    {
      "id": "epa608-001",
      "answer": "The full text of the model's response...",
      "confidence": "high",
      "citations": ["05-type-ii/02-recovery-evacuation-levels.md"]
    }
  ]
}
```

- `citations` field only present for skillbook condition
- `confidence` is the model's self-reported confidence (high/medium/low)
- Raw files preserve the exact model output for re-scoring or auditing

## Promoting to README

The eval report lives in `eval/` by default — separate from the README. Authors who want to highlight their results can add a summary section to their README:

```markdown
## Skill Eval

Tested against Claude Sonnet 4 and Gemini 3.1 Pro (March 2026):
- **Baseline accuracy:** 1.6–1.9/3.0 (training knowledge only)
- **With skillbook:** 3.0/3.0 (100% perfect answers)
- **Citation rate:** 100% of answers cite specific pages
- Full report: [eval/EVAL.md](eval/EVAL.md)
```

This is optional. The `eval/EVAL.md` is discoverable by agents through the SKILL.md TOC or by convention (always at `eval/EVAL.md`).

## Validation

`skillbook validate` checks:
- If `eval/` exists, `EVAL.md` and `eval-report.json` must both be present
- `eval-report.json` must parse as valid JSON with required fields
- At least one model must have both baseline and skillbook results
- Question count must be ≥ 10

## When to Re-Run Evals

- **Major version bump** — content has changed significantly, re-eval
- **New model release** — optionally add a new model to the report
- **Significant content additions** — if you added a new section, add questions covering it

See also: [Self-Review Checklist](01-self-review-checklist.md) | [Common Mistakes](02-common-mistakes.md)
