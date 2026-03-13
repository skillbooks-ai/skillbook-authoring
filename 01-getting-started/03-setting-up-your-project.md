---
tags: [project-setup, init, directory-structure, scaffolding]
---

# Setting Up Your Project

Every skillbook starts with `skillbook init`. This creates the project scaffolding with
correct metadata in both `package.json` and `SKILL.md`.

## Initialize

```bash
npm i -g @skillbooks/cli
skillbook init
```

The CLI prompts for:
- **name** — URL-safe identifier (lowercase, hyphens, max 64 chars)
- **description** — What the book covers (max 1024 chars)
- **author** — Publisher (you or your organization)
- **license** — License identifier (e.g., `CC-BY-4.0`, `all-rights-reserved`)
- **title** — Human-readable display title
- **content author** — The original author of the content (if different from publisher)
- **price** — Full book price (`$0.00` for free)
- **server** — Base URL for serving (default: `https://skillbooks.ai`)

## What Gets Created

```
my-skillbook/
├── SKILL.md          ← Agent entry point with frontmatter + starter TOC
├── README.md         ← Human-facing overview template
├── package.json      ← Project manifest with skillbook config
└── 01-introduction/
    └── 00-overview.md  ← Starter section
```

## After Init

1. **Plan your sections** before creating them — see [Section Organization](../02-content-strategy/03-section-organization.md)
2. **Create section directories** — `mkdir 01-topic 02-topic 03-topic`
3. **Write `00-overview.md`** for each section first
4. **Add content pages** — one concept per file, 40-100 lines
5. **Run `skillbook validate`** after every section is complete

## Naming Your Book

The `name` field is your book's permanent identifier. Choose carefully:
- It appears in URLs: `skillbooks.ai/my-book/01/01`
- It's first-come, first-served on the server
- It can't be changed after publishing
- Use the convention: `skillbook-{topic}` (e.g., `skillbook-eu-ai-act`)

---

[Previous: Choosing Source Material](02-choosing-source-material.md) | [Section](00-overview.md) | [Home](../SKILL.md)
