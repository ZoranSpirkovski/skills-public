---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [safety, browser, guardrails]
---

# ask-before-acting-mode

The primary safety primitive in the Claude for Chrome extension. When enabled, Claude states what it plans to do, waits for the user to approve, and only then acts. The mode exists because the extension can click Send, submit forms, and make purchases. It is the recommended default for email and calendar automation, where a wrong action causes real consequences. The principle behind it is the same constraint-setting taught in Foundation 1.3: decide what Claude can do, what Claude can draft, and what stays fully manual, before you start.

## Claims

- Ask-before-acting makes Claude announce the intended action and wait for approval before executing [sources/playbooks-2-1-setting-up-claude-in-chrome] [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Recommended default for email and calendar automation because the extension can click Send [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Claude pauses at logins and CAPTCHAs by design, regardless of the mode [sources/playbooks-2-1-setting-up-claude-in-chrome]
- Used alongside a three-tier decomposition of tasks: stays manual (money, contracts, sensitive), draft-only (routine scheduling, simple confirms), fully automatic only if the downside is low (archiving promos, labeling) [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Decision rule: "what happens if Claude gets this wrong? If not much, automate. If real problems, keep it manual." [sources/playbooks-2-4-inbox-and-scheduling-autopilot]
- Anthropic's extension embeds prompt-injection protection and site-level permissions as additional layers [sources/playbooks-2-1-setting-up-claude-in-chrome]

## Relationships

- Operates inside the [[claude-in-chrome]] extension
- Extends the constraint-setting discipline from [[prompt-framework-5-part]]
- Complementary to [[chrome-shortcut-recording]] for trusted repeat tasks
