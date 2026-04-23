---
type: synthesis
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [cross-course, patterns]
---

# spec-prd-brief-same-document-different-scale

Three terms appear in different courses for what looks like three distinct artifacts: the spec (Playbooks), the PRD (Stack), and the briefing document (Playbooks and Stack). Reading them in isolation they seem like different things. Read together, they are the same pattern at three scales of work.

## The spec: Playbooks Module 1

[[playbooks-1-1-building-animations-with-claude-code]] and [[playbooks-1-3-ai-animation-workflow-companion]] define the spec as a markdown document that maps a script to an animation beat-by-beat. It contains: a beat map, visual philosophy, key moments, and audio sync points. It does not contain: frame numbers, pixel positions, component props, or code. Van Clief's own line is "the spec is a contract between the voiceover and the animation". It sits between Script Lab and Animation Studio in the [[two-workspace-setup]].

## The PRD: Stack Modules 1 and Playbooks 3.1

[[stack-1-2-how-i-use-claude-code-in-build]] and [[playbooks-3-1-build-and-deploy-website]] both rest on a PRD (Product Requirements Document) written as markdown. The PRD describes: what the project is, which existing repos are being borrowed from, what stacks they use, what to cut, the phases, the stepwise plan. The [[prd-first-methodology]] is: write the PRD before any code, re-read it every session. The PRD lives in the workspace as persistent context.

## The briefing document: Playbooks 3.3 and Stack 1.2

[[playbooks-3-3-pre-build-planning-and-prompt-sequencing]] names a briefing document as the output of steps 1 and 2 of the [[pre-build-planning-sequence]]: analyze what exists, then document it in markdown for Claude Code to read. [[stack-1-2-how-i-use-claude-code-in-build]] describes the same handoff: Claude chat explores, then drops a markdown file into the workspace before Claude Code starts. The briefing document is shorter than a PRD. It captures state, not intent.

## The same pattern at three scales

| Artifact | Scale | What it captures | When it is written |
|---|---|---|---|
| Briefing document | One session's worth of setup | State of the current thing (existing site, existing process) | Before Claude Code starts |
| Spec | One unit of output (one animation, one page) | The contract between intent and execution | Before the build loop starts |
| PRD | One project | Architecture, phases, scope, what to cut | Before any file is created |

Underneath all three: a plain markdown file, in the workspace, that Claude reads on every invocation. The differences are scope and lifespan. A briefing document might live for one day. A spec lives until the animation ships. A PRD lives for the project's lifetime.

## What the cross-corpus view reveals

Three observations:

1. **The point of all three is to front-load decisions.** Each artifact moves work from token-expensive code-generation time to token-cheap markdown-editing time. The shared slogan, from Playbooks 3.3: "spend your thinking before you spend your tokens."

2. **They stack rather than replace.** A project might have a PRD at the root, a spec per animation in `/animation-studio/specs/`, and a briefing document dropped in whenever a session starts. The [[routing-table]] can point at each in its own row.

3. **They are all instances of the same underlying discipline.** Putting intent, scope, and constraints into a markdown file Claude can re-read means Claude does not rebuild understanding on every prompt. This is [[workspace-as-memory]] applied at the document level. It is also a direct expression of [[folder-as-workspace]]: the document is the app's state, not a temporary prompt.

## Related pages

- [[prd-first-methodology]] - the operational discipline
- [[briefing-document]] - one specific instance
- [[spec-driven-pipeline]] - the animation-specific instance
- [[script-spec-build-render-pipeline]] - the four-stage workflow
- [[pre-build-planning-sequence]] - the five-step plan-first method
- [[workspace-as-memory]] - the underlying pattern
- [[three-layer-routing]] - where these documents live in the architecture
