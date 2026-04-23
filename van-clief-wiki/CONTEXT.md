# van-clief-wiki

## What happens here

A navigable body of Jake Van Clief's teachings compiled from his courses (Foundation, Archive / Old But Gold, Playbooks, Stack) and the folder-system transcript. Loaded when a `pocket-clief` change needs a fidelity check, when a wiki page needs an edit, or when new source material is being ingested.

Only `pocket-clief` is bound by this wiki's fidelity rule. Other skills in the repo may reference it, but are not constrained by it.

This workspace gets a `CONTEXT.md` rather than its own `CLAUDE.md`. The root `CLAUDE.md` handles Layer 1 — adding a second one here would break the single-router rule.

## What files matter

- `SCHEMA.md` — page-type rulebook (source, concept, entity, synthesis). Read in full before editing or adding pages.
- `index.md` — full page inventory grouped by category.
- `log.md` — append-only ingest log. One line per pass; update on ingest, lint, or synthesis work.
- `sources/` — one page per ingested lesson or document, with summary, key claims, entities mentioned, and open questions. ~48 pages.
- `concepts/` — one page per recurring idea across sources. ~47 pages.
- `entities/` — one page per person, product, or organization cited. ~75 pages.
- `synthesis/` — cross-source pages identifying patterns across multiple sources.

Raw transcripts (`.wiki/raw/*` in the original compilation) are **not** in this repo. Source-page references to those paths resolve only in the user's private working copy.

## What to avoid

- Do not edit a page without reading `SCHEMA.md` first. The rulebook is load-bearing for this wiki.
- Do not paraphrase Van Clief from memory into a concept or synthesis page. Every claim traces to a source-page citation.
- Do not load wiki content into sessions that are editing non-`pocket-clief` skills. The fidelity rule is scoped to `pocket-clief` only.
- Do not log ingest or lint passes in both `log.md` and elsewhere — `log.md` is the single location.
