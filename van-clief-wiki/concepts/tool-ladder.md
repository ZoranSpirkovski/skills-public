---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [stack, interfaces, tool-choice]
---

# tool-ladder

Van Clief's four-level scale for deciding how much UI scaffolding you actually need around Claude. Level 1: Claude Projects on claude.ai, using project instructions and knowledge files (no code). Level 2: Claude Cowork, inside the Anthropic app, more control than chat without full filesystem access. Level 3: VS Code plus Claude Code, full readability and folder navigation, the layer most people should land on. Level 4: a custom front-end built around Claude Code. Each level adds both complexity and capability. Anthropic keeps replacing Level 4 features with native Level 1-3 ones, so the philosophy is know how to build custom, always ask whether you need to, and move up only when the level below hits a wall.

## Claims

- Four levels: Claude Projects, Claude Cowork, VS Code plus Claude Code, custom front-end [sources/stack-1-1-starting-the-build-process]
- Most people should land at Level 3 and only move to Level 4 when Level 3 cannot solve their problem [sources/stack-1-1-starting-the-build-process]
- Each level adds complexity; each level adds capability [sources/stack-1-1-starting-the-build-process]
- Features that required Level 4 a year ago often exist in Level 1-3 now. Anthropic keeps shipping native features that replace custom builds [sources/stack-1-1-starting-the-build-process]
- Philosophy: know how to build custom so you can when you need to, but always ask whether you need to. The best tool is the simplest one that solves the problem [sources/stack-1-1-starting-the-build-process]

## Relationships

- Level 3 is the runtime context for [[three-layer-routing]] in practice via [[vs-code]] and [[claude-code]]
- Level 2 is [[claude-cowork]]
- Level 4 is the subject of the Building Your Stack course
- Related to [[three-interfaces]] (interfaces over one Claude model) but orthogonal: three-interfaces is about Claude's access surface, tool-ladder is about how much UI you build around it
