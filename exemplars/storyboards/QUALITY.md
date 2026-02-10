# Storyboard Exemplar Quality Scores

Exemplars ranked by Uplimit platform compliance. Use top-scoring exemplars for `/build-storyboard-v2`.

**Audit Date:** 2026-02-10
**Audit Method:** uplimit-auditor-agent against 7 criteria

## Scoring Criteria

1. **Infobox compliance** - 50-100 words, simple paragraphs only
2. **Widget introductions** - Challenge/Practice/How 4-component structure
3. **Text block length** - Under 150 words
4. **Element table format** - Order/Element/Content columns
5. **Version header** - Version number with changelog
6. **iframe accessibility** - title and aria-label attributes
7. **Module transition** - Explicit transition to next module

---

## Golden Set (7/7) - Use These First

| Exemplar | Score | Best For |
|----------|-------|----------|
| `week4/module-4-interactive.md` | 7/7 | Interactive/widget-heavy modules |
| `week3/module-3-core-content.md` | 7/7 | Core content with multiple widgets |

---

## Production Ready (6/7+)

| Exemplar | Score | Notes |
|----------|-------|-------|
| `week3/module-1-welcome.md` | 7/7 | Fixed: Added widget intros, module transition |
| `week3/module-6-assessment.md` | 7/7 | Fixed: Condensed infobox to 95 words |
| `week4/module-5-case-study.md` | 7/7 | Fixed: Converted infobox to accordion, added transition |
| `week2/module-0-bridge-in.md` | 7/7 | Fixed: Added 4-component widget intro |

---

## Audit History

### 2026-02-10: Initial Audit + Fixes

**Before fixes:**
- week4/module-4-interactive.md: 7/7 ✓
- week3/module-3-core-content.md: 6.5/7 (minor placement issue)
- week3/module-1-welcome.md: 6/7 (missing widget intros, no transition)
- week3/module-6-assessment.md: 6/7 (infobox over limit)
- week2/module-0-bridge-in.md: 5/7 (widget intro incomplete)
- week4/module-5-case-study.md: 4/7 (infobox violations, missing transition)

**Fixes applied:**
1. `module-5-case-study.md`: Converted infobox to Details Accordion, added Element 5 transition
2. `module-1-welcome.md`: Added widget intro text for both widgets, added Element 8 transition
3. `module-6-assessment.md`: Condensed infobox from 145 to 95 words, removed bullets
4. `module-0-bridge-in.md`: Expanded widget intro to 4-component structure

**After fixes:** All exemplars now score 7/7

---

## Usage in /build-storyboard-v2

The command should:
1. Read 2-3 exemplars from the Golden Set based on module type
2. Match patterns implicitly (no explicit rules)
3. Generate storyboard that looks like the exemplars
4. Self-evaluate against the 7 criteria

Since all exemplars now pass compliance, any can be used. Prefer:
- `module-4-interactive.md` for widget-heavy modules
- `module-3-core-content.md` for core content
- `module-1-welcome.md` for welcome/intro modules
- `module-6-assessment.md` for assessment modules
- `module-5-case-study.md` for case study modules
- `module-0-bridge-in.md` for bridge/diagnostic modules
