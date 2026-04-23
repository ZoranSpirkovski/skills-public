---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 6
tags: [core, pattern]
---

# workspace-isolation

The property that when Claude enters one workspace (e.g. Writing Room), only that workspace's context loads - not sibling workspaces (Production, Community). The routing table in `CLAUDE.md` tells Claude which workspace a task belongs to, and the workspace's own `CONTEXT.md` is the only per-workspace file loaded. Work in one workspace does not bleed into others. Freelancers use this to keep Client A's context separate from Client B's without Claude confusing the two.

## Claims

- When Claude is told to work in a given workspace, it reads only that workspace's `CONTEXT.md` - no sibling context bleed [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- This is the mechanism that preserves [[context-window]] budget for the actual task [sources/folder-system-transcript]
- Critical for freelancers: Client A's workspace contents never reach Client B's session [sources/foundation-3-1-full-walkthrough]
- Freelancer workspace blueprint encodes the isolation as an explicit rule: "never reference one client's information in another client's workspace" [sources/foundation-3-2-customizing-for-your-use-case]
- Lightest testable version: two separate folders with their own `CLAUDE.md` files; running tasks in each should produce visibly different behavior [sources/foundation-4-5-where-this-goes]
- The animation pipeline uses sibling workspaces (Script Lab, Animation Studio) so scripts are authored without loading the build pipeline and vice versa [sources/playbooks-1-1-building-animations-with-claude-code]
- Clean folder structure plus a single `CLAUDE.md` enables multiple Claude Code sessions in parallel on the same project without collision (one on components, one on content, one on research) [sources/playbooks-3-2-github-and-folder-structure]

## Relationships

- Enabled by [[three-layer-routing]] (specifically Layer 2 loading discipline)
- Guarded by rules declared in `CLAUDE.md` (the routing table and workspace-specific rules)
- Pre-requisite for multi-client or multi-project folder setups
