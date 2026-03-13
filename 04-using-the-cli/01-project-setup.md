---
tags: [cli, project-setup]
---

# Project Setup with skillbook init

The `skillbook init` command scaffolds a new project with correct metadata, directory
structure, and starter files.

## Installation

```bash
npm i -g @skillbooks/cli
```

## Running Init

```bash
mkdir my-skillbook && cd my-skillbook
skillbook init
```

The CLI prompts for each metadata field interactively:

```
? name: skillbook-my-topic
? description: A guide to my topic for AI agents
? author: your-org
? license: CC-BY-4.0
? title: My Topic Guide
? content author: Original Author Name
? price: $0.00
? server: https://skillbooks.ai
```

## What Init Creates

```
my-skillbook/
├── SKILL.md            ← Frontmatter + starter TOC
├── README.md           ← Human-facing overview
├── package.json        ← Manifest with skillbook config
└── 01-introduction/
    └── 00-overview.md  ← First section scaffold
```

## After Init: Your First Steps

1. **Edit `README.md`** — replace the template with your book's actual description
2. **Plan sections** — decide your 4-8 sections before creating directories
3. **Create section directories** — `mkdir 02-topic 03-topic 04-topic`
4. **Write overviews first** — every section starts with `00-overview.md`
5. **Validate early** — run `skillbook validate .` after your first section is complete

## Common Init Mistakes

| Mistake | Fix |
|---------|-----|
| Name with spaces or uppercase | Use lowercase kebab-case: `skillbook-my-topic` |
| Skipping description | Write a real description — it appears in SKILL.md frontmatter |
| Wrong license | Verify before publishing — this can't be changed retroactively |
| Forgetting to `cd` into the directory | Init writes files to the current directory |

## Re-running Init

You can run `skillbook init` in an existing project to regenerate scaffolding. It will
not overwrite existing content files, but it will update `SKILL.md` and `package.json`
metadata if you confirm.

---

[Section](00-overview.md) | [Next: Validation](02-validation.md) | [Home](../SKILL.md)
