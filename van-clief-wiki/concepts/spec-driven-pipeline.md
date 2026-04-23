---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [production, pipeline, creative]
---

# spec-driven-pipeline

Van Clief's production workflow for creative output. The leverage is the spec - a markdown file that describes what the output should be, not vaguely but precisely. Timing, structure, emphasis, what stays in the background. The spec references supporting files: a style guide (visual language, color palette, animation timing, decisions that stay the same across every video) and a component registry (reusable building blocks already built). Claude reads all three and composes existing components into new output. The creative thinking lives in the spec; the execution is delegated to the model plus the component library. The pattern generalizes beyond video: the spec is always the leverage point for any AI-delegated work.

## Claims

- The spec is the hard work, not the AI or the code [sources/foundation-2-6-video-as-code]
- A tight spec means the model makes fewer interpretive guesses; a loose spec means more guessing [sources/foundation-2-6-video-as-code]
- Three files drive the pipeline: spec, style guide, component registry [sources/foundation-2-6-video-as-code]
- The approach generalizes: the spec is the leverage for any AI-delegated work, not just video [sources/foundation-2-6-video-as-code]
- Constraints improve output, not limit it; there is an inverted-U relationship between constraints and creative output [sources/foundation-2-6-video-as-code]
- Dr. Seuss wrote Green Eggs and Ham under a 50-word constraint and it became his best-selling book ever [sources/foundation-2-6-video-as-code]
- Spielberg's mechanical shark failures in Jaws made the film better by forcing suggestion over display [sources/foundation-2-6-video-as-code]
- One person replaces 4-6 specialists and 8-12 weeks of production because the system lets one person handle execution; AI did not create the art [sources/foundation-2-6-video-as-code]
- In the Implementation Playbooks animation pipeline, the spec is a markdown contract between voiceover and visuals with beat map, visual philosophy, key moments, audio sync points [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-3-ai-animation-workflow-companion]
- Specs must exclude frame numbers, pixel positions, component props, and code. Including those constrains the model and produces worse output [sources/playbooks-1-1-building-animations-with-claude-code]
- Van Clief learned the "no pixels in the spec" rule the hard way: tight code-level control made his own animations worse [sources/playbooks-1-1-building-animations-with-claude-code]
- The SVG-layered design-to-animation variant adds a labelled-SVG layer: layer names become element IDs Claude can target for surgical edits [sources/playbooks-1-2-illustrator-to-web-animations]
- The 30-second explainer uses a 5-field brief (concept, audience, hook, explanation, payoff, visual style) as the input to spec generation [sources/playbooks-1-4-community-challenge-30s-explainer]

## Relationships

- Specific implementation of [[three-layer-routing]] - spec and style guide are Layer 2 context files, component registry is a skills-style artifact
- Uses [[remotion]] as the render engine and [[claude-code]] as the composer
- Embodies the principle behind [[folder-as-workspace]] applied to production work
- David Ogilvy quote ("give me the freedom of a tight brief") is the operating aphorism
- Expressed for animation as [[script-spec-build-render-pipeline]]
- Sibling design workflow uses [[svg-layer-naming]]
