# Vybe Plugins

Skills, rules, agents, hooks, and MCP wiring for **Vybe Desktop**. Each plugin is a standalone directory at the repository root with its own `.vybe-plugin/plugin.json` manifest.

## Plugins

| `name` | Plugin | Author | Category | `description` (from marketplace) |
|:-------|:-------|:-------|:---------|:-------------------------------------|
| `teaching` | [Teaching](teaching/) | Vybe | — | Skill mapping, practice plans, and learning retrospectives. |
| `continual-learning` | [Continual Learning](continual-learning/) | Vybe | Developer Tools | Incremental transcript-driven memory updates for AGENTS.md using high-signal bullet points only. |
| `vybe-team-kit` | [Vybe Team Kit](vybe-team-kit/) | Vybe | Developer Tools | Team workflows for CI, code review, and shipping. |
| `create-plugin` | [Create Plugin](create-plugin/) | Vybe | Developer Tools | Scaffold and validate new Vybe plugins. |
| `ralph-loop` | [Ralph Loop](ralph-loop/) | Vybe | — | Iterative self-referential AI loops (Ralph Wiggum technique). |
| `agent-compatibility` | [Agent Compatibility](agent-compatibility/) | Vybe | Developer Tools | CLI-backed repo compatibility scans plus agents that audit startup, validation, and docs against reality. |
| `cli-for-agent` | [CLI for Agents](cli-for-agent/) | Vybe | Developer Tools | Patterns for designing CLIs that coding agents can run reliably: flags, help with examples, pipelines, errors, idempotency, dry-run. |

Author values match each plugin’s `plugin.json` `author.name` (Vybe).

## MCP catalog (separate repo today)

Icons and `server.json` for MCP servers live in **[VYBE-MCP-Servers](https://github.com/vybe/vybe-mcp-servers)** (`servers/<name>/`). **Planned:** merge that tree into this repository as `mcp-servers/` so one clone carries **plugins + MCP metadata**, with Vybe Desktop resolving icons from that subtree or a published URL.

## Repository structure

Multi-plugin marketplace: root `.vybe-plugin/marketplace.json` lists all plugins; each plugin has its own manifest:

```
├── .vybe-plugin/
│   └── marketplace.json       # Marketplace index
├── <plugin-name>/
│   ├── .vybe-plugin/
│   │   └── plugin.json        # Per-plugin manifest
│   ├── skills/
│   ├── rules/
│   ├── mcp.json               # optional
│   └── ...
└── schemas/                   # JSON Schema for manifests
```

## License

MIT
