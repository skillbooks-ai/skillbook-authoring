---
tags: [cli, tags, publishing]
---

# Mechanical Tools

These CLI commands handle deterministic tasks — generating indexes, counting pages,
synchronizing metadata. They don't require judgment, just execution.

## skillbook tag-index

Generates `TAG-INDEX.json` from frontmatter tags across all content pages.

```bash
skillbook tag-index .
```

Output is a flat JSON map of tag → page paths:
```json
{
  "validation": [
    "04-using-the-cli/02-validation.md",
    "05-quality/01-self-review-checklist.md"
  ]
}
```

Run this after all pages are tagged. Commit the output alongside your content.

## skillbook toc

Generates or updates the table of contents in SKILL.md based on the current
directory structure and page titles.

```bash
skillbook toc .
```

Always run this after all content is written — the TOC should reflect what exists,
not what you planned. Review the output to ensure section and page ordering is correct.

## skillbook sync

Synchronizes metadata between `SKILL.md` and `package.json`. If you update one,
sync keeps the other consistent.

```bash
skillbook sync .
```

This is especially useful after changing the title, description, or version in
either file.

## skillbook overview

Generates or regenerates `00-overview.md` scaffold files for sections. It reads
the pages in each section directory and produces a file index.

```bash
skillbook overview .
```

Use this as a starting point — the generated overviews list files correctly but
need human editing to add "When to Read" guidance and reading order notes.

## skillbook count

Counts total content pages across all sections.

```bash
skillbook count .
```

Output: a single integer. Use this to set `skillbook-pages` in your frontmatter
and `pages` in `package.json`. Only overviews and content pages count — `SKILL.md`,
`README.md`, and `TAG-INDEX.json` do not.

## Putting It Together

A typical end-of-authoring sequence:

```bash
skillbook validate .     # fix any errors first
skillbook tag-index .    # generate tag lookup
skillbook toc .          # regenerate TOC from actual content
skillbook count .        # get final page count
skillbook sync .         # ensure metadata consistency
```

---

[Previous: Validation](02-validation.md) | [Section](00-overview.md) | [Next: Publishing](04-publishing.md) | [Home](../SKILL.md)
