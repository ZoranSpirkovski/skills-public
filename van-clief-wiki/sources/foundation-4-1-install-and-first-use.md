---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, claude-code, install, interfaces]
---

# foundation-4-1-install-and-first-use

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~1777-1933. Foundation Module 4, Lesson 1 (Session 1 of 5).

## Summary

The hands-on install session. Three ways to use Claude (Desktop/claude.ai, Claude Code in VS Code, Claude Code in terminal) are not three different AIs but one model with three interfaces. The difference is what each interface lets the model see and do. Desktop cannot reach files; Claude Code can. The lesson walks through installing Claude Desktop, Node.js, Claude Code via npm, and the Claude Code VS Code extension, with a troubleshooting list. Ends with a hands-on comparison exercise: run the same task in Desktop and in VS Code to feel the manual-work gap.

## Key claims

1. Three interfaces, one model: Desktop (conversation layer), Claude Code in VS Code (editor layer), Claude Code in terminal (command-line layer). Same brain, different reach.
2. Desktop can only see uploaded files and cannot edit anything; Claude Code sees files in the current folder and can edit them.
3. Install order: Claude Desktop from claude.ai/download, Node.js LTS from nodejs.org, Claude Code via `npm install -g @anthropic-ai/claude-code`, then the Claude Code VS Code extension from the marketplace.
4. Trip-up: in VS Code, the Claude panel does not appear in an empty folder; open a file first. VS Code's native chat is a separate product from the Claude Code extension.
5. The value-unlock moment is the comparison: summarize the same file in Desktop (upload + copy-paste) vs VS Code (Claude reads the folder directly). Same answer quality; very different manual-work cost.
6. Claude Code is what makes the full folder architecture from Module 3 operational - it reads `CLAUDE.md`, navigates workspaces, loads per-workspace context, follows the routing table.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[claude-desktop]]
- [[vs-code]]

## Open questions

- Cursor, Windsurf, Copilot, Antigravity are named as VS Code forks or alternatives; not given entities yet.
- The exact URLs (claude.ai/download, nodejs.org) are load-bearing for a first-time user; kept in the source.
