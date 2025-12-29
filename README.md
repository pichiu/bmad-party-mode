# BMAD Plugins

A collection of Claude Code plugins by Pi Chiu.

## Installation

```bash
# Add the marketplace
/plugin marketplace add pichiu/bmad-plugins

# Install a specific plugin
/plugin install party-mode@bmad-plugins
```

## Available Plugins

### Party Mode

Multi-agent conversation orchestration - enables dynamic group discussions with 10 AI agents, each with unique personality and expertise.

**Features:**
- **10 Specialized Agents**: Business analysts, architects, developers, testers, and more
- **Intelligent Agent Selection**: Automatically selects 2-3 relevant agents per topic
- **Character Consistency**: Each agent maintains their unique voice and principles
- **Cross-Agent Dialogue**: Agents can reference and build on each other's responses

**Usage:**
```
/bmad-party-mode
```

Or with a topic:
```
/bmad-party-mode How should we design our authentication system?
```

[View full documentation](./plugins/party-mode/README.md)

## Repository Structure

```
bmad-plugins/
├── .claude-plugin/
│   └── marketplace.json      # Plugin registry
├── plugins/
│   └── party-mode/           # Party Mode plugin
│       ├── .claude-plugin/
│       │   └── plugin.json
│       ├── commands/
│       ├── skills/
│       └── data/
└── README.md
```

## License

MIT
