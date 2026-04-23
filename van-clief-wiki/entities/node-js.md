---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [runtime, javascript, tool]
---

# node-js

JavaScript runtime that runs code on the local machine. Required dependency for [[claude-code]] (installed via `npm`) and for [[remotion]]. Van Clief recommends installing it for anyone getting into AI-native work because it enables `npm` and `npx` commands that install packages from GitHub and elsewhere without browser-based downloads.

## Claims

- Required for Claude Code (`npm install -g @anthropic-ai/claude-code`) [sources/playbooks-1-1-building-animations-with-claude-code]
- Required for Remotion's render pipeline [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-3-ai-animation-workflow-companion]
- Recommended as a baseline install for anyone using AI in business; enables the `npm`/`npx` package-install flow [sources/playbooks-1-1-building-animations-with-claude-code]
- Claude can walk the user through installation on request [sources/playbooks-1-1-building-animations-with-claude-code]

## Relationships

- Dependency of [[claude-code]] and [[remotion]]
- Installed from nodejs.org
