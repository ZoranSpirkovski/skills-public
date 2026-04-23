---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, custom-ui, prd, tool-ladder]
---

# stack-1-1-starting-the-build-process

> Van Clief classroom, course "Building Your Stack", Module 1 Lesson 1. Raw file at `.wiki/raw/stack/lesson-1-1-starting-the-build-process.md`.

## Summary

Opening lesson of the Building Your Stack course. Before writing any code, climb the tool ladder: Claude Projects, Claude Cowork, VS Code plus Claude Code, and only then a custom front-end. Anthropic keeps shipping native features that replace custom builds, so the philosophy is to know how to build custom but always ask whether you need to. The course is a behind-the-scenes build of a control surface for Van Clief's animation workflow: workflow map on the left, file editor in the middle, Claude Code chat on the right, with a fluid switch between "I'm driving" and "Claude's driving". The build starts with a PRD (product requirements document) in markdown that lives in the workspace and gets read at the start of every session.

## Key claims

1. The tool ladder has four levels: Level 1 Claude Projects on claude.ai, Level 2 Claude Cowork, Level 3 VS Code plus Claude Code, Level 4 custom front-end. Each level adds both complexity and capability.
2. Most people should land at Level 3 (VS Code plus Claude Code) and only move to Level 4 when they hit a wall Level 3 cannot solve.
3. Anthropic keeps replacing custom-build features with native ones. Features that required custom builds a year ago now exist in the default interface.
4. The course is a behind-the-scenes project: session recordings plus written companions. It is not a step-by-step tutorial.
5. The project being built is a control surface for Van Clief's animation workflow. The key insight is switching between "I'm driving" and "Claude's driving" modes fluidly.
6. Before any code, research existing repos, pull the parts that work, strip away what you do not need, build around your existing folder structure. "Don't reinvent the wheel. Make a better wheel. Make the wheel yours."
7. Before any code, Claude creates a PRD: a markdown file describing what is being built, repos being pulled from, stacks, what to keep and cut, phases from MVP to full version.
8. The PRD lives in the workspace and gets read at the start of every session. Markdown is low token cost, easy for Claude to read, and editable anywhere.
9. Build the front-end inside the existing workspace, not in a separate folder, so Claude can reference the actual workflow while building the tool around it.
10. Work in sessions. Claude runs out of tokens; you run out of energy. Each session picks up from the last because PRD and workspace context persist.
11. Course prerequisite: Foundation course or equivalent comfort with Claude Code.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[claude-cowork]]
- [[vs-code]]

## Open questions

- Exact link to "David" (the community member whose question seeded the build) is not resolved.
- "Claude Projects" is named as Level 1 but has no entity page yet; may be worth creating if cited again.
