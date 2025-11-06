# Education Toolkit

Comprehensive Claude Code plugin for educational developers, instructional designers, and course creators.

## Features

- **18 Specialized Agents**: Strategic course planning, accessibility auditing, assessment design, code review, and more
- **14 Slash Commands**: Quick-access workflows for common tasks
- **Automatic Code Review**: PostToolUse hooks for fullstack quality enforcement
- **Knowledge Base**: 614 KB of bundled course design principles and AI assessment research

## Installation

```bash
/plugin add jameskruck/education-toolkit
```

## Key Capabilities

### Course Design
- **course-outline-creator**: Strategic CLO/MLO planning with QM compliance
- **uplimit-storyboard-builder**: Detailed module design with interactivity analysis
- **cohort-structure-checker**: Validates WLO-based cohort course patterns
- **self-paced-structure-checker**: Validates MLO-based self-paced structures

### Consistency & Quality
- **terminology-consistency-checker**: Build course glossaries, flag term variations
- **concept-threading-checker**: Ensure Week 1 concepts appear in later weeks
- **assessment-consistency-checker**: Validate PAIRR methodology, rubric alignment
- **branding-checker**: Platform branding compliance (Canvas/Uplimit)

### Widget & Design
- **widget-designer**: Generate/audit HTML widgets with standardized design system
- **widget-tester**: Test widgets with 3 student personas
- **accessibility-auditor**: WCAG 2.2 AA compliance checking

### Assessment & Pedagogy
- **assessment-designer**: PAIRR, AI Roleplay, diagnostic rubrics (464 KB research)
- **rubric-generator**: Create QM-compliant rubrics
- **udl-content-generator**: Universal Design for Learning implementation

### Code Review
- **backend-reviewer**: FastAPI/Python security & best practices
- **frontend-reviewer**: React/JSX with WCAG 2.2 AA focus

### Testing & Simulation
- **peer-review-simulator**: 6 ID specialists review (comprehensive QA)
- **student-journey-simulator**: 4 learner personas test experience

## Structure

```
EdTools/
├── .claude-plugin/
│   ├── marketplace.json    # Marketplace distribution config
│   └── plugin.json          # Plugin manifest
├── agents/                  # 18 agent definitions
├── commands/                # 14 slash commands
├── skills/                  # 3 executable Python skills
├── hooks/                   # Automatic quality enforcement
├── assessment-knowledge/    # 464 KB assessment research
└── course-design-knowledge/ # 150 KB Ivey process & patterns
```

## Version

**3.0.0** - Fresh marketplace structure with strict mode

## License

MIT License - See LICENSE file

## Author

James Kruck
Ivey Business School
jkruck@ivey.ca
