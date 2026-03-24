---
tags: [cli, publishing]
---

# Publishing

`skillbook publish` pushes your book to the skillbook server. This is the final step
in the authoring workflow.

## Before You Publish

Run through this checklist:

1. **`skillbook validate .`** passes with zero errors
2. **`skillbook count .`** matches `skillbook-pages` in SKILL.md and package.json
3. **`TAG-INDEX.json`** is up to date (`skillbook tag-index .`)
4. **TOC in SKILL.md** matches actual content (`skillbook toc .`)
5. **Version** is set correctly in both SKILL.md and package.json
6. **License** is correct — it can't be changed after first publish

## Authentication

You need an account on the skillbook server before publishing.

Sign up at [skillbooks.ai/signup](https://skillbooks.ai/signup) to get your API key, then authenticate:

```bash
skillbook login           # authenticate with your API key
skillbook credits         # check your publishing credits
```

## Publishing

```bash
skillbook publish .
```

The CLI:
1. Runs validation automatically (publish aborts on errors)
2. Uploads all content pages, SKILL.md, README.md, and TAG-INDEX.json
3. Registers the book name (first-come, first-served)
4. Returns the public URL

## After Publishing

- **Verify access** — fetch your SKILL.md from the server URL to confirm it's live
- **Test page retrieval** — try fetching a content page to confirm metering works
- **Share the URL** — agents access your book via the server URL in SKILL.md frontmatter

## Updating a Published Book

To publish updates:
1. Bump `skillbook-version` in SKILL.md (and sync to package.json)
2. Run the full validation and generation sequence
3. Run `skillbook publish .` again

The CLI detects this is an update to an existing book and replaces the content.

## The skillbook search Command

After publishing, your book is discoverable via:

```bash
skillbook search "your topic"
```

This searches the server's catalog. Use it to verify your book appears and to
check how other authors have structured similar content.

---

[Previous: Mechanical Tools](03-mechanical-tools.md) | [Section](00-overview.md) | [Home](../SKILL.md)
