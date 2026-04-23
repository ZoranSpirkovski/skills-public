---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [hosting, deployment, static]
---

# github-pages

GitHub's free static-site hosting. Used as the default deployment target for the Playbooks Module 3 website build. Two paths exist: the simple path (upload an `index.html`, enable Pages in settings, get a URL in three minutes) and the build-based path (Astro, React, frameworks where GitHub Actions runs a build step and deploys). A common first-deploy failure is CSS paths that assume a local URL prefix; the fix is a short note to Claude about the broken paths.

## Claims

- Free static hosting provided by GitHub; live URL updates about a minute after a push [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-2-github-and-folder-structure]
- Simple route: create a repo, upload `index.html`, turn on Pages, select main branch. Three minutes [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-2-github-and-folder-structure]
- Build-based route: GitHub Actions runs the build (Astro, React, etc.) and deploys; Claude Code sets up the workflow file [sources/playbooks-3-2-github-and-folder-structure]
- A common first-deploy failure: CSS pathing breaks because local and GitHub environments have different URL prefixes; fixed by a short prompt or screenshot [sources/playbooks-3-1-build-and-deploy-website]
- For a single-page site, an HTML artifact from Claude chat can be uploaded directly; Claude Code is unnecessary [sources/playbooks-3-1-build-and-deploy-website]

## Relationships

- Hosted on [[github]]
- Deployment target for [[pre-build-planning-sequence]] outputs
- Alternative: Vercel (mentioned as a deployment-target option in Lesson 3.3)
