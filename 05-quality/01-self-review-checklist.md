---
tags: [quality, validation, publishing]
---

# Self-Review Checklist

Run through this checklist before publishing. It catches the problems that automated
validation can't — content quality, clarity, and completeness.

## Structure Check

- [ ] Every section has a `00-overview.md` that indexes all pages
- [ ] Sections are numbered sequentially with no gaps
- [ ] Pages within sections are numbered sequentially
- [ ] SKILL.md TOC lists every page in the correct order
- [ ] `skillbook validate .` passes with zero errors

## Content Check

- [ ] Every content page answers a clear, specific question
- [ ] Opening sentence states the page's purpose — no filler preambles
- [ ] Pages are self-contained — an agent fetching one page gets a complete answer
- [ ] No duplicate content across pages — cross-reference instead of restating
- [ ] Tables, lists, and headers are used instead of dense paragraphs
- [ ] Examples show concrete good/bad patterns, not abstract descriptions

## Navigation Check

- [ ] Every content page has Previous/Section/Next/Home footer links
- [ ] All cross-references resolve to real files
- [ ] Cross-references are genuinely helpful, not decorative
- [ ] First page in each section omits "Previous" link
- [ ] Last page in each section omits "Next" link

## Tags Check

- [ ] Every content page has frontmatter tags (overviews are exempt)
- [ ] Tags use the defined vocabulary — no synonyms or one-off terms
- [ ] 2-4 tags per page typical; no page has 6+
- [ ] `TAG-INDEX.json` is regenerated and committed

## Metadata Check

- [ ] `skillbook-pages` count matches actual page count from `skillbook count .`
- [ ] Version, license, and author are correct in both SKILL.md and package.json
- [ ] Description is accurate and under 1024 characters
- [ ] `skillbook sync .` reports no differences

## The "Agent Test"

Imagine an agent that has never seen this book. It reads the TOC, picks a page based
on a question, and fetches that single page. Ask yourself:

1. Would the agent find the right page from the TOC and tags?
2. Would that page alone answer the agent's question?
3. Would the agent know where to go next if it needs more?

If any answer is "no", revise.

---

[Section](00-overview.md) | [Next: Common Mistakes](02-common-mistakes.md) | [Home](../SKILL.md)
