---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [tools, interfaces, claude]
---

# three-interfaces

Van Clief's framing of Claude availability: one model, three interfaces. Claude Desktop (conversation layer, browser or app), Claude Code in VS Code (editor layer, reads and edits files in the open folder), Claude Code in terminal (command-line layer, same capabilities without the IDE). Same model behind all three. The difference is what each interface lets the model see and do. Desktop cannot reach files directly; the other two can. The pairing recipe is "Desktop for decisions, Code for execution": 15 minutes of thinking in Desktop saves 90 minutes of building the wrong thing in Code.

## Claims

- Three interfaces, one model: Claude Desktop (conversation), Claude Code in VS Code (editor), Claude Code in terminal (command line) [sources/foundation-4-1-install-and-first-use]
- Desktop cannot see your files directly; Claude Code can read and edit files in the current folder [sources/foundation-4-1-install-and-first-use]
- The quality of answer is the same across all three; the difference is manual work around the answer [sources/foundation-4-1-install-and-first-use]
- Desktop is better for thinking with you: challenging assumptions, finding blind spots, pressure-testing ideas [sources/foundation-4-3-claude-desktop-thinking-partner]
- Code is better for reading and writing files, running tasks that iterate on output [sources/foundation-4-3-claude-desktop-thinking-partner]
- The "Desktop for decisions, Code for execution" pairing saves time because planning in the wrong interface wastes both [sources/foundation-4-3-claude-desktop-thinking-partner]

## Relationships

- Instantiated by [[claude-desktop]], [[claude-code]], and the terminal form of [[claude-code]]
- Feeds into [[three-layer-routing]] - the folder architecture runs on Claude Code specifically
- Orthogonal to [[tool-ladder]]: three-interfaces is about Claude's access surface, tool-ladder is about how much UI you build around it
