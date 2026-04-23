# Wiki Schema

> Placed at `.wiki/wiki/SCHEMA.md` by the `llm-wiki` skill during bootstrap.
> This is the rulebook for any LLM agent working on this wiki. Read it in full before making any changes.

## Domain

**Topic:** Van Clief's teachings on AI-native folder workflows - the three-layer routing architecture (root `CLAUDE.md` → workspace `CONTEXT.md` → files), routing tables, naming conventions as lightweight DB, folder-as-workspace / folder-as-UI ergonomics, and the broader software-engineering history ("rules of transparency / composition") he cites as foundational. The wiki's job is to compile a navigable body of Van Clief's ideas and supporting references so future sessions can query it without re-reading long transcripts.

**Source types expected:** Video transcripts (YouTube talks), long-form research / foundational documents written by Van Clief, course / class note exports, and occasionally third-party references he cites (papers, essays from earlier software history). User's own working examples (e.g. `productivity/mk-domains/CLAUDE.md`) may be referenced by path from synthesis pages but are not copied into `.wiki/raw/`.

This document and the wiki itself co-evolve. As conventions become clearer, update this file.

## Layers

Everything lives under `.wiki/` at the project root (`productivity/Van Clief/`).

- `.wiki/raw/` - immutable source documents. Read-only for the LLM. The user owns this directory; if a source is wrong, the user edits it.
- `.wiki/digested/` - LLM-generated preprocessed markdown. Mirrors the folder hierarchy of `.wiki/raw/`, with a slug-named subdirectory at each leaf. LLM-owned.
- `.wiki/wiki/` - all LLM-generated wiki pages. LLM-owned. The user reads; the LLM writes.
- `.wiki/wiki/SCHEMA.md` - this file. The rulebook.

## Page types

Four canonical types. Each page has frontmatter declaring its `type`.

### Source pages (`.wiki/wiki/sources/<slug>.md`)

One per ingested source. Contains:
- Frontmatter (see below)
- `## Summary` - two to five sentences
- `## Key claims` - numbered list, each claim stands alone
- `## Entities mentioned` - list, each linked with `[[entity-slug]]`
- `## Open questions` - things the source raised but didn't answer

### Entity pages (`.wiki/wiki/entities/<slug>.md`)

One per person, library, project, system, organization. In this wiki: Van Clief himself, referenced tools (Claude Code, VS Code, Obsidian), named methodologies he credits (e.g. Unix philosophy authors he cites in the foundation paper), and specific apps/frameworks he names. Contains:
- Frontmatter
- A one-paragraph description
- `## Claims` - bullet list, each claim cites its source: `- Three-layer routing is the core pattern [sources/folder-system-transcript]`
- `## Relationships` - bullet list of links to other entities
- `## Contradictions` - only if contradictions exist. Never overwrite a claim on contradiction; flag both.

### Concept pages (`.wiki/wiki/concepts/<slug>.md`)

One per idea, pattern, term, or abstraction. Expected for this wiki: `three-layer-routing`, `routing-table`, `folder-as-workspace`, `naming-conventions-as-db`, `context-window-hygiene`, `workspace-isolation`, `folder-as-ui`, `skill-wired-per-task`, and terms Van Clief pulls from software history (`rule-of-transparency`, `rule-of-composition`, etc.). Same structure as entity pages.

### Synthesis pages (`.wiki/wiki/synthesis/<slug>.md`)

One per comparison, analysis, or filed-back query answer. Natural synthesis pages for this wiki: `van-clief-vs-pas`, `three-layer-vs-five-layer`, `when-to-skip-pas-for-van-clief`, applied walkthroughs keyed to real workspaces (e.g. `mk-domains-as-three-layer-example`). Contains:
- Frontmatter
- A narrative section that synthesizes multiple sources
- Every claim cites the source page it comes from

## Page frontmatter

Every wiki page starts with this YAML block:

```yaml
---
type: source | entity | concept | synthesis
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: <integer>
tags: [tag1, tag2]
---
```

`sources` semantics: source pages use `1` (self). Entity, concept, and synthesis pages use the count of distinct source pages whose claims they currently cite.

Keep it short. Do not add fields beyond this spec unless you're also extending this schema document.

## Slug rules

- Lowercase, hyphens, no spaces or underscores.
- Source slugs derive from the source title or filename: trim punctuation, drop leading articles. `folder-system-transcript.md` → `folder-system-transcript`. `the-foundation.md` → `foundation`.
- Entity and concept slugs use the canonical name: `van-clief`, `claude-code`, `three-layer-routing`, `routing-table`.
- Never rename a slug once it exists. If a name changes, create a new page and add a redirect stub in the old one.

## Digest workflow

Digest preprocesses a raw source into clean, structured markdown before ingest. For this wiki's expected sources (markdown transcripts, markdown long-form documents), digest is usually **skippable** - the raw files are already clean markdown. Run digest explicitly only if a non-markdown source arrives (PDF course handouts, scanned notes).

Steps (when needed):

1. Identify the source in `.wiki/raw/` and derive a slug.
2. Create the digest directory mirroring the source's folder path.
3. Extract text using the right tool for the format.
4. Extract and describe images if the source has them.
5. Write `digest.md` - combined text + image descriptions with extraction metadata.
6. Log with op `digest`. Note format, tools used, and any extraction gaps.

## Ingest workflow

For every new source:

1. **Read the source.** Markdown sources in `.wiki/raw/` can be read directly. PDFs / docx / images route through digest first.
2. **Discuss key takeaways with the user** - three to five bullets, short message. This is your checkpoint.
3. **Read existing related pages FIRST** - use `.wiki/wiki/index.md` to find candidates. This is how contradictions get caught at ingest time.
4. **Write the source summary page** at `.wiki/wiki/sources/<slug>.md`.
5. **Update or create entity and concept pages.** Every entity/concept mentioned gets a page. Every new claim cites the source.
6. **Flag contradictions** by adding a `## Contradictions` section to affected pages - never silently overwrite.
7. **Update `.wiki/wiki/index.md`** - add the new source and any new entity/concept pages.
8. **Append to `.wiki/wiki/log.md`** with the canonical prefix: `## [YYYY-MM-DD] ingest | <source title>`
9. **Report pages touched** to the user.

A single source typically touches 5–15 pages. Do not artificially limit yourself.

**Long-source note:** `the-foundation.md` is ~2400 lines. Ingest it in passes: first pass creates the source page + top-level entity/concept pages from its headings. Subsequent lint/ingest passes can deepen individual concept pages as they're cited by other sources.

## Query workflow

1. Read `.wiki/wiki/index.md` to find candidate pages.
2. Read candidate pages in full, following cross-references.
3. Synthesize an answer with one citation per claim.
4. Offer to file the answer back as a synthesis page. If the user agrees, write it, update the index, log it with op `query`.

## Lint workflow

Run whenever the wiki feels stale. Check for:

- **Contradictions** - pages with unresolved `## Contradictions` sections.
- **Orphan pages** - no inbound links.
- **Stale claims** - claims from one old source not confirmed or actively weakened by newer ones.
- **Missing cross-refs** - a page mentions an entity by name but doesn't link to its page.
- **Concepts without pages** - a term appears in three or more pages with no page of its own. Promote it.
- **Van Clief's five-layer paper** - if any concept page cites claims only from the transcript, check whether `the-foundation.md` has deeper material worth pulling in.

Report findings as a list with proposed fixes. Do not fix silently - let the user approve. Log with op `lint`.

## Index structure

`.wiki/wiki/index.md` uses these fixed top-level headers:

```
## Sources
## Entities
## Concepts
## Synthesis
```

Under each, one line per page: `- [[slug]] - one-line description`. Sorted alphabetically within each category.

## Log format

`.wiki/wiki/log.md` is append-only. Every operation gets one entry. Canonical prefix:

```
## [YYYY-MM-DD] <op> | <title>
```

Where `<op>` is one of: `bootstrap`, `digest`, `ingest`, `query`, `lint`, `schema`. This format is load-bearing: it makes `grep "^## \[" log.md | tail -5` a usable timeline tool.

## What NOT to do

- Do not edit files in `.wiki/raw/`.
- Do not write new claims without reading existing related pages first.
- Do not silently overwrite a claim when new information contradicts it - flag both.
- Do not skip the log entry.
- Do not put wiki conventions in the project `CLAUDE.md` - it only holds a pointer line plus this project's Van Clief routing layer.
- Do not rename slugs.
- Do not create a page type beyond the four canonical types without also updating this schema.

## Format handling

| Format | Text extraction | Image extraction | Visual pass |
|--------|----------------|------------------|-------------|
| `.md`, `.txt` | Read tool (copy as-is) | N/A | N/A |
| `.html` | Read tool | N/A | N/A |
| `.pdf` | `pdftotext` (poppler) | `pdfimages` (poppler) | Describe extracted images |
| `.jpg`, `.png` | N/A | File is the image | Read tool visual description |

**Domain-specific notes:** Video transcripts in this wiki are expected as plain markdown (already transcribed). Course-note exports are expected as markdown too. If a source arrives as a raw auto-caption VTT or SRT, convert to markdown before dropping in `.wiki/raw/`.

## Co-evolve me

This schema is not immutable. Examples of changes worth making as the wiki grows:

- New page types (e.g. `course` or `lesson` if Van Clief's courses have internal structure worth preserving).
- New frontmatter tags (e.g. `course:`, `lesson-number:`).
- Custom lint checks specific to this domain.
- Format handling notes if new source types appear.

Log schema edits in `.wiki/wiki/log.md` with op `schema`.
