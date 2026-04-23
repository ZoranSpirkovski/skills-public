---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [archive, orchestration, discipline, 60-30-10]
---

# archive-3-4-computational-orchestration

## Summary

Lesson 3.4 names the discipline the rest of the course was pointing toward: computational orchestration. Not using AI, but knowing which computation to apply to which part of a problem. Traditional code for the deterministic, LLMs for the semantic, humans for the judgment calls. Van Clief ties this back to the Module 2 coding pyramid and the THINK acronym as early versions of the same idea. The 60/30/10 pattern (60% regular database queries, 30% if-then logic, 10% actual AI calls) is the pattern that recurs in every successful AI implementation he has built or observed. The 10% makes the system feel intelligent; the 90% makes it actually work.

## Key claims

1. Computational orchestration is the discipline of knowing which type of computation fits which problem and when to use which.
2. The pattern recurs: 60% traditional database queries (fast and cheap), 30% basic if-then logic (debuggable), 10% actual AI calls (only where semantic understanding matters).
3. Most AI transformations fail not because the tech fails but because no one is orchestrating it. Everyone is given a trumpet and told to play loud.
4. An AI scheduling system was replaced by a Google Calendar integration with Gemini handling the loose parts. Hours instead of weeks. Working system instead of impressive one.
5. The discipline has three markers. Abstraction without abandonment: a semantic layer on top of code, not a replacement for it. Judgment and implementation: knowing when not to use AI is harder than making it work. Flow over features: a regex in the right spot beats GPT-4 in the wrong spot.
6. We are accumulating computation types: deterministic code, probabilistic ML, semantic LLMs, quantum (soon), biological (already). Someone has to orchestrate them.
7. The compiler transition of the 1950s is the historical parallel. Assembly programmers protested; the abstraction layer won. The code is not dying. It is moving up a level.
8. The skill question shifts from "can you code?" to "can you orchestrate code?" within five years.
9. The Module 2 coding pyramid (machine code, Python, LLMs) and the THINK acronym were both early versions of computational orchestration named before the name existed.
10. Van Clief signs the article as "Computational Orchestration Architect", framing it as naming an emerging job rather than inventing a new one.

## Entities mentioned

- [[van-clief]]
- [[google-calendar]]
- [[google-gemini]]

## Open questions

- What are the canonical test cases where a junior engineer consistently over-applies AI to deterministic work? A taxonomy of the failure modes would extend the discipline.
- How does the 60/30/10 ratio shift for research software (the Ethics Engine), consumer product (Moltbot), and personal folder architectures? The lesson asserts the ratio recurs; the variance within it is unmapped.
