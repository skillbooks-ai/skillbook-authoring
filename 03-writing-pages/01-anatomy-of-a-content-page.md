---
tags: [page-structure, writing, content-pages, best-practices]
---

# Anatomy of a Content Page

A well-structured content page follows a consistent pattern that agents can parse
efficiently and humans can scan quickly.

## The Template

```markdown
---
tags: [relevant-tag, another-tag]
---

# Page Title

One-sentence summary of what this page covers.

## Core Content

The main material — structured with headers, lists, tables, and examples.
Use whatever format best conveys the information.

## Additional Detail (if needed)

Supporting content, edge cases, exceptions.

---

[Previous: Title](prev.md) | [Section](00-overview.md) | [Next: Title](next.md) | [Home](../SKILL.md)
```

## What Makes a Good Page

**Start with the answer.** The first sentence should tell the agent what this page is
about. Don't build up to it — state it.

**Use structure.** Headers, lists, and tables are easier to parse than paragraphs.
Agents extract information more reliably from structured content.

**Be self-contained.** A page should make sense on its own. An agent that fetches only
this page should get a complete answer to the question this page addresses.

**End with navigation.** Previous/next links and the section/home links help agents
traverse the book without returning to the TOC.

## What to Avoid

- **Filler openings.** No "In this page, we will explore..." — just explore it.
- **Walls of prose.** Break up long paragraphs with headers and lists.
- **Duplicate content.** If another page covers it, cross-reference instead of restating.
- **HTML or custom syntax.** Pure markdown only — no `<div>`, no custom directives.

## Example: Good vs Bad

**Bad opening:**
> In this section, we will take a closer look at the concept of high-risk AI systems
> as defined by the EU AI Act and explore what this classification means in practice.

**Good opening:**
> High-risk AI systems face the strictest compliance requirements under the EU AI Act.
> Two routes lead to high-risk classification: Annex III listing and safety-component use.

The good version tells the agent what it needs to know immediately.

---

[Section](00-overview.md) | [Next: Writing Section Overviews](02-writing-section-overviews.md) | [Home](../SKILL.md)
