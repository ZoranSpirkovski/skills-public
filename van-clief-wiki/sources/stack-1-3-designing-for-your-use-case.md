---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, claude-code, plan-mode, sub-agents, workspace]
---

# stack-1-3-designing-for-your-use-case

> Van Clief classroom, course "Building Your Stack", Module 1 Lesson 3. Raw file at `.wiki/raw/stack/lesson-1-3-designing-for-your-use-case.md`. Contains both a full working-session transcript and a polished lesson companion.

## Summary

A live build session. The PRD is done, the workspace is set up, Claude Code runs through the build while Van Clief observes. The abstract goal is articulated: not a prettier front-end but a control surface that lets Van Clief fluidly switch between "I'm driving" and "Claude's driving". Claude enters plan mode, spawns sub-agents (visible on Claude 4.6), runs bash searches, does web fetches. When told to clone repos, Claude realizes it is more efficient to fetch only the specific files needed. The session shows why the PRD plus workspace-as-memory plus stateful prompting pattern works in practice: markdown files persist, Claude's context does not.

## Key claims

1. The abstract goal of the build is explicitly: "a control surface that I can fluidly switch, between I'm driving or Claude's driving".
2. Sometimes you want to edit every individual file; sometimes you want to automate the whole pipeline. The interface must let you switch modes without friction.
3. Plan mode vs execution mode: plan mode has Claude think through steps before acting; execution mode runs commands, writes code, fetches files. Claude usually chooses on its own.
4. Claude 4.6 spawns sub-agents to save tokens. The main Claude orchestrates while sub-agents handle fetching and studying. This looks like Claude doing multiple things at once, and it effectively is.
5. Claude can make better decisions than your instructions. Told to clone the repos, Claude chose to search and fetch only needed files. Let Claude be smarter than your instructions when it makes sense.
6. Workspace context matters. Building inside the Animation Studio folder means Claude's `find` command sees the real Script Lab, specs, renders. Outside the workspace Claude would have no context.
7. Stateful prompting: normal Claude conversations are stateless, but a markdown file persists. The PRD turns a stateless tool into one with memory. The memory lives in the filesystem, not the context window.
8. Markdown is load-bearing for this pattern: small (low token cost), Claude reads it well, easy to edit, persists between sessions, convertible to formatted Google Docs if needed.
9. Long builds hit token limits. When Claude gets slow, start a new session and have Claude re-read the PRD. The workspace is the continuity.
10. The PRD keeps the build aligned. When Claude drifts, point back to the document.
11. You cannot get a perfect build in one session. You get progress. The workspace accumulates progress across sessions.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[vs-code]]
- [[claude-code-web]]
- [[op-code]]

## Open questions

- Specific Claude 4.6 sub-agent behavior is described experientially but not technically; details for when sub-agents are or are not spawned are not in this source.
- "Plan mode vs execution mode" is named but not documented anywhere else in the wiki yet.
