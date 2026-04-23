---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [architecture, distinction, strategy]
---

# orchestration-vs-intelligence

Van Clief's distinction between the model (the intelligence) and everything around it (the orchestration). The orchestration is the conductor; the model is the musician. Moltbot has 100,000 GitHub stars and no AI inside it - the value is the routing, the channel integrations, the session management, the security. The Ethics Engine runs psychometric tests across Claude, GPT, Llama, and Gemini; the AI is roughly 10% of the system, the other 90% is orchestration and data processing. The practical consequence: when evaluating any AI tool, ask where the intelligence lives, where the value lives, and what gets commoditized next.

## Claims

- The model is the intelligence; everything around it (routing, integrations, session management, data processing) is the orchestration [sources/foundation-2-5-clawdbot-moltbot]
- The conductor/musician analogy: the conductor makes no sound, the musicians are the talent, but the conductor coordinates who plays when [sources/foundation-2-5-clawdbot-moltbot]
- Four terms kept distinct: Model, Wrapper, Agent, Orchestration Layer [sources/foundation-2-5-clawdbot-moltbot]
- An "agent" in most deployed systems is a collection of prompts structured and sequenced by traditional code; the orchestration layer decides the next prompt, not the model [sources/foundation-2-7-nazi-psychology-ai-auditing]
- Three questions for any AI tool: where is the intelligence, where is the value, what gets commoditized next [sources/foundation-2-5-clawdbot-moltbot]
- The folder architecture is personal orchestration in plain English: folders, context files, routing tables do the coordination; Claude is the model plugged in [sources/foundation-2-5-clawdbot-moltbot]
- Genuine autonomous-loop agents are an emerging next layer; most "agents" today are not that [sources/foundation-2-7-nazi-psychology-ai-auditing]
- Becomes the core of the named discipline of computational orchestration: knowing when boring (plain code) beats brilliant (AI) is the scarce skill [sources/archive-3-4-computational-orchestration]
- Canonical example: replace a proposed AI meeting-scheduling system with a Google Calendar integration plus Gemini for the loose parts; works perfectly in under an hour [sources/archive-3-4-computational-orchestration]

## Relationships

- Operationalized by [[60-30-10-framework]]
- Exemplified by [[moltbot]] (100K stars, zero AI) and [[ethics-engine]] (10% AI calls)
- The folder methodology from [[three-layer-routing]] is a plain-English instance of the orchestration layer
- Related to [[abstraction-ladder]] - value migrates to the orchestration when the intelligence gets cheap
- Subsumed by [[computational-orchestration]] as the named discipline
