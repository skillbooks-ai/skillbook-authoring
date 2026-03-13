---
tags: [workflow, authoring, content-strategy]
---

# Converting Existing Content

The most common skillbook workflow: take an existing book, manual, or document and
restructure it into the skillbook format. This is the manual path — you read the source,
plan the decomposition, and write each page.

## The Conversion Pipeline

1. **Obtain and read the source** — get the full text in a machine-readable format
2. **Analyze structure** — identify chapters, sections, and atomic concepts
   (see [Analyzing Source Material](../02-content-strategy/01-analyzing-source-material.md))
3. **Plan sections** — map source structure to 4-8 skillbook sections
4. **Initialize the project** — `skillbook init`, set metadata
5. **Write section by section** — overview first, then content pages
6. **Tag and cross-reference** — add frontmatter tags, link related pages
7. **Validate and refine** — iterate until `skillbook validate` passes cleanly

## Source Format Handling

| Format | Approach |
|--------|----------|
| PDF | Extract text first (OCR if needed). Expect formatting loss. |
| EPUB/MOBI | Convert to text or markdown. Chapter boundaries usually survive. |
| HTML docs | Markdown conversion preserves most structure. |
| Plain text | Cleanest starting point — no formatting artifacts to clean up. |
| Physical book | OCR or manual transcription. Verify accuracy before structuring. |

## What Changes During Conversion

You're not copying — you're restructuring. Expect these transformations:

- **Chapter → Section**: A source chapter often maps to a skillbook section, but
  dense chapters may become multiple sections.
- **Subheading → Page**: Each significant subheading or topic becomes its own page.
- **Linear prose → Structured content**: Convert paragraphs to tables, lists, and
  headers wherever structure improves parseability.
- **Implicit relationships → Explicit cross-references**: Where the source says
  "as discussed earlier", add an explicit link.

## Licensing Reminder

Converting content doesn't transfer rights. Verify you have permission to redistribute
the source material in skillbook format. Public domain and Creative Commons works are
safe. Copyrighted material requires explicit licensing.

---

[Section](00-overview.md) | [Next: Automated Conversion](02-automated-conversion.md) | [Home](../SKILL.md)
