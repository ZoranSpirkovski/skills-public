---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, abstraction-series, orchestration, 60-30-10]
---

# foundation-2-5-clawdbot-moltbot

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~850-980. Foundation Module 2, Lesson 5.

## Summary

Moltbot (Clawdbot) has over 100,000 GitHub stars, 500 pull requests, 200 contributors, and zero AI inside. Open its 50,000 lines of code and no model, weights, or training data appear. Van Clief uses this to separate four often-confused terms - model, wrapper, agent, orchestration layer - and introduces the 60/30/10 framework: production AI systems should be roughly 60% traditional code, 30% rule-based logic and routing, and 10% actual AI calls. Moltbot is a highway system. You bring your own car (the model). The value lives in the orchestration, not the intelligence.

## Key claims

1. Moltbot contains zero AI: no weights, no training data, no model. It is pure orchestration with empty hooks for external AI providers.
2. Four terms to keep distinct: AI Model (the intelligence), Wrapper (thin API layer), Agent (AI taking actions, still needs an external AI), Orchestration Layer (coordinates AI, tools, channels, context).
3. Moltbot's code breakdown: ~35% channel integrations (WhatsApp, Telegram, Discord, Signal), ~25% gateway (routing, session, security), ~20% tools (browser, bash, files), ~10% CLI + AI calls.
4. The 60/30/10 framework: build AI systems with ~60% traditional code, ~30% rule-based logic/routing, ~10% AI processing. Moltbot pushes the 10% entirely external.
5. Three questions to ask about any AI tool: where is the intelligence, where is the value, what gets commoditized next.
6. The folder architecture from [[foundation-1-2-your-first-folder]] is itself a personal orchestration layer expressed in plain English - folders, context files, routing tables - with Claude as the intelligence plugged in.
7. Open-source, model-agnostic, self-hosted orchestration (like Moltbot) is resilient against being "Sherlocked" by frontier-model vendors building native features.

## Entities mentioned

- [[van-clief]]

## Open questions

- Moltbot's library dependencies (Baileys for WhatsApp, Grammy for Telegram, Discord.js, Signal CLI) are named but not given entities; skip.
- The 60/30/10 ratio is presented as Van Clief's workshop framework; its origin is not sourced.
