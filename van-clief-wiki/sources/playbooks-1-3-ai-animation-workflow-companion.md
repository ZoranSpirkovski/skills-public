---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, animation, reference, module-1]
---

# playbooks-1-3-ai-animation-workflow-companion

> Source: Implementation Playbooks course, Module 1 Lesson 1.3. Written companion reference page (no video). File: `.wiki/raw/playbooks/lesson-1-3-ai-animation-workflow-companion.md`.

## Summary

A bookmarkable reference that condenses Lessons 1.1 and 1.2 into a single quick-reference page: the four stages in table form, the canonical folder structure, essential Claude Code commands, what goes in a spec, SVG export settings, layer naming conventions, and a troubleshooting block. No new concepts. This page is the cheat sheet for someone doing the work.

## Key claims

1. The canonical Animation Studio folder layout: `CLAUDE.md` at root, `scripts/` (long-form + short-form), `specs/`, `projects/` (with `src/compositions/`, `components/`, `scenes/`, plus `remotion.config.ts`), and `output/`.
2. Claude builds the folder as you go; you do not need to create it manually, but knowing the structure helps you find things.
3. Spec inclusions: beat map, visual philosophy, key moments, audio sync points. Spec exclusions: frame numbers, pixel positions, component props, code.
4. The critical SVG export setting is Object IDs = Layer Names; without it, the layer labels do not survive export.
5. Common troubleshooting: missing Node.js (install first), failed render (ask Claude to audit imports), preview port collision (kill and restart), timing drift (review beat map), ambiguous edits (be more specific).
6. The full workflow in one line: script → spec → build → render → editor.
7. When the file structure gets messy, the fix is a prompt: "Clean up this project folder and update CLAUDE.md to reflect the structure."

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[remotion]]
- [[capcut]]
- [[node-js]]

## Open questions

- None of substance. This is a compiled reference.
