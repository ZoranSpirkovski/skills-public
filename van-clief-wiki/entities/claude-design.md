---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [anthropic, product, tool, design]
---

# claude-design

Anthropic's product that generates design systems, slide decks, prototypes, and animated content from existing brand assets. Accepts GitHub repos, Figma files, or local folders as inputs and produces folders, markdown voice documents, color/typography tokens, component references, and a custom skill with routing. Powered by Claude Code behind the interface. Van Clief's key observation: it is the packaged version of the folder-plus-skills pattern the Implementation Playbooks have been teaching since the start. The exported zip runs in any IDE with any coding agent.

## Claims

- Generates folders, markdown files, and components from existing assets (GitHub, Figma, local folder) [sources/playbooks-1-5-claude-design-folder-structure]
- Underneath the interface: Claude Code + skills + folder structure; the same pattern Van Clief has been teaching [sources/playbooks-1-5-claude-design-folder-structure]
- Burns tokens fast; Van Clief reports consuming 83% of Max plan usage in a single day of testing [sources/playbooks-1-5-claude-design-folder-structure]
- Generated skill embeds routing: important files, non-negotiables, main colors; essentially Van Clief's routing process automated [sources/playbooks-1-5-claude-design-folder-structure]
- Export as zip opens in Claude Code, VS Code, or any IDE; any coding agent that reads files and makes tool calls can use it [sources/playbooks-1-5-claude-design-folder-structure]
- Export flows: duplicate project, download as zip, export to PowerPoint or HTML, import to Canva, or send to Claude Code directly [sources/playbooks-1-5-claude-design-folder-structure]
- Generated `CLAUDE.md` does not include the folder tree; Van Clief recommends adding it manually so Claude does not search [sources/playbooks-1-5-claude-design-folder-structure]
- Project types: design system, slide deck, prototype, animated video, full branded documents [sources/playbooks-1-5-claude-design-folder-structure]
- Demonstrated proof-point for [[appless-work]]: the product is an interface on a folder pattern that runs unchanged locally [sources/playbooks-1-5-claude-design-folder-structure]

## Relationships

- Product of [[anthropic]], runs [[claude-code]] behind the interface
- Accepts [[figma]] and [[github]] repos as input
- Exported zip works with open-source local models: [[qwen-3-coder]], [[code-gemma]], [[devstral]], [[deepseek-coder]]
- Concrete instance of [[appless-work]]
