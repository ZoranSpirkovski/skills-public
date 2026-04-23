# skill-maintenance

## What happens here

This is where skills are edited: SKILL.md changes, new plugin scaffolding, version bumps in `plugin.json`, and implementation of GitHub issues filed against any skill in this repo. The plugin source lives under `../plugins/<name>/`; this workspace is the discipline around editing it, not a mirror.

GitHub is authoritative for issue state. Read each issue with `gh issue view <n>` and do the work here. Close the issue after the fix is on `main` with `gh issue close <n> --comment "Addressed in <short-sha>."`.

`pocket-clief` is the only skill that carries a fidelity rule: changes to it are checked against the Van Clief source material in `../van-clief-wiki/` before shipping.

This workspace gets a `CONTEXT.md` rather than its own `CLAUDE.md`. The root `CLAUDE.md` handles Layer 1 — adding a second one here would break the single-router rule.

## What files matter

- `../plugins/<plugin>/skills/<skill>/SKILL.md` — the skill itself.
- `../plugins/<plugin>/.claude-plugin/plugin.json` — version and metadata.
- `../plugins/<plugin>/skills/<skill>/templates/` — templates the skill writes from.
- `../.claude-plugin/marketplace.json` — adds or removes plugins from the marketplace.
- `gh issue view <n>` output — the issue body is the spec when implementing one.

## What to avoid

- Do not change a plugin without bumping its version in the same push. The bump discipline is in root `CLAUDE.md` Rules.
- For `pocket-clief` specifically, follow the fidelity rule in root `CLAUDE.md` — the wiki check is non-optional.
- Do not mirror issue bodies into local files. GitHub is the store of record; read via `gh issue view` each time you need the text.
- Do not close an issue until its fix is on `main`. The close comment cites a sha that must exist.
