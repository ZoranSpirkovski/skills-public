---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, repos, research, references]
---

# stack-1-4-repo-tour-open-source-references

> Van Clief classroom, course "Building Your Stack", Module 1 Lesson 4. Raw file at `.wiki/raw/stack/lesson-1-4-repo-tour-open-source-references.md`. Curated research resource, updated as new repos appear.

## Summary

A curated list of open-source projects worth studying when building AI interfaces. Organized into four categories: Claude Code wrappers (Claude Code Web, Op Code, Claude CLI UI), custom chat UIs (Open WebUI, Lobe Chat), workflow and agent tools (n8n, Langflow), and design skills (UIUX Pro Skill). For each repo Van Clief notes what it does, what is worth studying, and what he would borrow or skip. The page is not a tutorial; it is a research map for anyone picking up pieces for their own build.

## Key claims

1. Don't clone all of these. Pick the ones relevant to what you are building. Read the code, see how they solved problems, take what is useful.
2. Claude Code Web: worth studying for session persistence, the websocket connection between front-end and Claude Code CLI, and their streaming-response approach.
3. Op Code: another Claude Code wrapper focused on project management with usage tracking, multi-project switching, and a config system. Too feature-heavy for Van Clief's needs but patterns are solid.
4. Claude CLI UI: a terminal UI (TUI) for Claude Code. Better visual organization while staying in the terminal. Worth studying for output parsing and keyboard navigation.
5. Open WebUI: self-hosted web interface supporting multiple LLM providers. Worth studying for the multi-provider abstraction layer if you need multiple backends.
6. Lobe Chat: polished open-source chat UI with plugins, agents, knowledge base. Worth studying for plugin architecture and file-upload patterns. Useful as a "full-featured reference" so you know what to cut when you build minimal.
7. n8n: visual node-based workflow automation tool, not AI-specific but increasingly used for AI. Worth studying for node-editor implementation and workflow state.
8. Langflow: visual framework for building LLM applications. Drag-and-drop for AI workflows. Worth studying for how they visualize chains and bridge visual representation to execution.
9. UIUX Pro Skill: not a repo to run but a skill package of prompts teaching Claude better design sense for front-end work. Worth studying as an example of how to create domain-specific skills.
10. Routing advice: building a Claude Code front-end, start with Claude Code Web and Op Code. Custom chat, look at Open WebUI and Lobe Chat. Workflow visualization, study n8n and Langflow. Want Claude to build prettier front-ends, get UIUX Pro Skill.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[claude-code-web]]
- [[op-code]]
- [[claude-cli-ui]]
- [[open-webui]]
- [[lobe-chat]]
- [[n8n]]
- [[langflow]]
- [[uiux-pro-skill]]

## Open questions

- Exact repo URLs are not embedded in this source; the page is described as "updated as new repos appear".
- Van Clief says "[LINK TO future lessons when available]" - more stack lessons are planned beyond 1.4.
