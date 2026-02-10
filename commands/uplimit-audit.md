---
description: Audit Uplimit storyboards for platform compliance (infobox limits, AI roleplay format, widget intros, structure)
---

You are auditing Uplimit storyboards for **platform compliance**.

Use the **uplimit-auditor-agent** to verify content against Uplimit platform specifications and get specific, copy-paste-ready corrections for any violations.

## What This Command Checks

The uplimit-auditor-agent verifies:

### Infobox Compliance
- Word count: 50-100 words
- Format: Simple paragraph, no headings/bullets/lists
- Style: Flowing prose, not structured content

### AI Roleplay Configuration
- Tab 1 (Prompt): Student-facing instructions
- Tab 2 (Scenario): Third-person objective language
- Tab 3 (Hidden Context): AI character instructions
- Tab 4 (Criteria): Exactly 3 levels, "The learner" language

### Widget Introductions
- Activity header with emoji
- Learning outcome connection
- Contextual introduction (100-150 words)
- Technical specification

### Text Response Criteria
- 3 levels when evaluation enabled
- "The learner" language
- Observable behaviors

### Module Structure
- Required components by module type
- Element sequencing
- Course type consistency (WLO vs MLO)

### V3 Interactive-First
- Widget density (every 2-3 elements)
- Text block limits (<150 words)
- Engagement ratio (75% active)

## When to Use This Command

### Pipeline Step 3
- After using `/uplimit-build` to create content
- Before using `/uplimit-accessibility` for final review

### Quality Assurance
- Before publishing storyboards to Uplimit
- After receiving content from SMEs or writers
- Periodic compliance checks on existing content

### Troubleshooting
- When Uplimit rejects content (word limits, format issues)
- Identifying why AI roleplay isn't working correctly

## Example Usage

```
/uplimit-audit modules/week3/storyboards/module-3.md
/uplimit-audit check this storyboard for compliance
/uplimit-audit verify infobox word counts
```

## Expected Output

```markdown
# Uplimit Compliance Audit Report

**File:** module-3-storyboard.md
**Course Format:** Cohort
**Audit Date:** 2025-02-03

---

## Summary

| Check | Status | Issues |
|-------|--------|--------|
| Infobox Compliance | ⚠️ | 2 |
| AI Roleplay Format | ❌ | 1 |
| Widget Introductions | ✅ | 0 |
| Module Structure | ✅ | 0 |
| V3 Interactive-First | ✅ | 0 |
| Course Type Consistency | ✅ | 0 |

**Overall Status:** NEEDS REVISION

---

## Issues Found

### ❌ CRITICAL: AI Roleplay Tab 2 uses second-person

**Location:** Element 8, Tab 2 Scenario
**Line:** 145

**Current Content:**
```
You are a sports business consultant advising Brookfield Capital.
Your task is to present your findings...
```

**Problem:** Tab 2 must use third-person language ("The learner will...").

**Corrected Version:**
```
**Context:**
Brookfield Capital is considering a $500M investment in a sports team.
The learner will present findings on sports revenue ecosystems...

**Role of Student:**
The learner plays the role of a sports business consultant...
```

---

### ⚠️ WARNING: Infobox over word limit

**Location:** Element 5
**Word Count:** 156 words (limit: 100)

**Current Content:**
[Full current infobox]

**Corrected Version (condensed to 85 words):**
[Condensed version]

---

## → NEXT STEP

**NEEDS REVISION:** Apply corrections above, then re-audit.

After passing, use `/uplimit-accessibility` for final review.
```

---

**Pipeline Position:**
- Step 1: `/uplimit-structure` (create structure)
- Step 2: `/uplimit-build` (create content)
- **Step 3**: Auditor Agent (this command)
- Step 4: `/uplimit-accessibility` (final review)

Or use `/build-storyboard` to run the full pipeline automatically.
