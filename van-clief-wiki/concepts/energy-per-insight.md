---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [infrastructure, energy, metric]
---

# energy-per-insight

Van Clief's reframing of the AI energy debate. The usual metric, energy per query, compares an AI call (about 0.0003 kWh) to a Wikipedia page view (about 0.0000118 kWh) and concludes AI is 25x more wasteful. This comparison fails because the two operations do different things. Wikipedia retrieves a static article; AI synthesizes a new, situation-specific answer from multiple domains. The right metric is energy per insight or energy per problem solved. In the apocalypse-laptop scenario, 9.4 hours of AI time outperforms 33 hours of Wikipedia browsing because the AI produces bespoke instructions for the exact materials at hand.

## Claims

- "Energy per query" is the wrong metric; "energy per insight" and "energy per problem solved" capture real-world value [sources/archive-3-3-real-cost-of-knowledge]
- AI queries cost about 25 times more energy than a Wikipedia page view but produce synthesized output rather than retrieval [sources/archive-3-3-real-cost-of-knowledge]
- A single AI response can synthesize chemistry, engineering, and survival knowledge into one set of instructions for the user's actual materials [sources/archive-3-3-real-cost-of-knowledge]
- Wikipedia can only return what already exists; every new article, edit, or update requires human energy (the most expensive kind) [sources/archive-3-3-real-cost-of-knowledge]
- The right frame compares total time and total energy to a resolved problem, not the cost of one lookup [sources/archive-3-3-real-cost-of-knowledge]

## Relationships

- Underpins the case for [[local-vs-cloud-ai]]
- Operationalized by the [[60-30-10-framework]] (run AI only on the 10% that needs semantic synthesis)
- Indirect support for [[computational-orchestration]] as energy policy, not only as engineering discipline
