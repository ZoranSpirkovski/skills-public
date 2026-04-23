# skills-public

A public Claude Code plugin marketplace.

## Add this marketplace

From inside Claude Code:

```
/plugin marketplace add ZoranSpirkovski/skills-public
```

## Available plugins

| Plugin | What it does |
|--------|--------------|
| [`pocket-clief`](plugins/pocket-clief) | Set up a Claude Code workspace using Jake Van Clief's folder-architecture method: root `CLAUDE.md` with a routing table, workspace subfolders with `CONTEXT.md` files, and naming conventions as a lightweight database. |

Install a plugin:

```
/plugin install pocket-clief@skills-public
```

## Contributing

Each plugin lives under `plugins/<name>/` with its own `.claude-plugin/plugin.json` and a `skills/` folder. The marketplace manifest is `.claude-plugin/marketplace.json` at the repo root. Open a pull request to add a new plugin or improve an existing one.

## License

MIT. See [LICENSE](LICENSE).
