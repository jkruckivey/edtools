# Education Toolkit

Claude Code plugin for educational developers, instructional designers, and course creators.

## Installation

Install directly from GitHub:

```bash
/plugin add github:jkruckivey/edtools
```

## Features

### 18 Specialized Agents
- **course-outline-creator** - Strategic CLO/MLO planning with QM compliance
- **uplimit-storyboard-builder** - Detailed module design with interactivity analysis
- **cohort-structure-checker** - Validates WLO-based cohort course patterns
- **self-paced-structure-checker** - Validates MLO-based self-paced structures
- **terminology-consistency-checker** - Build glossaries, flag term variations
- **concept-threading-checker** - Ensure Week 1 concepts appear later
- **assessment-consistency-checker** - Validate PAIRR methodology, rubric alignment
- **assessment-designer** - PAIRR, AI Roleplay, diagnostic rubrics (464 KB research)
- **rubric-generator** - Create QM-compliant rubrics
- **widget-designer** - Generate/audit HTML widgets with design system
- **widget-tester** - Test widgets with 3 student personas
- **accessibility-auditor** - WCAG 2.2 AA compliance checking
- **branding-checker** - Platform branding compliance (Canvas/Uplimit)
- **peer-review-simulator** - 6 ID specialists review (comprehensive QA)
- **student-journey-simulator** - 4 learner personas test experience
- **backend-reviewer** - FastAPI/Python security & best practices
- **frontend-reviewer** - React/JSX with WCAG 2.2 AA focus
- **udl-content-generator** - Universal Design for Learning implementation

### 14 Slash Commands
Quick workflows: `/build-storyboard`, `/check-branding`, `/design-assessment`, `/peer-review`, `/test-widget`, and more

### 3 Executable Skills
- **assessment-template-generator** - PAIRR, AI roleplay, diagnostic rubrics
- **accessibility-audit-tools** - WCAG 2.2 AA automated testing
- **qm-validator** - Quality Matters validation

### 5 Automatic Quality Hooks
- Smart content validator (PostToolUse on Edit/Write)
- Educational context loader (SessionStart)
- Protected content guardian (PreToolUse on Edit/Write)
- Storyboard auto-formatter (PostToolUse on Edit/Write)
- Widget auto-tester (PostToolUse on Write)

### 614 KB Knowledge Base
- **Assessment research** (464 KB) - UDL, QM, AI assessment frameworks
- **Course design patterns** (150 KB) - Ivey 6-phase process, threading guides

## Structure

```
edtools/
├── .claude-plugin/
│   └── plugin.json
├── agents/           (18 specialized agents)
├── commands/         (14 slash commands)
├── skills/           (3 executable Python skills)
├── hooks/            (5 automatic quality hooks)
├── assessment-knowledge/
└── course-design-knowledge/
```

## Version

**3.0.0** - Direct plugin installation

## License

MIT - See LICENSE file

## Author

James Kruck
Ivey Business School
jkruck@ivey.ca
