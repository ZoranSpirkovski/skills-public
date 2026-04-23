---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 2
tags: [stack, ui, workflow, driving-modes]
---

# control-surface

Van Clief's framing of what a custom front-end for Claude should actually be. Not a prettier chat UI, but a surface that lets you fluidly switch between two modes: "I'm driving" (editing every individual file manually) and "Claude's driving" (automating the whole pipeline and trusting Claude to run it). The specific layout in Van Clief's build: workflow map on the left (visual nodes, not a folder tree), file editor in the middle, Claude Code chat on the right. Panels collapse. Multiple chats open. The point is switching modes without friction, not adding features.

## Claims

- The abstract goal is "a control surface that I can fluidly switch, between I'm driving or Claude's driving" [sources/stack-1-3-designing-for-your-use-case]
- Two driving modes: manual per-file editing, and automated pipeline execution [sources/stack-1-3-designing-for-your-use-case]
- The panel layout: workflow map left, file editor middle, Claude Code chat right. Multiple chats, collapsible panels, minimal [sources/stack-1-2-how-i-use-claude-code-in-build] [sources/stack-1-3-designing-for-your-use-case]
- Not a prettier Claude front-end. The goal is control over files, routing, automation, and file swapping [sources/stack-1-3-designing-for-your-use-case]
- Built by wrapping Claude Code (riding the subscription), not by making direct API calls [sources/stack-1-2-how-i-use-claude-code-in-build]

## Relationships

- The Level 4 artifact on [[tool-ladder]]
- Implements [[folder-as-ui]] by giving the folder a visual node-map and editable panels
- Runtime is [[claude-code]]; the workflow map idea draws visual patterns from [[n8n]] and [[langflow]]
- Built inside an existing [[folder-as-workspace]] so Claude can reference the pipeline it is wrapping
