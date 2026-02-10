# MODULE 5: LIV Golf - The Sportswashing Dilemma
**Version:** 1.0.0 | **Last Updated:** 2026-01-20

**Purpose:** Explore ethical sponsorship decisions through interactive tools (supports WLOs 3.3, 3.4, 3.5)

### Simplified Version Changes
- **REMOVED:** Case reading requirement, comprehension quiz, 150-word reflection, required roleplay
- **KEPT:** 2 interactive widgets, optional roleplay, optional AI coach
- **RESULT:** ~15 minutes, focused on decision-making

**Uplimit Structure:** Fifth module in Unit 3

| Order | Element | Content/Purpose | Time | Notes |
|-------|---------|-----------------|------|-------|
| 1 | **Text** ⬤ Required | The LIV Golf dilemma (150 words) | 2 min | Sets up the ethical tension |
| 2 | **Video** ⬤ Required | "Sportswashing Explained" (2 min) | 2 min | Visual explainer |
| 3 | **iFrame Widget** ⬤ Required | Ethical Sponsorship Decision Tool | 5 min | Evaluate brand-property fit |
| 4 | **iFrame Widget** ⬤ Required | Brand Risk Calculator | 4 min | Model reputation vs. ROI |
| 5 | **Table** ○ Optional | LIV Golf Sponsor Decisions | 1 min | Who signed, who walked |
| 6 | **AI Roleplay** ○ Optional | Phil Mickelson's Decision | Optional | For those who want to go deeper |
| 7 | **AI Coach** ○ Optional | Ethical Sponsorship Discussion | Optional | Ask questions |

**Total Time:** ~15 minutes (core), +10-15 optional
**Active Engagement:** 75%+

---

## Element 1: The LIV Golf Dilemma

```markdown
# When Money Meets Ethics: LIV Golf

LIV Golf offers brands something unusual: access to golf's biggest names (Mickelson, DJ, Koepka) at lower sponsorship costs than the PGA Tour. The catch? It's funded by Saudi Arabia's sovereign wealth fund.

Critics call it "sportswashing"—using sports to distract from human rights concerns. Supporters say it's just business.

**The question for brands:** Does the ROI justify the reputation risk?

In this module, you'll use two tools to analyze this decision. No right answer—just trade-offs.
```

---

## Element 2: Video - Sportswashing Explained

- **File:** `week3-sportswashing-explainer.mp4`
- **Duration:** 2 minutes
- **Title:** "What is Sportswashing?"
- **Content:** Quick visual explainer of sportswashing concept, examples (Saudi Arabia, Qatar, Russia), and why it matters for brands

---

## Element 3: Ethical Sponsorship Decision Tool

**Widget:** `ethical-sponsorship-decision-tool.html`

```html
<iframe
  src="../../widgets/ethical-sponsorship-decision-tool.html"
  width="100%"
  height="650"
  title="Ethical Sponsorship Decision Tool"
></iframe>
```

**What students do:** Evaluate a hypothetical sponsorship opportunity across multiple dimensions—brand fit, audience alignment, stakeholder impact, reputation risk. See how different weightings change the recommendation.

---

## Element 4: Brand Risk Calculator

**Widget:** `brand-risk-calculator.html`

```html
<iframe
  src="../../widgets/brand-risk-calculator.html"
  width="100%"
  height="600"
  title="Brand Risk Calculator"
></iframe>
```

**What students do:** Model the financial trade-off between sponsorship value and reputation cost. Adjust assumptions about consumer backlash, media coverage, and brand resilience.

---

## Element 5: LIV Golf Sponsor Decisions (Optional)

**Table: Who's In, Who's Out**

| Brand | Decision | Rationale |
|-------|----------|-----------|
| Michelob Ultra | Declined | Brand safety concerns |
| Rolex | Declined | Heritage protection |
| Callaway | Signed | Player relationships |
| FedEx | Left PGA, didn't join LIV | Complex positioning |
| Mastercard | Declined | ESG commitments |
| LIV Corporate sponsors | Signed | Saudi-adjacent companies |

---

## Element 6: AI Roleplay - Phil Mickelson's Decision (Optional)

**For students who want to go deeper**

**Roleplay Setup:**
```
You are Phil Mickelson in early 2022. You've been offered $200 million guaranteed to join LIV Golf. You're 51 years old, your PGA Tour earnings are declining, and this could secure your family's financial future.

But: You know about the Saudi government's human rights record. You know there will be backlash. Your sponsors may leave. Your legacy may be tarnished.

What do you do?
```

**Student Instructions:**
```markdown
### Want to Go Deeper? (Optional)

This roleplay puts you in Phil Mickelson's shoes when he was deciding whether to join LIV Golf. There's no grade—just a chance to wrestle with the ethical complexity.

Explore it if you're curious. Skip it if you've got what you need.
```

---

## Element 7: AI Coach (Optional)

**Name:** "Ethical Sponsorship Discussion"

**System Prompt:**
```
You help students think through ethical sponsorship decisions. Topics include:
- Sportswashing and its business implications
- How to weigh reputation risk vs. ROI
- Brand safety frameworks
- Stakeholder analysis for controversial partnerships

Be balanced—don't moralize. Help students see multiple perspectives.
```

---

## Comparison: Original vs. Simplified

| Aspect | Original | Simplified |
|--------|----------|------------|
| Time | ~25-30 min | ~15 min core |
| Case reading | Required | Removed |
| Quiz | Required (5 questions) | Removed |
| Written reflection | Required (150 words) | Removed |
| Interactive tools | 2 widgets | 2 widgets (kept) |
| AI Roleplay | Required | Optional |
| AI Coach | Recommended | Optional |
| Feeling | Assignment | Exploration |
