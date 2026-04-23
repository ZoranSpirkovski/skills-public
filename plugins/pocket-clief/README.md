# pocket-clief

A Claude Code skill that helps you set up a workspace using Jake Van Clief's folder-architecture method.

## What it does

Run the skill and it walks you through a short workflow: what kind of work this workspace supports, which subfolders (workspaces) it needs, a routing table that maps tasks to files and skills, and a `CLAUDE.md` under 50 lines that acts as the index. You end up with a working scaffold on disk: a root `CLAUDE.md`, one or more workspace subfolders, and a `CONTEXT.md` inside each.

The method: three layers (map, rooms, tools), a routing table as the primary primitive, folder-as-workspace as the thesis, naming conventions instead of a database. All in plain markdown.

## Install

From inside Claude Code:

```
/plugin marketplace add ZoranSpirkovski/skills-public
/plugin install pocket-clief@skills-public
```

## Use

Open the folder you want to organize in Claude Code. Then ask:

- "Help me set up a Claude Code workspace for {{your kind of work}}."
- "Structure this folder using the Van Clief method."
- "Build me a CLAUDE.md and a routing table."

The skill activates, asks a few questions, and produces the scaffold.

## Credit

The method this skill applies was taught by Jake Van Clief. Go deeper at https://www.skool.com/quantum-quill-lyceum-1116.
