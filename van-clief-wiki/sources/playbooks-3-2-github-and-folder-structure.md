---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, website, github, module-3]
---

# playbooks-3-2-github-and-folder-structure

> Source: Implementation Playbooks course, Module 3 Lesson 3.2. Written lesson (video pending). File: `.wiki/raw/playbooks/lesson-3-2-github-and-folder-structure.md`.

## Summary

The slow-down companion to Lesson 3.1. Teaches the minimum GitHub model (repo, branches, push, Pages, Actions, `.gitignore`) and why folder structure changes what Claude Code can do. The load-bearing argument: the folder structure you build locally is what GitHub stores; if the folders are clean and `CLAUDE.md` maps them, Claude pays zero tokens figuring out where files live. Includes an example project folder layout with folder-level README files and an explicit rule that `CLAUDE.md` should stay under 50 lines because it is read on every prompt.

## Key claims

1. You will use one repo per website or project; `main` is the live branch; branching matters more for teams.
2. Pushing sends local files to GitHub; Claude Code handles the first-time setup and every subsequent push is a single prompt.
3. GitHub Pages has two routes: simple (upload `index.html`, enable Pages) and build-based (Astro, React, etc., where GitHub Actions runs a build step). Claude Code sets up the Actions workflow (`.github/workflows/deploy.yml`).
4. `.gitignore` must exclude `.env` files, `node_modules`, build/cache output, and any private markdown (e.g. internal `CLAUDE.md`, brand voice docs). Pushing `.env` to a public repo is the most common beginner security mistake.
5. `.gitignore` test: "would I be comfortable if a stranger read this file?" If no, add it.
6. The reason folder structure matters is routing. `CLAUDE.md` is read first; if it names the folders accurately, Claude starts working immediately instead of scanning.
7. `CLAUDE.md` under 50 lines. Every token in it is re-read on every prompt; bloat costs on every single prompt.
8. Folder-level READMEs carry detailed context for each folder. Claude reads them when it enters that folder. This keeps root `CLAUDE.md` lean while still giving Claude full context on demand.
9. Example structure: `CLAUDE.md` at root; `docs/` with brand-voice, design-tokens, PRD; `src/` with `components/`, `pages/`, `layouts/` each with READMEs; `public/images/`; `.gitignore`.
10. Clean folders enable multiple Claude Code sessions on the same project in parallel (one on components, one on content, one on research), all coordinated by the same `CLAUDE.md`.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[github]]
- [[github-pages]]
- [[astro]]

## Open questions

- Branching and PR workflows are intentionally held back for team contexts; not taught here.
- Deploy.yml contents are referenced but not shown.
