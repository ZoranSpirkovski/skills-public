---
type: synthesis
created: 2026-04-23
updated: 2026-04-23
sources: 6
tags: [core, cross-course, spine]
---

# three-layer-routing-across-the-corpus

The [[three-layer-routing]] pattern is the load-bearing idea that every course in Van Clief's corpus either introduces, teaches, applies, or extends. Tracing it across sources shows the same architecture doing different work at different scales.

## Origin: the YouTube talk

[[folder-system-transcript]] is the first public statement of the architecture. It names the three layers (map, rooms, workspace), introduces the [[routing-table]] as the single most important pattern, and frames [[naming-conventions-as-db]] as the mechanism that lets Claude navigate the folder without a query layer. The talk sketches the pattern with a content-creator example (Community, Production, Writing Room) and predicts voice-driven folders as the next stage.

## Canonical teaching: Foundation 3.1

[[foundation-3-1-full-walkthrough]] is the structured teach. Where the transcript argues from a worked example, 3.1 names each layer's job explicitly: Layer 1 as always-loaded router, Layer 2 as per-workspace `CONTEXT.md` loaded on entry, Layer 3 as skills wired into the workspaces that need them. The lesson pins the architecture to 1972-onward software engineering (separation of concerns, modular composition) and references a five-layer research paper of which it teaches the three most important layers.

## Entry point: Foundation 1.2

[[foundation-1-2-your-first-folder]] offers the stripped-down entry: three files ([[claude-md-three-file-pattern]]) and five minutes of work. This is not the full architecture. It is the route onto the full architecture. A reader who starts with 1.2 graduates into 3.1 by adding routing tables, naming conventions, and more workspaces as the project demands.

## Domain adaptation: Foundation 3.2

[[foundation-3-2-customizing-for-your-use-case]] shows the layers do not change shape across domains. Content creators get Script Lab / Production / Distribution; freelancers get Client Alpha / Client Beta / Templates / Business Dev; developers get Planning / Src / Docs / Ops. The routing table, the `CONTEXT.md` files, and the naming conventions all appear in every archetype. Only labels and content change.

## Applied to animation: Playbooks Module 1

Playbooks Module 1 is Foundation 3.2 made concrete. The [[two-workspace-setup]] (Script Lab + Animation Studio) is the content-creator instance. The [[script-spec-build-render-pipeline]] runs inside Animation Studio, driven by a [[routing-table]] row that says "build an animation" and a workspace `CONTEXT.md` describing specs, builds, outputs. [[svg-layer-naming]] is a [[naming-conventions-as-db]] specialization for vector assets.

## Applied to session persistence: Stack 2.4

[[stack-2-4-session-persistence-across-devices]] extends the architecture into a time dimension. The files do not only organize the current task. They are the [[workspace-as-memory]] that carries context across sessions. A `PROGRESS.md` at project root ([[progress-md-pattern]]) adds a reflex step to the routing table. Remote Control ([[remote-control]]) gives the same architecture mobile and desk access to one running session.

## The 2023-2024 retrospective: Archive 1.2, 2.1

Archive 1.2 and 2.1 look backward from 2026. [[archive-2-1-mindset-before-method]] names folder-based routing as one of the patterns Van Clief was already teaching in the January 2024 Flagler workshop. [[archive-1-2-2000-year-overnight-success]] situates the three-layer method as the current layer on the 2,000-year stack of abstraction-and-forgetting ([[thinking-machines]], [[abstraction-ladder]]).

## What the cross-corpus view reveals

Three observations only visible when the courses are read together:

1. **The same primitives recur at every scale.** `CLAUDE.md` + workspace `CONTEXT.md` + routing table + naming conventions are present in the five-minute onboarding, the twenty-three-minute deep teach, the animation pipeline, and the multi-device build. Nothing is thrown away at each level.

2. **Skills wire in differently per use case but never globally.** [[skills-wired-per-task]] shows up as `testing-skill` on developer `/src` rows, as Remotion inside the animation workspace, as Claude for Chrome inside the browser workspace. The mechanism is constant; the wiring is local.

3. **The folder gains responsibility as the user grows.** For a new user it is a three-file starter. For an experienced user it is a control surface spanning desk and mobile, holding process state across sessions. The architecture does not change; the user's relationship to it does.

## Related pages

- [[three-layer-routing]] - the concept itself
- [[routing-table]] - the operational primitive
- [[context-md-workspace-files]] - Layer 2 discipline
- [[skills-wired-per-task]] - Layer 3 discipline
- [[workspace-as-memory]] - the time-dimensional extension
- [[tool-ladder]] - the separate question of whether you need the architecture at all
