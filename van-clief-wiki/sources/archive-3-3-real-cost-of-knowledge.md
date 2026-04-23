---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [archive, infrastructure, energy, local-ai]
---

# archive-3-3-real-cost-of-knowledge

## Summary

Lesson 3.3 presents the apocalypse-laptop thought experiment. Solar-powered laptop, internet gone. Do you load all of Wikipedia or a local AI model? Van Clief argues for the AI and walks through the energy math to show why. Wikipedia retrieves what already exists. AI synthesizes new, situation-specific answers from multiple domains. Most of AI's apparent energy cost comes from data centers, where up to 40% of power goes to cooling and the Power Usage Effectiveness (PUE) multiplier nearly doubles consumption. Local inference strips away network transmission and centralized cooling. The right metric is energy per insight, not energy per query.

## Key claims

1. A modern M-series laptop draws roughly 15W at normal use; a 100W solar panel at five peak sun hours gives about 500 watt-hours per day, or 33 hours of Wikipedia browsing.
2. Running a local language model adds about 38W, cutting daily runtime to 9.4 hours, or roughly 1,128 queries per day at 30 seconds each.
3. AI queries cost about 25 times more energy than a Wikipedia page view (0.0003 kWh versus 0.0000118 kWh) but produce synthesized, situation-specific output, not retrieval.
4. Data centers consume 240 to 340 TWh globally per year, 1 to 2 percent of global electricity, comparable to the entire aviation industry.
5. Up to 40% of data center energy goes to cooling; typical Power Usage Effectiveness runs 1.58 to 2.0, meaning every watt of compute is paired with nearly a watt of overhead.
6. GPT-3 training used 1,287 MWh and 700,000 liters of fresh water; Gemini Ultra training reportedly cost $191 million, much of it in energy.
7. Inference (not training) accounts for 60 to 90 percent of a model's lifetime energy consumption. Centralized inference is where the waste compounds.
8. Local AI inference eliminates network transmission and centralized cooling, making the marginal 38W much less expensive in real terms.
9. The right frame is energy per insight and energy per problem solved, not energy per query.
10. Distributed local inference may undo decades of "move everything to the cloud" thinking. Hyperscale data centers are sometimes more efficient at steady state; the overhead of centralization may still outweigh the benefits.
11. The 60/30/10 framework is partly an energy policy. Running only the 10% that needs semantic understanding on AI, with the rest handled by traditional code and rules, avoids wasting compute on the wrong layer.

## Entities mentioned

- [[van-clief]]
- [[wikipedia]]
- [[chatgpt]]
- [[google-gemini]]
- [[apple-silicon]]

## Open questions

- What is the actual aggregate energy profile of a fleet of laptops running local models versus a hyperscale data center serving the same query volume? The lesson gestures at the comparison without numbers.
- Which specific local model setup (weights, quantization, runtime) is assumed for the 38W figure, and how does it change with hardware generation?
