---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, abstraction-series, memory, prompting]
---

# foundation-2-3-1953-word-game

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~611-849. Foundation Module 2, Lesson 3.

## Summary

The 1953 invention of Mad Libs by Leonard Stern and Roger Price becomes the pivot for reframing programming as template-filling. Every programming layer is a typed-slot template composed into larger templates, all the way down. Memory in traditional computing is a hierarchy (registers, cache, RAM, disk, archive) with a strict code-versus-data boundary. In AI systems the hierarchy rhymes (weights, context window, system prompt, retrieved context, persistent memory) but the boundary collapses: code and data are the same thing. Prompting is therefore not tips and tricks but programming at the highest abstraction layer yet built. Grace Hopper's 1952 compiler story is cited as precedent: every new abstraction starts untrusted and becomes trustworthy through infrastructure.

## Key claims

1. Mad Libs is not a metaphor for programming; programming is structurally Mad Libs - typed slots in templates, composed into larger templates.
2. Traditional computing enforces a hard boundary between code and data; mixing them is a security vulnerability (buffer overflow).
3. AI systems collapse that boundary: system prompt, user message, retrieved document, skill file are all text in one sequence the model attends to and continues. Reading is execution.
4. Prompt injection works because the architecture has no code/data distinction - "this is not a bug. It is the architecture."
5. AI memory hierarchy: weights (read-only), context window (working memory), system prompt (firmware), retrieved context (load-from-disk), persistent memory (carries across sessions).
6. Grace Hopper built a working compiler in 1952 that nobody would touch - "they told me computers could only do arithmetic." Each new abstraction layer (assembly, high-level languages, interpreted languages, AI) hit the same skepticism and then became infrastructure.
7. The folder architecture from [[foundation-1-2-your-first-folder]] is a practical implementation of the AI memory hierarchy: `CLAUDE.md` is the system prompt layer, workspace context is retrieved context, skills are on-demand tooling.
8. The prompting framework from [[foundation-1-3-how-to-structure-any-prompt]] maps directly onto the typed-slot pattern - Identity, Task, Context, Constraints, Output Format are five blanks in a template.

## Entities mentioned

- [[van-clief]]

## Open questions

- Grace Hopper is named and quoted but has no entity page yet. Candidate for a later ingest pass.
- Leonard Stern and Roger Price (Mad Libs inventors) are named once but carry no further weight in the corpus; skip for now.
- The "code and data are the same thing" claim for AI is load-bearing; some cryptographic or sandboxing arguments might challenge it. No contradiction yet in the wiki.
