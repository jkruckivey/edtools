# Uplift Platform Capabilities

**Authority Level:** CANONICAL — All storyboard agents reference this document.

This is the single source of truth for Uplimit platform constraints, element types, and formatting rules. Structure, Builder, and Auditor agents must comply with these specifications.

---

## Course Format Terminology

**CRITICAL:** Determine course format FIRST. Never mix terminology.

| Aspect | COHORT | SELF-PACED |
|--------|--------|------------|
| Time units | Week 1, Week 2, Week 3 | Module 1, Module 2, Module 3 |
| Learning outcomes | WLO X.X (Week Learning Outcomes) | MLO X.X (Module Learning Outcomes) |
| Project name | Anchor Project | Final Project |
| Progress markers | Milestone with firm deadlines | Checkpoint with flexible pacing |
| Pacing language | "Submit by Friday 11:59 PM ET" | "When you're ready" |
| Module 6 assessment | PAIRR with peer review | Individual assessment (NO peer review) |

**Detection:**
- WLO terminology in content → COHORT
- MLO terminology in content → SELF-PACED
- If unclear, ASK before proceeding

---

## Supported Element Types

### Text (▬)
- **Purpose:** Connecting intros, bridges, transitions, explanations
- **Constraints:** Target 100-150 words maximum (V3 Interactive-First)
- **Format:** Markdown with proper heading hierarchy (H2 → H3 → H4)
- **When to use:** Module openers, concept introductions, transitions between activities

### Infobox (ⓘ)
- **Purpose:** Key insights, callouts, warnings
- **Constraints:**
  - **50-100 words MAXIMUM**
  - **Simple paragraph text ONLY**
  - **NO headings** (no bold section headers)
  - **NO bullet lists**
  - **NO numbered lists**
  - **NO multi-paragraph structures**
- **Variants:** Callout, Note, Insight, Warning, Assessment (purple), Next Steps (green)
- **When to use:** Single key insight that deserves visual prominence
- **When NOT to use:**
  - Complex content with structure → Use Text
  - Multiple points → Use Vertical List or Tiles
  - Long explanations → Use Details Accordion

### Video (▶)
- **Purpose:** Instructional content, executive interviews
- **Requirements:**
  - MP4 file upload
  - VTT caption file (accessibility requirement)
  - Transcript in Details accordion (recommended)
- **Duration guidance:** 2-12 minutes typical

### iFrame Widget (⚙)
- **Purpose:** Interactive tools, learning outcomes displays, calculators, simulations
- **Required attributes:**
  ```html
  <iframe src="[URL]"
          width="800"
          height="600"
          title="[Descriptive title for accessibility]"
          frameborder="0"
          allowfullscreen>
  </iframe>
  ```
- **Widget introduction format:** See Widget Introduction Requirements section

### Details Accordion (▤)
- **Purpose:** Optional depth, hints, transcripts, supplementary content
- **Format:** Title + expandable content (can include headings, paragraphs, lists)
- **When to use:** Content learners may want but isn't required

### AI Chat Widget (◈)
- **Purpose:** Q&A assistants, concept clarification, ongoing support
- **Configuration:**
  - Widget Name
  - System Prompt (detailed instructions)
  - Welcome Message
  - Show System Prompt: No (default)
- **Module pattern:** Configure ONE AI Chat Widget per module, reference it throughout
  - Place widget after first major concept
  - Add "Need clarification?" prompts that direct back to the widget
  - Don't create multiple AI chat widgets for same purpose

### AI Roleplay (◈)
- **Purpose:** Conversational assessments, stakeholder simulations
- **Configuration:** See AI Roleplay Tab Requirements section
- **Types:** Diagnostic (pre-learning), Formative (practice), Summative (graded)

### Vertical List (☰)
- **Purpose:** Numbered or bulleted items with titles and descriptions
- **Format:** Title + Description for each item
- **When to use:** Sequential steps, ranked items, categorized information

### Tiles (▦)
- **Purpose:** Card grids for options, categories, comparisons
- **Format:** Title + Description for each tile (2-4 tiles typical)
- **Layouts:** 2x2 grid, 1x3 horizontal, 1x4 horizontal
- **When to use:** Parallel options, category overviews, scannable choices

### Table (▭)
- **Purpose:** Comparative data, frameworks, structured information
- **Format:** Markdown table with headers, optional table note
- **When to use:** Side-by-side comparisons, data presentation

### Text Response Question (📝)
- **Purpose:** Written submissions (typed or file upload)
- **Configuration:** See Text Response Requirements section

---

## Widget Introduction Requirements

**Applies to:** All interactive widgets EXCEPT learning outcomes displays

**Four required components:**

### 1. Activity Header
```markdown
### ⚙ Interactive Activity: [Widget Name]
```

### 2. Learning Outcome Connection
```markdown
**Practice: WLO X.X ([Brief description])** ← Cohort
**Practice: MLO X.X ([Brief description])** ← Self-paced
```

### 3. Contextual Introduction (100-150 words)
Must include:
- **Readiness statement:** "You're now ready to..." or "Now that you understand..."
- **What they'll do:** Specific interaction description
- **Why it matters:** Real-world relevance or industry connection
- **What they'll gain:** Learning outcome and application

### 4. Technical Specification
```html
<iframe src="[URL]"
        width="800"
        height="600"
        title="[Descriptive title]"
        frameborder="0"
        allowfullscreen>
</iframe>
```

**Violations:**
- ❌ Generic introduction ("This widget helps you learn about...")
- ❌ Missing learning outcome connection
- ❌ Jumping straight to iframe without setup
- ❌ Too brief (<50 words) or too long (>200 words)

---

## AI Roleplay Tab Requirements

### Tab 1: Learning Objective
- Widget Name
- Learning Objective statement
- Scenario Setup: Diagnostic | Formative | Summative

### Tab 2: Scenario (THIRD-PERSON FORMAT)

**Required structure:**
```markdown
**Context:**
[Third-person objective description — "The learner will..." NOT "You are..."]

**Role of AI:**
[One sentence describing AI character]

**Role of Student:**
[One sentence describing learner's role]
```

**PROHIBITED in Tab 2:**
- ❌ Second-person language ("You are...", "Your task...", "Your goal...")
- ❌ "Your Task:" section
- ❌ "What to Have Ready:" section
- ❌ "Key Questions to Prepare For:" section
- ❌ Bullet lists of tasks or preparation items

### Tab 3: Hidden Context
- AI character personality traits and constraints
- Conversation strategy and behavior guidelines
- Information AI knows but student doesn't see
- How AI should respond to different situations

### Tab 4: Criteria (3-LEVEL FORMAT)

**Required structure:**
```markdown
**CRITERION 1: [Name]**

**Points:** 10

**Description:**
[Short one-sentence summary]

**Does not meet expectations:**
The learner [description of insufficient performance]

**Partially meets expectations:**
The learner [description of partial achievement]

**Fully meets expectations:**
The learner [description of complete achievement]
```

**PROHIBITED in Tab 4:**
- ❌ 4-level rubrics (Excellent/Proficient/Developing/Needs Improvement)
- ❌ Point ranges like "(9-10 pts)" — use single number only
- ❌ Long descriptions in criterion header — put details in level descriptions
- ❌ "Student" — always use "The learner"

---

## Text Response Requirements

### Tab 1: Instructions
- **Question Text:** Brief prompt (1-2 sentences)
- **Additional Instructions:** Optional checklist format
- **Template Upload:** Optional file template

### Tab 2: Criteria

**Configuration toggles:**
- Enable automated AI grading (on/off)
- Include evaluation levels (on/off)
- Apply points (on/off)

**When evaluation levels ON:** Use same 3-level format as AI Roleplay Tab 4

**When evaluation levels OFF:** Simple format allowed
```markdown
CRITERION 1: [Name]

Points: 10

[One-sentence description]
```

---

## Module Structure Requirements

### All Modules (2-7)
1. **Element 1:** Connecting text (100-150 words, recap + preview)
2. **Element 2:** Learning outcomes widget (SUBSET of WLOs/MLOs practiced in this module)
3. **Elements 3 to N-2:** Content delivery (V3 Interactive-First)
4. **Element N-1:** Final Project Connection (SPECIFIC references, not generic)
5. **Element N:** Module Complete → Transition to next module

### Module 0 (Self-Assessment)
1. Why this course matters + learner motivation
2. Learning outcomes widget (CLOs + first unit's WLOs/MLOs)
3. Course-level baseline quiz
4. AI results coach (formative, non-graded)
5. Course roadmap & suggested pacing

### Module 1 (Welcome)
1. Text: Course overview
2. Infobox: ALL Course Learning Outcomes (CLOs)
3. Video: Executive introduction or course preview
4. Learning outcomes widget: ALL WLOs/MLOs for the week/unit
5. Content elements
6. Final Project introduction

### Module 6 (Assessment)

**COHORT — PAIRR Structure:**
- Draft submission (80% of points)
- Peer feedback instructions
- AI feedback instructions
- Comparative reflection (peer vs AI feedback) — 2 bonus points
- Revision submission
- Post-revision reflection — 1 bonus point
- Total bonus: 5 points typical

**SELF-PACED — Individual Structure:**
- Assignment instructions
- AI feedback tool (optional for practice)
- Submission element with rubric
- AI-assisted grading enabled
- NO peer review, NO PAIRR, NO deadlines

### Module 7 (Week Wrap-Up)
- Key takeaways (3-5 insights with data)
- Final Project checkpoint/milestone
- Preview of next week/module
- Optional: Reflection prompt

---

## V3 Interactive-First Compliance

**Required metrics:**
- Widget every 2-3 elements
- Text blocks under 150 words (1 minute read max)
- 75% active engagement target
- Progressive complexity (simple lists → complex simulations)

**Text reduction targets:**
- 60-70% less text than traditional approaches
- Break readings into micro-chunks (100-150 words each)
- Replace explanatory paragraphs with interactive widgets

---

## Final Project Connection Requirements

**SPECIFIC references required — generic statements prohibited.**

**Good example:**
```markdown
Element 4's revenue model framework (media rights, ticketing, merchandising)
directly applies to **Checkpoint 3 of your Final Project**: Revenue Stream Analysis.
```

**Bad example:**
```markdown
This content will help with your final project.
```

**Required components:**
- What you learned (specific frameworks/tools from this module)
- How to apply it (specific checkpoint/milestone reference)
- Real-world connection (how practitioners use these concepts)
