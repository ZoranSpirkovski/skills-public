---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [platform, ownership, hosting, deployment]
---

# github

Code hosting and collaboration platform. Van Clief cites it as the working proof that students and developers can own the output of their work. CS majors are hired now on the strength of their GitHub portfolios, not their GPAs. Van Clief uses GitHub as the reference architecture for what an equivalent AI-ownership platform would look like for student-trained models. In the Implementation Playbooks Module 3, GitHub also serves as the deployment target and storage layer for every Claude Code project, with `.gitignore`, GitHub Actions, and GitHub Pages taught as the load-bearing primitives.

## Claims

- Proof that individual creators can own their code rather than surrender it to institutions [sources/archive-3-2-questions-schools-should-be-asking]
- CS hiring now runs on GitHub portfolios (actual code, real projects, proof of build ability) [sources/archive-3-2-questions-schools-should-be-asking]
- One repo per website or project; `main` is the live branch; branching matters more for teams [sources/playbooks-3-2-github-and-folder-structure]
- Claude Code handles first-time setup (install GitHub CLI, authenticate, create repo, set up `.gitignore`) then pushes in a single prompt on subsequent changes [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-2-github-and-folder-structure]
- Hosts [[github-pages]] as free static hosting for sites built with Claude Code [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-2-github-and-folder-structure]
- GitHub Actions runs build steps for React/Astro/complex builds via a `.github/workflows/deploy.yml` Claude Code generates [sources/playbooks-3-2-github-and-folder-structure]
- `.gitignore` must exclude `.env`, `node_modules`, build cache, and private markdown; pushing `.env` is the most common beginner security mistake [sources/playbooks-3-2-github-and-folder-structure]

## Relationships

- Cited as precedent for [[ai-ownership-in-education]] alongside [[substack]] and [[bandcamp]]
- Hosts [[github-pages]]
- Integrated with [[claude-code]] via the GitHub CLI
- Governed by [[gitignore-discipline]]
