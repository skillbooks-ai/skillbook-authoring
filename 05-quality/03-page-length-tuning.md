---
tags: [quality, page-structure, content-strategy]
---

# Page Length Tuning

The 40-100 line target is a guideline for concept density, not a formatting rule.
Right-sized pages deliver complete answers without wasting agent context.

## When to Split a Page

A page needs splitting when:

- **It answers multiple questions.** "What are tags and how do I validate them?" is two
  pages: one on tagging, one on validation.
- **The reader only needs half.** If an agent searching for validation advice has to read
  through tagging guidance first, the page is too broad.
- **It exceeds 100 lines.** Length alone isn't the trigger, but it's a strong signal that
  multiple concepts are packed together.

### How to Split

1. Identify the natural boundary — where does the subject shift?
2. Create two files with clear, distinct titles
3. Move content to the appropriate file
4. Add cross-references between the two new pages
5. Update the section overview and navigation footers

## When to Merge Pages

A page needs merging when:

- **It's under 30 lines** and can't be meaningfully expanded. The concept may be too
  narrow to stand alone.
- **Two pages are always read together.** If every reader of page A immediately needs
  page B, they should be one page.
- **The split is artificial.** "Part 1" and "Part 2" of the same concept should usually
  be unified.

### How to Merge

1. Pick the file that should survive (usually the one with broader scope)
2. Move content from the other file into it
3. Delete the empty file
4. Renumber remaining pages if needed
5. Update the section overview and all cross-references

## Finding Concept Boundaries

The best boundaries are where a reader can stop and have a complete understanding of
one thing. Test with this question: "If an agent reads only this page, do they get a
whole answer or half an answer?"

**Whole answer (good boundary):**
> "How do I run validation?" — page covers the command, what it checks, and how to
> fix common errors. Complete.

**Half answer (bad boundary):**
> "How do I set up tags?" — page explains frontmatter syntax but stops before
> explaining TAG-INDEX.json generation. Reader must fetch another page to finish
> the task.

## The Goldilocks Zone

| Lines | Signal | Action |
|-------|--------|--------|
| < 30 | Too thin | Merge with related page or expand depth |
| 30-40 | Borderline | Acceptable if focused; consider expanding |
| 40-100 | Target | Well-scoped concept with adequate depth |
| 100-120 | Borderline | Acceptable if cohesive; look for split points |
| > 120 | Too dense | Split at the natural concept boundary |

---

[Previous: Common Mistakes](02-common-mistakes.md) | [Section](00-overview.md) | [Home](../SKILL.md)
