---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, planning, prompt, module-3]
---

# playbooks-3-3-pre-build-planning-and-prompt-sequencing

> Source: Implementation Playbooks course, Module 3 Lesson 3.3. Written lesson (video pending). File: `.wiki/raw/playbooks/lesson-3-3-pre-build-planning-and-prompt-sequencing.md`.

## Summary

The full decomposition of the planning phase from Lesson 3.1, generalized beyond websites. Five steps run in Claude chat before any file is created: analyze what exists, write a briefing document for Claude, craft a first-prompt that bundles folder structure, deployment, scope, and an "ask me three questions" suffix, answer the alignment questions, and request a PRD. The method works for internal tools, content systems, and client work. The thesis in one line: "spend your thinking before you spend your tokens." Four to five planning prompts upfront, two or three build prompts, total under ten.

## Key claims

1. The five-step planning sequence precedes every file: (1) analyze existing, (2) briefing document, (3) first prompt with boundaries, (4) answer alignment questions, (5) request PRD.
2. Step 1 lives in Claude chat, not Claude Code. The browser session loads context about the current state.
3. Step 2 is the move that saves the most tokens long-term. The briefing document is markdown; it is written for Claude Code to read, not for the user.
4. Claude chat and Claude Code do not share memory. The markdown file is how you transfer context between them.
5. The first prompt bundles five jobs: folder structure request with `CLAUDE.md`, deployment target, scope boundaries ("we do not need user accounts yet"), tech-stack preference (or "let us decide together"), and the alignment-question suffix.
6. "Ask me three questions" forces Claude to process everything before building and surfaces gaps the user did not think to specify.
7. Step 4 answers are cheap. Answering an alignment question costs a few tokens. Discovering the same gap after 15 files exist costs hundreds in rework.
8. Step 5 requests a PRD markdown and explicitly says "do not start building yet." This is the last free checkpoint. Editing here is free; editing after code is expensive.
9. Why the method works: most people open Claude Code and start asking for things, accumulating mess by prompt 15. This method spends 4-5 prompts thinking, then 2-3 prompts building. Under ten total.
10. Generalized beyond websites: same sequence for internal tools (analyze current workflow, document, scope, align, PRD, build), content systems (taxonomy analysis, doc, scope, align, PRD, build), and client work (steps 1-2 during discovery call, steps 3-5 before showing the client anything).
11. Client-work application: the briefing document comes out of the discovery call as the tangible deliverable.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]

## Open questions

- Exact PRD template is referenced but not supplied here (the UX/UI Design Skill owns it).
- Post-PRD build-iteration prompts are mentioned as "2-3" but not enumerated.
