---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [animation, workspace, folder-architecture]
---

# two-workspace-setup

Van Clief's animation production organizes work into two sibling folders inside one parent: a Script Lab (where scripts live in `long-form/` and `short-form/` subfolders) and an Animation Studio (where production happens, with `specs/`, `builds/`, `output/`). A root `CLAUDE.md` routes between them. The pattern is an applied instance of [[three-layer-routing]]: Script Lab and Animation Studio are each a Layer 2 workspace, and the root `CLAUDE.md` is Layer 1. When Van Clief says "let's build an animation from a spec," Claude Code knows to enter Animation Studio, read its context file, find the named spec, and begin building. The same folder pattern was previewed in the content-creator archetype of Foundation 3.2.

## Claims

- Script Lab holds scripts (long-form and short-form subfolders); Animation Studio holds specs, builds, and output [sources/playbooks-1-1-building-animations-with-claude-code]
- A root `CLAUDE.md` routes between the two workspaces [sources/playbooks-1-1-building-animations-with-claude-code]
- Claude Code uses the context file to find the right spec without rereading the whole project [sources/playbooks-1-1-building-animations-with-claude-code]
- The two-workspace split lets the user stay at any stage (write scripts only, spec only, build only) or automate end-to-end [sources/playbooks-1-1-building-animations-with-claude-code]
- The pattern is the content-creator archetype from Foundation 3.2 put into practice [sources/playbooks-1-1-building-animations-with-claude-code]

## Relationships

- Specific instance of [[three-layer-routing]]
- Drives [[script-spec-build-render-pipeline]]
- Uses [[routing-table]] in the root `CLAUDE.md`
- Related to [[folder-as-workspace]]
