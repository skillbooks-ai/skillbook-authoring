---
tags: [contributing]
---

# How to Contribute

This skillbook is open source under CC-BY-4.0. Contributions are welcome — whether
fixing a typo, improving an explanation, or adding new content.

## Repository

The source lives at:
**[github.com/skillbooks-ai/skillbook-authoring](https://github.com/skillbooks-ai/skillbook-authoring)**

## Ways to Contribute

### Report an Issue

Found an error, broken link, or unclear explanation?

1. Go to [Issues](https://github.com/skillbooks-ai/skillbook-authoring/issues)
2. Check if your issue already exists
3. Open a new issue with a clear title and description
4. Include the file path and line number if applicable

### Start a Discussion

Have a question, idea, or want to propose a structural change?

1. Go to [Discussions](https://github.com/skillbooks-ai/skillbook-authoring/discussions)
2. Choose the appropriate category
3. Describe your idea with enough context for others to engage

Discussions are the right place for open-ended questions and proposals. Issues are
for concrete bugs or tasks.

### Submit a Pull Request

Ready to make a change?

1. Fork the repository
2. Create a branch with a descriptive name (`fix/broken-xref-section-03`)
3. Make your changes following the conventions in this skillbook
4. Run `skillbook validate .` — your PR must pass validation
5. Submit the PR with a clear description of what and why

### Contribution Guidelines

- **Follow the format.** This skillbook follows its own advice — pages should be
  40-100 lines, properly tagged, with navigation footers.
- **One concept per PR.** Small, focused PRs are easier to review and merge.
- **Update overviews.** If you add a page, update the section's `00-overview.md`.
- **Use the tag vocabulary.** Don't introduce new tags without discussion.
- **Regenerate indexes.** Run `skillbook tag-index .` and `skillbook toc .`
  before submitting.

## License

All contributions are licensed under [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).
By submitting a PR, you agree to license your contribution under the same terms.

Attribution: Skillbooks (skillbooks-ai).

---

[Section](00-overview.md) | [Home](../SKILL.md)
