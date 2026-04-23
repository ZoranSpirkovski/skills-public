# skills-public

## Identity

Public Claude Code plugin marketplace owned by Zoran Spirkovski. Houses skills — currently `pocket-clief` — and the discipline for maintaining them. Shared on the Van Clief Skool community, so craft and source-fidelity matter. This scaffold is early: the rules and routing table below are what we have learned so far and are expected to evolve with use.

## Workspaces

- `skill-maintenance/`: edit existing skills, scaffold new ones, version bumps, and implementation of GitHub issues.
- `van-clief-wiki/`: Van Clief source material used to check `pocket-clief` fidelity. LLM does not edit this folder after intake.
- `plugins/`: the actual plugin sources. Not a workspace — editing routes through `skill-maintenance/`.

GitHub hosts the issues at https://github.com/ZoranSpirkovski/skills-public/issues. Manage them with `gh issue` and the normal GitHub flow — there is no local issue mirror.

## Routing table

| Task | Go to | Read | Skills |
|------|-------|------|--------|
| Edit an existing skill | `skill-maintenance/` | `skill-maintenance/CONTEXT.md`, target `plugins/<name>/skills/<name>/SKILL.md` | (none) |
| Add a new plugin or skill | `skill-maintenance/` | `skill-maintenance/CONTEXT.md`, `plugins/pocket-clief/` as reference shape | `superpowers:writing-skills` |
| Bump a plugin version | `skill-maintenance/` | `skill-maintenance/CONTEXT.md`, `plugins/<name>/.claude-plugin/plugin.json` | (none) |
| Change `pocket-clief` (any edit) | `skill-maintenance/` | `skill-maintenance/CONTEXT.md`, `van-clief-wiki/CONTEXT.md`, relevant files under `van-clief-wiki/notes/` | `pocket-clief:pocket-clief` |
| Implement a GitHub issue | `skill-maintenance/` | `skill-maintenance/CONTEXT.md`, issue body via `gh issue view <n>` | (none) |
| Add Van Clief source material | `van-clief-wiki/` | `van-clief-wiki/CONTEXT.md` | (none) |

## Naming conventions

- Skill files: `plugins/<plugin>/skills/<skill>/SKILL.md`.
- Plugin version: semver in `plugins/<plugin>/.claude-plugin/plugin.json`. Behavior change means at minimum a minor bump.
- Issue close comment: `Addressed in <short-sha>.` The sha must exist on `main` before closing.
- Van Clief source notes: `van-clief-wiki/notes/YYYY-MM-DD-<slug>.md`, each with a `source:` front-matter line naming the file in `van-clief-wiki/sources/` it cites.

## Rules (working discipline, revise as we learn)

- Never reference one workspace's information inside another workspace's session.
- Do not rename a workspace folder once it exists. Leave a stub pointer if you must.
- Edits to `plugins/pocket-clief/` must be checked against `van-clief-wiki/` before shipping. This fidelity rule is scoped to `pocket-clief` only, not every skill.
- Behavior-changing edits to a plugin require a version bump in the same push. One missed bump earlier had to be corrected after the fact; do not repeat.
- `van-clief-wiki/sources/` is not LLM-edited after intake. Synthesis goes in `van-clief-wiki/notes/` and must cite a file in `sources/`.
- Keep this file under 50 lines. Every line re-loads on every prompt.
