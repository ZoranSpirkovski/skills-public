---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [tool, video-editor]
---

# capcut

Consumer video editor used at the end of Van Clief's animation pipeline. Remotion renders a video file; CapCut (or another editor) is where voiceover, music, captions, and pacing get finished. Van Clief treats the split as separation of concerns: the spec-driven pipeline builds the animation, the editor finishes the film.

## Claims

- The final edit happens in CapCut or equivalent: voiceover, music, captions, pacing, cuts [sources/playbooks-1-1-building-animations-with-claude-code]
- The rendered animation is a strong starting point, not a finished video [sources/playbooks-1-1-building-animations-with-claude-code]
- Some edits are faster by hand than by spec; scrubbing a transition to land on a specific word is an editor task, not an AI task [sources/playbooks-1-1-building-animations-with-claude-code]
- Listed as a required tool in the Module 1 companion reference [sources/playbooks-1-3-ai-animation-workflow-companion]

## Relationships

- Downstream of [[remotion]] in the [[script-spec-build-render-pipeline]]
- Alternative: DaVinci Resolve, Premiere (lesson neutral on editor choice)
