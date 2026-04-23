---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 8
tags: [tool, ide, microsoft]
---

# vs-code

Microsoft's free IDE. Used in the folder-system demos to show sidebars of files and folders side-by-side with Claude Code. Explicitly declared optional in both the folder-system talk and Foundation 3.1 - the architecture works equally well in a plain file explorer with Notepad.

## Claims

- Optional for the methodology - "you do not need VS Code to do any of this" [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- Convenient for managing many files: open without double-clicking, jump between files in a sidebar [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- Alternatives named: plain file explorer + Notepad, [[claude-cowork]], or forks like Cursor / Antigravity [sources/foundation-3-1-full-walkthrough]
- Named as one of the two recommended editors (with [[cursor-editor]]) for Foundation setup [sources/foundation-1-1-what-you-need]
- Claude Code VS Code extension installs from the marketplace; panel only appears when a file is open in a non-empty folder [sources/foundation-4-1-install-and-first-use]
- VS Code's built-in chat is a separate product from the Claude Code extension; users must distinguish the two [sources/foundation-4-1-install-and-first-use]
- With Claude Code, forms Level 3 on the [[tool-ladder]] and is where most people should land; move to Level 4 only when Level 3 hits a wall [sources/stack-1-1-starting-the-build-process]
- Van Clief's preferred IDE for animation work: file tree + preview + Claude Code in one window [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-2-illustrator-to-web-animations]
- Opens Claude Design exported zips unchanged; the design-system skill runs the same way as if opened directly in Claude Code [sources/playbooks-1-5-claude-design-folder-structure]

## Relationships

- Common host for [[claude-code]] sessions
- Declared optional for [[three-layer-routing]] and [[folder-as-workspace]]
- Parent editor of [[cursor-editor]] and other AI-native forks
