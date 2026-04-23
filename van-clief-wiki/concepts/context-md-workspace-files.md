---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [core, layer-2]
---

# context-md-workspace-files

Layer 2 of [[three-layer-routing]]: a `CONTEXT.md` file inside each workspace folder, loaded only when Claude enters that workspace. Describes what this workspace is for, the process that happens here, which files are inside and how they are organized, and any skills the workspace uses. Short - "a few paragraphs in plain English." Written by hand or drafted by Claude from a brief.

## Claims

- Each workspace owns a `CONTEXT.md` that describes: purpose, process, files, skills [sources/foundation-3-1-full-walkthrough]
- Loads only when Claude enters the workspace - not on project startup [sources/foundation-3-1-full-walkthrough]
- Short format - a few paragraphs in plain English, not a project brief or policy document [sources/foundation-3-1-full-walkthrough]
- Result: almost no prompting needed once inside a workspace - "go to writing room, let's start making something" is enough [sources/foundation-3-1-full-walkthrough]
- Writing the `CONTEXT.md` should describe the work, not Claude's personality; common mistake is the inverted ratio where personality instructions dominate [sources/foundation-3-3-common-mistakes]
- Living document - stale context files are the single most common reason Claude seems to "get worse" over time [sources/foundation-3-3-common-mistakes] [sources/foundation-3-2-customizing-for-your-use-case]
- Each of the three archetypes (content creator, freelancer, developer) writes its `CONTEXT.md` per workspace in the same format but with completely different content [sources/foundation-3-2-customizing-for-your-use-case]

## Relationships

- Layer 2 of [[three-layer-routing]]
- Pointed at from the Read column of the [[routing-table]]
- Supplements Layer 1 (`CLAUDE.md`) without duplicating its routing content
