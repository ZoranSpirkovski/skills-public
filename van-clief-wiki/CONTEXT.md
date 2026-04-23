# van-clief-wiki

## What happens here

Read-only source of truth for Jake Van Clief's folder-architecture method as it applies to the `pocket-clief` skill. Contains cited source material in `sources/` and synthesized notes in `notes/`. Loaded when a `pocket-clief` change needs a fidelity check, or when new source material is being added.

Only `pocket-clief` leans on this wiki. Other skills in the repo are not bound by Van Clief's philosophy and do not check here.

This workspace gets a `CONTEXT.md` rather than its own `CLAUDE.md`. The root `CLAUDE.md` handles Layer 1 — adding a second one here would break the single-router rule.

## What files matter

- `sources/`: raw cited material — links with short excerpts, transcript fragments, screenshots. The user's material. LLM does not edit after intake.
- `notes/`: synthesized notes that attribute claims back to `sources/`. Filename `YYYY-MM-DD-<slug>.md`, each with a `source:` front-matter line pointing at a file in `sources/`.
- `README.md`: public-facing description for GitHub visitors.

## What to avoid

- Do not paraphrase Van Clief's teaching from memory into `notes/`. Every note must cite a specific file in `sources/`.
- Do not edit files in `sources/` after they are committed. If material is wrong, add a correction note in `notes/` rather than rewriting the source.
- Do not load wiki content into sessions that are editing non-`pocket-clief` skills. This wiki's defense is scoped to `pocket-clief` only.
