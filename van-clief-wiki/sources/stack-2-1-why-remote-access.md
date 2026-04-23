---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, remote-control, mobile, claude-code]
---

# stack-2-1-why-remote-access

> Van Clief classroom, course "Building Your Stack", Module 2 Lesson 1. Raw file at `.wiki/raw/stack/lesson-2-1-why-remote-access.md`. Video placeholder (not yet recorded); lesson companion is complete.

## Summary

The opening of the Remote Access module. Claude Code now has Remote Control built in: start a session at your desk, scan a QR code, continue from your phone. Execution stays local; files, MCP servers, CLAUDE.md all stay on your machine. The mobile app is just a window into your local session. The feature enables async workflows, mobile monitoring, quick interventions, and voice input. Limitations: one session per machine, terminal must stay running, currently Max tier only, still being refined. The pattern it enables: start something at your desk, walk away, come back, session and context intact.

## Key claims

1. Remote Control is built into Claude Code: one command plus a QR code connects your phone to a session running on your machine.
2. What used to require SSH tunnels, web interfaces, or custom front-ends is now native.
3. Remote Control is not cloud computing. Execution happens on your machine. The mobile app and web interface are windows into the local session.
4. Local setup is irreplaceable. Cloud Claude Code starts fresh every time. Remote Control keeps everything.
5. Four use cases: async workflows (kick off a long build, close the laptop, check from your phone), mobile monitoring, quick interventions at decision points, voice input when typing is inconvenient.
6. Four limitations: one Remote Control session per machine, terminal must stay running (process death kills the session), currently requires Max tier ($100-200/month) with Pro coming, still has occasional bugs.
7. Before Remote Control you chose between local Claude Code (powerful but immobile) and web Claude Code (mobile but no local context). Remote Control gives both: local power plus mobile access.
8. Remote Control is a mobility tool, not a replacement for desk work. If the task needs full attention, stay at the desk.
9. Decision heuristic: use Remote Control when you are often away from your desk during builds, when builds run 30+ minutes, and if you have Max tier.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]

## Open questions

- The video for this lesson is marked Coming Soon; the companion text is canonical for now.
- Pro-tier availability date is unspecified.
