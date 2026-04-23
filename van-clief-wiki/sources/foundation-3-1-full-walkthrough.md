---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, three-layer, canonical, folder-architecture]
---

# foundation-3-1-full-walkthrough

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~1250–1449. Foundation Module 3, Lesson 1. 23-minute video + written companion.

## Summary

The canonical walkthrough of the three-layer folder architecture. Where the folder-system YouTube talk is an intro, Foundation 3.1 is the structured teach: Layer 1 (`CLAUDE.md` as map), Layer 2 (per-workspace `CONTEXT.md` files as rooms), Layer 3 (skills / MCP servers / tools wired per-workspace). Names the routing table as "the most important pattern in the whole system", details naming conventions as the database replacement, and explicitly positions the architecture as applied separation-of-concerns from 1972-onward software engineering. A partial five-layer architecture is referenced via a research paper placeholder (`[ ICM PAPER ]`).

## Key claims

1. Three layers, each with a distinct job: Layer 1 = map (`CLAUDE.md`), Layer 2 = rooms (workspace context files), Layer 3 = tools (skills, MCP, plug-and-play).
2. `CLAUDE.md` is a routing file - not a project brief, not a style guide, not a brain dump. Its job is to tell Claude where things are and where to go.
3. The routing table (task → go to → read → skills) inside `CLAUDE.md` is the most important pattern in the whole system; without it, Claude either reads everything, guesses wrong, or produces uneditable work.
4. Workspace `CONTEXT.md` files load only when Claude enters that workspace, containing the workspace's purpose, process, and relevant skills - a few paragraphs in plain English.
5. Skills are not loaded globally; they are wired into the workspaces that need them. A project may reference 100 skills; each workspace loads only the ones relevant to its tasks.
6. Naming conventions inside `CLAUDE.md` replace the need for databases, indices, or vector stores. The AI finds files by convention ("pull my demo v2") without any query layer.
7. The architecture is domain-agnostic: the layers do not change; only the labels and context do. Content creators, freelancers, and developers all use the same three-layer structure with different workspace names and routing rules.
8. The approach is rooted in 1972-onward software engineering principles (separation of concerns, modular composition). A fuller five-layer architecture exists in research-paper form; this lesson covers the three most important layers.

## Entities mentioned

- [[van-clief]] - author
- [[claude-code]] - the demo's runtime
- [[claude-cowork]] - mentioned as a folder-aware alternative to VS Code
- [[vs-code]] - used in the video demo, explicitly declared optional
- [[john-gruber]] - markdown inventor, 2004
- [[markdown]] (concept) - the file format of the whole system
- [[notepad]] - mentioned as a sufficient text editor

## Open questions

- The research paper is cited as `[ ICM PAPER ]` - an editorial placeholder. Actual URL / citation not in this source.
- The two additional layers (beyond the three taught here) are named as existing in the paper but not detailed.
- The "Workspace Blueprint" template referenced as being in The Vault (Premium) - not inline.
- Claude Cowork is mentioned but not taught; its relationship to Claude Code is left implicit.
