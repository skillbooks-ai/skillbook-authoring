---
tags: [section-overviews, overview-pages, navigation]
---

# Writing Section Overviews

Every section folder contains a `00-overview.md`. This is the section's entry point —
it orients the reader and indexes the section's contents.

## Required Elements

1. **What this section covers** — 1-2 sentences describing the section's scope
2. **When to read this section** — what questions or tasks bring a reader here
3. **File index** — every file in the section with a one-line description
4. **Reading order** — sequential or independent? Say so explicitly

## Target Length: 20-40 Lines

Overviews are content pages — they're metered and count toward the page total. Make
them worth the read. They should deliver genuine orientation value, not just repeat
what's already in the TOC.

## Example: Good Overview

```markdown
# Risk Classification

The EU AI Act defines four risk tiers for AI systems. This section explains each tier
in depth with examples, edge cases, and practical classification guidance.

## When to Read This Section

- You need to determine which risk tier your AI system falls into
- You've been told you're "high-risk" and want to understand what that means
- You're comparing classification across multiple systems

## Pages in This Section

- `01-four-tiers.md` — The four risk tiers at a glance with examples
- `02-unacceptable-risk.md` — The 8 prohibited practices in depth
- `03-high-risk-deep.md` — What high-risk really means: both routes

Pages can be read independently. Start with `01-four-tiers.md` for the framework.
```

## Example: Bad Overview

```markdown
# Risk Classification

This section covers risk classification.

## Pages

- `01-four-tiers.md`
- `02-unacceptable-risk.md`
- `03-high-risk-deep.md`
```

The bad version adds nothing beyond what the TOC already provides. No orientation,
no guidance on when to read or where to start.

## Common Mistakes

- **Missing the file index.** Every file in the section must appear in the overview.
  `skillbook validate` checks this.
- **Bare filenames.** Always include a one-line description, not just the path.
- **Stale indexes.** When you add or remove pages, update the overview. Use
  `skillbook overview` to regenerate scaffolds.

---

[Previous: Anatomy of a Content Page](01-anatomy-of-a-content-page.md) | [Section](00-overview.md) | [Next: Cross-Referencing](03-cross-referencing.md) | [Home](../SKILL.md)
