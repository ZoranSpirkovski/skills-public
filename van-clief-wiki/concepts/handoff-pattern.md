---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, mobile, workflow, prompts]
---

# handoff-pattern

Two explicit prompts that bracket a desk-to-mobile-to-desk transition. Desk to mobile: "I'm stepping away. Continue with [current task]. If you hit a blocker, describe it clearly and wait for my input. I'll check in from my phone." Mobile to desk: "What happened while I was away? Summarize progress and any decisions you need from me." The first prompt tells Claude you will not be watching closely so it should not ask unnecessary questions but should flag real blockers. The second prompt gets a concise status update so you are back in context without reading the whole log.

## Claims

- Desk-to-mobile prompt: "I'm stepping away. Continue with [current task]. If you hit a blocker, describe it clearly and wait for my input. I'll check in from my phone." [sources/stack-2-3-mobile-workflow-patterns]
- Mobile-to-desk prompt: "What happened while I was away? Summarize progress and any decisions you need from me." [sources/stack-2-3-mobile-workflow-patterns]
- First prompt purpose: Claude knows you are not watching closely, so it avoids unnecessary questions and flags real blockers clearly [sources/stack-2-3-mobile-workflow-patterns]
- Second prompt purpose: get back in context fast without re-reading the whole session log [sources/stack-2-3-mobile-workflow-patterns]

## Relationships

- Pairs with [[mobile-workflow-modes]]
- Runs on [[remote-control]]
- A behavioral counterpart to [[progress-md-pattern]] (which handles session-to-session), where handoff-pattern handles mid-session device transitions
