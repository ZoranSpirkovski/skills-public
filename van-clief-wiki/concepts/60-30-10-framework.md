---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 4
tags: [architecture, framework, production]
---

# 60-30-10-framework

Van Clief's prescription for the shape of a production AI system. Roughly 60% traditional code (platform integrations, networking, file handling, the plumbing that has nothing to do with AI), 30% rule-based logic and routing (decision flow, security, session management), and 10% actual AI calls. The ratio recurs across domains. Moltbot's 100,000-star codebase is almost exactly 35% integrations, 25% gateway, 20% tools, 10% AI calls. The Ethics Engine pipeline that administers psychometric tests across AI models is ~60% data processing, ~30% async orchestration, ~10% AI calls. The framework is descriptive (well-built systems look like this) and prescriptive (build yours to match).

## Claims

- Production AI systems should be roughly 60% traditional code, 30% rule-based logic and routing, 10% actual AI processing [sources/foundation-2-5-clawdbot-moltbot] [sources/foundation-2-7-nazi-psychology-ai-auditing]
- Moltbot instantiates the ratio: ~35% channel integrations, ~25% gateway, ~20% tools, ~10% CLI and AI calls [sources/foundation-2-5-clawdbot-moltbot]
- The Ethics Engine instantiates the ratio in a research-software context: ~60% data processing, ~30% orchestration, ~10% AI calls [sources/foundation-2-7-nazi-psychology-ai-auditing]
- The ratio is a marker of maturity: well-built systems look like this; bad ones ignore it [sources/foundation-2-5-clawdbot-moltbot]
- The value lives in the 60% and the 30%, not the 10% [sources/foundation-2-5-clawdbot-moltbot] [sources/foundation-2-7-nazi-psychology-ai-auditing]
- The ratio recurs inside the named discipline of computational orchestration: 60% regular database queries, 30% if-then logic, 10% AI calls only where semantic understanding matters [sources/archive-3-4-computational-orchestration]
- The 10% makes a system feel magical; the 90% makes it actually work [sources/archive-3-4-computational-orchestration]
- The coding pyramid (machine code, Python, LLMs) is the abstraction-layer seed that grew into this ratio [sources/archive-2-2-raise-the-bar]
- Also functions as energy policy: running AI only on the semantic 10% avoids wasting compute on tasks the other layers handle cheaper [sources/archive-3-3-real-cost-of-knowledge]

## Relationships

- Demonstrated by [[moltbot]] and [[ethics-engine]]
- Paired with [[orchestration-vs-intelligence]] - the 90% around the AI is where value accrues
- The folder methodology from [[three-layer-routing]] is "60/30/10 in plain English" - folders and markdown do the orchestration work instead of Python
- Canonical ratio inside [[computational-orchestration]] as a named discipline
- Underwrites [[energy-per-insight]] and [[local-vs-cloud-ai]] as practical energy policy
