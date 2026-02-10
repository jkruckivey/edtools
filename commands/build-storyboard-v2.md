# /build-storyboard-v2

Exemplar-based storyboard generation using the Bitter Lesson principle.

## Philosophy

> "General methods that leverage computation are ultimately the most effective." — Rich Sutton

Instead of following explicit rules from platform capability docs, this command learns patterns from production storyboards. The exemplar library contains real, shipped content that represents current practice—not historical assumptions about what we "should" do.

## Process

### Step 1: Select Exemplars

Based on the request, read 2-3 relevant exemplars from `exemplars/storyboards/`:

**For cohort courses:**
- `cohort/week3/modules/module-1-welcome.md` — Welcome module pattern
- `cohort/week3/modules/module-3-core-content.md` — Core content with widgets
- `cohort/week4/modules/module-4-interactive.md` — Interactive simulation focus
- `cohort/week4/modules/module-5-case-study.md` — Case study pattern
- `cohort/week3/modules/module-6-assessment.md` — Assessment module pattern

**For self-paced courses:**
- (Add exemplars when available)

**Selection heuristic:**
- Match module type (welcome, core content, interactive, case study, assessment, wrap-up)
- Match complexity (simple intro vs. widget-heavy)
- Include at least one with similar widget count

### Step 2: Extract Patterns (Implicitly)

Read the selected exemplars. Do NOT create a rules document. Let the patterns emerge through generation.

Key patterns to absorb:
- Version header format
- Element table structure
- Widget introduction format
- Quiz/assessment format
- Transition/bridge text style
- iframe embed attributes

### Step 3: Generate Storyboard

Given the course context and learning outcomes, generate a storyboard that *looks like* the exemplars. Match:

- Document structure (headers, tables, code blocks)
- Element ordering conventions
- Text length and tone
- Widget introduction components
- Transition patterns between elements

### Step 4: Self-Evaluate

Compare generated output against exemplars:

| Criterion | Check |
|-----------|-------|
| Version header present? | ✓/✗ |
| Element table format matches? | ✓/✗ |
| Widget intros have Challenge/Practice/How sections? | ✓/✗ |
| Text blocks under 150 words? | ✓/✗ |
| iframe embeds have accessibility attrs? | ✓/✗ |
| Module transition present? | ✓/✗ |

If score < 5/6, iterate.

## Usage

```
/build-storyboard-v2 Module 3 for "Intro to Python" - variables and data types
/build-storyboard-v2 Week 2 welcome module for "Leadership Fundamentals"
/build-storyboard-v2 Interactive module with 3 widgets for "Financial Modeling"
```

## Required Inputs

1. **Course title and format** (cohort or self-paced)
2. **Module position** (which week, which module number)
3. **Module focus** (welcome, core content, interactive, case study, assessment, wrap-up)
4. **Learning outcomes** (WLOs or MLOs this module addresses)
5. **Widget requirements** (if any)

## Output

Single markdown file matching exemplar structure:
- Version header with changelog
- Element table
- Full copy-paste content for each element
- Widget introductions with standard structure
- Module transition to next module

## What This Command Does NOT Do

- Follow explicit platform capability rules
- Add elements not present in exemplars (AI Chat configs, implementation checklists)
- Ask clarifying questions (infer from context or use sensible defaults)
- Run through multi-agent pipeline

## Comparison to Pipeline Approach

| Aspect | /build-storyboard (pipeline) | /build-storyboard-v2 (exemplar) |
|--------|------------------------------|--------------------------------|
| Process | 4 agents, clarifying questions | Single pass, pattern matching |
| Rules | Explicit (platform docs) | Implicit (learned from examples) |
| Output style | Follows encoded rules | Matches production practice |
| Drift risk | Rules diverge from practice | Auto-aligned with current exemplars |
| Speed | ~4 minutes | ~30 seconds |

## Updating the Approach

To improve output quality:
1. Add better exemplars to `exemplars/storyboards/`
2. Remove weak exemplars
3. That's it. No rules to update.

The approach improves by improving the examples, not by writing more rules.
