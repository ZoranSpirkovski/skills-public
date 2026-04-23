---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, abstraction-series, production-pipeline, animation]
---

# foundation-2-6-video-as-code

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~981-1127. Foundation Module 2, Lesson 6.

## Summary

Van Clief's animation pipeline: what used to take a week of After Effects work takes under an hour with a markdown spec, a style guide, a component registry, [[claude-code]], and [[remotion]]. The point is not the tools. The point is the process: software engineering applied to a creative problem through separation of concerns, reusable components, and tight specs. The spec is the leverage. One person replaces 4-6 specialists and 8-12 weeks of production, not because AI created the art but because the system let one person handle the execution. Constraints make the output better, not worse, and research on the inverted-U relationship between constraints and creativity backs this up.

## Key claims

1. Animations that would take a week in After Effects take under an hour using a spec-driven pipeline; the finished video still takes longer because editing, voiceover, and footage integration stay manual.
2. The four tools: Claude Code (or any coding agent), a code editor, Remotion, CapCut. Tools are interchangeable; the process is the point.
3. The hard work is the spec - a markdown file with headings per scene, timing notes, emphasis cues. "Give me the freedom of a tight brief" (David Ogilvy) is quoted as the operating principle.
4. Remotion (by Jonny Burger) treats video as a function of images over time. React components render frame-by-frame; the entire JavaScript/CSS/SVG ecosystem becomes available as animation primitives.
5. Pipeline: Claude reads the spec plus a style guide and a component registry, composes existing components into scenes, renders via Remotion, and the author refines in CapCut.
6. Constraints improve output: Dr. Seuss wrote Green Eggs and Ham to win a 50-word bet (200 million copies sold); Spielberg's mechanical shark failures made Jaws better.
7. The animation pipeline is the [[folder-as-workspace]] / three-layer architecture applied to production work. Spec, style guide, and component registry are files read per-task, not loaded globally.
8. [[remotion]] is cited as the textbook example of a library that fits the [[skills-wired-per-task]] pattern - only loaded inside the production workspace.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[remotion]]

## Open questions

- Jonny Burger (Remotion creator) is named once; entity optional.
- CapCut and After Effects are named for comparison but carry no standalone weight.
- "4-6 specialists, 8-12 weeks" is Van Clief's estimate; no external citation.
