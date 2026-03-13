---
tags: [cross-references, linking, navigation, related-pages]
---

# Cross-Referencing

Cross-references help agents discover related content without returning to the TOC.
They're the internal web of your skillbook.

## When to Cross-Reference

Link to another page when:
- You mention a concept covered in depth elsewhere
- A reader of this page will likely need the other page next
- Two concepts are related but live in different sections

Do not cross-reference when:
- The link would be purely decorative ("see also everything")
- The related page is the next page in sequence (use navigation links instead)
- You'd be linking to avoid writing needed content on this page

## Syntax

Use standard relative markdown links:

    For details on page structure, see
    Anatomy of a Content Page → ../03-writing-pages/01-anatomy-of-a-content-page.md

    This builds on the four-tier framework → 01-four-tiers.md

**Within the same section:** use just the filename, e.g. `[Title](same-dir-file)`

**Across sections:** include the relative path, e.g. `[Title](../other-section/file)`

## Placement

- **Inline** — when the reference is part of the explanation: "This requires a valid
  `package.json` (see `package.json setup` in the project section)."
- **End of section** — when listing related pages: "See also: Tags and Validation pages."
- **Navigation footer** — Previous/Next/Section/Home links at the page bottom.

## Navigation Footer Convention

Every content page should end with:

    ← Previous: Title | ↑ Section | Next: Title → | 🏠 Home

- First page in a section: omit "Previous"
- Last page in a section: omit "Next"
- `00-overview.md` files: just a Home link

## Validation

`skillbook validate` checks that all cross-reference paths resolve to actual files.
Broken links are errors, not warnings. Fix them before publishing.

---

[Previous: Writing Section Overviews](02-writing-section-overviews.md) | [Section](00-overview.md) | [Next: Tag Discipline](04-tag-discipline.md) | [Home](../SKILL.md)
