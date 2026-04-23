---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [product, google, integration]
---

# google-calendar

Google's calendar service. Used as the canonical orchestration example in Lesson 3.4. A small startup asked Van Clief to build an AI system to schedule their meetings. He built a Google Calendar integration instead and routed only the loose, semantic parts through Gemini. Built in under an hour. Works perfectly. The story is Van Clief's clean illustration of "knowing when boring beats brilliant". Returns later in Playbooks 2.4 as the target surface for the Claude for Chrome extension: Claude reads the calendar, adds events, blocks focus time, and moves meetings through the sidebar.

## Claims

- Replaced a proposed AI scheduling system as the orchestration-example integration in Lesson 3.4 [sources/archive-3-4-computational-orchestration]
- Integration built in under an hour, delegating only semantic-fit decisions to a language model [sources/archive-3-4-computational-orchestration]
- Controlled via the Claude for Chrome sidebar: view today/week, add events, block time, move meetings, find free slots [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Cannot access others' calendars unless shared and visible; reads what the tab shows [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Paired with Gmail for integrated inbox-plus-schedule prompts ("read Mike's email and add the call to my calendar") [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Recommended constraint rules: never delete without asking, never schedule over existing events, protect 12-1pm as lunch [sources/playbooks-2-4-inbox-and-scheduling-autopilot]

## Relationships

- Canonical example of the "judgment layer" in [[computational-orchestration]]
- Paired with [[google-gemini]] as the 10% AI layer in the 60/30/10 system
- Automated by [[claude-in-chrome]] inside the Playbooks Module 2 workflow
- Paired with [[gmail]] in the inbox-plus-schedule pattern
