---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 3
tags: [core, prompting, framework]
---

# prompt-framework-5-part

Van Clief's five-part prompt framework. A prompt is an instruction set, and any useful prompt lives somewhere in five slots: Identity (who Claude is right now), Task (what needs to get done), Context (what Claude needs to know), Constraints (what to avoid), and Output Format (what shape the answer should take). Not every prompt needs all five, but knowing the five lets the user diagnose which one is missing when output goes wrong. The framework pairs with the folder architecture: persistent slots (Identity, Context) live in files, per-task slots (Task, Constraints, Output Format) live in the prompt itself.

## Claims

- Five slots: Identity, Task, Context, Constraints, Output Format [sources/foundation-1-3-how-to-structure-any-prompt]
- Identity is the most-skipped slot; without it output is always more generic [sources/foundation-1-3-how-to-structure-any-prompt]
- Constraints save editing time; every constraint is a mistake Claude will not make [sources/foundation-1-3-how-to-structure-any-prompt]
- Output Format determines whether output is immediately usable or needs 20 minutes of reformatting [sources/foundation-1-3-how-to-structure-any-prompt]
- Pairs with folder architecture: Identity and Context live in files, Task and Constraints in the prompt, Output Format in the prompt [sources/foundation-1-3-how-to-structure-any-prompt]
- Structurally identical to the Mad Libs typed-slot pattern [[foundation-2-3-1953-word-game]] teaches [sources/foundation-2-3-1953-word-game]
- Inside [[claude-code]] the framework simplifies: Identity and Context come from the folder files; Task, Constraints, Output Format go in each message [sources/foundation-4-2-claude-code-in-practice]

## Relationships

- Pairs with [[claude-md-three-file-pattern]] and [[three-layer-routing]] (folder handles persistent slots)
- Application of the template pattern discussed under memory and abstraction in [[foundation-2-3-1953-word-game]]
