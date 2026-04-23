---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [tool, ai-agent, anthropic]
---

# claude-desktop

Anthropic's conversational / browser-based Claude interface. Used for thinking, planning, and challenging assumptions before work moves into [[claude-code]]. In the three-file minimum-viable folder pattern, supports Projects (upload `CLAUDE.md`/`CONTEXT.md`/`REFERENCES.md` as project knowledge) or plain paste-at-top-of-message as ways to give Claude persistent context.

## Claims

- Supports Projects for uploading `CLAUDE.md`/`CONTEXT.md`/`REFERENCES.md` as knowledge files Claude reads every conversation [sources/foundation-1-2-your-first-folder]
- Copy-paste-at-top workflow is the fallback when Projects aren't used [sources/foundation-1-2-your-first-folder]
- Downloadable from claude.ai/download; free tier works for learning prompting [sources/foundation-1-1-what-you-need] [sources/foundation-4-1-install-and-first-use]
- Cannot see user files directly; all context must be uploaded or pasted - same model as [[claude-code]], different reach [sources/foundation-4-1-install-and-first-use] [sources/foundation-4-2-claude-code-in-practice]
- Excels at thinking with the user: challenging assumptions, finding blind spots, pressure-testing ideas, structuring messy thinking, exploring trade-offs [sources/foundation-4-3-claude-desktop-thinking-partner]
- Projects are a browser-based lightweight version of the folder context pattern: persistent context loaded into every conversation inside the project [sources/foundation-4-3-claude-desktop-thinking-partner]

## Relationships

- Complementary to [[claude-code]] - "Desktop for decisions, Code for execution" is the paired workflow
- Entry point for [[claude-md-three-file-pattern]] users without terminal setup
- Part of [[three-interfaces]] alongside [[claude-code]] (VS Code and terminal forms)
