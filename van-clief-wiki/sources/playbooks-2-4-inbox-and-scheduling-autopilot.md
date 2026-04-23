---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, browser, email, calendar, module-2]
---

# playbooks-2-4-inbox-and-scheduling-autopilot

> Source: Implementation Playbooks course, Module 2 Lesson 2.4. Written lesson (video pending). File: `.wiki/raw/playbooks/lesson-2-4-inbox-and-scheduling-autopilot.md`.

## Summary

Apply the Claude for Chrome extension to Gmail and Google Calendar. The loop is: summarize unread email, filter by criteria (today, sender, from-real-person), draft replies, then let Claude click Send with approval. Calendar work mirrors this (see today, add events, block focus time, move meetings). The core lesson is guardrails. Before any automation, decide what stays manual, what Claude can draft, and what Claude can act on. "Ask before acting" mode is the default recommendation for email because the extension can click Send. A sample constraint-rules file is given: never send without approval, never handle money or contracts, protect lunch, never schedule over existing events.

## Key claims

1. Gmail and Google Calendar are controlled by talking to the sidebar while the relevant tab is open; Claude sees what is visible.
2. The morning triage pattern: "summarize unread emails and flag anything urgent", then drill into specific threads ("draft a reply saying I'll send the invoice by end of day").
3. Claude drafts, you approve. Drafts appear in the sidebar; pasting into the compose box is a separate step ("put that in the reply field").
4. Claude can read an email and act on the calendar in one prompt ("read Mike's email about the call and add it to my calendar").
5. "Ask before acting" mode makes every sending or scheduling action a confirm step.
6. Three-tier guardrail decomposition: stays manual (money, contracts, boss, sensitive), draft-only (routine scheduling, confirmations, newsletter triage), fully automatic if trusted (archiving promos, labeling, summarizing).
7. Decision rule: "What happens if Claude gets this wrong? If not much, automate it. If real problems, keep it manual."
8. Scheduled shortcuts (from Lesson 2.3) combine with email: record morning inbox cleanup, schedule for 8am daily, busywork done before you open the laptop.
9. Claude cannot read email attachments or access unloaded emails; it only sees what is on screen.
10. Sample email-rules block: "never send without approval; never reply to anything involving money, contracts, or legal; flag anything that looks urgent even if I didn't ask." Sample calendar-rules block: "never delete events without asking; never schedule over existing events; protect 12-1pm as lunch."
11. The module closes the Ultimate Browser course track with three capabilities: extract data, record workflows, automate inbox and calendar.

## Entities mentioned

- [[van-clief]]
- [[claude-in-chrome]]
- [[gmail]]
- [[google-calendar]]

## Open questions

- Non-Gmail providers are called "slower or less accurate" but not characterized.
- Attachment-aware handling (even just filename summaries) is not covered.
