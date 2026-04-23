---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [fundamentals, tokens]
---

# context-window

The number of tokens an AI can hold and attend to at once. The window is finite; exceeding it causes degraded output, dropped earlier content, or outright failure. The whole motivation for the folder-as-workspace architecture is context-window scarcity: if an AI writing a blog post is also reading unrelated video production notes, tokens are spent on irrelevant material. Separating work into workspaces and loading only what the task requires is the mechanism that keeps the window available for the actual task.

## Claims

- Context window = the finite number of tokens an AI can see at once [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- Dumping unrelated work into one conversation wastes window on content that has nothing to do with the current task [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- The folder architecture's primary benefit is context-window hygiene - not organization for its own sake [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- Token cost is paid on every prompt for everything loaded - so every fact in `CLAUDE.md` and every file the routing table says to read is a recurring cost [sources/foundation-3-1-full-walkthrough]
- Claude's window is ~200K tokens; a typical meeting note is ~2,000 tokens; 15 notes fit comfortably when Claude Code fills the window from the file system rather than from pasted content [sources/foundation-4-2-claude-code-in-practice]
- In AI systems the window sits inside a hierarchy of weights, system prompt, retrieved context, and persistent memory - and unlike traditional memory the boundary between code and data is gone [sources/foundation-2-3-1953-word-game]
- The scaling motivation for task routing: 200K sounds huge until filled with irrelevant files; the folder architecture keeps per-task input clean [sources/foundation-4-5-where-this-goes]

## Relationships

- Measured in [[tokens]]
- Preserved by [[three-layer-routing]] and [[routing-table]]
- Primary concern that drives [[workspace-isolation]]
- Related to the broader theme that probabilistic/finite systems become reliable through architecture (see [[archive-1-2-2000-year-overnight-success]] on CPU branch prediction, cosmic-ray bit flips, and computing as reliability-engineering over chaos)
