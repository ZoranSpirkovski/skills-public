---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 8
tags: [core, pattern, skills]
---

# skills-wired-per-task

Van Clief's Layer 3 discipline: skills (reusable AI instruction packages) are referenced *by task*, not loaded globally. A project may reference 15, 20, or 100 skills, but each workspace only loads the ones its tasks actually need. This keeps the [[context-window]] unbothered by unused tools while still making the full skill library addressable.

## Claims

- Skills are referenced from the routing table on a per-task basis, not loaded on session start [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- A project can reference arbitrarily many skills; only the ones the routing table calls for in a given task are activated [sources/folder-system-transcript]
- Example: a writing workspace references a humanizer skill and a doc co-authoring skill; a production workspace references a front-end design skill and a web app testing skill; each is only loaded when the relevant task runs [sources/folder-system-transcript]
- Skills are themselves folders full of markdown + code examples; they work because they sit inside the same markdown-native folder ecosystem [sources/folder-system-transcript]
- The animation pipeline wires Remotion, component registry, and style-guide reading per-task inside the production workspace - never globally loaded [sources/foundation-2-6-video-as-code]
- Developer routing tables demonstrate a Skills column: `testing-skill` on /src rows, `doc-authoring-skill` on /docs rows; the planning workspace has no skills column populated [sources/foundation-3-2-customizing-for-your-use-case]
- Wiring skills per task is the operational mechanism that makes Layer 3 work and keeps the [[context-window]] lean [sources/foundation-4-5-where-this-goes]
- [[uiux-pro-skill]] is a concrete front-end design skill Van Clief recommends for Claude Code builds [sources/stack-1-4-repo-tour-open-source-references]
- The Remotion agent skill loads lazily: Claude reads only the sub-file relevant to the current task (3D, DOM, Tailwind, transitions) rather than everything at once [sources/playbooks-1-1-building-animations-with-claude-code]
- Claude Design packages skill generation: pointing the product at a GitHub repo or Figma file produces a custom skill with routing to brand assets, colors, and voice [sources/playbooks-1-5-claude-design-folder-structure]

## Relationships

- The operational mechanism of Layer 3 in [[three-layer-routing]]
- Referenced from the Skills column of the [[routing-table]]
- Examples used: [[remotion]] (animation), humanizer, PDF skill, web app testing skill, [[uiux-pro-skill]]
