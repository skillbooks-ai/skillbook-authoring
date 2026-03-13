---
tags: [workflow, overview, authoring-process]
---

# The Authoring Workflow

Building a skillbook follows a consistent pipeline regardless of source material.

## The Pipeline

1. **Evaluate source material** — Is this content suitable? Is it structured enough?
2. **Initialize the project** — `skillbook init`, configure metadata
3. **Plan sections** — Decompose the source into logical sections with dependency ordering
4. **Define page boundaries** — Identify atomic concepts, aim for 40-100 lines each
5. **Write content** — Section overviews first, then content pages
6. **Tag pages** — Add frontmatter tags for O(1) lookup
7. **Cross-reference** — Link related pages within and across sections
8. **Validate** — Run `skillbook validate` early and often
9. **Refine** — Split oversized pages, merge thin ones, fix cross-references
10. **Publish** — Final validation, version bump, publish

## Key Principles

**Work section by section.** Don't try to write the whole book in one pass. Complete one
section — overview, pages, tags, cross-references — before moving to the next.

**Validate continuously.** Run `skillbook validate` after every major change. Catching
issues early prevents cascading problems.

**Write the TOC last.** The SKILL.md table of contents should reflect what you actually
wrote, not what you planned to write. Generate it with `skillbook toc` after all content
is complete.

**Let the source guide structure.** The best skillbooks mirror the natural organization
of their source material. Don't impose an artificial structure — find the one that's
already there.

## Your Role as an Agent

You are the authoring partner. The human provides the source material, domain expertise,
and editorial judgment. You provide the structural discipline, format compliance, and
content organization. Work collaboratively — propose structure, get feedback, iterate.

---

[Section](00-overview.md) | [Next: Choosing Source Material](02-choosing-source-material.md) | [Home](../SKILL.md)
