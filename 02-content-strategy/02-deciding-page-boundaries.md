---
tags: [page-boundaries, atomic-content, page-length, splitting]
---

# Deciding Page Boundaries

Page boundaries are concept boundaries — not line counts. A page should cover exactly
one idea deeply enough to be useful, and no more.

## The One-Concept Rule

Ask: "What question does this page answer?" If the answer involves "and", you probably
have two pages. Good page scopes:

- "What are the four risk tiers?" — one page
- "What makes a system high-risk?" — one page
- "What are the four risk tiers and what makes a system high-risk?" — two pages

## Finding Natural Boundaries

Look for these signals in source material:

| Signal | What it means |
|--------|---------------|
| New heading at the same level | Likely a new page |
| "Furthermore" / "In addition" | The author is moving to a new sub-concept |
| Change of scope (general → specific) | Split at the transition |
| New example or case study | Consider a separate page if substantial |
| A list of items each needing explanation | Each item may deserve its own page |

## The 40-100 Line Target

This is a guideline, not a hard rule. The goal:

- **Under 40 lines** usually means the page is too thin — either the concept is too narrow
  or the treatment is too shallow. Consider merging with a related page.
- **Over 100 lines** usually means the page covers too much ground. Look for a natural
  split point.
- **Right-sized pages** are token-efficient — an agent reads one page and gets a complete
  answer without wasting context on unrelated content.

## When to Split

Split a page when:
- It answers more than one distinct question
- An agent looking for one part would be forced to read the other
- Two different tags would naturally apply to different halves

## When to Merge

Merge pages when:
- A page is under 30 lines and can't be meaningfully expanded
- Two pages always need to be read together
- The split creates an artificial dependency

## Example: Good vs Bad Boundaries

**Bad:** A single page called "Risk Classification" covering all four tiers, each tier's
requirements, and the classification process (200+ lines, multiple concepts).

**Good:** Separate pages for "The Four Tiers at a Glance" (overview), "Unacceptable Risk"
(deep dive), "High Risk" (deep dive), "Limited Risk" (deep dive), "Minimal Risk" (deep dive).
Each answers one question; an agent needing only high-risk info fetches one page.

---

[Previous: Analyzing Source Material](01-analyzing-source-material.md) | [Section](00-overview.md) | [Next: Section Organization](03-section-organization.md) | [Home](../SKILL.md)
