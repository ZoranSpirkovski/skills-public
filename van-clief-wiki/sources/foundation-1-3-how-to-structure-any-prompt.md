---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [foundation, prompting, framework]
---

# foundation-1-3-how-to-structure-any-prompt

> Packaged inside `.wiki/raw/the-foundation.md`, lines ~173-335. Foundation Module 1, Lesson 3.

## Summary

The five-part prompt framework. A prompt is an instruction set; clearer instructions produce better results. Van Clief names Identity, Task, Context, Constraints, and Output Format as the five slots. Folder files carry the persistent parts (Identity, Context); prompts carry the per-task parts (Task, Constraints, Output Format). The lesson also covers chunking large projects into sequential prompts and chunking large inputs into structured sections with a table-of-contents handshake.

## Key claims

1. A useful prompt has five parts: Identity, Task, Context, Constraints, Output Format. Not every prompt uses all five.
2. Identity is the part most people skip; without it output is always more generic.
3. Constraints save editing time: every constraint given is a mistake Claude will not make.
4. Output Format is the difference between reusable output and output that takes 20 minutes to reformat.
5. The folder from [[foundation-1-2-your-first-folder]] handles persistent Identity and Context; prompts handle per-task Task, Constraints, Output Format.
6. Chunking: break large projects into sequential prompts, each asking one clear thing; break large inputs into ordered sections after giving Claude a table of contents.
7. Tabular or spreadsheet data should stay tabular; converting tables to prose wastes tokens and degrades reading.

## Entities mentioned

- [[van-clief]]

## Open questions

- The framework borrows from classical technical-writing advice but no external citation is offered.
- No formal measurement of how much each part contributes; the claims are qualitative.
