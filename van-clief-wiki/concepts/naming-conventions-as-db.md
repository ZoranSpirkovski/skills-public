---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [core, pattern, spine]
---

# naming-conventions-as-db

Predictable filename patterns that let Claude find, sort, and move files without any database, index, or vector store. Blog drafts are `topic-name_draft.md`; final scripts `topic-name_final.md`; newsletters `YYYY-MM-platform-topic.md`; demo script version 2 is `demo_v2.md`. Because the naming convention is declared in `CLAUDE.md`, saying "pull my demo v2 and build a spec from it" is enough - Claude knows where to look, what to pull, and what to do next. No SQL, no vector DB, no Python framework: just a convention agreed between the user and Claude.

## Claims

- Predictable filename patterns replace the need for a database, index, or vector store [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- Naming conventions are declared once inside `CLAUDE.md` and then apply everywhere in the project [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- The user can issue natural-language commands ("pull my demo v2") and Claude resolves them by convention without any query layer [sources/folder-system-transcript]
- Common patterns: `_draft.md`, `_final.md`, `_v2.md`, date-prefixed files (`YYYY-MM-DD-…`), platform-prefixed output files [sources/foundation-3-1-full-walkthrough]
- This is a deliberate substitution for code/infrastructure - "zero code technically speaking" is the stance [sources/folder-system-transcript]
- Each archetype brings its own conventions: content creators use `topic_draft.md` / `topic_final.md` / `YYYY-MM-platform-topic.md`; developers use `feature_spec.md`, PascalCase components, `feature.test.ts`, `YYYY-MM-DD-decision-title.md` [sources/foundation-3-2-customizing-for-your-use-case]
- At project level, naming conventions sit in the `CLAUDE.md` alongside the routing table - the two primitives together let Claude resolve natural-language file references [sources/foundation-4-4-making-claude-understand]
- Extended into design files via [[svg-layer-naming]]: Illustrator layer names become SVG element IDs and then become the surface Claude targets for natural-language edits [sources/playbooks-1-2-illustrator-to-web-animations]

## Relationships

- Lives inside Layer 1 of [[three-layer-routing]], typically as a section beneath the [[routing-table]]
- Enables the "read" column of the [[routing-table]] to work without ambiguity
- The mechanism that makes [[folder-as-workspace]] navigable at scale
