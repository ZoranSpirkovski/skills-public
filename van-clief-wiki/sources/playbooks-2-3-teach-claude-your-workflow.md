---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, browser, shortcuts, module-2]
---

# playbooks-2-3-teach-claude-your-workflow

> Source: Implementation Playbooks course, Module 2 Lesson 2.3. Written lesson (video pending). File: `.wiki/raw/playbooks/lesson-2-3-teach-claude-your-workflow.md`.

## Summary

Record a browser workflow once and replay it with a single slash-command. The recording captures both actions (clicks, text inputs, scrolls) and microphone narration. The narration is the load-bearing piece: it gives Claude your intent ("I'm clicking the Export button") so the shortcut still works when the site's layout shifts. Three ways to create a shortcut: record, convert a conversation, or save a good prompt. Shortcuts can be scheduled for daily, weekly, or monthly runs. The lesson includes a "worth-automating" decision rubric and explicit guidance for handling logins (Claude records the steps but not the password; it pauses if the session is dead).

## Key claims

1. Claude for Chrome records the screen and the user's voice simultaneously to build a replayable shortcut.
2. Narration matters more than click coordinates. Spoken intent lets Claude re-find a button that moved; silent recordings break when layouts shift.
3. Three creation paths all produce the same artifact: a recorded workflow, a "Convert to task" button on an existing conversation, or "save prompt as shortcut" from a well-formed message.
4. Shortcuts run via `/` in the sidebar. They can be scheduled (daily, weekly, monthly) and a model choice can be fixed per shortcut.
5. Scheduled shortcuts require Chrome to be open and the machine awake; they do not run in the background if the browser is closed.
6. Four-question rubric for "worth automating": frequency (daily/weekly yes, twice-yearly no), step count (3-15 ideal), stability (same steps each time), and judgment-lightness (if you make different choices based on what you see, keep it manual).
7. Passwords are never stored. If the session is still alive, Claude continues; if not, Claude pauses and asks the user to sign in.
8. Recordings can be combined with follow-up prompts: "Run 'download weekly sales report' and then summarize what the numbers show."
9. Better recordings come from clean dry runs, simple names, short sequences (5-step shortcuts are more reliable than 25-step), and immediately running the shortcut after saving to verify.
10. A workflow-documentation template is supplied: name, trigger, starting point, steps, end state, variations, and a "worth automating" checklist.

## Entities mentioned

- [[van-clief]]
- [[claude-in-chrome]]

## Open questions

- How shortcuts interact with websites that use CAPTCHA loops is named as a failure mode but not resolved.
- Version drift across extensions is not discussed.
