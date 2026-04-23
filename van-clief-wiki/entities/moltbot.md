---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [tool, orchestration, open-source]
---

# moltbot

Open-source AI orchestration layer (also called Clawdbot in some contexts). Over 100,000 GitHub stars, 500 pull requests, 200 contributors, roughly 50,000 lines of code. Contains no AI model, no weights, no training data. Connects messaging platforms (WhatsApp, Telegram, Discord, Signal) to external AI providers through a local websocket gateway. Van Clief uses Moltbot as the canonical example of how a hugely valuable AI tool can have zero AI inside it - the value is the orchestration.

## Claims

- Over 100,000 GitHub stars, 500 pull requests, 200 contributors, ~50,000 lines of code [sources/foundation-2-5-clawdbot-moltbot]
- Contains no model, no weights, no training data [sources/foundation-2-5-clawdbot-moltbot]
- Architecture: channel layer (Baileys for WhatsApp, Grammy for Telegram, Discord.js, Signal CLI), a gateway (routing, session, security), tools (browser, bash, file ops), and empty hooks for external AI providers [sources/foundation-2-5-clawdbot-moltbot]
- Code breakdown: ~35% channel integrations, ~25% gateway, ~20% tools, ~10% CLI and AI calls [sources/foundation-2-5-clawdbot-moltbot]
- Model-agnostic, self-hosted, open-source - positioned as resilient against being "Sherlocked" by frontier-model vendors building native features [sources/foundation-2-5-clawdbot-moltbot]

## Relationships

- Canonical example of [[orchestration-vs-intelligence]] and the [[60-30-10-framework]]
- Runtime for third-party AI models (Claude, GPT, Llama) via empty hooks
