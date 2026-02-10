---
description: Create complete copy-paste-ready content for Uplimit storyboards from structure tables
---

You are creating **complete, copy-paste-ready content** for Uplimit storyboards.

Use the **uplimit-builder-agent** to transform element structure tables into full implementation guides with all content written and ready to paste into Uplimit.

## What This Command Creates

The uplimit-builder-agent produces:

### Complete Content for Every Element
- Full text content (markdown, ready to paste)
- Complete infobox content (50-100 words)
- Widget introductions (4-component format)
- AI roleplay configurations (all 4 tabs)
- Rubric criteria with level descriptions
- iFrame embed codes with accessibility attributes
- Assessment instructions

### Implementation Guide
- Step-by-step Uplimit implementation instructions
- Element-by-element build checklist
- AI Chat Widget placement notes

## Input Required

This command works best with a structure table from `/uplimit-structure`:

```markdown
| Order | Element | Purpose | Time |
|-------|---------|---------|------|
| 1 | **▬ Text** | Connecting intro | 2 min |
| 2 | **⚙ Widget** | Learning Outcomes | 1 min |
...
```

If no structure provided, the agent will ask clarifying questions.

## When to Use This Command

### Pipeline Step 2
- After using `/uplimit-structure` to create element sequence
- Before using `/uplimit-audit` to verify compliance

### Content Creation
- Transforming SME content into Uplimit-ready format
- Writing all module content in one pass
- Creating consistent formatting across elements

### Revision
- Rewriting specific elements to meet platform requirements
- Updating content while maintaining structure

## Example Usage

```
/uplimit-build [paste structure table]
/uplimit-build create content for Module 3 using this structure
/uplimit-build write full content for Week 2 assessment
```

## Expected Output

```markdown
# MODULE 3: [Title] — Complete Build Guide

**Course Format:** Cohort
**Platform Reference:** uplimit-platform-capabilities.md

---

## Element 1: Connecting Introduction

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

You've explored how sport generates revenue through media rights,
ticketing, and merchandise. Now we turn to the engine that powers
it all: **sponsorship**.

In this module, you'll calculate actual sponsorship value using
industry metrics and design activation strategies that convert
brand investment into measurable results.

---

## Element 2: Learning Outcomes Widget

**Uplimit Implementation:**
1. Select **iFrame** element
2. Paste embed code:

<iframe src="widgets/learning-outcomes-module-3.html"
        width="100%"
        height="400"
        title="Module 3 Learning Outcomes"
        frameborder="0">
</iframe>

---

[Continue for all elements...]

---

## Implementation Checklist

- [ ] All elements created in Uplimit
- [ ] AI Chat Widget configured once, referenced throughout
- [ ] Widget links tested
- [ ] Preview module in Uplimit

---

## → NEXT STEP: Auditor Agent

Use `/uplimit-audit` to verify platform compliance before publishing.
```

## Style Rules Applied

The Builder Agent follows strict learner-facing style rules:

- **No em dashes** — use commas, periods, or colons
- **Bold for labels only** — never bold entire sentences
- **15-20 word sentences** — vary for rhythm, avoid 35+ words
- **Second person ("you")** — for learner-facing content
- **Third person ("the learner")** — for rubrics and AI roleplay Tab 2/4

---

**Pipeline Position:**
- Step 1: `/uplimit-structure` (create structure)
- **Step 2**: Builder Agent (this command)
- Step 3: `/uplimit-audit` (verify compliance)
- Step 4: `/uplimit-accessibility` (final review)

Or use `/build-storyboard` to run the full pipeline automatically.
