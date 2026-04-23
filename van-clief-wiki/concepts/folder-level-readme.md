---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [folder-architecture, context, routing]
---

# folder-level-readme

A small markdown file inside each major folder that describes what is in it and why. Claude Code reads these when it enters the folder. The pattern keeps the root `CLAUDE.md` lean (under 50 lines, re-read on every prompt) while still giving Claude detailed context on demand. In the website-build example, `src/components/`, `src/pages/`, and `src/layouts/` each carry their own README; Claude reads the root first, understands the structure, then enters the specific folder it needs. The layout refines [[three-layer-routing]]: Layer 1 stays light, Layer 2 carries detail per room.

## Claims

- Each major folder can have its own small markdown file explaining what is inside [sources/playbooks-3-2-github-and-folder-structure]
- Claude Code reads these when it enters that folder; this is how detailed context loads without bloating the root `CLAUDE.md` [sources/playbooks-3-2-github-and-folder-structure]
- Root `CLAUDE.md` should stay under 50 lines because it is re-read on every prompt [sources/playbooks-3-2-github-and-folder-structure]
- Example: `src/components/README.md` (components present, how they connect), `src/pages/README.md` (page list, routing logic), `src/layouts/README.md` (layout templates, when to use each) [sources/playbooks-3-2-github-and-folder-structure]
- Clean folders enable multiple Claude Code sessions on the same project in parallel, coordinated by the same `CLAUDE.md` [sources/playbooks-3-2-github-and-folder-structure]

## Relationships

- Practical instance of [[context-md-workspace-files]]
- Supports [[three-layer-routing]] by giving Layer 2 per-folder detail
- Enables session parallelism inside [[workspace-isolation]]
