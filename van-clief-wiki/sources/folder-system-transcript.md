---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [methodology, origin, folder-system, three-layer]
---

# folder-system-transcript

## Summary

Transcript of Van Clief's YouTube talk (`MkN-ss2Nl10`) introducing the folder-as-workspace / three-layer routing architecture. Addressed to a general audience with a VS Code + Claude Code demo, the talk argues that most people using AI are wasting tokens by dumping everything into one conversation, and that a three-layer folder system (root `CLAUDE.md` as map → per-workspace `CONTEXT.md` → files) with a natural-language routing table inside `CLAUDE.md` solves routing, context hygiene, and editability at once. This is the origin document for the workspace-as-app thesis that later lessons extend.

## Key claims

1. Context windows are finite; dumping unrelated work into one chat wastes tokens on content that does not matter to the current task.
2. Three layers - map (`CLAUDE.md`) → rooms (workspace `CONTEXT.md`) → workspace (files) - decouple what is always loaded from what is loaded only when a task enters that workspace.
3. The single most important pattern in the whole system is a routing table inside `CLAUDE.md` telling Claude, for each task: go here, read these files, skip those, use these skills.
4. Naming conventions (e.g. `blog_draft_v2.md`, `2026-03-launch-week.md`, `demo_v2.md`) replace the need for any database, index, or vector store - Claude finds work by convention.
5. The folder is the UI. VS Code is optional; Claude can work just as well in plain Finder/Explorer. The next stage Van Clief predicts is voice-driven folders.
6. Skills should be wired per-workspace, not globally loaded. A project can reference 100 skills but each workspace only loads the ones its tasks need.
7. This is not a prompt trick. It is the application of decades-old software engineering principles (separation of concerns, rules of transparency and composition) to AI workflow - a research paper is in progress outlining a five-layer architecture of which this talk covers three.

## Entities mentioned

- [[van-clief]] - the author, presenter of the talk
- [[claude-code]] - the CLI agent the demo runs in
- [[vs-code]] - the IDE used for the demo (though explicitly declared optional)
- [[john-gruber]] - credited as the inventor of markdown in 2004
- [[markdown]] (concept, also a named artifact) - the file format every workspace file uses
- [[remotion]] - mentioned in a content-creator example as an animation library
- [[obsidian]] - mentioned in passing as a suitable reading environment

## Open questions

- The full five-layer architecture referenced but not detailed - research paper not included in this source.
- Voice-driving workspaces ("within six months, everyone's going to be doing this") - predicted but not demonstrated.
- No concrete handling of multi-user or team scenarios - system is presented as single-operator.
