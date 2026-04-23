---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [tool, library, video, react]
---

# remotion

React-based library that renders React components to video frame-by-frame. Created by Jonny Burger. The central tool in the Implementation Playbooks animation pipeline (script → spec → build → render). Mentioned briefly in the folder-system talk as the kind of task-specific library that gets wired into a workspace via skills.

## Claims

- Turns React components into video, frame-by-frame [sources/folder-system-transcript]
- Cited as the example of a library that fits the skills-wired-per-task pattern [sources/folder-system-transcript]
- Core insight: a video is a function of images over time; if the React state is the current frame number, changing state per frame yields animation [sources/foundation-2-6-video-as-code]
- Anything that works in a browser (CSS, SVG, canvas, the JavaScript library ecosystem) becomes available as animation primitives [sources/foundation-2-6-video-as-code]
- Pairs with CapCut for finish editing (voiceover, pacing, transitions) in Van Clief's pipeline [sources/foundation-2-6-video-as-code]
- Ships an agent-skill package on GitHub: markdown plus code samples teaching Claude 3D content, DOM elements, Tailwind, transitions, video decodability checks [sources/playbooks-1-1-building-animations-with-claude-code]
- Skills load lazily: Claude reads only the sub-file relevant to the current task, not all of them at once [sources/playbooks-1-1-building-animations-with-claude-code]
- Installs via a single prompt in a fresh folder; Claude handles Node.js, Remotion, and the skill package [sources/playbooks-1-1-building-animations-with-claude-code]
- Each scene in the pipeline is a separate React component file Claude generates and edits independently [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-2-illustrator-to-web-animations]
- Remotion Studio is the browser-based preview for scrubbing through animations during build [sources/playbooks-1-1-building-animations-with-claude-code]
- The same Remotion-built components work outside Remotion inside any React website (scroll-triggered animation, hover reactions) [sources/playbooks-1-2-illustrator-to-web-animations]
- Canonical Animation Studio project layout: `src/compositions/`, `src/components/`, `src/scenes/`, plus `remotion.config.ts` [sources/playbooks-1-3-ai-animation-workflow-companion]

## Relationships

- Example of [[skills-wired-per-task]] - referenced by animation workspaces, not globally loaded
- Render engine inside [[spec-driven-pipeline]] and [[script-spec-build-render-pipeline]]
- Tool primary to Implementation Playbooks Module 1
- Pairs with [[capcut]] for finishing
