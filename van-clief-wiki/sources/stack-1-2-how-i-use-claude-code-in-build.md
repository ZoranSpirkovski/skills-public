---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, claude-code, prd, workspace, research]
---

# stack-1-2-how-i-use-claude-code-in-build

> Van Clief classroom, course "Building Your Stack", Module 1 Lesson 2. Raw file at `.wiki/raw/stack/lesson-1-2-how-i-use-claude-code-in-build.md`. Contains both a full video transcript and a polished lesson companion.

## Summary

The research and planning phase of the custom build. David's question (can I build a front-end UI to control and monitor Claude?) seeds the project. The obvious approach (direct Anthropic API calls from a new app) is rejected because API costs explode; instead the front-end wraps Claude Code and rides the subscription. Van Clief has Claude research existing repos (Claude Code Web, Op Code, Claude CLI UI), identifies what to borrow and what to cut, then asks Claude to write a PRD markdown that Claude Code will read when building. The PRD lives inside the existing Animation Studio workspace in a new `front-end/` subfolder, so Claude has context on the workflow it is wrapping.

## Key claims

1. David's question seeded the course: how do you build a front-end UI that lets you control and monitor Claude without burning API credits?
2. The architectural decision that shapes everything: build a front-end that controls Claude Code (riding the subscription), not one that replaces it with direct API calls.
3. Research first. Before writing code, ask Claude to survey existing open-source repos that do pieces of what you want.
4. The PRD does three jobs: forces decisions before code, creates persistent context for Claude across sessions, and can be audited by a second Claude instance.
5. PRD contents: what we are building, target user, existing repos and what to take, tech stack recommendations, features to cut, phases from MVP to full, and ordered steps to execute.
6. The PRD is a markdown file that gets read at the start of every session. It turns a stateless tool into something with memory.
7. Panel layout Van Clief wants: workflow map on the left (like a mind map, not a folder tree), file editor in the middle, Claude Code chat on the right. Multiple chats, collapsible panels, minimal design.
8. Build inside the existing workspace in a `front-end/` subfolder rather than a separate project, so Claude can reference the real animation pipeline while building its interface.
9. The existing repos had good ideas but too many features (provider switching, complex settings). Strip them to fit the workflow.
10. You can audit a PRD by feeding it into a second Claude session: "what is overcomplicated, what is missing, what would you simplify?"

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[claude-desktop]]
- [[vs-code]]
- [[claude-code-web]]
- [[op-code]]
- [[claude-cli-ui]]

## Open questions

- Exact repo URLs for Claude Code Web, Op Code, and Claude CLI UI are implied but not given here; the repo tour in 1.4 lists them.
- "Animation Studio" and "Script Lab" are mentioned as folders in Van Clief's existing workspace; no dedicated pages yet.
