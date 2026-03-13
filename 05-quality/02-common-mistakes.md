---
tags: [quality, authoring]
---

# Common Mistakes

These are the mistakes that show up most often in skillbook drafts. Learn to recognize
them and you'll save significant revision time.

## Structural Mistakes

**Sections with one or two pages.** A section with fewer than three content pages is
probably too narrow. Merge it with an adjacent section or expand its scope.

**Monolithic pages.** A 200-line page covering multiple concepts. Split it — each
concept deserves its own page. Look for places where the subject changes.

**Missing overviews.** Every section needs `00-overview.md`. It's not optional — it's
how agents navigate into the section. `skillbook validate` catches this.

## Content Mistakes

**Filler openings.** "In this page, we will explore the concept of..." — delete it
and start with the actual content. Agents don't need warm-up paragraphs.

**Restating instead of cross-referencing.** If you catch yourself rewriting content
that exists on another page, replace it with a link. Duplication causes drift.

**Abstract advice without examples.** "Write good pages" is useless. "Compare these
two openings — one states the answer, the other builds up to it" is useful. Always
show, don't just tell.

**Walls of prose.** Five consecutive paragraphs with no headers, lists, or tables.
Structure helps agents parse content. Break it up.

## Tagging Mistakes

**Synonym tags.** Using both `setup` and `project-setup`, or `errors` and
`common-mistakes`. Pick one term and use it everywhere.

**Over-tagging.** Six or more tags on a single page usually means the page covers too
much ground — split it. Or some tags are too generic to add value.

**Forgetting to regenerate TAG-INDEX.json.** Tags in frontmatter do nothing for lookup
until `skillbook tag-index .` generates the index file.

## Navigation Mistakes

**Broken cross-references after restructuring.** Moving or renaming files invalidates
existing links. Always run `skillbook validate` after any file reorganization.

**Cross-references to the next page.** If the link is just to the next page in sequence,
use the navigation footer instead. Inline cross-references should connect non-adjacent
pages.

**Missing Home links.** Every page needs `[Home](../SKILL.md)` in the footer. It's the
agent's escape hatch back to the TOC.

## The Fix Pattern

For every mistake: find it with `skillbook validate`, understand why it's wrong, fix
the root cause (not the symptom), and re-validate. Don't fix broken links by deleting
the link — fix the path or add the missing file.

---

[Previous: Self-Review Checklist](01-self-review-checklist.md) | [Section](00-overview.md) | [Next: Page Length Tuning](03-page-length-tuning.md) | [Home](../SKILL.md)
