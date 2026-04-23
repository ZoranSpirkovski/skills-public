---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 4
tags: [anthropic, browser, extension, tool]
---

# claude-in-chrome

Anthropic's browser extension that embeds Claude as a sidebar inside Chrome or Edge. Powered by Sonnet 4.5 (per Anthropic's announcement). Reads the current page, clicks buttons, fills forms, navigates across tabs, and drafts email. Central tool for the Implementation Playbooks Module 2 (Browser Flow). Requires a paid Claude plan and works only in Chrome and Edge at time of writing.

## Claims

- Requires a paid Claude plan (Pro, Max, Team, Enterprise) and works in Chrome or Edge; Brave and Arc do not work yet [sources/playbooks-2-1-setting-up-claude-in-chrome]
- Powered by Sonnet 4.5, "Anthropic's state-of-the-art model for computer use" per the product announcement [sources/playbooks-2-1-setting-up-claude-in-chrome]
- Restarting Chrome after install initializes the native messaging host; skipping this step is the source of "90%" of connection errors [sources/playbooks-2-1-setting-up-claude-in-chrome]
- Needs two browser permissions: read/change data on sites visited, and access to tabs [sources/playbooks-2-1-setting-up-claude-in-chrome]
- Ships with prompt-injection protection, site-level permissions, and an ask-before-acting mode for sensitive actions [sources/playbooks-2-1-setting-up-claude-in-chrome]
- Pauses at login screens and CAPTCHAs by design [sources/playbooks-2-1-setting-up-claude-in-chrome] [sources/playbooks-2-3-teach-claude-your-workflow]
- Reads what is on screen: text, tables, prices, descriptions, links, legible image text. Does not read content behind login walls, dropdown-only content, PDFs, or files [sources/playbooks-2-2-structured-data-from-any-page]
- Handles pagination, scroll-to-load, detail-page expansion, and multi-tab comparison [sources/playbooks-2-2-structured-data-from-any-page]
- Records browser workflows with microphone narration to build replayable shortcuts triggered by `/` [sources/playbooks-2-3-teach-claude-your-workflow]
- Shortcuts can be scheduled daily, weekly, or monthly; Chrome must stay open and the machine awake for them to run [sources/playbooks-2-3-teach-claude-your-workflow]
- Used to summarize unread Gmail, draft replies (without sending), and manage Google Calendar via the sidebar [sources/playbooks-2-4-inbox-and-scheduling-autopilot]

## Relationships

- Product of [[anthropic]]
- Runs [[ask-before-acting-mode]] as the primary safety primitive
- Hosts [[chrome-shortcut-recording]]
- Acts on [[gmail]] and [[google-calendar]] in Module 2 workflows
