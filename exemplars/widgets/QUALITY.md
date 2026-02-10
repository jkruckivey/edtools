# Widget Exemplar Quality Scores

Widgets ranked by design system compliance. Use top-scoring exemplars for `/build-widget-v2`.

**Audit Date:** 2026-02-10
**Audit Method:** widget-designer agent against 7 criteria

## Scoring Criteria

1. **Geist font family** - Uses 'Geist', system-ui, sans-serif
2. **Neutral color palette** - Uses grays (#f5f5f5, #e5e5e5, #737373, etc.)
3. **No emojis in UI** - Clean professional appearance
4. **Accessible iframes** - If embedded, has title and aria-label
5. **Semantic HTML** - Proper heading hierarchy, labels for inputs
6. **Keyboard navigation** - Focusable elements, visible focus states
7. **Responsive design** - Works at different widths

---

## Golden Set (7/7) - Use These First

| Exemplar | Type | Score | Best For |
|----------|------|-------|----------|
| `simulators/streaming-wars-strategy.html` | Simulator | 7/7 | Strategy games, multi-scenario |
| `calculators/athlete-brand-calculator.html` | Calculator | 7/7 | Complex multi-tab calculators |

---

## Production Ready (6/7+)

| Exemplar | Type | Score | Notes |
|----------|------|-------|-------|
| `explorers/athlete-decision-tree.html` | Explorer | 6.5/7 | Minor: tablet breakpoint |
| `quizzes/sponsorship-roi-pre-assessment.html` | Quiz | 6/7 | Mobile <400px needs work |
| `calculators/sponsorship-roi-calculator.html` | Calculator | 7/7 | Fixed: Added ARIA live region |

---

## Needs Work (Exclude from exemplar generation)

| Exemplar | Type | Score | Issues |
|----------|------|-------|--------|
| `infographics/serena-williams-comic.html` | Infographic | 4/7 | 30+ emojis, incomplete a11y |

**Note:** The comic widget uses emojis extensively for visual flair (trophies, icons). This violates the "no emojis" standard but may be intentional for the comic book aesthetic. Consider either:
1. Refactoring to use CSS-based icons
2. Accepting as an exception for narrative widgets
3. Excluding from exemplar set for generation

---

## Selection Guide by Widget Type

| Widget Type | Golden Exemplar | Backup |
|-------------|-----------------|--------|
| **Calculator** | athlete-brand-calculator.html | sponsorship-roi-calculator.html |
| **Simulator** | streaming-wars-strategy.html | - |
| **Explorer** | athlete-decision-tree.html | - |
| **Quiz** | sponsorship-roi-pre-assessment.html | - |
| **Infographic** | *(none passing - use explorer patterns)* | - |

---

## Audit History

### 2026-02-10: Initial Audit + Fixes

**Audited 6 widgets across all types:**

| Widget | Before | After | Action |
|--------|--------|-------|--------|
| streaming-wars-strategy.html | 7/7 | 7/7 | None needed |
| athlete-brand-calculator.html | 7/7 | 7/7 | None needed |
| athlete-decision-tree.html | 6.5/7 | 6.5/7 | Minor issue, acceptable |
| sponsorship-roi-pre-assessment.html | 6/7 | 6/7 | Minor issue, acceptable |
| sponsorship-roi-calculator.html | 5/7 | 7/7 | Added ARIA live region |
| serena-williams-comic.html | 4/7 | 4/7 | Excluded - too many emojis |

**Fix applied:**
- `sponsorship-roi-calculator.html`: Added `.sr-only` class, ARIA live region, screen reader announcement

---

## Common Issues Found

1. **Missing ARIA live regions** - Results don't announce to screen readers
2. **Hardcoded colors** - Some use hex instead of CSS variables
3. **Emojis** - Visual flair but violates professional standard
4. **Mobile breakpoints** - Often missing <400px handling

## What Makes a Good Widget Exemplar

From the golden set, these patterns emerged:

- **CSS Variables**: Full neutral color scale defined in `:root`
- **Geist Font**: Loaded from Google Fonts CDN
- **Focus States**: Global `*:focus` rule with visible outline
- **ARIA**: Live regions for dynamic content, labels on controls
- **Responsive**: At least one breakpoint (768px), ideally also 480px
- **Semantic**: Proper heading hierarchy, labeled inputs
- **No Emojis**: Professional text labels only
