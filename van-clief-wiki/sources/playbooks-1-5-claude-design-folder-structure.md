---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, claude-design, module-1, local-models]
---

# playbooks-1-5-claude-design-folder-structure

> Source: Implementation Playbooks course, Module 1 Lesson 1.5. Video transcript plus written text companion. File: `.wiki/raw/playbooks/lesson-1-5-claude-design-folder-structure.md`.

## Summary

Anthropic's new Claude Design product generates folders, markdown files, and custom skills from existing brand assets (GitHub repos, Figma files, local folders). Van Clief opens the zip and confirms: underneath the interface, it is Claude Code plus a set of skills plus a folder structure, the same pattern the Implementation Playbooks already teach. The lesson walks through building a design system in the product, then exporting the zip and running the same workflow locally with Claude Code or with an open-source model (Qwen 3 Coder Next, Code Gemma, Devstral, DeepSeek Coder V2). The point: the pattern is model-agnostic because it is just files.

## Key claims

1. Claude Design burns usage fast. Van Clief consumed 83% of a Max plan in a day testing features.
2. The product creates a design system out of whatever assets you point it at: GitHub repo, Figma file, or local folder.
3. Generated artifacts include a voice document, color and typography tokens, component references, and a custom skill with routing to each artifact.
4. The generated skill embeds routing: "here are the important files, here are the non-negotiables, here are the main colors." Van Clief calls this his routing process automated.
5. Behind the interface it is still Claude Code plus skills plus folders. Any coding agent that reads files and makes tool calls can use the exported zip.
6. Four local-model fallbacks named: Qwen 3 Coder Next (Alibaba, 80B with partial-parameter loading), Code Gemma (Google DeepMind), Devstral (Mistral, API or local), DeepSeek Coder V2 (open source).
7. The exported zip opens in Claude Code, VS Code, or any IDE; `/init` generates a `CLAUDE.md` that references the design-system files.
8. Strong advice to invest design time in Figma first, then let the tool amplify. "Figma is not useless anymore."
9. The generated `CLAUDE.md` does not show the folder structure; Van Clief recommends adding it manually so Claude does not spend tokens searching.
10. [[obsidian]] is mentioned as useful for visualizing the folder graph but is positioned as an advanced tool, not essential for early users.
11. "Productionize your opinion." In a world where everyone gets decent output, the designer's point of view becomes the valuable input.
12. The broader claim: more tools like Claude Design will appear. Learn the fundamentals (folder structure, routing) so you are not locked to one vendor.

## Entities mentioned

- [[van-clief]]
- [[claude-code]]
- [[claude-design]]
- [[figma]]
- [[obsidian]]
- [[vs-code]]
- [[qwen-3-coder]]
- [[code-gemma]]
- [[devstral]]
- [[deepseek-coder]]

## Open questions

- Official Claude Design URL not inlined.
- The Adoba design system referenced is Van Clief's own company; no public link.
- Remotion animation video referenced but not named.
