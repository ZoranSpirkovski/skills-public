---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 4
tags: [animation, pipeline, stages, spec]
---

# script-spec-build-render-pipeline

The four-stage production workflow at the center of Implementation Playbooks Module 1. Stage 1 is the script (what needs to be said). Stage 2 is the spec (the markdown contract between voiceover and visuals). Stage 3 is the build (Claude Code writes React components scene-by-scene). Stage 4 is the render (Remotion compiles frames into a video file). The AI can automate every stage, or the user can intervene at any stage. Each stage produces an artifact that is legible by itself and revisable without rebuilding the others. The pipeline is a specific application of [[spec-driven-pipeline]] tuned for animation, with the spec as the load-bearing artifact.

## Claims

- Four stages: script, spec, build, render [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-3-ai-animation-workflow-companion]
- The spec is a contract between the voiceover and the animation, making the script's timing carry over into the visuals [sources/playbooks-1-1-building-animations-with-claude-code]
- Spec contents: beat map (timestamped), visual philosophy, key moments, audio sync points [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-3-ai-animation-workflow-companion]
- Spec exclusions: frame numbers, pixel positions, component props, code. Including those constrained Claude and produced worse animations [sources/playbooks-1-1-building-animations-with-claude-code]
- Build stage: each scene is a separate React component file Claude generates and edits independently [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-2-illustrator-to-web-animations]
- Render stage produces a video file that goes into a traditional video editor (CapCut) for voiceover, music, captions, and pacing [sources/playbooks-1-1-building-animations-with-claude-code]
- The rendered animation is a starting point, not a finished video; the finish happens in the editor [sources/playbooks-1-1-building-animations-with-claude-code]
- The workflow is practiced on a 30-second explainer as a community exercise: long enough to be real, short enough to finish in one session [sources/playbooks-1-4-community-challenge-30s-explainer]
- A 5-field brief (concept, audience, hook, explanation, payoff, visual style) drives spec generation for the 30s exercise [sources/playbooks-1-4-community-challenge-30s-explainer]

## Relationships

- Specific implementation of [[spec-driven-pipeline]]
- Runs inside [[two-workspace-setup]]
- Uses [[remotion]] and [[claude-code]]
- Connects to [[capcut]] for finishing
