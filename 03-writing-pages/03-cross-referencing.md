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

```markdown
For details on page structure, see [Anatomy of a Content Page](../03-writing-pages/01-anatomy-of-a-content-page.md).

This builds on the [four-tier framework](01-four-tiers.md).
```

**Within the same section:** use just the filename — `[Page](02-page.md)`

**Across sections:** use the relative path — `[Page](../02-section/01-page.md)`

## Placement

- **Inline** — when the reference is part of the explanation: "This requires a valid
  `package.json` (see [package.json setup](../04-project/01-package-json.md))."
- **End of section** — when listing related pages: "See also: [Tags](03-tags.md),
  [Validation](../05-tooling/01-validation.md)."
- **Navigation footer** — Previous/Next/Section/Home links at the page bottom.

## Navigation Footer Convention

Every content page should end with:

```markdown
---

[Previous: Title](prev.md) | [Section](00-overview.md) | [Next: Title](next.md) | [Home](../SKILL.md)
```

- First page in a section: omit "Previous"
- Last page in a section: omit "Next"
- `00-overview.md` files: just `[Home](../SKILL.md)`

## Validation

`skillbook validate` checks that all cross-reference paths resolve to actual files.
Broken links are errors, not warnings. Fix them before publishing.

---

[Previous: Writing Section Overviews](02-writing-section-overviews.md) | [Section](00-overview.md) | [Next: Tag Discipline](04-tag-discipline.md) | [Home](../SKILL.md)
