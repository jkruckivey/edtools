# /build-widget-adaptive

Generate widgets by learning from examples rather than explicit rules.

## Philosophy: The Bitter Lesson

This command implements Rich Sutton's "Bitter Lesson" - that general methods leveraging computation (search and learning) ultimately outperform human-knowledge-based approaches.

**Traditional approach:** Encode 50+ explicit rules about colors, fonts, spacing, accessibility...
**This approach:** Show 3-4 exemplars, let the model discover patterns, iterate until quality matches.

## Usage

```
/build-widget-adaptive [widget-type] for [topic]
```

Examples:
- `/build-widget-adaptive calculator for customer lifetime value`
- `/build-widget-adaptive explorer for marketing channels`
- `/build-widget-adaptive quiz for brand positioning concepts`

## Process

### Step 1: Load Exemplars

Read 3-4 reference widgets from the course repository:
- One calculator (sponsorship-roi-calculator.html)
- One explorer/infographic (revenue-streams-explorer.html)
- One quiz/assessment (sponsorship-roi-pre-assessment.html)
- One similar to requested type if available

### Step 2: Pattern Extraction (Implicit)

Do NOT write explicit rules. Instead, internalize:
- "These widgets look and feel a certain way"
- "They share structural patterns"
- "They handle interactivity similarly"

### Step 3: Generate First Draft

Create a widget for the requested topic that "feels like" the exemplars.
Write to: `./output/[widget-name]-draft-1.html`

### Step 4: Self-Evaluate

Compare your draft against the exemplars. Ask:
1. Does it visually match the reference style?
2. Does the structure follow similar patterns?
3. Are interactive behaviors consistent?
4. Would it blend in with the other widgets?

Score: 1-10 (aim for 8+)

### Step 5: Iterate (if needed)

If score < 8, identify specific gaps and revise.
Maximum 3 iterations.
Write final to: `./output/[widget-name].html`

### Step 6: Report

Output:
- Final widget path
- Confidence score (1-10)
- Key patterns matched
- Any deviations and why

## What This Command Does NOT Do

- Provide a checklist of design rules
- Specify exact hex colors
- Define font sizes or spacing values
- List accessibility requirements explicitly

The model should discover these from the examples.

## Why This Might Work

Claude's training includes vast exposure to HTML/CSS patterns. By showing specific exemplars, we're essentially doing few-shot learning - letting the model match patterns rather than following rules.

The iteration loop adds "search" - exploring the solution space and converging on quality.

## Why This Might Fail

- 3-4 examples may not be enough to capture all patterns
- Without explicit rules, edge cases may be missed
- Accessibility requirements might be inconsistently applied
- The model may "average" patterns rather than match them precisely

## Experiment Notes

This is experimental. Compare outputs against rule-based `/design-widget` to measure:
- Visual consistency
- Code quality
- Accessibility compliance
- Development speed

---

**Implementation:** When this command is invoked, Claude should:

1. Read the exemplar files (paths hardcoded for now)
2. Generate a first draft matching their patterns
3. Self-critique against the exemplars
4. Iterate if needed
5. Output the final widget with a confidence assessment
