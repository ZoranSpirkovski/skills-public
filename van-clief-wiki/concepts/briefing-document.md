---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [planning, handoff, markdown, workspace]
---

# briefing-document

The markdown file that transfers context between Claude chat (the browser product) and Claude Code (the file-aware agent). The two are separate sessions and do not share memory. The briefing document is the bridge. Van Clief runs analysis in Claude chat, then asks: "Based on what you found, create a markdown file describing the structure and build. Write it for Claude Code to read, not for me." The file drops into the project folder and becomes the opening context for the build. The same idea generalizes to [[claude-design]] exports and client-work discovery calls, where the tangible deliverable is the briefing document.

## Claims

- Claude chat and Claude Code are separate sessions; they do not share memory [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- The briefing document is the transfer mechanism between the two [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Prompt pattern: "create a markdown file describing the structure and build. Write it for Claude Code to read, not for me." [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Without it, the user re-explains everything in the first Claude Code prompt: slow, expensive, and usually incomplete [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- The move that saves the most tokens long-term: the markdown briefing [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- For client work, the briefing document comes out of the discovery call and is the tangible deliverable [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Can also be generated or sourced from [[claude-design]] exports (slide deck briefings, design-system documents) and handed into a Claude Code project [sources/playbooks-1-5-claude-design-folder-structure]

## Relationships

- Step 2 inside [[pre-build-planning-sequence]]
- Feeds the first [[claude-md-three-file-pattern]] file in a new Claude Code project
- Format is [[markdown]]
