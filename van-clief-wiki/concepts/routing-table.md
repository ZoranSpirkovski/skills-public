---
type: concept
created: 2026-04-23
updated: 2026-04-23
sources: 5
tags: [core, pattern, spine]
---

# routing-table

A plain-markdown table placed inside `CLAUDE.md` that maps tasks to the workspaces, files, and skills they need. Columns are typically: `Task | Go to | Read | Skills`. Each row names a kind of work the user does, the workspace Claude should enter for it, the specific files to load, and the skills (if any) to activate. The purpose is to tell Claude, for each task, exactly what to read and what to skip - eliminating the failure modes of reading everything (token waste), guessing wrong (poor output), or producing work that cannot be edited at each step. Van Clief calls this the single most important pattern in the whole system.

## Claims

- The routing table is the most important pattern in the folder system - without it Claude reads everything, guesses wrong about what matters, or produces uneditable work [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- Standard columns: task, go-to (workspace), read (files), skills (tools) [sources/foundation-3-1-full-walkthrough] [sources/folder-system-transcript]
- The table is plain markdown and human-editable in place - no configuration language, no DSL [sources/folder-system-transcript]
- Each row is a piece of function-calling: same pattern software engineers have used for decades, now expressed in natural-language rows rather than code [sources/folder-system-transcript]
- Can be rearranged with a simple line move - swap skills in and out per task by editing the row [sources/folder-system-transcript]
- Three archetype examples demonstrated with explicit tables: content creator, freelancer, developer. The developer table is the one that shows the Skills column [sources/foundation-3-2-customizing-for-your-use-case]
- Skipping the routing table is one of the seven common mistakes - without it Claude guesses wrong, reads everything, or produces inconsistent output [sources/foundation-3-3-common-mistakes]
- Three columns are the minimum (task, go-to, read); four if skills are wired [sources/foundation-3-3-common-mistakes]
- Claude Design's auto-generated skill embeds routing inside the skill file itself (important files, non-negotiables, main colors): the routing process automated [sources/playbooks-1-5-claude-design-folder-structure]

## Relationships

- Lives inside Layer 1 of [[three-layer-routing]]
- Drives loading of workspace [[context-md-workspace-files]] (Layer 2)
- Names which [[skills-wired-per-task]] to activate (Layer 3)
- Relies on [[naming-conventions-as-db]] to make "read these files" unambiguous without a query layer
- The routing table is the feature that most distinguishes mature workspaces from the three-file [[claude-md-three-file-pattern]] entry point
