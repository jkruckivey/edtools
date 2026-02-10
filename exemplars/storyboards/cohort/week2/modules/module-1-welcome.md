# MODULE 1: Welcome & Learning Outcomes
**Version:** 2.0.0 | **Last Updated:** 2026-01-13

### Version 2.0.0 Changes
- **STANDARDIZED:** Module structure to match course-wide template (4 elements)
- **REMOVED:** CFL Project milestone section (moved to Module 7)
- **REMOVED:** Extra design rationale and details sections

**Purpose:** Orient students to Week 2, establish learning expectations
**Estimated Time:** 5-7 minutes

**Uplimit Structure:** First module in Unit 2

| Order | Element | Content/Purpose | Source | Implementation Notes |
|-------|---------|----------------|--------|---------------------|
| 1 | **ⓘ Infobox (Callout)** ⬤ Required | Display all 4 WLOs | Type directly | Blue variant, icon: ◉ |
| 2 | **▬ Text** ⬤ Required | Week 2 introduction | Type directly | Connects to Week 1 revenue foundations |
| 3 | **◫ Tiles** ◐ Recommended | 3 media strategy topics | Type directly | Blue variant |
| 4 | **⚙ iFrame Widget** ◐ Recommended | Learning Outcomes Widget | Embed `learning-outcomes-week.html` | WLO-CLO mapping |
| 5 | **⚙ iFrame Widget** ◐ Recommended | CFL Project Tie-In | Embed `cfl-project-tie-in.html` | Shows project progression, Week 2 highlighted |

---

## Element 1: Infobox Content

```
Title: ◉ Week 2 Learning Outcomes

By the end of this week, you will:

**WLO 2.1: Explain how media rights deals are valued and monetized** (Bloom's: Understand)
Describe the frameworks broadcasters and streaming platforms use to price sports content, including audience reach, exclusivity value, and subscription/advertising revenue potential.

**WLO 2.2: Compare linear broadcasting to streaming/DTC models** (Bloom's: Analyze)
Contrast traditional broadcasting economics (advertising-driven, mass audience) with direct-to-consumer streaming models (subscription-driven, targeted engagement) and assess trade-offs for leagues and media companies.

**WLO 2.3: Describe fan engagement monetization strategies** (Bloom's: Understand)
Identify how platforms extend value beyond passive viewing through interactive features, betting integration, social engagement, and multi-platform distribution.

**WLO 2.4: Evaluate the Rogers $5.2B NHL deal and its implications** (Bloom's: Evaluate)
Analyze Rogers Communications' 12-year NHL rights acquisition, assess its strategic outcomes, and determine lessons for future media rights negotiations.

**This week focuses on CLO 2: Evaluating Media & Fan Monetization**
```

---

## Element 2: Text Content

```
Media Rights: The Billion-Dollar Core Product

In Week 1, you learned that media rights typically represent 40–60% of total revenue for major professional leagues, varying by sport. This week, we examine WHY sports content commands such premium valuations and HOW rights deals are structured, negotiated, and monetized.

Sports remain the last "appointment viewing" in an era of on-demand entertainment. Live games can't be spoiled by social media or watched later without losing cultural currency. This unique characteristic makes sports the most valuable programming for traditional broadcasters defending against cord-cutting—and the most expensive content for streaming platforms trying to acquire subscribers.

You'll analyze the Rogers Communications / NHL deal: $5.2 billion over 12 years for exclusive Canadian rights. Was it worth it? How do you value something this complex? What did Rogers get wrong—and what did they get right? By week's end, you'll understand media economics well enough to evaluate mega-deals yourself.
```

---

## Element 3: Tiles Content

Create 3 tiles:

**Tile 1 - Title:** "Media Rights Valuation"
**Tile 1 - Description:** "How broadcasters and streamers price sports content. Learn the frameworks behind billion-dollar deals."

**Tile 2 - Title:** "Linear vs. Streaming"
**Tile 2 - Description:** "Traditional broadcasting vs. direct-to-consumer platforms. Economics, trade-offs, and strategic implications."

**Tile 3 - Title:** "Fan Engagement Monetization"
**Tile 3 - Description:** "Beyond passive viewing: how engagement drives advertising, subscription, and sponsorship value."

---

## Element 4: Learning Outcomes Widget

**Widget Purpose:** Interactive visualization showing how Week 2's learning outcomes connect to course-level goals

**Embed Code:**
```html
<iframe
  src="../../widgets/learning-outcomes-week.html"
  width="100%"
  height="600"
  style="border: none; border-radius: 8px;"
  title="Week 2 Learning Outcomes"
  aria-label="Interactive tool showing Week 2 learning outcomes and their connection to course goals"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 5: CFL Project Tie-In Widget

**Widget Purpose:** Orient students to this week's milestone in the course-long CFL Expansion Project

**Embed Code:**
```html
<iframe
  src="../../widgets/cfl-project-tie-in.html"
  width="100%"
  height="500"
  style="border: none; border-radius: 8px;"
  title="CFL Expansion Project - Week 2 Milestone"
  aria-label="Interactive project tracker showing Week 2 milestone in the CFL Expansion Project"
  allowfullscreen
  loading="lazy">
</iframe>
```

**Widget Features:**
- Shows 5-week milestone progression with Week 2 highlighted (Week 1 marked complete)
- "This Week" section explains the media strategy milestone
- Links milestone to week's learning content
