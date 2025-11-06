# Education Toolkit Marketplace

Claude Code plugin marketplace for educational developers, instructional designers, and course creators.

## Installation

Add this marketplace to Claude Code:

```bash
/plugin marketplace add jkruckivey/edtools
```

Then install the education-toolkit plugin:

```bash
/plugin install education-toolkit@education-toolkit
```

## Plugins

### education-toolkit v3.0.0

Comprehensive toolkit with:
- **18 specialized agents** for course design, accessibility, assessment, and code review
- **14 slash commands** for quick workflows
- **Automatic quality hooks** for code and content validation
- **614 KB knowledge base** of assessment research and course design patterns

## Structure

```
edtools/
├── .claude-plugin/
│   └── marketplace.json
└── plugins/
    └── education-toolkit/
        ├── plugin.json
        ├── agents/        (18 specialized agents)
        ├── commands/      (14 slash commands)
        ├── skills/        (3 executable Python skills)
        ├── hooks/         (5 automatic quality hooks)
        ├── assessment-knowledge/
        └── course-design-knowledge/
```

## License

MIT - See LICENSE in plugin directory
