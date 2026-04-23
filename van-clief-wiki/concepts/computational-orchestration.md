---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [discipline, architecture, orchestration]
---

# computational-orchestration

The name Van Clief gives to the discipline the rest of his work was pointing toward. Not using AI, but knowing which type of computation fits which part of a problem and when to use which. Traditional code for the deterministic, language models for the semantic, humans for the judgment calls. The Module 2 coding pyramid (machine code, Python, LLMs) and the THINK acronym were both early versions of the same idea before the name existed. The 60/30/10 pattern is the signature: 60% regular database queries (fast, cheap), 30% basic if-then logic (debuggable), 10% actual AI calls (only where semantic understanding matters). The 10% makes the system feel magical; the 90% makes it actually work.

## Claims

- Computational orchestration is the discipline of knowing which computation fits which problem and when to apply which [sources/archive-3-4-computational-orchestration]
- The canonical shape: 60% traditional database queries, 30% if-then logic, 10% AI calls [sources/archive-3-4-computational-orchestration]
- Most AI transformations fail not because the tech fails but because no one orchestrates it; everyone is given a trumpet and told to play loud [sources/archive-3-4-computational-orchestration]
- Three markers of the discipline: abstraction without abandonment, judgment plus implementation, flow over features [sources/archive-3-4-computational-orchestration]
- "Abstraction without abandonment": a semantic layer on top of code, not a replacement for code [sources/archive-3-4-computational-orchestration]
- "Flow over features": a regex in the right spot beats GPT-4 in the wrong spot [sources/archive-3-4-computational-orchestration]
- Example: replace an AI-native meeting scheduler with a Google Calendar integration that lets Gemini handle the loose parts [sources/archive-3-4-computational-orchestration]
- We are accumulating computation types (deterministic, probabilistic, semantic, quantum, biological); someone must orchestrate across them [sources/archive-3-4-computational-orchestration]
- The compiler transition of the 1950s is the historical parallel; the code is not dying, it is moving up a level [sources/archive-3-4-computational-orchestration]
- The Module 2 coding pyramid and the THINK acronym were both early unnamed versions of this discipline [sources/archive-2-2-raise-the-bar] [sources/archive-3-4-computational-orchestration]

## Relationships

- Operationalized by [[60-30-10-framework]]
- Contains and extends [[orchestration-vs-intelligence]]: orchestration is the full discipline; orchestration-vs-intelligence is the core distinction
- Seeded by [[raise-the-bar]] (coding pyramid) and [[think-acronym]]
- Applied by [[three-layer-routing]] as personal orchestration in plain English
- Has an energy-policy dimension via [[energy-per-insight]] and [[local-vs-cloud-ai]]
