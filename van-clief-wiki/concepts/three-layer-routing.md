---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 10
tags: [core, folder-architecture, spine]
---

# three-layer-routing

The load-bearing pattern of Van Clief's folder methodology. A project is structured as three distinct layers, each with its own loading rule and its own job. Layer 1 is the **map**: a `CLAUDE.md` at the project root that is read on every task entry; it contains the workspace inventory, naming conventions, and a routing table. Layer 2 is the **rooms**: a `CONTEXT.md` inside each workspace folder, loaded only when Claude enters that workspace, describing what happens there and which files or skills are relevant. Layer 3 is the **tools**: skills, MCP servers, or other plug-and-play artifacts, wired into whichever workspaces need them - never loaded globally. The point of separating the layers is token hygiene: the AI sees the map always, the current workspace's context on demand, and only the tools relevant to the immediate task.

## Claims

- Three layers, each with a distinct job: map (`CLAUDE.md`), rooms (workspace `CONTEXT.md`), tools (skills / MCP / plug-ins) [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- Layer 1 is always loaded; Layer 2 loads per workspace; Layer 3 loads per task [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- The layers are domain-agnostic - content creators, freelancers, and developers all use the same three layers with different workspace labels [sources/foundation-3-1-full-walkthrough]
- Separating what is always-loaded from what is sometimes-loaded is the mechanism that preserves [[context-window]] budget for the actual task [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- The pattern is a direct application of 1972-onward software-engineering separation of concerns [sources/foundation-3-1-full-walkthrough]
- A full five-layer extension is under research-paper development; the three-layer form taught here is the practical core [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- The minimum-viable entry to this architecture is a three-file folder (`CLAUDE.md` + `CONTEXT.md` + `REFERENCES.md`) - the layers are sketched but only fully activated once workspaces and routing tables are added [sources/foundation-1-2-your-first-folder]
- The same three layers adapt across three archetypes (content creator, freelancer, developer) with different labels and context files but identical architecture [sources/foundation-3-2-customizing-for-your-use-case]
- Seven common failure modes have been catalogued with fixes, all of them degenerations of the three-layer discipline (too-long CLAUDE.md, no routing table, too many workspaces, personality-over-work context, stale context, flat folders, over-building before use) [sources/foundation-3-3-common-mistakes]
- Becomes fully operational when run through Claude Code: routing tables, per-workspace context loading, and naming conventions require the file-aware agent to reach files [sources/foundation-4-5-where-this-goes]
- Scales on three principles: one fact one location, new sessions start clean, the system is hand-offable because context lives in files not people [sources/foundation-4-5-where-this-goes]
- Applied to animation as the [[two-workspace-setup]]: Script Lab plus Animation Studio, linked by a root `CLAUDE.md` that routes between them [sources/playbooks-1-1-building-animations-with-claude-code]
- Root `CLAUDE.md` under 50 lines for website builds because every token in it is re-read on every prompt [sources/playbooks-3-2-github-and-folder-structure]
- Folder-level README files carry detailed context; Claude reads them when it enters a folder, keeping root `CLAUDE.md` lean [sources/playbooks-3-2-github-and-folder-structure]
- Confirmed by Claude Design: underneath Anthropic's product is the same folder-plus-skills pattern; the exported zip runs unchanged locally with any coding agent [sources/playbooks-1-5-claude-design-folder-structure]

## Relationships

- Operationalized by [[routing-table]] - the primitive inside Layer 1 that drives workspace selection
- Depends on [[naming-conventions-as-db]] - Layer 1 names files by convention so Layer 3 can find them without a query layer
- Expressed in [[markdown]] - every file at every layer is plain markdown
- Entry point: [[claude-md-three-file-pattern]] (the three-file starter that becomes the full three-layer system)
- Solves [[workspace-isolation]] and [[context-window-hygiene]]
- Central to [[folder-as-workspace]] - the broader thesis that the folder IS the app
