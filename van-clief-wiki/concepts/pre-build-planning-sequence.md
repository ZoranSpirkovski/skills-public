---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [planning, prompt, method, tokens]
---

# pre-build-planning-sequence

The five planning steps that run in Claude chat before Claude Code writes a single file: (1) analyze what exists, (2) write a briefing document, (3) send a first prompt with folder structure, deployment target, scope boundaries, and the "ask me three questions" suffix, (4) answer the alignment questions, (5) request a PRD and explicitly block building. The thesis in one line: "spend your thinking before you spend your tokens." Four to five planning prompts upfront, two or three build prompts. Total under ten. The method works for websites, internal tools, content systems, and client work.

## Claims

- Five steps: analyze, brief, first-prompt-with-boundaries, answer alignment questions, request PRD [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing] [sources/playbooks-3-1-build-and-deploy-website]
- Step 1 lives in Claude chat, not Claude Code; the browser session loads context about the current state [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Step 2 produces the markdown briefing that transfers context between sessions [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Step 3's first prompt bundles five jobs: folder structure with `CLAUDE.md`, deployment target, scope boundaries, tech preference, and the alignment-question suffix [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing] [sources/playbooks-3-1-build-and-deploy-website]
- The "ask me three questions" suffix forces Claude to process everything and surface gaps before building [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Answering alignment questions is cheap; discovering the same gap after 15 files exist is hundreds of tokens of rework [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Step 5 requires "do not start building yet". The PRD is the last free checkpoint before code [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Method generalizes: internal tools, content systems, and client work all use the same five steps with different inputs [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Total prompt count for a full project when the method is followed: under ten [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]

## Relationships

- Produces a [[briefing-document]] at Step 2
- Produces a PRD at Step 5, see [[prd-first-methodology]]
- Seeds the [[claude-md-three-file-pattern]] in the Claude Code project
- Core discipline: planning saves tokens (see [[tokens]])
