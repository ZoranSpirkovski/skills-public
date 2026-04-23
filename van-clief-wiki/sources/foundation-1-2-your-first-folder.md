---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, onboarding, three-file-pattern]
---

# foundation-1-2-your-first-folder

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~70–172. Part of the Foundation course (Module 1, Lesson 2).

## Summary

The onboarding lesson in Van Clief's Foundation course. Teaches the minimum-viable folder: a project folder containing three markdown files - `CLAUDE.md` (identity + rules), `CONTEXT.md` (current project), `REFERENCES.md` (background). Point Claude at it (via Claude Code, Projects, or paste) and the first response is already different. The lesson positions this as a stripped-down entry to the full three-layer architecture taught later in Module 3.

## Key claims

1. Every conversation in an untouched Claude starts from zero; structured files make Claude behave like someone who already knows the project from the first message.
2. Three files are sufficient for the first win: one for identity + rules, one for the current project, one for background.
3. Templates should be short - brackets filled in, not long paragraphs. Edit them whenever the project changes.
4. The pattern works equally via Claude Code (reads automatically on `cd` + `claude`), Claude Projects (upload as knowledge), or simple paste-at-top.
5. This is the entry point; the full three-layer system with routing tables and naming conventions is Foundation 3.1 and builds directly on these three files.

## Entities mentioned

- [[van-clief]] - author
- [[claude-code]] - the terminal agent
- [[claude-desktop]] - the browser-based Claude (referenced as "Claude in the browser")

## Open questions

- No routing table in this first-pass version; that primitive is deferred to Foundation 3.1.
- No naming conventions at this stage - deferred.
- The transition from three-file minimum to full multi-workspace architecture is sketched but not walked end-to-end until Module 3.
