---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, remote-control, setup, claude-code]
---

# stack-2-2-setting-up-remote-sessions

> Van Clief classroom, course "Building Your Stack", Module 2 Lesson 2. Raw file at `.wiki/raw/stack/lesson-2-2-setting-up-remote-sessions.md`. Video placeholder; lesson companion is the canonical text.

## Summary

Hands-on lesson for starting Remote Control. Three ways to start: server mode (`claude remote-control` or `claude rc`) where the terminal only shows status, interactive plus remote (`claude --remote-control` or `claude --rc`) where you can type at the terminal too, and mid-session enablement via the slash command `/remote-control` or `/rc`. Connect from the phone by scanning the QR code, using the session URL, or finding the session in claude.ai/code. Messages sync both ways; commands run locally. If the terminal process exits, the session ends. Tips: keep the terminal running, check power settings, name your sessions, start remote-enabled from the beginning if you might step away.

## Key claims

1. Three ways to start Remote Control. Server mode: `claude remote-control` or `claude rc`. Interactive plus remote: `claude --remote-control` or `claude --rc`. Mid-session: the `/remote-control` or `/rc` slash command inside an existing session.
2. Server mode's terminal only shows connection status; all interaction happens from the phone or browser. Press spacebar to toggle the QR code display.
3. Interactive plus remote gives the full terminal experience with remote access layered on top. Both sides stay in sync.
4. Three connection paths: scan the QR code, paste the session URL into any browser, or find the session in the Claude mobile app or claude.ai/code (computer icon plus green dot).
5. Remote sessions give full control, not read-only access: send messages, approve file changes, monitor tool activity, stop and redirect.
6. If the Claude app closes or you navigate away, the session keeps running on your machine and auto-reconnects when you return.
7. If your laptop sleeps, the session usually survives. If the terminal process exits, the session ends.
8. Name sessions explicitly with `--name "animation-build"` or `/rename animation-build` when running multiple projects.
9. Tip: start with `claude --rc` instead of plain `claude` if there is any chance you will step away. Easier than remembering `/rc` later.
10. Troubleshooting: can't find your session (process likely died), messages not syncing (check both network connections), API errors (restart the session), session died while away (check for hibernation or closed terminal).
11. Official docs live at `code.claude.com/docs/en/remote-control`.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]

## Open questions

- The lesson video is not yet produced.
- Behavior on non-macOS platforms (Windows, Linux) is not called out explicitly; commands are presumed cross-platform.
