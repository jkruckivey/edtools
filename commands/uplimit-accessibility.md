---
description: Final accessibility audit for Uplimit storyboards (WCAG 2.2 AA, keyboard navigation, screen readers, UDL principles)
---

You are performing the **final accessibility and UDL review** for Uplimit storyboards.

Use the **uplimit-accessibility-auditor** to verify WCAG 2.2 AA compliance, keyboard navigation, screen reader support, and Universal Design for Learning principles. This is the last step before launch.

## What This Command Checks

The uplimit-accessibility-auditor verifies:

### WCAG 2.2 AA Compliance

**Widget Accessibility:**
- `title` attribute with descriptive text
- Keyboard navigation (Tab, Enter, Escape)
- Screen reader support (ARIA labels, live regions)
- Color contrast (4.5:1 for text, 3:1 for UI)
- Visible focus indicators

**Video Accessibility:**
- Captions available (VTT file)
- Transcript provided
- Audio description (if needed for complex visuals)

**Text Accessibility:**
- Heading hierarchy (H1 → H2 → H3, no skips)
- Descriptive link text (not "click here")
- Reading level appropriate

**Assessment Accessibility:**
- Clear instructions in plain language
- Time estimates provided
- Rubric visible before submission

### Universal Design for Learning (UDL)

**Multiple Means of Representation:**
- Text + Video + Visual + Interactive (3+ formats)
- Content in multiple modalities

**Multiple Means of Engagement:**
- Learner choice (optional depth, Details accordions)
- Real-world relevance connections
- Self-regulation support (progress indicators)

**Multiple Means of Action/Expression:**
- Written responses
- Verbal/conversational (AI roleplay)
- Interactive manipulation (widgets)
- Choice-based (multiple choice, scenarios)

## When to Use This Command

### Pipeline Step 4 (Final)
- After passing `/uplimit-audit` (platform compliance)
- Last check before publishing to Uplimit

### Pre-Launch Review
- Final accessibility verification
- UDL coverage confirmation
- Launch readiness determination

### Accessibility Audits
- Periodic compliance checks
- Widget accessibility verification
- Video accessibility review

## Example Usage

```
/uplimit-accessibility modules/week3/storyboards/module-3.md
/uplimit-accessibility final review before launch
/uplimit-accessibility check widget accessibility
```

## Expected Output

```markdown
# Accessibility & UDL Audit Report

**File:** module-3-storyboard.md
**Audit Date:** 2025-02-03
**Pre-requisite:** ✅ Passed platform compliance (Auditor Agent)

---

## Summary

| Category | Status | Issues |
|----------|--------|--------|
| Widget Accessibility | ⚠️ | 2 |
| Video Accessibility | ✅ | 0 |
| Text Accessibility | ✅ | 0 |
| UDL: Representation | ✅ | 0 |
| UDL: Engagement | ✅ | 0 |
| UDL: Expression | ✅ | 0 |

**WCAG 2.2 AA Status:** NEEDS REMEDIATION
**UDL Status:** STRONG

**Overall:** REMEDIATION REQUIRED

---

## WCAG 2.2 AA Issues

### ❌ Missing Widget Title - WCAG 1.1.1

**Location:** Element 5, Sponsorship Calculator
**Criterion:** 1.1.1 Non-text Content
**Level:** A

**Current:**
```html
<iframe src="widget.html" width="800" height="600">
```

**Remediation:**
```html
<iframe src="widget.html"
        width="800"
        height="600"
        title="Sponsorship Valuation Calculator - Input parameters to calculate ROI"
        aria-label="Interactive calculator for sponsorship valuation">
```

**Priority:** Critical

---

### ⚠️ Color Contrast Below 3:1 - WCAG 1.4.11

**Location:** Widget success state
**Current:** #22c55e on #ffffff = 2.8:1 (fails 3:1)

**Remediation:**
Change success green to #16a34a (3.9:1) or add dark background.

**Priority:** High

---

## UDL Analysis

### Multiple Means of Representation
**Current Formats:** Text, Video, Widget, Infographic
**Coverage:** 4/3 minimum ✅
**Status:** ✅ Strong

### Multiple Means of Engagement
**Choice Elements:** Details accordions, optional depth
**Status:** ✅ Strong

### Multiple Means of Expression
**Expression Types:** Written, AI Roleplay, Widget interaction
**Status:** ✅ Strong

---

## → COURSE READY STATUS

**REMEDIATION REQUIRED**

Complete these fixes before launch:

### Critical (Must Fix)
1. Add title/aria-label to Sponsorship Calculator widget

### High (Fix Within First Week)
1. Adjust success state color for 3:1 contrast

After remediation, re-run this audit to confirm compliance.
```

---

**Pipeline Position:**
- Step 1: `/uplimit-structure` (create structure)
- Step 2: `/uplimit-build` (create content)
- Step 3: `/uplimit-audit` (verify compliance)
- **Step 4**: Accessibility Auditor (this command) → **LAUNCH READY**

Or use `/build-storyboard` to run the full pipeline automatically.
