---
tags: [cli, validation, quality]
---

# Validation

`skillbook validate` is your primary quality gate. Run it after every major change —
it catches structural problems before they reach readers.

## Running Validation

```bash
skillbook validate .
```

The validator checks:
- Frontmatter completeness in SKILL.md
- Section directory structure and naming
- Overview files index all pages in their section
- Cross-reference links resolve to real files
- Page line counts fall within range
- Tag format and consistency
- package.json skillbook metadata

## Understanding Errors

Errors are blocking — they must be fixed before publishing. Warnings are advisory.

### Common Errors

**`missing-overview`** — A section directory has no `00-overview.md`.
```
ERROR 04-using-the-cli: missing 00-overview.md
```
Fix: Create the overview file. Every section needs one.

**`broken-xref`** — A cross-reference link points to a file that doesn't exist.
```
ERROR 03-writing-pages/03-cross-referencing.md: broken link ../04-tools/01-validate.md
```
Fix: Update the path to the correct file location.

**`missing-from-overview`** — A page exists in the section but isn't listed in its overview.
```
ERROR 02-content-strategy/04-content-types.md: not listed in 00-overview.md
```
Fix: Add the page to the overview's file index.

**`frontmatter-missing`** — A content page has no YAML frontmatter tags.
```
ERROR 01-getting-started/01-authoring-workflow.md: missing frontmatter
```
Fix: Add `---\ntags: [relevant-tags]\n---` to the top of the file.

### Common Warnings

**`page-too-short`** — Page is under 40 lines. Consider expanding or merging.

**`page-too-long`** — Page exceeds 100 lines. Consider splitting.

**`unused-tag`** — A tag appears on only one page. May indicate inconsistent vocabulary.

## Validate Early, Validate Often

Run validation after:
- Completing a section (all pages + overview)
- Adding or renaming files
- Writing cross-references
- Before publishing

Catching problems incrementally is far easier than fixing a full book's worth of
errors at the end.

---

[Previous: Project Setup](01-project-setup.md) | [Section](00-overview.md) | [Next: Mechanical Tools](03-mechanical-tools.md) | [Home](../SKILL.md)
