---
description: Create module structure (element order, types, timing) for Uplimit storyboards - no content, just structure
---

You are creating module **structure only** for Uplimit storyboards.

Use the **uplimit-structure-agent** to design element order, types, and timing. This agent produces structure tables but **never writes copy-paste content** - that's the Builder Agent's job.

## What This Command Creates

The uplimit-structure-agent produces:

### Element Tables
- Order/sequence of elements
- Element type selection (Text, Widget, Infobox, Video, AI Roleplay, etc.)
- Purpose description for each element
- Time estimates per element

### Pedagogical Rationale
- Why elements appear in this order
- How structure supports learning outcomes
- V3 Interactive-First compliance verification

### Hand-off to Builder
- Clear instructions for next step
- Notes on special requirements

## What This Command Does NOT Create

- Full text content ready to paste
- Complete infobox content
- Written rubric criteria
- AI roleplay scenarios with hidden context
- iFrame embed codes

## Element Type Symbols

| Symbol | Type | When to Use |
|--------|------|-------------|
| **▬** | Text | Connecting intros, bridges, transitions |
| **⚙** | iFrame Widget | Interactive tools, learning outcomes |
| **ⓘ** | Infobox | Key insights, callouts (50-100 words) |
| **▶** | Video | Instructional content, interviews |
| **▤** | Details Accordion | Optional depth, hints, transcripts |
| **◈** | AI Chat/Roleplay | Q&A assistants, roleplay assessments |
| **☰** | List | Numbered or bulleted items |
| **▦** | Tiles | Card grids for options, categories |
| **▭** | Table | Comparative data, frameworks |

## When to Use This Command

### New Module Design
- Starting a new module from learning outcomes
- Designing element sequence before writing content
- Planning time allocation

### Structure Review
- Checking if current structure follows V3 Interactive-First
- Verifying widget density (every 2-3 elements)
- Ensuring text blocks stay under 150 words

### Pipeline Step 1
- First step in the full storyboard pipeline
- Before using `/uplimit-build` to create content

## Example Usage

```
/uplimit-structure Module 3: The Sponsorship Playbook
/uplimit-structure create structure for Week 2 assessment module
/uplimit-structure plan element sequence for intro module
```

## Expected Output

```markdown
# MODULE 3: The Sponsorship Playbook

**Purpose:** Apply sponsorship ROI frameworks through interactive practice

**Uplimit Structure:** Third module in Unit 3 (Week 3)

| Order | Element | Purpose | Time |
|-------|---------|---------|------|
| 1 | **▬ Text** ⬤ | Connecting intro from Module 2 | 2 min |
| 2 | **⚙ Widget** ⬤ | Learning Outcomes (WLO 3.1-3.3 subset) | 1 min |
| 3 | **ⓘ Infobox** ⬤ | Key insight: sponsorship as financial backbone | — |
| 4 | **▶ Video** ⬤ | "Why Brands Pay" (2 min instructional) | 2 min |
| 5 | **⚙ Widget** ⬤ | Sponsorship Valuation Calculator | 8 min |
...

**Total Time:** 31 minutes

**V3 Compliance:** ✅ 3 widgets, text blocks target <150 words each
**Pedagogical Flow:** Video → Calculate → Design (concrete to applied)

---

**→ NEXT STEP:** Use `/uplimit-build` to create copy-paste content.
```

---

**Pipeline Position:**
- **Step 1**: Structure Agent (this command)
- Step 2: `/uplimit-build` (create content)
- Step 3: `/uplimit-audit` (verify platform compliance)
- Step 4: `/uplimit-accessibility` (final accessibility review)

Or use `/build-storyboard` to run the full pipeline automatically.
