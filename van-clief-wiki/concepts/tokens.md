---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 6
tags: [fundamentals]
---

# tokens

The unit an AI measures input in. Roughly three-quarters of a word, sometimes a full word, sometimes (for long words like "hamburger") three tokens. The term comes from NLP research in the 1990s, borrowed from linguistics (which borrowed it from Old English "taken" - a sign or symbol). A token is the smallest meaningful chunk the model operates on. The [[context-window]] is counted in tokens; "burning tokens" is the idiom for spending the window on content that does not serve the task.

## Claims

- A token is ~3/4 of a word; sometimes a full word; sometimes several per word [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- Origin: 1990s NLP research, needed a unit smaller than the word because languages don't all break the same way; from Old English "taken" (sign/symbol) [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- Token cost is recurring - every prompt pays the token cost of whatever is loaded into the [[context-window]] [sources/foundation-3-1-full-walkthrough]
- Practical scale: a typical meeting note is ~2,000 tokens; Claude's window holds many of them comfortably when filled from the file system rather than clipboard [sources/foundation-4-2-claude-code-in-practice]
- Task routing is the scaling mechanism: load only the tokens the current task needs [sources/foundation-4-5-where-this-goes]
- Practical cost guidance: keep root `CLAUDE.md` under 50 lines because every token in it is re-read on every prompt [sources/playbooks-3-2-github-and-folder-structure]
- "Spend your thinking before you spend your tokens." The five-step planning sequence takes 4-5 prompts upfront, saves hundreds of tokens of rework [sources/playbooks-3-3-pre-build-planning-and-prompt-sequencing]
- Every "I should have done this earlier" moment during a build is a token cost; planning is the mechanism that prevents the expense [sources/playbooks-3-1-build-and-deploy-website]

## Relationships

- Unit of account for [[context-window]]
- Economic reason for [[workspace-isolation]] and [[routing-table]]
