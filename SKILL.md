---
name: skillbook-authoring
description: "A practical guide to building high-quality skillbooks — for AI agents helping humans create structured knowledge bases."
author: skillbooks-ai
license: "CC-BY-4.0"
compatibility: "Requires HTTPS access to https://skillbooks.ai"
metadata:
  skillbook-title: "Skillbook Authoring Guide"
  skillbook-author: "Skillbooks"
  skillbook-contact: "https://github.com/skillbooks-ai/skillbook-authoring/discussions"
  skillbook-server: "https://skillbooks.ai"
  skillbook-version: "1.1.0"
  skillbook-pages: "30"
  skillbook-price: "$0.00"
  skillbook-tags: "true"
---

# Skillbook Authoring Guide

A practical guide to building high-quality skillbooks — for AI agents helping humans
create structured knowledge bases. This skillbook follows the exact format it teaches.

## How to Use This Skillbook

1. Read the **Table of Contents** below to find the section relevant to your task
2. Start with the section's `00-overview.md` for orientation
3. Read individual pages for specific guidance
4. Use `TAG-INDEX.json` for O(1) lookup by topic

## Quick Start Paths

**First-time author:** Start with [01-getting-started](01-getting-started/00-overview.md) →
read sections in order.

**Converting an existing book:** Jump to
[06-workflows/01-converting-existing-content.md](06-workflows/01-converting-existing-content.md).

**Need CLI help:** Go to [04-using-the-cli](04-using-the-cli/00-overview.md).

**Ready to publish:** Read the
[Self-Review Checklist](05-quality/01-self-review-checklist.md), then
[Publishing](04-using-the-cli/04-publishing.md).

## Table of Contents

### 01 — Getting Started
- [00-overview.md](01-getting-started/00-overview.md)
- [01-authoring-workflow.md](01-getting-started/01-authoring-workflow.md) — The end-to-end authoring pipeline
- [02-choosing-source-material.md](01-getting-started/02-choosing-source-material.md) — Evaluating content suitability
- [03-setting-up-your-project.md](01-getting-started/03-setting-up-your-project.md) — Project scaffolding and configuration

### 02 — Content Strategy
- [00-overview.md](02-content-strategy/00-overview.md)
- [01-analyzing-source-material.md](02-content-strategy/01-analyzing-source-material.md) — Decomposition mindset and section planning
- [02-deciding-page-boundaries.md](02-content-strategy/02-deciding-page-boundaries.md) — The one-concept rule and finding natural boundaries
- [03-section-organization.md](02-content-strategy/03-section-organization.md) — Dependency ordering and section naming
- [04-content-types.md](02-content-strategy/04-content-types.md) — Patterns for manuals, regulations, tutorials, and reference works

### 03 — Writing Pages
- [00-overview.md](03-writing-pages/00-overview.md)
- [01-anatomy-of-a-content-page.md](03-writing-pages/01-anatomy-of-a-content-page.md) — Page structure and conventions
- [02-writing-section-overviews.md](03-writing-pages/02-writing-section-overviews.md) — How to write effective 00-overview.md files
- [03-cross-referencing.md](03-writing-pages/03-cross-referencing.md) — When and how to link between pages
- [04-tag-discipline.md](03-writing-pages/04-tag-discipline.md) — Consistent vocabulary and TAG-INDEX.json

### 04 — Using the CLI
- [00-overview.md](04-using-the-cli/00-overview.md)
- [01-project-setup.md](04-using-the-cli/01-project-setup.md) — The skillbook init walkthrough
- [02-validation.md](04-using-the-cli/02-validation.md) — Running skillbook validate and fixing errors
- [03-mechanical-tools.md](04-using-the-cli/03-mechanical-tools.md) — tag-index, toc, sync, overview, count
- [04-publishing.md](04-using-the-cli/04-publishing.md) — The skillbook publish workflow

### 05 — Quality
- [00-overview.md](05-quality/00-overview.md)
- [01-self-review-checklist.md](05-quality/01-self-review-checklist.md) — Pre-publish quality gate
- [02-common-mistakes.md](05-quality/02-common-mistakes.md) — Frequent errors and how to fix them
- [03-page-length-tuning.md](05-quality/03-page-length-tuning.md) — When to split vs merge pages
- [04-skill-eval.md](05-quality/04-skill-eval.md) — Proving your skillbook's value with automated A/B testing

### 06 — Workflows
- [00-overview.md](06-workflows/00-overview.md)
- [01-converting-existing-content.md](06-workflows/01-converting-existing-content.md) — Manual PDF/book/manual → skillbook
- [02-automated-conversion.md](06-workflows/02-automated-conversion.md) — Gutenberg pipeline overview
- [03-iterative-authoring.md](06-workflows/03-iterative-authoring.md) — Write → validate → refine loop
- [04-multi-agent-authoring.md](06-workflows/04-multi-agent-authoring.md) — Splitting work across agents

### 07 — Contributing
- [00-overview.md](07-contributing/00-overview.md)
- [01-how-to-contribute.md](07-contributing/01-how-to-contribute.md) — Issues, discussions, and pull requests

## License

Licensed under [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).
Free for all use with attribution.
