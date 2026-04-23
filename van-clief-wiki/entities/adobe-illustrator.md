---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [design, tool, vector]
---

# adobe-illustrator

Adobe's vector-graphics editor. Used in Playbooks Lesson 1.2 as the starting point for design-to-animation pipelines. The learner draws characters or storyboards, labels layers meaningfully, and exports as SVG. Claude reads the SVG directly (SVG is essentially HTML) and turns labelled elements into animated React components. Van Clief's buddy's storyboard, built by hand in Illustrator, was the real-world project that motivated the lesson.

## Claims

- Illustrator files are the starting point for the design-to-animation pipeline; SVG is the handoff format [sources/playbooks-1-2-illustrator-to-web-animations]
- The critical export step sets Object IDs to Layer Names so meaningful layer names survive as SVG element IDs [sources/playbooks-1-2-illustrator-to-web-animations]
- Layers must be named meaningfully before export ("left_eye", "right_iris") for Claude to target parts on request [sources/playbooks-1-2-illustrator-to-web-animations]
- Once the SVG is in the folder, most edits happen in natural language, not Illustrator; the folder becomes the editor [sources/playbooks-1-2-illustrator-to-web-animations]
- Van Clief's framing: Illustrator provides the creative first pass; the folder amplifies the designer's work [sources/playbooks-1-2-illustrator-to-web-animations]

## Relationships

- Produces input for [[svg-layer-naming]]
- Starting point of [[script-spec-build-render-pipeline]] when working from existing designs
- Alternative source: [[figma]]
