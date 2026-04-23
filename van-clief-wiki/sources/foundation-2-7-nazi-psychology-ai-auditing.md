---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, abstraction-series, ethics-engine, mcp, apis]
---

# foundation-2-7-nazi-psychology-ai-auditing

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~1128-1249. Foundation Module 2, Lesson 7. Companion to Van Clief's paper on the Ethics Engine (arxiv 2510.11742).

## Summary

Van Clief takes apart his Ethics Engine, a pipeline that administers 1950s-era psychometric instruments (moral foundations, authoritarianism scales, personality dimensions) across AI models and providers. From outside it looks like one intelligence studying another. Inside it is async programming, HTTP+JSON requests, rate-limit retries, regex parsing, and SciPy/NumPy statistical methods that predate language models by decades. The AI is ~10% of the system. The final lesson in the Abstraction series consolidates: APIs as contracts, MCP (Model Context Protocol) as the LSP-style standardization of AI tooling, and the 60/30/10 ratio reappearing exactly where you would expect it. "Agent" gets defined carefully as a collection of prompts structured and sequenced by traditional code, not an autonomous entity.

## Key claims

1. The Ethics Engine runs psychometric tests across Claude, GPT, Llama, and Gemini; outputs scores on moral foundations, authoritarianism scales, and personality dimensions.
2. Ratio breakdown: ~10% AI calls, ~30% orchestration (async, rate limiting, retry, queue), ~60% data processing (parsing, scoring, reliability stats).
3. An "agent" in most deployed systems is a collection of prompts structured and sequenced by traditional code; the orchestration layer decides the next prompt, not the model.
4. An API is a contract: two pieces of software agree in advance on the shape of the conversation. HTTP + JSON is how AI endpoints work - nothing architecturally new.
5. MCP (Model Context Protocol), introduced by Anthropic in late 2024, is explicitly inspired by LSP (Language Server Protocol). Same pattern as USB and HTTP: standardize the interface to avoid the N-by-M integration explosion.
6. MCP architecture: host (AI application) + client (connection handler) + server (wraps the external tool, speaks MCP).
7. Statistical methods used (Cronbach's alpha, test-retest correlation, SciPy/NumPy) predate LLMs by decades and are unchanged; the math is not new.
8. The 60/30/10 ratio from [[foundation-2-5-clawdbot-moltbot]] reappears unchanged in a research-software context.
9. Grace Hopper analogy: every new abstraction layer starts unreliable, becomes reliable through infrastructure. Genuine autonomous loops are the next such layer; the engineering work around them (error handling, reliability patterns) will mirror every previous layer.

## Entities mentioned

- [[van-clief]]

## Open questions

- Grace Hopper is named repeatedly across the series; still no entity page. Promote on next pass.
- MCP deserves a concept page if it appears in three or more sources; currently at two (this lesson and references elsewhere). Hold until a third citation.
- The Ethics Engine paper (arxiv 2510.11742) is a self-cite; entity coverage already under Van Clief.
