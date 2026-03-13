---
tags: [tags, content-strategy, page-structure]
---

# Tag Discipline

Tags enable O(1) page lookup via `TAG-INDEX.json`. Good tagging makes a skillbook
searchable. Bad tagging makes it noisy.

## What Tags Are For

An agent with a question fetches `TAG-INDEX.json`, finds pages tagged with the relevant
concept, and retrieves only those pages. Tags are the bridge between a question and the
pages that answer it.

## Semantic Tags vs Topic Tags

**Semantic tags** describe what a page *does*:
- `workflow` — a process or sequence of steps
- `validation` — checking correctness
- `page-structure` — how to organize a page

**Topic tags** describe what a page *is about*:
- `cli` — related to the command-line tool
- `gutenberg` — related to automated conversion
- `cross-references` — about linking between pages

Use both. Semantic tags help agents find pages by task ("I need a workflow"). Topic
tags help agents find pages by subject ("I need info about the CLI").

## Consistent Vocabulary

Pick a tag vocabulary early and stick to it. Inconsistent tags fracture lookup.

| Bad | Good | Why |
|-----|------|-----|
| `setup`, `install`, `getting-started` | `project-setup` | One tag, one concept |
| `errors`, `mistakes`, `bugs` | `common-mistakes` | Pick one term |
| `verify`, `check`, `validate` | `validation` | Consistent verb form |

Define your vocabulary in a list before tagging. For this skillbook, the vocabulary is:
`authoring`, `content-strategy`, `page-structure`, `cli`, `validation`, `publishing`,
`quality`, `workflow`, `tags`, `cross-references`, `gutenberg`, `contributing`.

## How Many Tags Per Page

- **2-4 tags** is typical. Enough for discoverability, few enough to stay meaningful.
- **1 tag** is fine for focused pages — not every page is a crossroads.
- **6+ tags** means you're either tagging too broadly or the page covers too much.

## When Tags Help

- An agent searching for "how do I validate?" finds all `validation`-tagged pages
- A page about CLI publishing gets `cli` and `publishing` — discoverable from either angle
- Tags surface connections that section structure alone doesn't show

## When Tags Clutter

- Tagging every page with `skillbook` — that's the whole book, it adds no signal
- Using tags that only apply to one page — a tag with one entry isn't useful for lookup
- Synonym tags — `quality` and `quality-assurance` splitting the same concept

## Generating TAG-INDEX.json

After tagging all pages, run:

```bash
skillbook tag-index .
```

This reads frontmatter tags from every content page and produces `TAG-INDEX.json` —
a flat map of tag → page paths. Commit it alongside your content.

---

[Previous: Cross-Referencing](03-cross-referencing.md) | [Section](00-overview.md) | [Home](../SKILL.md)
