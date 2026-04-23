---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [tool, open-source, claude-code-wrapper]
---

# claude-code-web

An open-source web-based front-end for [[claude-code]]. Runs Claude Code through a browser interface instead of the terminal. Studied as a reference during Van Clief's Building Your Stack front-end build. Notable for session persistence, websocket connection between front-end and Claude Code CLI, and streaming responses.

## Claims

- Web-based front-end that wraps Claude Code in a browser interface [sources/stack-1-4-repo-tour-open-source-references]
- Session persistence patterns are worth borrowing: close the browser, come back to the same conversation [sources/stack-1-4-repo-tour-open-source-references]
- Uses a websocket connection between front-end and the Claude Code CLI [sources/stack-1-4-repo-tour-open-source-references]
- Van Clief borrowed the session-persistence pattern from it for his own build [sources/stack-1-4-repo-tour-open-source-references]
- Named alongside [[op-code]] as the first two repos to study if you are building a Claude Code front-end [sources/stack-1-4-repo-tour-open-source-references]
- Van Clief's build spawned sub-agents that fetched only specific files from this repo rather than cloning it whole [sources/stack-1-3-designing-for-your-use-case]
- Surveyed by Claude during the initial research phase for the Van Clief front-end build [sources/stack-1-2-how-i-use-claude-code-in-build]

## Relationships

- Wraps [[claude-code]]
- Paired with [[op-code]] and [[claude-cli-ui]] as the Claude Code wrapper category on [[tool-ladder]] Level 4
- Reference repo for Van Clief's [[control-surface]] build
