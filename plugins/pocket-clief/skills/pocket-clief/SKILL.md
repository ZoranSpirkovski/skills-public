---
name: pocket-clief
description: Use when the user wants to set up a new Claude Code workspace, structure an existing folder for Claude to navigate, or apply Jake Van Clief's folder-architecture teaching. Triggers on "set up a workspace", "organize my folder for Claude", "how do I structure this project", "build me a CLAUDE.md", "routing table". Produces a working scaffold: a lean root CLAUDE.md with a routing table, one or more workspace subfolders each with a CONTEXT.md, and naming conventions as a lightweight database. Teaches three-layer routing, folder-as-workspace, and workspace isolation as it goes.
---

# pocket-clief

Help the user stand up a Claude Code workspace the way Jake Van Clief teaches it. This skill applies Van Clief's folder-architecture method and labels where it extends or interprets his teaching.

When invoked, walk the user through the workflow below and produce a working scaffold on disk. Teach the teachings as you go. Do not substitute other frameworks or invent new primitives.

## Core teachings (read before acting)

The architecture has three layers. Each layer has a distinct job and a distinct loading rule. Keeping them separate is what preserves the context window for the actual task.

Provenance note: claims tagged `[Van Clief]` paraphrase his public teaching on folder architecture; claims tagged `[synthesis]` are this skill's own framing, interpretation, extension, or specific numeric threshold, not his direct words. When uncertain, this skill prefers `[synthesis]`. A heavier source-cross-check against his Skool and YouTube material is a follow-up audit.

**Layer 1: the map.** `[Van Clief]` A single `CLAUDE.md` at the project root. It is read on every task entry. It holds the workspace inventory, the routing table, the naming conventions, and the rules. Keep it under 50 lines (the 50 number is this skill's threshold, `[synthesis]`). Every token in it is re-read on every prompt, so bloat costs continually.

**Layer 2: the rooms.** `[Van Clief]` A `CONTEXT.md` inside each workspace folder. It loads only when Claude enters that workspace. It describes what happens in that room, which files matter, and what to avoid. Sibling workspaces never load each other's context.

**Layer 3: the tools.** `[synthesis]` Skills, MCP servers, and other plug-and-play artifacts. They are wired into specific tasks through the routing table, not loaded globally. A project may reference many skills; only the ones the current task names activate. (The exact "Layer 3" framing and the Skills column of the routing table are this skill's extension; Van Clief's canonical three-layer framing may describe the third layer differently.)

**The root is where Claude is running.** `[synthesis]` "Project root" for this skill means the directory in which the user invoked Claude for this session. Not the VS Code workspace folder, not the nearest ancestor with `.git/`, nothing inferred. Sub-folders of the cwd are sub-workspaces (Layer 2, `CONTEXT.md`). Parent folders are out of scope for the session, even if they contain their own `CLAUDE.md` files that Claude Code auto-loads. Nested project roots (a sub-workspace that later functions as its own root when a scoped subagent runs inside it) are a deferred pattern, not the default.

**The routing table is the most important pattern in the whole system.** `[Van Clief]` It is a plain markdown table in `CLAUDE.md` with columns `Task | Go to | Read | Skills`. Each row names a kind of work, the workspace to enter for it, the specific files to load, and the skills (if any) to activate. Without it, Claude reads everything (token waste), guesses wrong (poor output), or produces work that cannot be edited step by step. Three columns are the minimum; four if skills are wired. (The fourth `Skills` column is this skill's extension, `[synthesis]`.)

**Folder-as-workspace is the thesis.** `[Van Clief]` The folder IS the app. Each workspace (subfolder) is a mode of work. No database, no framework, no custom code. Editing the folder is editing the system. Claude Code is the runtime.

**Naming conventions are the database.** `[Van Clief]` Predictable filename patterns replace indices and vector stores. Declare them once in `CLAUDE.md` and they apply everywhere. Common patterns: `_draft.md`, `_final.md`, `_v2.md`, date prefixes (`YYYY-MM-DD-…`), platform prefixes. "Pull my demo v2" becomes unambiguous because the convention already says where to look.

**Workspace isolation is a freelancer superpower.** `[Van Clief]` When Claude is told to work in Workspace A, only A's `CONTEXT.md` loads. Work in Client A's folder never bleeds into Client B's session. Encode the rule explicitly in `CLAUDE.md`.

**The three-file minimum is the starter.** `[Van Clief]` A new project can begin with exactly three files in one folder: `CLAUDE.md` (identity, rules), `CONTEXT.md` (what we are building, what good looks like, what to avoid), `REFERENCES.md` (background, examples, links). Five minutes of work. Responses change on the first message. Graduate to the full multi-workspace system when a second kind of work shows up. (The specific `CLAUDE.md + CONTEXT.md + REFERENCES.md` trio as a named starter is at least partly this skill's framing, `[synthesis]`.)

## Workflow

Use this flow when the user asks for help setting up or restructuring a workspace. Treat each numbered step as a checkpoint: confirm with the user before moving on.

1. **Confirm the root, then understand the intent.** Before proposing any shape, do all four:

   a. *State the cwd explicitly.* "I am running in `<pwd>`. I will treat this as the project root for this session. Any sub-folders you name will be sub-workspaces of this root. Sound right?" Give the user a chance to correct, in case they started Claude in the wrong place or actually wanted a different folder as root.

   b. *Ask the intent questions.* The shape of the scaffold depends on what the user is trying to produce, not on folder names. Ask at least:
      - What will you produce in this workspace, concretely, in a week?
      - Who consumes that output?
      - What made a previous attempt at organizing this fail, if any?
      - What would make you abandon this scaffold in a month?

   c. *Ask the shape question directly.* "Is this a new project (root `CLAUDE.md` + `CONTEXT.md` + `REFERENCES.md` triad) or a sub-workspace inside an existing project (just a `CONTEXT.md`)?" The answer decides the output shape and whether a Layer 1 file is part of the scaffold at all.

   d. *Decide starter vs. multi-workspace.* Is this one kind of work or several? Single project or multi-client? If the user is new to this method, default to the three-file starter and plan the graduation path.

   (If the user already ran `superpowers:brainstorming` or a similar preflight, parts of (b) may already be answered. Inline questions remain the default here.)

2. **Propose the workspaces.** For a multi-workspace setup, suggest 2 to 5 subfolders. Each is a mode of work, not a filing category. Typical names: `writing-room/`, `production/`, `research/`, `community/`, `admin/`, or for developers `frontend/`, `backend/`, `infra/`. Name them in plain language the user will remember. Confirm the list before writing anything.

3. **Draft the routing table together.** This is the core deliverable. For every kind of task the user anticipates doing, fill one row: `Task | Go to | Read | Skills`. Start with 4 to 8 rows; the table grows as the user notices new tasks. If the user cannot picture a column value yet, put `(none)` or leave it blank rather than invent one. The table will be wrong in parts; that is expected. It becomes right by use.

4. **Write the root `CLAUDE.md`.** Use `templates/claude-md-template.md` as the starting shape. Sections: Identity (1 to 3 lines: who owns this, what rules always apply), Workspaces (the list, each with a one-line description), Routing table (from step 3), Naming conventions (optional, add when the user knows theirs), Rules (isolation rule for multi-client, any other invariants). Target: under 50 lines. Trim ruthlessly.

5. **Before writing any files: if you offered multiple shapes, force an explicit pick.** If the plan you drafted presented more than one shape for the user to compare (e.g. "Option A: three-file minimal" vs. "Option B: multi-workspace with sub-routing"), stop and ask the user to pick A or B explicitly before running any Write or Edit. Plan approval is not a shape selection. This applies even under auto mode. If the user picked a shape up front in step 1, skip this step.

6. **Create each workspace folder and its `CONTEXT.md`.** Use `templates/context-md-template.md`. Three sections: What happens here (the mode of work), What files matter (the artifacts in this room), What to avoid (sibling-workspace leaks, anti-patterns, or file-naming traps). One `CONTEXT.md` per workspace. Keep each short: if Claude needs to read 200 lines before starting work, the context itself has become the bloat.

   When you create a sub-workspace's `CONTEXT.md` inside an existing project root, surface one sentence to the user as part of the action: *"This sub-workspace gets a `CONTEXT.md` rather than its own `CLAUDE.md`. The root `CLAUDE.md` at `<root-path>` handles Layer 1; adding a second one here would break the single-router rule."* Users often expect a new `CLAUDE.md` per workspace; teaching this at scaffold time prevents the surprise.

7. **Optionally add `REFERENCES.md` at root.** For background material the user wants available but does not want re-loaded every prompt. Examples, links, brand voice notes, prior work. Do not pre-fill it with placeholders; leave it empty or omit the file until the user has something to put there.

8. **Walk the user through using the table.** Show them how to phrase a request so Claude looks up the task, enters the right workspace, and loads only the files the row names. Example: "Draft a Monday newsletter" means Claude consults the table, enters `writing-room/`, reads the files named in the Read column, and activates the skills named in the Skills column. If the request does not match a row, the user either adds a new row or does the work outside the table.

9. **Verify the scaffold respects the load-bearing rules.** Before ending the session, walk this checklist by hand and surface any finding to the user in plain language rather than ship it silently:

   - *One fact, one location.* For each convention, style rule, or workspace fact the scaffold wrote, grep across the other scaffold files. If the same fact appears in more than one file, name the duplication and ask which file should own it.
   - *Line ceiling.* Run `wc -l` on the root `CLAUDE.md`. If it is over 50 lines, flag for trim.
   - *Workspace isolation.* If the scaffold is multi-workspace, confirm the isolation rule is present verbatim in `CLAUDE.md`.
   - *Root discipline.* If you created any nested `CLAUDE.md` inside a sub-workspace, flag it — that is a nested-root pattern, not the default shape, and the user should confirm they want it.

   Some duplication is intentional (e.g. a sub-workspace slated to become its own root later). The point is not to be rigid; it is to surface deviation so the user decides, rather than discover it later by reading the scaffold.

## Rules (load-bearing)

Apply these without exception when scaffolding. They are the discipline that makes the architecture work.

- **CLAUDE.md stays under 50 lines.** `[synthesis — the 50 threshold]` / `[Van Clief — keep it lean]` Every line re-loads every prompt. Move anything that is not structural into a workspace `CONTEXT.md` or `REFERENCES.md`.
- **One fact, one location.** `[Van Clief]` Do not duplicate context across workspaces. If two workspaces need the same fact, it lives in `REFERENCES.md` at root and each workspace points to it.
- **Skills load per-task via the routing table.** `[synthesis]` Never globally. If a skill belongs to every task, it belongs in Layer 1; if it belongs to one task, it goes in that row only.
- **Workspace isolation is an explicit rule.** `[Van Clief]` For multi-client or multi-project setups, write the rule into `CLAUDE.md` verbatim: "Never reference one workspace's information inside another workspace's session." Do not assume Claude will infer it.
- **Never rename a workspace folder once it exists.** `[Van Clief]` Renaming silently breaks every row in the routing table that points to it. If the name must change, leave a stub pointer in the old folder.
- **Do not over-build before use.** `[Van Clief]` Resist the urge to define seven workspaces and a 30-row routing table upfront. Start minimal, grow when a real task exposes a gap. Over-building before use is a common failure mode of this method.
- **Sources are the user's.** `[Van Clief]` If the user has raw materials (transcripts, PDFs, recordings), keep them in one folder the LLM does not edit (`raw/` or similar). LLM output goes in sibling folders so the source of truth is always clear.

## Graduation path from the three-file starter

If you began with the three-file minimum and the user now wants to add structure, do this in order:

1. Add the first workspace subfolder and move the relevant working files into it. Give it a `CONTEXT.md`.
2. Add the routing table to `CLAUDE.md` (even with two rows, it pays off immediately).
3. Add naming conventions to `CLAUDE.md` once the user notices themselves naming files inconsistently.
4. Add the second workspace only when a second kind of work shows up. Not before.

This order keeps the system useful at every step and matches how the method was taught: evolve under pressure, do not design upfront.

## Templates

Fill these in during the workflow:

- `templates/claude-md-template.md`: the root `CLAUDE.md` scaffold. Sections: Identity, Workspaces, Routing table, Naming conventions, Rules. Contains `{{placeholders}}` you replace.
- `templates/context-md-template.md`: the per-workspace `CONTEXT.md` scaffold. Sections: What happens here, What files matter, What to avoid.

## See also

The method taught by this skill originates with Jake Van Clief. To go deeper: https://www.skool.com/quantum-quill-lyceum-1116
