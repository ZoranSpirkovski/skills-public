---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, persistence, workspace-as-memory, progress]
---

# stack-2-4-session-persistence-across-devices

> Van Clief classroom, course "Building Your Stack", Module 2 Lesson 4. Raw file at `.wiki/raw/stack/lesson-2-4-session-persistence-across-devices.md`. Video placeholder; lesson companion is canonical. Module 2 closer.

## Summary

Two kinds of persistence. Remote Control handles short-term persistence within a session across devices. Workspace files handle long-term persistence across sessions. Claude's memory does not persist between sessions; your files do. The fix: make the workspace the memory. Keep a PRD (project definition), a CLAUDE.md (structure), and a PROGRESS.md (current status) at the root. Start every session by reading these; end every session by updating PROGRESS.md. This turns the workspace into stateful memory while Claude stays stateless. Session-start and session-end prompts become reflexes. The pattern scales from single sessions to multi-device work to team collaboration: same pattern at every scale.

## Key claims

1. Two kinds of persistence. Remote Control gives within-session persistence across devices. Workspace files give across-session persistence when sessions end.
2. Claude's memory does not persist between sessions. Your files do. The fix: put everything Claude needs to know in the workspace.
3. Three layers of what to persist. Project definition (PRD, CLAUDE.md, folder structure) always. Progress markers (PROGRESS.md, STATUS.md) regularly. Session notes (key decisions, reasons) when they would be frustrating to forget.
4. The PROGRESS.md template has sections: Current Status, Last Session (Completed, In Progress, Blocked, Next), Decisions Made, Open Questions.
5. Update PROGRESS.md before walking away, after significant decisions, and when hitting token limits.
6. Reconnection workflow has three steps. Orient ("Read CLAUDE.md and PROGRESS.md. Summarize where we are."), Verify (does the progress file match reality in the code?), Continue ("Let's continue with [next task]").
7. Remote Control and workspace persistence pair together. Remote Control is short-term memory within a conversation. Workspace files are long-term memory across conversations.
8. Unexpected session ends are normal. Don't assume the last task completed; check the files and ask Claude to assess.
9. Two reflex prompts. Session start: "Read CLAUDE.md and PROGRESS.md. Summarize: what is this project, where are we, what should we work on next?" Session end: "Update PROGRESS.md with what we accomplished this session and what's next."
10. The bigger pattern: the folder architecture is the source of truth. Claude is stateless; the workspace is stateful. Same pattern at every scale: single session, multi-device, team collaboration.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]

## Open questions

- The lesson video is not yet produced.
- How PROGRESS.md interacts with multi-project or multi-workspace setups is not explored here.
