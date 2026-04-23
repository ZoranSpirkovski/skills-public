---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, persistence, workspace, progress]
---

# progress-md-pattern

A single PROGRESS.md (or STATUS.md) file at the root of each project, updated regularly, that tracks where the work is. Sections: Current Status (one sentence), Last Session (Completed, In Progress, Blocked, Next), Decisions Made (with brief reasoning), Open Questions. Updated before walking away, after significant decisions, and when hitting token limits. Paired with session-start and session-end prompts that become reflexes: start with "Read CLAUDE.md and PROGRESS.md. Summarize: what is this project, where are we, what should we work on next?" End with "Update PROGRESS.md with what we accomplished this session and what's next." Takes 30 seconds, saves 10 minutes of re-orienting.

## Claims

- PROGRESS.md lives at the root of each project and tracks current state [sources/stack-2-4-session-persistence-across-devices]
- Template sections: Current Status, Last Session (Completed / In Progress / Blocked / Next), Decisions Made, Open Questions [sources/stack-2-4-session-persistence-across-devices]
- Update triggers: before walking away, after significant decisions, at token limits, before session ends [sources/stack-2-4-session-persistence-across-devices]
- Session-start reflex prompt: "Read CLAUDE.md and PROGRESS.md. Summarize: what is this project, where are we, what should we work on next?" [sources/stack-2-4-session-persistence-across-devices]
- Session-end reflex prompt: "Update PROGRESS.md with what we accomplished this session and what's next." [sources/stack-2-4-session-persistence-across-devices]
- Reconnection workflow is three steps: Orient (read files), Verify (does progress match reality in code?), Continue (work on next task) [sources/stack-2-4-session-persistence-across-devices]
- Takes 30 seconds to update, saves 10 minutes next session [sources/stack-2-4-session-persistence-across-devices]

## Relationships

- Concrete instance of [[workspace-as-memory]]
- Pairs with [[prd-first-methodology]]: PRD is "what we are building", PROGRESS.md is "where we are"
- Complements [[claude-md-three-file-pattern]] at the project root
