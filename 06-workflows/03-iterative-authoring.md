---
tags: [workflow, validation, quality]
---

# Iterative Authoring

The write → validate → refine loop is the core rhythm of skillbook authoring. Small
cycles catch problems early and keep quality high throughout the process.

## The Loop

```
Write section → Validate → Fix errors → Review content → Repeat
```

Don't write the entire book and validate at the end. Work in section-sized increments.

## Step 1: Write a Complete Section

Write all pages in one section before validating:
1. `00-overview.md` — index and orientation
2. Content pages in sequence — one concept each
3. Navigation footers on every page
4. Frontmatter tags on every content page

## Step 2: Validate

```bash
skillbook validate .
```

Fix every error before moving on. Common first-pass issues:
- Missing pages in the overview index
- Broken cross-references (typos in paths)
- Missing frontmatter tags
- Pages outside the 40-100 line range

## Step 3: Content Review

Validation catches structural problems. Content review catches quality problems.
For each page, ask:

- Does the opening sentence state what this page covers?
- Would an agent get a complete answer from this page alone?
- Is the content structured (headers, lists, tables) or wall-of-prose?
- Are cross-references genuinely useful?

## Step 4: Refine and Move On

Fix content issues, re-validate, then start the next section. Don't over-polish —
you'll do a full-book review pass at the end.

## The Full-Book Pass

After all sections are complete, do one final pass:
1. Run `skillbook validate .` on the full book
2. Check cross-references across sections (not just within)
3. Verify tag consistency across the entire vocabulary
4. Run the [Self-Review Checklist](../05-quality/01-self-review-checklist.md)
5. Regenerate `TAG-INDEX.json` and the TOC

## Why Small Loops Work

- **Errors don't compound.** A broken cross-reference in section 2 doesn't cascade
  through sections 3-7.
- **Context stays fresh.** You remember what you just wrote. Fixing issues is faster.
- **Progress is visible.** Each validated section is a milestone.

---

[Previous: Automated Conversion](02-automated-conversion.md) | [Section](00-overview.md) | [Next: Multi-Agent Authoring](04-multi-agent-authoring.md) | [Home](../SKILL.md)
