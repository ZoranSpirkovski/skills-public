---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [stack, remote-control, mobile, claude-code]
---

# remote-control

Claude Code's built-in feature for connecting a phone or browser to a session running on your machine. Start a session at your desk, scan a QR code or open the session URL, continue from anywhere. Execution stays local; files, MCP servers, CLAUDE.md stay on your machine. The mobile app and web interface are windows into your local session. Commands route to your machine; results stream back. Three start modes: server-only (`claude rc`), interactive plus remote (`claude --rc`), and mid-session enablement via `/rc`. Current limits: one Remote Control session per machine, terminal must stay running, Max tier only for now, still being refined.

## Claims

- Claude Code has Remote Control built in. One command plus a QR code connects a phone to a local session [sources/stack-2-1-why-remote-access]
- Not cloud computing. Execution, files, MCP servers, CLAUDE.md all stay on the user's machine. The mobile app is a window into the local session [sources/stack-2-1-why-remote-access]
- Three start modes: server mode `claude remote-control` or `claude rc`, interactive plus remote `claude --remote-control` or `claude --rc`, mid-session `/remote-control` or `/rc` [sources/stack-2-2-setting-up-remote-sessions]
- Press spacebar in server mode to toggle the QR code display [sources/stack-2-2-setting-up-remote-sessions]
- Three connection paths: scan QR, paste session URL into any browser, find the session in the Claude app or claude.ai/code [sources/stack-2-2-setting-up-remote-sessions]
- Full control from the phone: send messages, approve file changes, monitor tool activity, stop and redirect [sources/stack-2-2-setting-up-remote-sessions]
- Four limitations: one session per machine, terminal must stay running (process death kills the session), Max tier only currently, still has occasional bugs [sources/stack-2-1-why-remote-access]
- Solves "AI coding tied to your desk": before this, you chose local power or mobile access. Remote Control gives both [sources/stack-2-1-why-remote-access]
- Pairs with [[workspace-as-memory]]: Remote Control is short-term memory within a conversation, workspace files are long-term memory across conversations [sources/stack-2-4-session-persistence-across-devices]
- Sessions can be named explicitly with `--name` or renamed with `/rename` [sources/stack-2-2-setting-up-remote-sessions]

## Relationships

- Built into [[claude-code]]
- Enables [[mobile-workflow-modes]] and the [[handoff-pattern]]
- Paired with [[workspace-as-memory]] for across-session persistence
- Currently requires a [[van-clief]]-era Max subscription to use
