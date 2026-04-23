---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, claude-code, claude-md, project-level]
---

# foundation-4-4-making-claude-understand

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~2097-2206. Foundation Module 4, Lesson 4 (Session 4 of 5).

## Summary

One file gets Claude Code from "smart stranger" to "team member who has been here a month" - the project-root `CLAUDE.md`. Fifteen lines. Ten minutes. Claude Code reads it automatically on every start. Van Clief names five sections: project overview, tech stack, how to run things, key conventions, what to avoid. The full example is a React + Express + PostgreSQL + TypeScript project with four-line sections for each category. The A/B test (same task with and without the file) is positioned as the value-unlock. This lesson is a project-level variant of the identity/context files introduced in [[foundation-1-2-your-first-folder]].

## Key claims

1. One file changes Claude Code's behavior visibly: a project-root `CLAUDE.md` read automatically on every start.
2. Five sections cover it: project overview (2-3 sentences), tech stack, commands (dev/test/build), conventions, what to avoid.
3. Fifteen lines is enough; ten minutes to write. A mediocre CLAUDE.md beats no CLAUDE.md.
4. The before/after A/B test is the recommended way to feel the value: run the same task with and without the file.
5. Without a project `CLAUDE.md`: generic code style, guessed file structure, unknown commands, wrong libraries. With one: matched conventions, known structure, correct commands, correct dependencies.
6. The file is a living document - updated as the project evolves, same rule as [[foundation-3-3-common-mistakes]].
7. Works for non-code projects too: describe the document types, organization, and how to use the files.
8. This CLAUDE.md is a project-specific version of the identity file from [[foundation-1-2-your-first-folder]]. It becomes Layer 1 when the user grows into the full three-layer architecture.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]

## Open questions

- The template here is narrower than the "routing-table-bearing" CLAUDE.md of Foundation 3.1. Worth flagging: the project-level CLAUDE.md is a subset of the map/layer-1 CLAUDE.md. Not quite a contradiction; a scale difference.
