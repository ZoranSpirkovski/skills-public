---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, claude-code, workflow, iteration]
---

# foundation-4-2-claude-code-in-practice

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~1934-2003. Foundation Module 4, Lesson 2 (Session 2 of 5).

## Summary

Claude Code is not smarter than Claude Desktop; it is the same model with more reach. The difference is the iteration loop: Read, Think, Write, Check, Adjust. Desktop runs that loop once and stops. Claude Code runs it until the job is done. The worked example is 15 meeting notes to analyse: Desktop takes about an hour of copy-paste; Claude Code takes 90 seconds with one prompt pointed at the folder. Context-window math is covered (a typical meeting note is ~2,000 tokens, 15 of them fit well inside the ~200K window). Tips: be specific, write outputs directly to files, and iterate by describing the fix rather than starting over.

## Key claims

1. Claude Code uses the same model as Claude Desktop; the difference is reach, not intelligence.
2. The Claude Code loop is Read → Think → Write → Check → Adjust; it continues until the task completes.
3. Example: 15 meeting notes summarized by project takes ~1 hour in Desktop (15 uploads, manual combine) vs 90 seconds in Claude Code (one folder-pointed prompt).
4. Context-window math: ~200K tokens; a typical meeting note ~2,000 tokens; 15 notes fit easily. Claude Code fills working memory from the file system, not the clipboard.
5. Best practices: write specific tasks (not "analyze this"), tell Claude where to save output, iterate by describing what's wrong rather than restarting.
6. Desktop is better when the task is "help me think through a decision"; Claude Code wins when the task involves reading/writing files.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[claude-desktop]]

## Open questions

- The video for this session is marked "Coming Soon" in the source; future update may deepen the claims.
- The 200K context-window number is current-generation Claude; will drift as models change.
