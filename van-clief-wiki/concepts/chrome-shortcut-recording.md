---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [browser, automation, shortcuts]
---

# chrome-shortcut-recording

Record a browser workflow once; replay it with a slash-command. The Claude for Chrome extension captures both screen actions (clicks, text, scrolls) and microphone narration. Narration is the load-bearing piece: it gives Claude the user's intent ("I'm clicking the Export button") so the shortcut survives when a site's layout shifts. Shortcuts can be created three ways: from a live recording, by converting an existing conversation, or by saving a well-formed prompt. They can be scheduled to run daily, weekly, or monthly, provided Chrome stays open. A decision rubric decides what is worth automating at all.

## Claims

- Recording captures screen actions plus microphone audio in one pass [sources/playbooks-2-3-teach-claude-your-workflow]
- Spoken intent outperforms click coordinates. Silent recordings break when layouts shift; narrated recordings adapt [sources/playbooks-2-3-teach-claude-your-workflow]
- Three equivalent creation paths: record a workflow, "convert to task" on a conversation, or save a prompt as a shortcut [sources/playbooks-2-3-teach-claude-your-workflow]
- Shortcuts run via `/` in the sidebar [sources/playbooks-2-2-structured-data-from-any-page] [sources/playbooks-2-3-teach-claude-your-workflow]
- Scheduling requires Chrome open and the machine awake; they do not run headless [sources/playbooks-2-3-teach-claude-your-workflow]
- Four-question worth-automating rubric: frequency (daily/weekly yes), step count (3-15 ideal), stability (same steps each time), judgment-lightness (no per-run decisions) [sources/playbooks-2-3-teach-claude-your-workflow]
- Passwords are never stored; Claude pauses at login if the session is dead [sources/playbooks-2-3-teach-claude-your-workflow]
- Short recordings (5 steps) are more reliable than long ones (25 steps); break big tasks into smaller shortcuts [sources/playbooks-2-3-teach-claude-your-workflow]
- Recorded shortcuts compose with follow-up prompts: "run [shortcut] and then summarize the numbers" [sources/playbooks-2-3-teach-claude-your-workflow]

## Relationships

- Lives inside [[claude-in-chrome]]
- Complements [[ask-before-acting-mode]] for trusted repeat tasks
- Candidate workflows align with the morning-inbox pattern from Gmail automation
