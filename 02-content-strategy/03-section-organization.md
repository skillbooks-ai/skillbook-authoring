---
tags: [section-organization, dependency-ordering, section-naming, structure]
---

# Section Organization

Sections group related pages. The ordering of sections determines the reading flow of
the entire book.

## Ordering Principles

**Dependency-first.** If Section 3 references concepts from Section 2, Section 2 must
come first. Map the dependency graph from your source analysis and sort topologically.

**General to specific.** Start with foundations, context, and definitions. Move toward
detailed requirements, procedures, or applications.

**Common patterns:**

| Pattern | When to use | Example |
|---------|-------------|---------|
| Foundation → Application | Tutorials, textbooks | Concepts → Procedures → Examples |
| Overview → Deep Dive | Regulations, standards | Summary → Detailed Articles |
| Setup → Usage → Reference | Technical manuals | Install → Configure → API Reference |
| Context → Content → Quality | Meta-guides (like this one) | Why → How → Polish |

## Section Naming

- **2-digit prefix:** `01-`, `02-`, `03-` — always sequential, no gaps
- **Kebab-case:** `01-getting-started`, `02-risk-classification`
- **Descriptive:** The folder name should tell you what's inside without opening it
- **4-8 sections** is typical — fewer feels too sparse, more feels fragmented

## How Many Pages Per Section?

- **3-6 pages** per section is the sweet spot (plus the `00-overview.md`)
- **Under 3 pages:** Consider merging with an adjacent section
- **Over 8 pages:** Consider splitting into two sections
- An exception: large reference sections (e.g., 37 Shakespeare plays) can have many pages

## Restructuring

If you realize a section is too broad or too narrow after writing, restructure:

1. Move pages to their new locations
2. Update all cross-references (use `skillbook validate` to find broken ones)
3. Renumber section prefixes to stay sequential
4. Regenerate overviews and the TOC

It's easier to restructure early. Once you've written cross-references and tags across
sections, reorganization becomes more expensive. Get the section plan right before
writing content — see [Analyzing Source Material](01-analyzing-source-material.md).

---

[Previous: Deciding Page Boundaries](02-deciding-page-boundaries.md) | [Section](00-overview.md) | [Next: Content Types](04-content-types.md) | [Home](../SKILL.md)
