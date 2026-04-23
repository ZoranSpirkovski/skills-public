---
type: entity
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [model, local, open-source, alibaba]
---

# qwen-3-coder

Qwen 3 Coder Next: open-source coding model from Alibaba. Named in Playbooks 1.5 as one of four local fallbacks for running the Claude Design exported design-system workflow without burning Claude usage. Distinguished by a mixture-of-experts architecture: an 80-billion-parameter model that only loads a subset of parameters per inference, letting it run on modest graphics cards.

## Claims

- 80-billion-parameter model that loads parameters partially per inference; runs on smaller GPUs than the total size suggests [sources/playbooks-1-5-claude-design-folder-structure]
- Strong at file navigation and tool calls; viable for running exported Claude Design workspaces locally [sources/playbooks-1-5-claude-design-folder-structure]
- Van Clief's first-named local fallback when Claude usage limits are a concern [sources/playbooks-1-5-claude-design-folder-structure]

## Relationships

- Local alternative to [[claude-code]] for [[claude-design]] exported projects
- Peer of [[code-gemma]], [[devstral]], [[deepseek-coder]]
