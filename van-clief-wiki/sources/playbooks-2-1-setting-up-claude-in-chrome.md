---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, browser, module-2, setup]
---

# playbooks-2-1-setting-up-claude-in-chrome

> Source: Implementation Playbooks course, Module 2 Lesson 2.1. Short Anthropic marketing transcript plus a written install guide. File: `.wiki/raw/playbooks/lesson-2-1-setting-up-claude-in-chrome.md`.

## Summary

Install the Claude for Chrome extension and connect it to a paid Claude plan. The lesson is a five-minute setup: install, restart Chrome, pin the extension, sign in, grant permissions, test with a prompt, and review the safety basics. Only Chrome and Edge are supported (other Chromium browsers do not work yet). The short embedded Anthropic video positions the extension around home-renovation budgeting as the usage example and names "Ask before acting" mode and prompt-injection protections as core safety primitives.

## Key claims

1. Claude for Chrome requires a paid Claude plan (Pro, Max, Team, or Enterprise) and works in Chrome or Edge only. Brave and Arc are unsupported at time of writing.
2. The load-bearing setup step is restarting Chrome fully after install; this initializes the native messaging host. Connection errors are "90% of the time" fixed by restarting.
3. The extension needs two browser permissions: read/change data on sites visited, and access to tabs.
4. "Ask before acting" mode is the primary safety primitive; Claude pauses and asks before taking sensitive actions like making purchases.
5. Claude pauses for manual handling at logins and CAPTCHAs by design.
6. Prompt-injection protection and site-level permissions are built in; certain sites (banking, some corporate intranets, some Google properties) are intentionally blocked.
7. The powering model is Sonnet 4.5 (per the embedded Anthropic announcement transcript).
8. First-test prompts are trivial: "What page am I on?" or "Summarize this page."

## Entities mentioned

- [[van-clief]]
- [[claude-in-chrome]]
- [[anthropic]]

## Open questions

- No link is given to the Anthropic publisher page for the extension.
- Full list of blocked sites is not enumerated.
