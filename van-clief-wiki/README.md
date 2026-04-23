# van-clief-wiki

Source material and notes for Jake Van Clief's folder-architecture method. Used by the `pocket-clief` plugin in this repo to check fidelity when the skill is edited.

## Structure

- `sources/` — cited source material. Links, excerpts, transcript fragments. Not edited after intake.
- `notes/` — synthesized notes, each citing one item in `sources/`.

## Attribution

The folder-architecture method is Jake Van Clief's. Primary material: https://www.skool.com/quantum-quill-lyceum-1116

## Contributing source material

Open an issue or PR. Drop new source items into `sources/` with a link and a short excerpt. Write a summary in `notes/YYYY-MM-DD-<slug>.md` that cites the source via front-matter:

```
---
source: sources/<filename>
---
```
