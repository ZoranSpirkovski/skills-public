---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [email, google, tool]
---

# gmail

Google's webmail product. Used in Lesson 2.4 as the target application for the Claude for Chrome extension. Claude reads what is visible in the Gmail tab, summarizes unread, filters by sender or topic, drafts replies into the sidebar, and (with approval) pastes replies into the compose field. Claude cannot read attachments or access unloaded emails; it sees what is on screen.

## Claims

- Target application for the morning-triage workflow taught in Module 2 [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Claude can read visible emails, scroll, open threads, draft replies, paste into compose, click Send with approval, and archive/delete/label [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Claude cannot read attachments or access emails that are not on screen [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Other providers work but are "slower or less accurate" per the lesson [sources/playbooks-2-4-inbox-and-scheduling-autopilot]

## Relationships

- Automated by [[claude-in-chrome]] with [[ask-before-acting-mode]]
- Paired with [[google-calendar]] for the combined inbox-plus-schedule pattern
