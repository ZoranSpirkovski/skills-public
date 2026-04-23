---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 4
tags: [entry-point, minimum-viable]
---

# claude-md-three-file-pattern

The minimum-viable folder in Van Clief's Foundation course: a project folder containing exactly three markdown files - `CLAUDE.md` (identity + rules), `CONTEXT.md` (what the current project is, what good looks like, what to avoid), and `REFERENCES.md` (background material, examples, links). Five minutes of work. Claude's responses change on the first message. This is the entry point; the full [[three-layer-routing]] architecture with routing tables and naming conventions is the graduation path.

## Claims

- Three files are sufficient for a noticeable first-message improvement [sources/foundation-1-2-your-first-folder]
- Structure:
  - `CLAUDE.md`: identity - who this is, rules for behavior
  - `CONTEXT.md`: current project - what we're building, what good looks like, what to avoid
  - `REFERENCES.md`: background - examples, links, notes [sources/foundation-1-2-your-first-folder]
- Works via any route: [[claude-code]] (auto-reads on `cd`), [[claude-desktop]] Projects (upload as knowledge), or paste-at-top of first message [sources/foundation-1-2-your-first-folder]
- Explicitly positioned as the starter, not the full system [sources/foundation-1-2-your-first-folder]
- A narrower project-level variant uses a five-section `CLAUDE.md` (overview, tech stack, commands, conventions, avoid) - 15 lines is enough, the file changes Claude Code's behavior visibly on the first run [sources/foundation-4-4-making-claude-understand]
- For website builds, keep the root `CLAUDE.md` under 50 lines; every token is re-read on every prompt, so bloat costs continually [sources/playbooks-3-2-github-and-folder-structure]
- The first Claude Code prompt for a new project should explicitly request a folder structure with `CLAUDE.md` as part of the bundle of folder + deployment target + scope + alignment question [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing] [sources/playbooks-3-1-build-and-deploy-website]

## Relationships

- Entry point for [[three-layer-routing]] - the three files become Layer 1 + a single Layer 2 context
- Missing the [[routing-table]] and [[naming-conventions-as-db]] (those are introduced later)
- Used with [[claude-code]], [[claude-desktop]], or paste workflows
