---
tags: [workflow, gutenberg, authoring]
---

# Automated Conversion with Gutenberg

Gutenberg is the automated pipeline for converting public domain and licensed works
into skillbooks at scale. It handles the mechanical aspects of conversion while
maintaining quality standards.

## What Gutenberg Does

The pipeline automates:
- Source text ingestion and cleaning
- Chapter/section boundary detection
- Atomic concept extraction and page generation
- Frontmatter and tag generation
- Cross-reference insertion
- Validation and structural compliance

## What Gutenberg Doesn't Do

- **Editorial judgment** — it can't decide if content is worth converting
- **License verification** — you must verify rights before feeding content in
- **Domain expertise** — it structures content but doesn't evaluate accuracy
- **Quality polish** — output needs human review for clarity and completeness

## When to Use Gutenberg

| Scenario | Use Gutenberg? |
|----------|---------------|
| Converting a single book manually | No — manual conversion gives better results |
| Batch-converting a public domain catalog | Yes — scale demands automation |
| Structured source with clear chapters | Yes — Gutenberg handles this well |
| Heavily visual or diagram-dependent source | No — markdown can't carry the visuals |
| Source needing significant editorial rework | No — garbage in, garbage out |

## The Gutenberg Workflow

1. **Prepare source texts** — clean text files, one per work
2. **Configure the pipeline** — set metadata templates, section heuristics
3. **Run conversion** — Gutenberg produces a draft skillbook per source
4. **Review output** — check section boundaries, page quality, tag consistency
5. **Fix and refine** — manual editing for quality issues Gutenberg missed
6. **Validate and publish** — standard `skillbook validate` and `skillbook publish`

## Post-Gutenberg Quality Check

Automated output always needs review. Focus on:
- Are page boundaries at concept boundaries, or arbitrary line breaks?
- Do cross-references make sense, or are they mechanical and unhelpful?
- Are tags consistent with your vocabulary, or did Gutenberg invent its own?
- Are overviews genuine orientation, or just auto-generated file lists?

---

[Previous: Converting Existing Content](01-converting-existing-content.md) | [Section](00-overview.md) | [Next: Iterative Authoring](03-iterative-authoring.md) | [Home](../SKILL.md)
