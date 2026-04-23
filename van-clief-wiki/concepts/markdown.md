---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 6
tags: [fundamentals, format]
---

# markdown

A plain-text format with lightweight formatting (dashes for bullets, hashtags for headers, asterisks for bold/italic) created by [[john-gruber]] in 2004 as a play on "markup language". The whole folder-as-workspace system is written in markdown - every file at every layer. Claude already writes in markdown natively (bolding, headers, and structure in its responses are markdown rendering); Van Clief's system simply keeps the format end-to-end so the same files that Claude produces are readable by humans and re-readable by Claude without conversion.

## Claims

- Markdown was created by John Gruber in 2004 as "write something readable as plain text that can also render into a formatted document" [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- The name is a play on "markup language" - markdown strips the tag complexity of HTML and leaves plain English with a few symbols [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- Claude's responses are already markdown under the hood - copy a response into a plain text file and the formatting appears as markdown symbols [sources/folder-system-transcript] [sources/foundation-3-1-full-walkthrough]
- Every file in the folder methodology is a `.md` file; plain text editors (Notepad) are sufficient [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- Editing markdown does not break anything - "you can type whatever you want in here. It's just English" [sources/folder-system-transcript]
- Markdown is the format of the animation spec, the style guide, and the component registry in the spec-driven pipeline [sources/foundation-2-6-video-as-code]
- Load-bearing for stateful prompting: small (low token cost), Claude reads it well, editable anywhere, persists between sessions, convertible to formatted Google Docs [sources/stack-1-1-starting-the-build-process] [sources/stack-1-3-designing-for-your-use-case]
- Format of the PRD, CLAUDE.md, and PROGRESS.md at the root of every project [sources/stack-1-2-how-i-use-claude-code-in-build] [sources/stack-2-4-session-persistence-across-devices]

## Relationships

- File format of every artifact in [[three-layer-routing]] - `CLAUDE.md`, `CONTEXT.md`, `REFERENCES.md`, routing tables, source pages, naming convention declarations
- Enables [[folder-as-workspace]] - because every file is human-editable text, the folder itself becomes a direct UI
- Invented by [[john-gruber]]
