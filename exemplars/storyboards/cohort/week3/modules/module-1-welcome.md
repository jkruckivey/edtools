# MODULE 1: Welcome & Learning Outcomes
**Version:** 2.0.0 | **Last Updated:** 2026-01-13

### Version 2.0.0 Changes
- **STANDARDIZED:** Module structure to match course-wide template (4 elements)
- **REMOVED:** CFL Project milestone section (moved to Module 7)
- **REMOVED:** AI Chat diagnostic, executive video, widget development plan (belong elsewhere)

**Purpose:** Orient students to Week 3, establish learning expectations
**Estimated Time:** 5-7 minutes

**Uplimit Structure:** First module in Unit 3

| Order | Element | Content/Purpose | Source | Implementation Notes |
|-------|---------|----------------|--------|---------------------|
| 1 | **ⓘ Infobox (Callout)** ⬤ Required | Display all 4 WLOs | Type directly | Blue variant, icon: ◉ |
| 2 | **▬ Text** ⬤ Required | Week 3 introduction | Type directly | Connects to Week 2 media foundations |
| 3 | **◫ Tiles** ◐ Recommended | 3 sponsorship/betting topics | Type directly | Blue variant |
| 4 | **▬ Text** ◐ Recommended | Widget intro - Learning Outcomes | Type directly | Pre-widget context |
| 5 | **⚙ iFrame Widget** ◐ Recommended | Learning Outcomes Widget | Embed `learning-outcomes-week.html` | WLO-CLO mapping |
| 6 | **▬ Text** ◐ Recommended | Widget intro - CFL Project | Type directly | Pre-widget context |
| 7 | **⚙ iFrame Widget** ◐ Recommended | CFL Project Tie-In | Embed `cfl-project-tie-in.html` | Shows project progression |
| 8 | **▬ Text** ⬤ Required | Module complete + transition | Type directly | Module 2 preview |

---

## Element 1: Week 3 Learning Outcomes

```
Title: ◉ Week 3 Learning Outcomes

By the end of this week, you will:

**WLO 3.1: Explain sponsorship as the financial backbone of sport** (Bloom's: Understand)
Describe why sponsorship revenue exceeds ticketing in most leagues and how brands evaluate partnership opportunities.

**WLO 3.2: Analyze sports betting as a new growth driver** (Bloom's: Analyze)
Evaluate betting's impact on fan engagement, media consumption, and league revenue across regulatory environments.

**WLO 3.3: Calculate how brands measure ROI in sport partnerships** (Bloom's: Apply)
Use industry frameworks to quantify sponsorship value through reach, engagement, and conversion metrics.

**WLO 3.4: Design sponsorship activations that deliver measurable value** (Bloom's: Create)
Build a sponsorship activation plan with ROI projections using real brand and property examples.

**This week focuses on CLO 3: Evaluating Sponsorship & Betting Economics**
```

---

## Element 2: Text Content

```
Sponsorship & Betting: The Growth Engines

You've explored how media rights are valued, compared linear TV vs. streaming economics, and analyzed Rogers' $5.2B NHL deal. You understand how platforms monetize sports content through subscriptions, ads, and engagement.

But media rights are only one revenue stream. This week, we shift focus to two growth engines transforming sports business: sponsorship (the financial backbone that funds leagues, teams, and athletes) and sports betting (the fastest-growing revenue opportunity in North American sports).

These aren't independent topics—they're deeply interconnected. Sports betting partnerships are becoming the most valuable sponsorship category, brands activate through betting platforms, and fan engagement drives both sponsorship value and betting revenue. By the end of this week, you'll design a sponsorship activation plan that calculates measurable ROI.
```

---

## Element 3: Tiles Content

Create 3 tiles:

**Tile 1 - Title:** "Sponsorship Economics"
**Tile 1 - Description:** "Why sponsorship exceeds ticketing revenue in most leagues. How brands evaluate partnerships and measure ROI."

**Tile 2 - Title:** "Betting Revolution"
**Tile 2 - Description:** "Sports betting as the fastest-growing revenue stream. Engagement multipliers, data monetization, and regulatory landscape."

**Tile 3 - Title:** "Activation Design"
**Tile 3 - Description:** "Moving beyond logo placement. Creating activations that deliver measurable business outcomes for sponsors."

---

## Element 4: Widget Introduction - Learning Outcomes

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
### Your Learning Path This Week

The four learning outcomes above map to specific course-level goals. This interactive visualization shows how Week 3's skills build on Weeks 1-2 (media foundations) and contribute to CLO 3: Evaluating Sponsorship & Betting Economics. You'll see the progression from understanding sponsorship fundamentals to designing activations with measurable ROI.

*Time: 2 minutes*
```

---

## Element 5: Learning Outcomes Widget

**Embed Code:**
```html
<iframe
  src="../../widgets/learning-outcomes-week.html"
  width="100%"
  height="600"
  style="border: none; border-radius: 8px;"
  title="Week 3 Learning Outcomes"
  aria-label="Interactive tool showing Week 3 learning outcomes and their connection to course goals"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 6: Widget Introduction - CFL Project

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
### Your Project This Week

You're three weeks into building a CFL expansion strategy. This tracker shows where you've been (market analysis, media strategy) and where you're going (sponsorship & betting partnerships). Week 3 represents a critical milestone: identifying revenue opportunities beyond traditional media rights.

*Time: 2 minutes*
```

---

## Element 7: CFL Project Tie-In Widget

**Embed Code:**
```html
<iframe
  src="../../widgets/cfl-project-tie-in.html"
  width="100%"
  height="500"
  style="border: none; border-radius: 8px;"
  title="CFL Expansion Project - Week 3 Milestone"
  aria-label="Interactive project tracker showing Week 3 milestone in the CFL Expansion Project"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 8: Module Complete - Transition to Module 2

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
## Module 1 Complete: You're Ready to Explore Sponsorship

You've reviewed the four Week 3 learning outcomes and understand how sponsorship and betting revenue drive modern sports business. You've also seen how this week's milestone contributes to your CFL Expansion Project.

**Up Next: Module 2** explores the sponsorship ecosystem. You'll learn why sponsorship now exceeds ticketing revenue in most leagues and how brands evaluate partnership opportunities.
```
