---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [infrastructure, deployment, energy]
---

# local-vs-cloud-ai

Van Clief's infrastructure argument. AI's reputation as an energy monster comes from how it is deployed, not from what it is. Data centers consume 240 to 340 TWh globally per year, with up to 40% going to cooling and Power Usage Effectiveness of 1.58 to 2.0. Running AI locally eliminates network transmission and centralized cooling. A local model on an efficient laptop adds 38W to baseline power draw. That is not 38W on top of a hundred-watt cloud overhead; it is 38W total. The argument: centralized inference is where AI's waste actually lives, and local deployment may undo decades of "move everything to the cloud" thinking.

## Claims

- Global data centers use 240 to 340 TWh per year, 1 to 2 percent of world electricity, comparable to the aviation industry [sources/archive-3-3-real-cost-of-knowledge]
- Up to 40% of data center energy goes to cooling, not computing [sources/archive-3-3-real-cost-of-knowledge]
- Power Usage Effectiveness for typical data centers is 1.58 to 2.0: for each watt of compute, another watt of overhead [sources/archive-3-3-real-cost-of-knowledge]
- Inference (not training) accounts for 60 to 90 percent of a model's lifetime energy consumption [sources/archive-3-3-real-cost-of-knowledge]
- A local language model adds about 38W to baseline laptop draw; the overhead stack of a data center is stripped out [sources/archive-3-3-real-cost-of-knowledge]
- Hyperscale data centers with PUE near 1.1 and renewable contracts can still be more efficient at steady state; the question is whether centralization overhead outweighs the scale advantage [sources/archive-3-3-real-cost-of-knowledge]
- GPT-3 training used 1,287 MWh and 700,000 liters of fresh water [sources/archive-3-3-real-cost-of-knowledge]
- Gemini Ultra training reportedly cost $191 million, much of it energy [sources/archive-3-3-real-cost-of-knowledge]

## Relationships

- Supports [[energy-per-insight]] by showing where the waste actually lives
- Counterpart deployment question to [[three-interfaces]] (Desktop, Code, terminal all assume cloud inference today)
- Input to the deployment side of [[computational-orchestration]]
