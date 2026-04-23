---
type: synthesis
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [core, cross-course, orchestration]
---

# 60-30-10-across-four-courses

The [[60-30-10-framework]] is Van Clief's second biggest idea. 60% traditional deterministic code, 30% rule-based logic, 10% actual AI calls. The framework is introduced in Foundation, deepened across Archive, and applied in Playbooks and Stack. Tracing it across the corpus shows the same ratio doing different work at different levels.

## First statement: Foundation 2.5 (Clawdbot / Moltbot)

[[foundation-2-5-clawdbot-moltbot]] introduces the ratio via a specific artifact: [[moltbot]], a 100,000-star open-source orchestration project with *zero AI model code*. The whole system is routing, rules, and integrations. The lesson's punchline: the 10% AI is what makes the experience feel magical; the 90% non-AI is what makes it actually work. This inverts the intuition that AI projects are mostly AI.

## Deepened through a real pipeline: Foundation 2.7

[[foundation-2-7-nazi-psychology-ai-auditing]] applies the framework to Van Clief's [[ethics-engine]] - a psychometric pipeline running 1950s personality instruments against frontier LLMs. The breakdown: 10% AI calls, 30% orchestration (async, concurrency, rate limiting), 60% data processing (parsing, scoring, statistics). This lesson also names [[mcp]] (Model Context Protocol) as the standardization layer that makes the 30% orchestration portable.

## Framed as a discipline: Archive 3.4

[[archive-3-4-computational-orchestration]] is the moment the ratio becomes a named discipline: [[computational-orchestration]]. The article argues that the "AI person" in every shipping company is not a prompt engineer but an orchestrator. They spend 80% of their time preventing AI from being used where it should not be. The framework is restated as the ratio that keeps showing up in successful implementations.

## Implicit in Playbooks

The Implementation Playbooks course does not mention the 60/30/10 ratio explicitly. But every one of its pipelines follows it:

- The [[script-spec-build-render-pipeline]] is 60% markdown structure and naming, 30% routing between workspaces, 10% Claude Code generating code from specs.
- The browser workflows in Playbooks 2.x are 60% Chrome's own navigation and page rendering, 30% `/shortcut` recording and routing logic, 10% Claude understanding page semantics.
- The GitHub Pages deploy in Playbooks 3.1 runs under 10 prompts because the 90% of the architecture (folder structure, CLAUDE.md, .gitignore, deploy action) is deterministic by the time Claude writes anything.

## Implicit in Stack

Building Your Stack is 60/30/10 applied at the meta level:

- The [[tool-ladder]] is a decision-support structure (the 30%) for when to escalate from Claude Projects to Cowork to VS Code to a custom front-end.
- The [[prd-first-methodology]] front-loads the 60% (structure, scope, decisions) before any AI code generation begins.
- [[workspace-as-memory]] and [[progress-md-pattern]] are explicit 60% plumbing making the 10% AI appear continuous across sessions.

## What the cross-corpus view reveals

Three observations from reading the four courses together:

1. **The ratio is not a style preference; it is the shape of working systems.** Van Clief does not argue it should be 60/30/10. He observes that every successful system already is. The framework is descriptive, not prescriptive.

2. **The failure mode is asymmetric.** Over-indexing on AI (higher than ~10%) produces systems that are expensive, unpredictable, and hard to debug. Under-indexing on structure (lower than ~60%) produces systems where the AI has nowhere stable to write back to. The folder methodology is a way to build the 60% before the 10% shows up.

3. **The framework explains the Vault / Drawing Room tiers.** The paid content is described as workspace blueprints, PRD templates, workflow starters, spec templates. That is all 60% and 30% material. The free courses teach how to build it; the paid tier delivers it pre-built.

## Related pages

- [[60-30-10-framework]] - the ratio itself
- [[computational-orchestration]] - the discipline name from Archive 3.4
- [[orchestration-vs-intelligence]] - the underlying distinction
- [[moltbot]] - the canonical worked example
- [[ethics-engine]] - the applied research example
- [[prd-first-methodology]] - the operational discipline for front-loading the 60%
- [[three-layer-routing]] - the folder-methodology implementation of the 60%
