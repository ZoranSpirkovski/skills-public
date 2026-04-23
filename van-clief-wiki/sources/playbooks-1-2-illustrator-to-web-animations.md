---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, animation, svg, module-1]
---

# playbooks-1-2-illustrator-to-web-animations

> Source: Implementation Playbooks course, Module 1 Lesson 1.2. Video transcript plus written lesson. File: `.wiki/raw/playbooks/lesson-1-2-illustrator-to-web-animations.md`.

## Summary

Turn hand-drawn Adobe Illustrator designs into editable animated components controlled by natural language. The pipeline relies on SVG export because SVG is essentially text Claude can read and edit. The load-bearing prep step is labelling Illustrator layers (`left_eye`, `right_iris`, `hero_mouth`) so Claude can target specific parts on request. From a single labelled SVG, Claude builds character components, emotion profiles, and timing controls, each in separate files for surgical editing. The same components then work outside Remotion inside a React website. Van Clief uses this lesson to argue for "appless work": the folder structure is the software; Adobe Illustrator, Claude Code, and the browser preview replace a monolithic animation app.

## Key claims

1. SVG files are essentially HTML: text that describes shapes, colors, and positions; Claude can read and edit them directly.
2. Layer naming in Illustrator is the most important prep step; generic names ("Layer 1", "Group 3") force Claude to guess and guess wrong.
3. Recommended convention: `[character]_[part]_[side]` for characters, `[layer]_[element]_[number]` for scenes.
4. SVG export settings that matter: Object IDs = Layer Names (critical), Styling = Internal CSS, Minify = Off, Responsive = On.
5. From one labelled SVG, Claude builds four artifact types: character components (React with `emotion` / `blinkSpeed` props), animation profiles (joy, sadness, fear states), timing controls (iris speed, blink duration), scene integration (placement inside a Remotion composition).
6. All artifacts are kept in separate files. Character definition, emotion profile, and scene composition are each independently editable.
7. A project-level `CLAUDE.md` with correct paths to character files, emotion profiles, and scenes lets Claude edit a specific iris without rereading the whole codebase.
8. Two skills are recommended: the Remotion agent skill (animation) and the UIUX Pro skill (design sense for front-end polish).
9. Claude's surgical editing ability is presented as the key contrast to AI image generation. Image generators regenerate everything; SVG + folder lets you keep what works and fix what does not.
10. Multiple characters use the same pipeline with a prefixed naming convention (`char1_left_eye`, `char2_left_eye`).
11. The Remotion-built component library runs unchanged inside a React website. Same components animate on scroll or in Remotion exports.
12. "Appless work is now possible": no Adobe Illustrator required for editing once the SVG is in the folder; the folder itself becomes the editor.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[remotion]]
- [[adobe-illustrator]]
- [[figma]]
- [[vs-code]]

## Open questions

- UIUX Pro skill GitHub URL marked as TBD in the lesson.
- The website-build workflow that consumes these components (the friend's storyboard site) is described but not walked through end-to-end.
