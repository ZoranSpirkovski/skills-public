---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 24
tags: [tool, ai-agent, anthropic]
---

# claude-code

Anthropic's terminal/IDE agent - Claude running with direct read-write access to the user's files. Reads `CLAUDE.md` on entering a folder, can edit files, run commands, and iterate. Central runtime for the folder methodology: when Van Clief says "Claude enters a workspace" and reads context files, the "Claude" is typically Claude Code.

## Claims

- Reads `CLAUDE.md` automatically on entering a project folder via `cd <folder>` then `claude` [sources/foundation-1-2-your-first-folder] [sources/foundation-3-1-full-walkthrough]
- Operates inside folders directly - no cloud-based state, files stay local [sources/folder-system-transcript]
- Accessible via Pro and Max subscription tiers [sources/foundation-1-2-your-first-folder] [sources/foundation-1-1-what-you-need]
- Demo tool for the three-layer walkthrough in Foundation 3.1 and the folder-system talk [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- Installed via `npm install -g @anthropic-ai/claude-code` (requires Node.js) [sources/foundation-4-1-install-and-first-use] [sources/foundation-1-1-what-you-need]
- Same model as Claude Desktop; difference is reach and the iteration loop (Read → Think → Write → Check → Adjust) [sources/foundation-4-2-claude-code-in-practice]
- Available as both a terminal tool and a VS Code extension; they share the same engine [sources/foundation-4-1-install-and-first-use]
- Runtime for the spec-driven animation pipeline: reads spec, style guide, and component registry, composes components into scenes [sources/foundation-2-6-video-as-code]
- Project-level `CLAUDE.md` read automatically on every start of a project session [sources/foundation-4-4-making-claude-understand]
- Makes the full three-layer folder architecture operational - the piece that actually runs routing tables, per-workspace context loading, and naming conventions [sources/foundation-4-5-where-this-goes]
- Pairs with Claude Desktop in the "Desktop for decisions, Code for execution" workflow [sources/foundation-4-3-claude-desktop-thinking-partner]
- Positioned as Level 3 on the [[tool-ladder]] and the runtime wrapped by Level 4 custom builds [sources/stack-1-1-starting-the-build-process]
- In Van Clief's Building Your Stack build, the front-end wraps Claude Code (riding the subscription) rather than making direct API calls, to avoid cost explosion [sources/stack-1-2-how-i-use-claude-code-in-build]
- Claude 4.6 spawns sub-agents during long builds; main Claude orchestrates while sub-agents fetch and study [sources/stack-1-3-designing-for-your-use-case]
- Plan mode vs execution mode: plan mode thinks through steps first; Claude usually chooses on its own [sources/stack-1-3-designing-for-your-use-case]
- Remote Control is built in: `claude rc` (server mode), `claude --rc` (interactive plus remote), or `/rc` (mid-session) starts a phone-accessible session [sources/stack-2-1-why-remote-access] [sources/stack-2-2-setting-up-remote-sessions]
- Remote Control keeps execution local: files, MCP servers, CLAUDE.md stay on the user's machine; the phone is a window into the local session [sources/stack-2-1-why-remote-access]
- Installs Remotion, Node.js, and the Remotion agent skills directly from a single user prompt [sources/playbooks-1-1-building-animations-with-claude-code]
- Edits individual React scene components on natural-language requests without rewriting the rest of the pipeline [sources/playbooks-1-1-building-animations-with-claude-code] [sources/playbooks-1-2-illustrator-to-web-animations]
- Writes project memory to a local file automatically; no separate memory system needed beyond folder structure and `CLAUDE.md` [sources/playbooks-3-1-build-and-deploy-website]
- Installs GitHub CLI, authenticates, creates repos, sets up `.gitignore`, and pushes on behalf of the user [sources/playbooks-3-1-build-and-deploy-website] [sources/playbooks-3-2-github-and-folder-structure]
- Runtime underneath [[claude-design]]: the exported zip opens in Claude Code and runs the generated skill unchanged [sources/playbooks-1-5-claude-design-folder-structure]
- Multiple Claude Code sessions can run on the same project in parallel when the folder structure is clean and `CLAUDE.md` is current [sources/playbooks-3-2-github-and-folder-structure]

## Relationships

- Runtime for [[three-layer-routing]]
- Part of [[three-interfaces]] alongside [[claude-desktop]] and terminal Claude Code
- Alternative: [[claude-cowork]] (folder-aware, inside the Anthropic app)
- Often used inside [[vs-code]] or [[cursor-editor]], though those are explicitly optional
- Runtime used in [[spec-driven-pipeline]] and the Ethics Engine work
- Wrapped by [[claude-code-web]], [[op-code]], and [[claude-cli-ui]] in the open-source ecosystem
- Hosts [[remote-control]], [[mobile-workflow-modes]], [[handoff-pattern]], and Van Clief's [[control-surface]] build
