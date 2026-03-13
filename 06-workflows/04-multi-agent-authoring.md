---
tags: [workflow, authoring]
---

# Multi-Agent Authoring

For large skillbooks, splitting work across multiple agents can dramatically reduce
authoring time. The key is clean boundaries — each agent owns a section and produces
self-contained output.

## When Multi-Agent Works

- The book has 6+ sections with minimal cross-section dependencies
- Source material is large enough that a single agent would hit context limits
- Sections can be written independently without constant coordination

## When It Doesn't

- Sections are tightly interdependent (each page references three others)
- The book requires a consistent voice or style that's hard to specify
- The source material is ambiguous and requires editorial judgment at every step

## The Division Pattern

**One agent per section.** Each agent receives:
1. The section plan (which pages to write, what each covers)
2. The tag vocabulary (so tags are consistent across agents)
3. The cross-reference convention (how to link to other sections)
4. Example pages from a completed section (to match style)

**One coordinator agent.** Responsible for:
1. Creating the section plan and distributing work
2. Writing SKILL.md, README.md, and TAG-INDEX.json
3. Running full-book validation after all sections are assembled
4. Fixing cross-section cross-references
5. Ensuring tag vocabulary consistency

## Coordination Artifacts

Before agents start writing, the coordinator produces:

| Artifact | Purpose |
|----------|---------|
| Section plan | What sections exist, what pages each contains |
| Tag vocabulary | The complete list of allowed tags |
| Style example | 2-3 completed pages showing the expected pattern |
| Cross-reference map | Which pages will link to which (planned, not final) |

## Assembly Workflow

1. Coordinator creates the plan and distributes to section agents
2. Section agents write their assigned sections independently
3. Coordinator collects all sections into one project
4. Coordinator runs `skillbook validate .` and fixes cross-section issues
5. Coordinator regenerates TAG-INDEX.json and the TOC
6. Final review and publish

## Avoiding Conflicts

- Agents should never edit files outside their assigned section
- Cross-references to other sections use planned paths (coordinator verifies)
- Tag vocabulary is fixed before writing begins — no agent invents new tags
- If an agent discovers the section plan needs changes, it reports back to the
  coordinator rather than improvising

---

[Previous: Iterative Authoring](03-iterative-authoring.md) | [Section](00-overview.md) | [Home](../SKILL.md)
