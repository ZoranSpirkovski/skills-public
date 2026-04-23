---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [stack, persistence, stateful-prompting, workspace]
---

# workspace-as-memory

Claude does not remember between sessions. Your files do. The fix is to put everything Claude needs to know into the workspace so the workspace is the memory, not the context window. Project definition (PRD, CLAUDE.md, folder structure) lives there permanently. Progress markers (PROGRESS.md, STATUS.md) update regularly. Session notes capture key decisions when they would be frustrating to forget. Every session starts with "read CLAUDE.md and PROGRESS.md, summarize where we are" and ends with "update PROGRESS.md with what we accomplished and what's next." Claude is stateless; the workspace is stateful. Same pattern at every scale: single session, multi-device, team collaboration.

## Claims

- Normal Claude conversations are stateless; markdown files in the workspace persist [sources/stack-1-3-designing-for-your-use-case] [sources/stack-2-4-session-persistence-across-devices]
- Three layers of what to persist: project definition (always), progress markers (regularly), session notes (when frustrating to forget) [sources/stack-2-4-session-persistence-across-devices]
- The PRD turns a stateless tool into one with memory; the memory lives in the filesystem, not Claude's context window [sources/stack-1-3-designing-for-your-use-case]
- Long builds hit token limits. When Claude gets slow, start a new session and have Claude re-read the workspace files [sources/stack-1-3-designing-for-your-use-case] [sources/stack-2-4-session-persistence-across-devices]
- Reflex prompts: session start "Read CLAUDE.md and PROGRESS.md", session end "Update PROGRESS.md" [sources/stack-2-4-session-persistence-across-devices]
- Unexpected session ends are normal. Don't assume the last task completed; check the files [sources/stack-2-4-session-persistence-across-devices]
- The bigger pattern: Claude is stateless, the workspace is stateful. Same pattern at every scale [sources/stack-2-4-session-persistence-across-devices]
- Paired with Remote Control: Remote Control is short-term memory within a conversation, workspace files are long-term memory across conversations [sources/stack-2-4-session-persistence-across-devices]

## Relationships

- Operationalized by [[progress-md-pattern]] and [[prd-first-methodology]]
- Paired with [[remote-control]] to cover both short-term and long-term persistence
- Extension of [[folder-as-workspace]] into the time dimension: the folder remembers
- Runs on [[claude-code]] reading [[claude-md-three-file-pattern]] plus PROGRESS.md
- Uses [[markdown]] as its persistence format
