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
| Project name | Anchor Project | Final Project or Final Assessment |
| Progress markers | Milestone with firm deadlines | Checkpoint with flexible pacing |
| Pacing language | "Submit by Friday 11:59 PM ET" | "When you're ready" |
| Assessment modules | PAIRR with peer review | Individual assessment (NO peer review) |
| Unit outcomes | ULO (Unit Learning Outcomes) — optional | ULO (Unit Learning Outcomes) — common |

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

### Image (▭)
- **Purpose:** Visual content, diagrams, screenshots, decorative elements
- **Two types:**

**Informational Images:**
- Convey essential information (diagrams, charts, screenshots)
- **Require descriptive alt text** explaining what the image shows
- Example: `alt="Revenue breakdown pie chart showing Media 45%, Ticketing 25%, Sponsorship 20%, Merchandise 10%"`

**Decorative Images:**
- Visual breaks, mood-setting, aesthetic purposes
- **Empty alt text required:** `alt=""`
- Mark as decorative: `role="presentation"` or `aria-hidden="true"`
- Do NOT include informational content

**Specifications:**
- **Dimensions:** Full-width banner (1200×400px) or inline (max 600px width)
- **Formats:** PNG, JPG, WebP
- **File naming:** `m[#]-[purpose]-[description].png` (e.g., `m1-decorative-linear.png`)

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
  - **Suggested Prompts** (optional): Quick-start buttons displayed to students
    ```markdown
    **Suggested Prompts:**
    - "What does slope mean in business?"
    - "How do I interpret the intercept?"
    - "Can you explain break-even analysis?"
    - "Help me understand this Excel formula?"
    ```
- **Module pattern:** Configure ONE AI Chat Widget per module, reference it throughout
  - Place widget after first major concept
  - Add "Need clarification?" prompts that direct back to the widget
  - Don't create multiple AI chat widgets for same purpose
- **For Module Expert configuration:** See AI Chat Module Expert Requirements section

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

### Practice Quiz / Multiple Choice (📝)
- **Purpose:** Knowledge checks, comprehension verification, self-assessment
- **Configuration:** See Practice Quiz Requirements section
- **Types:** Graded (points assigned) or Ungraded (self-assessment)

---

## Widget Introduction Requirements

**Applies to:** All interactive widgets EXCEPT learning outcomes displays

**Four required components:**

### 1. Activity Header

Use ONE of these header patterns based on widget purpose:

```markdown
# Explore: [Topic Name]           ← Discovery/exploration widgets
# Practice: [Skill or Task]       ← Application/practice widgets
### ⚙ Interactive Activity: [Widget Name]  ← General interactive elements
```

### 2. Learning Outcome Connection

Embed in contextual introduction OR use explicit format:

```markdown
**Practice: WLO X.X ([Brief description])** ← Cohort (explicit)
**Practice: MLO X.X ([Brief description])** ← Self-paced (explicit)
```

Or embed naturally: "This activity supports WLO 1.3 by letting you evaluate..."

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
- ❌ Missing learning outcome connection (explicit or embedded)
- ❌ Jumping straight to iframe without setup
- ❌ Too brief (<50 words) or too long (>200 words)

---

## AI Roleplay Tab Requirements

### Tab 1: Learning Objective
- **Widget Name:** Descriptive title for the roleplay
- **Learning Objective:** Detailed statement of what students will demonstrate (can be multi-point)
- **Scenario Setup:** Choose based on purpose:
  - `Diagnostic` — Pre-learning baseline assessment
  - `Formative` — Practice with feedback (not graded or low stakes)
  - `Summative` — Graded assessment
  - `Experiential simulation` — Application-level learning through scenario

### Tab 2: Scenario (THIRD-PERSON FORMAT)

**Required structure:**
```markdown
**Context:**
[Third-person objective description — "The learner has just been hired as..." NOT "You are..."]

**Role of AI:**
[Character name and description — "Patricia Chen, Board Chair. Former Fortune 500 CEO..."]

**Role of Student:**
[One sentence describing learner's role — "The learner plays the Chief Revenue Officer making strategic decisions..."]
```

**PROHIBITED in Tab 2:**
- ❌ Second-person language ("You are...", "Your task...", "Your goal...")
- ❌ "Your Task:" section
- ❌ "What to Have Ready:" section
- ❌ "Key Questions to Prepare For:" section
- ❌ Bullet lists of tasks or preparation items

### Tab 3: Hidden Context

**Complexity varies by roleplay type.** Match detail level to assessment purpose:

---

#### GRADED ROLEPLAYS (Summative/Experiential Simulation)

For graded assessments with branching decisions, Tab 3 should be comprehensive (200-500 lines):

**Character Development:**
- Full background (career history, expertise, personality)
- Communication style ("Warm but direct", "Uses specific numbers", "Asks probing questions")
- How character responds to different student behaviors

**Course Knowledge:**
- Relevant learning objectives (WLOs/MLOs) this roleplay supports
- Key concepts students learned in prior modules
- Specific data, frameworks, or examples the AI should reference

**Simulation Flow (for branching scenarios):**
- Opening scenario and first decision point
- Decision options and consequences for each path
- How outcomes vary based on prior choices
- Closing reflection prompts

**Edge Case Handling:**
- What to do if student gives vague answers
- How to redirect off-topic responses
- How to probe for deeper reasoning
- How to handle students who recognize patterns early

**Success Indicators:**
- What demonstrates mastery vs. partial understanding
- Key insights students should discover through play

---

#### NON-GRADED ROLEPLAYS (Diagnostic/Formative)

For diagnostic or practice conversations, Tab 3 can be simpler (20-50 lines):

```markdown
You are a [role] helping students [purpose].

Your role:
- [3-4 bullet points describing behavior]
- Be encouraging and supportive

Ask 3-4 conversational questions about:
- [Topic 1]
- [Topic 2]
- [Topic 3]

Example opening: "[Sample greeting]"

Example closing: "[Sample wrap-up message]"
```

---

### Tab 4: Criteria

**Format depends on whether roleplay is graded:**

---

#### GRADED ROLEPLAYS — Full 3-Level Rubric

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

**PROHIBITED in graded rubrics:**
- ❌ 4-level rubrics (Excellent/Proficient/Developing/Needs Improvement)
- ❌ Point ranges like "(9-10 pts)" — use single number only
- ❌ Long descriptions in criterion header — put details in level descriptions
- ❌ "Student" — always use "The learner"

---

#### NON-GRADED ROLEPLAYS — Completion Only

For diagnostic/formative roleplays, Tab 4 contains configuration flags only:

```markdown
**Grading Configuration:**
- ❌ Enable automated AI grading: NO
- ✅ Track completion only: YES
- ✅ Provide formative feedback: YES (reassurance at end)
- ❌ No rubric/points assigned
```

Leave rubric section empty. Platform tracks completion but doesn't assign grades.

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

## Practice Quiz Requirements

### Element Setup
1. Select **Exercise → Practice Quiz** element
2. Configure as graded or ungraded (self-assessment)
3. Add multiple choice questions using ONE of the formats below

### Format Options

**Choose based on workflow:**
- **Detailed Format** — Separate code blocks for each field (easier copy-paste into Uplimit)
- **Compact Format** — Inline markdown (faster to read/review in storyboards)

---

### Detailed Format (Recommended for Uplimit Entry)

Each question uses separate markdown blocks for easy copy-paste:

**Question:**
```
[Full question text — be specific, reference content from the module]
```

**Option A:**
```
[First option text]
```

**Option B:**
```
[Second option text]
```

**Option C:**
```
[Third option text]
```

**Option D:**
```
[Fourth option text]
```

**Correct Answer:** [A, B, C, or D]

**After Submission:**
```
[General feedback shown to ALL students regardless of answer — explains why this matters]
```

**Feedback for correct answers:**
```
[Specific reinforcement — "Correct! [Explain WHY this is right with additional context]"]
```

**Feedback for incorrect answers:**
```
[Helpful redirect — guide them to reconsider without giving away answer, reference where to find info]
```

**Points:** [1-5 typical]

### Correct Answer Distribution

**IMPORTANT:** Vary the position of correct answers across questions.

- ❌ Don't make B or C always correct
- ❌ Don't follow predictable patterns (A, B, C, D, A, B...)
- ✅ Distribute correct answers roughly evenly across A, B, C, D
- ✅ For a 5-question quiz: aim for mix like A, C, B, D, A (not B, C, B, C, B)

### Question Writing Guidelines

**Good questions:**
- Reference specific content from the module ("Kevin describes...")
- Test understanding, not recall ("What is the PRIMARY driver..." not "What year did...")
- Have plausible distractors (wrong answers that reflect common misconceptions)

**Avoid:**
- Trick questions or "gotcha" wording
- "All of the above" or "None of the above" as options
- Questions answerable without watching/reading the content
- Overly long question stems (keep under 50 words)

### Example Question

**Question:**
```
According to Kevin Abrams, what determines the quality of output from the Giants' enterprise ChatGPT implementation?
```

**Option A:**
```
The processing power of the system
```

**Option B:**
```
The amount of training data available
```

**Option C:**
```
The quality of prompts users create
```

**Option D:**
```
The number of employees using it
```

**Correct Answer:** C

**After Submission:**
```
AI implementation success depends heavily on how users interact with the technology. This principle applies across industries adopting generative AI tools.
```

**Feedback for correct answers:**
```
Correct! Kevin emphasizes that "quality of prompts dictates output" when discussing their AI rollout. This principle applies broadly: AI tools are only as useful as the questions and instructions given to them.
```

**Feedback for incorrect answers:**
```
Kevin discusses their enterprise AI rollout and mentions a specific factor that determines success. It's not about the technology itself—it's about how employees interact with it. Think about what input users provide.
```

**Points:** 1

---

### Compact Format (For Storyboard Review)

Use inline markdown for faster reading during content review:

```markdown
**Q1: [Question text]**
- A) [Option text]
- B) [Option text] ✓
- C) [Option text]
- D) [Option text]

*After Submission:* [General feedback for all students]

*Correct:* [Feedback for correct answer]

*Incorrect:* [Feedback for incorrect answer]
```

**Example (Compact):**

```markdown
**Q1: With raisin price set to $2.00, what is the price reduction in pennies below baseline?**
- A) 10 pennies
- B) 15 pennies ✓
- C) 20 pennies
- D) 25 pennies

*After Submission:* Baseline is $2.15 (215 cents). Current price is $2.00 (200 cents). Reduction = 215 - 200 = 15 pennies.

*Correct:* Correct! The price is 15 cents below the $2.15 baseline.

*Incorrect:* Calculate: Baseline (215 cents) - Current price (200 cents) = 15 pennies below baseline.
```

**Notes:**
- Mark correct answer with `✓` (not `✅`)
- Use `*italics*` for feedback labels
- Compact format is easier to scan in long storyboards
- Convert to detailed format when entering into Uplimit

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

---

## AI Chat Module Expert Requirements

**Purpose:** Create AI Chat Widgets that serve as deep subject matter experts for each module, capable of explaining concepts in multiple ways and drawing on course content plus external knowledge.

### System Prompt Structure

Module Expert AI Chat Widgets require comprehensive system prompts with four sections:

---

#### Section 1: Course Context

```markdown
**Course:** [Course Name]
**Module:** [Module Number and Title]
**Format:** [Cohort/Self-paced]

**Learning Outcomes This Module:**
- [WLO/MLO X.X]: [Description]
- [WLO/MLO X.Y]: [Description]

**Prerequisites:** Students have completed [prior modules] and understand [key concepts].
```

---

#### Section 2: Content Knowledge

Inject relevant course content the AI should reference:

```markdown
**Key Concepts from This Module:**

1. **[Concept Name]:** [2-3 sentence explanation with specific data/examples from course]

2. **[Concept Name]:** [2-3 sentence explanation with specific data/examples from course]

**Frameworks & Models:**
- [Framework Name]: [Brief description of how it works]
- [Model Name]: [Brief description and when to apply]

**Key Data Points:**
- [Statistic from course content with source]
- [Data point students should know]

**Executive/Expert Quotes:**
- "[Direct quote from video/reading]" — [Speaker Name], [Title]
```

---

#### Section 3: External Knowledge

Provide curated external context the AI can draw upon:

```markdown
**Industry Context:**
- [Current trend or development relevant to module topic]
- [Real-world example beyond course content]

**Common Misconceptions:**
- Students often think [X], but actually [Y]
- [Another misconception] vs. [correct understanding]

**Deeper Resources (for curious students):**
- [Book/article title] by [Author] — [One-line description]
- [Industry report] — [Why it's relevant]
```

---

#### Section 4: Pedagogical Guidance

```markdown
**How to Respond:**
- Start by understanding what the student already knows
- Offer multiple explanations: simple analogy, technical detail, real-world example
- Reference specific module content when relevant ("As Kevin Abrams mentioned...")
- Ask clarifying questions before diving into complex explanations
- Encourage application: "How might this apply to your Final Project team?"

**Tone:** [Approachable expert / Coach / Collaborator] — supportive but rigorous

**Boundaries:**
- Stay focused on [module topic] and related concepts
- For questions about [other topics], redirect: "That's covered in Module X—but briefly..."
- If unsure about specific course policy, suggest asking the instructor

**Example Interactions:**

Student: "I don't understand break-even analysis."
AI: "Let me try a few angles. First, the simple version: break-even is the point where revenue exactly covers costs—no profit, no loss. Think of it like a seesaw balancing. Want me to walk through the formula, show you a restaurant example, or explain how it connects to the pricing exercise in Element 5?"

Student: "Why do media rights matter so much?"
AI: "Great question! In Module 1, Kevin Abrams mentioned the Giants rely on media revenue for nearly 45% of total income. The reason? Media rights provide predictable, long-term cash flow regardless of on-field performance. A team can have a losing season but still collect the same broadcast check. Want me to compare this to how ticketing revenue works differently?"
```

---

### Module Expert vs. General AI Chat

| Aspect | General AI Chat | Module Expert |
|--------|-----------------|---------------|
| Scope | Broad Q&A support | Deep expertise in one module |
| Knowledge | General AI capabilities | Injected course content + curated external sources |
| Personality | Helpful assistant | Subject matter expert in character |
| References | Generic responses | Cites specific module content, data, quotes |
| Depth | Surface-level help | Can explain same concept multiple ways |

---

### Implementation Notes

- **One expert per module:** Don't create multiple AI Chat Widgets for the same module content
- **Content injection:** The system prompt IS the knowledge base—write it comprehensively
- **Refresh quarterly:** Update industry context and data points to stay current
- **Test edge cases:** Try asking about misconceptions, adjacent topics, and "explain like I'm five" requests

---

## Citations & Further Reading Patterns

**Purpose:** Provide source attribution and optional deeper exploration WITHOUT cluttering the main content flow. Use expandable accordions, not inline citations.

### Pattern 1: Source Attribution Box

For data points, statistics, or claims that need sourcing:

**Element Type:** Details Accordion

```markdown
**📊 Source: [Topic]**

[Click to expand]

**Data Source:** [Organization/Publication Name]
**Publication:** "[Report/Article Title]" ([Year])
**Link:** [URL if available]

**Context:** [1-2 sentences explaining methodology or relevance]
```

**Example:**

```markdown
**📊 Source: NFL Franchise Valuations**

[Click to expand]

**Data Source:** Forbes
**Publication:** "The World's Most Valuable Sports Teams 2024" (September 2024)
**Link:** forbes.com/lists/nfl-valuations

**Context:** Forbes annually surveys team ownership, revenue, and operating income to calculate franchise values. The $6.49B average reflects a 57% increase since 2021, driven largely by new media rights deals.
```

---

### Pattern 2: Go Deeper Accordion

For students who want additional reading without requiring it:

**Element Type:** Details Accordion

```markdown
**📚 Go Deeper: [Topic]**

[Click to expand]

**Want to explore [topic] further?** Here are curated resources:

**Academic:**
- [Author Last Name] ([Year]). "[Article/Book Title]." *[Journal/Publisher]*. [One-line relevance]

**Industry:**
- [Publication] ([Year]). "[Report Title]." [One-line relevance]

**Accessible:**
- [Blog/Video Title] by [Creator]. [One-line relevance + why it's good for beginners]
```

**Example:**

```markdown
**📚 Go Deeper: Sports Media Economics**

[Click to expand]

**Want to explore media rights further?** Here are curated resources:

**Academic:**
- Noll, R. (2007). "Broadcasting and Team Sports." *Handbook on the Economics of Sport*. Foundational analysis of why sports content is uniquely valuable to broadcasters.

**Industry:**
- Sports Business Journal (2024). "NFL Media Rights Tracker." Real-time database of current and upcoming broadcast deals.

**Accessible:**
- "How ESPN Almost Went Bankrupt" — Wendover Productions (YouTube). 18-minute explainer on cord-cutting and sports media economics for general audiences.
```

---

### Pattern 3: The Data Behind This

For modules heavy on statistics, provide a consolidated data sources section:

**Element Type:** Details Accordion (placed after data-heavy content)

```markdown
**📈 The Data Behind This Module**

[Click to expand]

This module references data from:

| Claim | Source | Year |
|-------|--------|------|
| NFL franchise average value: $6.49B | Forbes NFL Valuations | 2024 |
| Media rights = 40-60% of revenue | Deloitte Sports Practice | 2023 |
| Premium seating = 40-50% of gate revenue | Team Marketing Report | 2024 |

**Note:** Industry data varies by methodology. These figures represent consensus ranges from major analysts.
```

---

### Pattern 4: Further Reading (End of Module)

Optional "bookshelf" for students completing the module:

**Element Type:** Details Accordion (in Module Complete section)

```markdown
**📖 Further Reading**

[Click to expand]

**Finished the module and want more?** Try these:

**Quick Reads (10-15 min):**
- "[Article Title]" — [Publication]. [One-line hook]

**Deep Dives (30+ min):**
- "[Book/Long-form Title]" by [Author]. [One-line hook]

**Podcasts:**
- *[Podcast Name]*, Episode [#]: "[Episode Title]." [One-line hook]
```

---

### What NOT to Do

**❌ Inline citations:** Don't write "According to Forbes (2024), franchise values..." in main text. This clutters the reading experience.

**❌ Footnotes:** Uplimit doesn't support footnote syntax. Don't use superscript numbers.

**❌ Required readings in accordions:** If students MUST read something, put it in main content. Accordions are for optional exploration.

**❌ Overwhelming lists:** Curate to 3-5 resources maximum. Quality over quantity.

---

### Placement Guidelines

| Pattern | Where to Place |
|---------|----------------|
| Source Attribution | Immediately after the statistic/claim in an accordion |
| Go Deeper | After the concept is fully explained (not mid-explanation) |
| Data Behind This | Near end of data-heavy sections or modules |
| Further Reading | In Module Complete section, before transition |
