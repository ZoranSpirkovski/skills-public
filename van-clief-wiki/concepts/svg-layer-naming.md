---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [svg, design, naming]
---

# svg-layer-naming

The prep rule that makes design-to-animation pipelines work. Before exporting from Illustrator or Figma, name every layer meaningfully so Claude can target parts on request. Generic names ("Layer 1", "Group 3") force Claude to guess; meaningful names ("left_eye", "right_iris", "hero_mouth") let Claude act. SVG is text, the layer names become element IDs on export, and those IDs are how Claude routes to specific parts when the user says "make the eyes blink" or "I don't like the sadness expression." The convention extends [[naming-conventions-as-db]] into design files.

## Claims

- SVG files are essentially HTML: text describing shapes, colors, and positions, directly readable and editable by Claude [sources/playbooks-1-2-illustrator-to-web-animations]
- Generic layer names make Claude guess; meaningful names let Claude act with precision [sources/playbooks-1-2-illustrator-to-web-animations]
- Character convention: `[character]_[part]_[side]` (e.g. `hero_eye_left`) [sources/playbooks-1-2-illustrator-to-web-animations]
- Scene convention: `[layer]_[element]_[number]` (e.g. `bg_mountain_01`, `fg_tree_left`) [sources/playbooks-1-2-illustrator-to-web-animations]
- Multi-character convention prepends a character prefix: `char1_left_eye`, `char2_left_eye` [sources/playbooks-1-2-illustrator-to-web-animations]
- The critical Illustrator export setting is Object IDs = Layer Names; without it, the labels do not survive export [sources/playbooks-1-2-illustrator-to-web-animations]
- Other export settings that matter: Styling = Internal CSS, Minify = Off, Responsive = On [sources/playbooks-1-2-illustrator-to-web-animations]

## Relationships

- Design-file extension of [[naming-conventions-as-db]]
- Feeds [[script-spec-build-render-pipeline]] via the build stage
- Pairs with [[appless-work]] - the folder plus the SVG replaces the need to re-enter Illustrator for edits
