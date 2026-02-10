## MODULE 4: Interactive Activity - Streaming Wars Strategy
**Version:** 1.5.0 | **Last Updated:** 2026-01-26

### Version 1.5.0 Changes
- **MODIFIED:** Widget simplified from 20-quarter simulation to Setup → Auto-simulate → Results flow
- **MODIFIED:** Element 2A and 3A updated for simplified widget
- **MODIFIED:** Time estimate reduced from 30-45 min to 10-15 min

### Version 1.4.0 Changes
- **ADDED:** Tooltip system for jargon (VOD, baseline context) for Maria persona
- **ADDED:** Summary dashboard showing all decisions before export
- **ADDED:** Restart functionality to replay simulation
- **FIXED:** Deprecated `onkeypress` → `keydown` for keyboard navigation
- **ENHANCED:** ARIA labels on progress tracker dots with completion status
- **ADDED:** Element 3A - Tool Instructions (expandable help for simulator)

**Purpose:** Active learning - simulate platform strategy decisions (supports WLO 2.2 - Application/Analysis level)

**Uplimit Structure:** Fourth module in Unit 2

| Order | Element | Content/Purpose | Source | Implementation Notes |
|-------|---------|----------------|--------|---------------------|
| 1 | **Text** ⬤ Required | Connecting introduction from Module 3 | Type directly | Pattern: "You've just [previous] → Now [current]" |
| 2 | **Infobox (Callout)** ⬤ Required | Activity instructions and learning outcomes | Type directly | Blue variant, clear task |
| 2A | **Text** ⬤ Required | Widget Introduction - Streaming Wars Strategy | Type directly | Structured intro with Your Challenge, How It Works |
| 3 | **iFrame** ◐ Recommended | Streaming Wars Strategy tool | Custom tool hosted | Interactive simulation |
| 3A | **Details** ○ Optional | Tool Instructions (expandable) | Type directly | Step-by-step how to use the simulator |
| 4 | **Text** ⬤ Required | Reflection prompt | Type directly | Connect activity to WLOs |
| 6 | **AI Coach** ◐ Recommended | Your Strategy Coach for simulation decisions | Configure in Uplimit | Named: "Platform Strategy Assistant" |
| 7 | **Details** ○ Optional | Hints and strategic considerations | Type directly | Accordion for struggling students |
| 8 | **Text** ⬤ Required | Discussion Prompt #2 - Share Your Strategy | Type directly | Forum post with screenshot requirement |
| 9 | **Text** ◐ Recommended | Mental Break #3 - Prepare for Case Analysis | Type directly | Rest before Module 5 case study |
| 10 | **Text** ⬤ Required | 🎯 Final Project Connection | Type directly | Connects simulation to Week 5 capstone |
| 11 | **Text** ⬤ Required | Module 4 Complete - Transition to Module 5 | Type directly | Preview Rogers case study |

**Detailed Content Specifications:**

---

## Element 1: Connecting Introduction

# Build Your Streaming Platform: Strategy in Action

You've just explored media rights valuation, exclusivity dynamics, and platform economics through frameworks and knowledge checks in Media Rights Frameworks. Now you'll **apply these concepts** in a strategic simulation where you build a sports streaming platform from scratch.

In this module, you'll step into the role of VP of Content Strategy for a Canadian streaming platform, making the same high-stakes decisions that Rogers, DAZN, and TSN faced when building their streaming services. This hands-on experience prepares you to critically analyze the Rogers $5.2B NHL deal in The Rogers Challenge.

**Estimated Time:** 10-15 minutes (can be completed in multiple sessions)

---

## Element 2: Activity Instructions

### Infobox Content:
```
Title: ■ Activity: Streaming Wars Strategy Simulation

You are the VP of Content Strategy for a new Canadian streaming platform with one goal: build a profitable sports streaming service by acquiring rights, setting pricing, and managing subscriber growth versus content costs. You'll apply media rights valuation (WLO 2.1), compare linear and streaming economics (WLO 2.2), and balance content investment with fan engagement tactics (WLO 2.3). Choose sports properties to bid on, set subscription pricing, make quarterly decisions about rights renewal and pricing changes, then achieve profitability within 5 years while managing churn. Time: 10-15 minutes, completable in multiple sessions.
```

---

### Element 2A: Widget Introduction - Streaming Wars Strategy

**Copy this markdown directly into Uplimit:**

```markdown
# Practice: Build Your Streaming Platform

You've learned the frameworks for valuing media rights and comparing linear vs. streaming economics. Now you'll **experience these trade-offs** firsthand by configuring a Canadian sports streaming platform and seeing how your decisions play out over 5 years.

## Your Challenge

You're the VP of Content Strategy for a new Canadian streaming platform with a $100M annual content budget. Your ownership group has one question: "Can we build a profitable sports streaming service?" Configure your platform—choose which rights to acquire, set exclusivity levels, and price your subscription—then see 5-year financial projections under different market scenarios.

## What You'll Practice

- Allocating a limited budget across competing sports rights
- Deciding when exclusive rights are worth the 2.5x premium
- Setting subscription pricing to balance growth against revenue per user
- Understanding how churn compounds over time
- Comparing outcomes under different market conditions (boom vs. downturn)

## How the Simulator Works

1. **Build Your Content Portfolio:** Choose from NHL Hockey ($40M), NBA Basketball ($25M), MLS/EPL Soccer ($15M), and Emerging Sports ($5M). For each, decide: Skip, Shared rights, or Exclusive (2.5x cost).
2. **Set Subscription Price:** Slide between $9.99/month (mass market) and $29.99/month (premium). See real-time preview of expected churn and market position.
3. **Launch & See Results:** Click "Launch Platform" to see 5-year projections including subscribers, cumulative profit/loss, and break-even timing.
4. **Compare Scenarios:** Toggle between Base Case, Streaming Boom, and Market Downturn to see how your strategy performs under different conditions.

## Strategic Considerations

- **Content costs are fixed, subscribers are variable:** You pay $40M/year for hockey rights whether you have 100K or 1M subscribers.
- **Exclusive rights attract subscribers but drain budget:** The 2.5x premium for exclusivity is only worth it if you can convert that differentiation into subscriber growth.
- **Churn compounds relentlessly:** 5% monthly churn loses 46% of subscribers annually. Content quality and pricing both affect churn.
- **Scenario planning matters:** A strategy that thrives in a streaming boom may collapse in a downturn. Test your assumptions.

## After the Simulator

Export your results and compare strategies with classmates. You'll reference this experience when analyzing Rogers' $5.2B NHL deal in The Rogers Challenge (Module 5).
```

---

## Element 3: Streaming Wars Strategy Tool

### ⚙ Interactive Activity: Streaming Wars Strategy

**Practice: WLO 2.2 (Compare linear broadcasting to streaming economics) + WLO 2.1 (Explore media rights valuation) + WLO 2.3 (Assess fan engagement monetization)**

You've learned the frameworks for valuing media rights and comparing linear vs. streaming economics in Media Rights Frameworks. Now you'll **experience these trade-offs** firsthand by building and managing a Canadian sports streaming platform from scratch.

As VP of Content Strategy, you'll make the same high-stakes decisions that Rogers, DAZN, and TSN executives face: Which leagues should you bid on? Hockey is expensive but popular ($40M/year). Soccer has growth potential but lower current demand ($15M/year). Emerging sports are cheap but risky ($5M/year). Price too high ($29.99/month) and subscribers won't sign up. Price too low ($9.99/month) and you'll never cover content costs. Invest heavily in content to attract subscribers or grow slowly and miss the market window? Streaming platforms typically lose money for 3-5 years—can you achieve profitability?

**What you'll discover:**

- Why content costs create massive downside risk (you pay regardless of subscriber count)
- How subscriber churn forces constant growth to maintain revenue (10% monthly cancellation is industry average)
- The 3-5 year break-even timeline for streaming (very different from linear TV's immediate ROI)
- Strategic trade-offs between exclusive rights (2-3× cost) versus non-exclusive broader portfolios
- How dynamic pricing (recall Al Dark's "checking account to portfolio management" insight from Inside the Media Business) applies to streaming subscriptions

**Connecting to the Fan Engagement Framework:**
Remember the fan engagement value chain from Media Rights Frameworks (passive viewer → engaged fan → super-fan)? In this simulation, you'll invest in engagement tactics that move subscribers up that chain—betting integration, fantasy features, social communities—to reduce churn and increase lifetime value.

**Time commitment:** 10-15 minutes (can be completed in multiple sessions)
**Learning outcomes practiced:** WLO 2.2 (Compare linear vs. streaming economics), WLO 2.1 (Media rights valuation with budget constraints), WLO 2.3 (Balance content investment with fan engagement)

---

**🎮 Tool Purpose:** Simulate streaming platform strategy decisions to understand trade-offs between content costs, pricing, and subscriber growth through hands-on experience.

**Status:** ✅ Phase 2 tool - BUILT AND READY

**How It Works:**

**Inputs:**
- Rights acquisition budget ($0-$100M/year across hockey, basketball, soccer, emerging sports)
- Subscription pricing ($9.99 - $29.99/month)
- Quarterly decisions: Renew rights? Adjust pricing? Invest in engagement features?

**Outputs:**
- Subscriber count (0-1M potential)
- Monthly churn rate (5%-20%)
- Monthly recurring revenue (MRR)
- Total content costs
- Profitability timeline (years to break even)

**Scenarios:**
- Competitor launches (pricing pressure)
- Recession hits (churn increases)
- Star player trade (subscriber spike)
- Playoff runs (retention boost)

**Real Examples:**
- Rogers Sportsnet NOW ($27.99/month, NHL exclusive)
- DAZN Canada ($24.99/month, multi-sport)
- TSN Direct ($19.99/month, TSN content)

**Learning:** Balance content investment vs. subscriber growth, understand 3-5 year payback timelines, experience streaming economics firsthand. Prepares students to analyze Rogers' $5.2B NHL deal in The Rogers Challenge.

**Uplimit Implementation:**

```html
<iframe
  src="https://jkruckivey.github.io/business-of-sports-marketing/modules/week2/widgets/streaming-wars-strategy.html"
  width="100%"
  height="700"
  style="border: none; border-radius: 8px;"
  title="Streaming Wars Strategy - Build a profitable sports streaming service"
  aria-label="Interactive strategy builder where you design a sports streaming service by choosing content, pricing, and distribution models"
  allowfullscreen
  loading="lazy">
</iframe>
```

**Accessibility:**
- ✅ Keyboard navigation functional (Tab, Arrow keys, Enter) - fixed deprecated `onkeypress`
- ✅ ARIA labels on all sliders and controls
- ✅ Progress tracker with role="status" and per-dot aria-labels (current/completed status)
- ✅ Screen reader announcements for quarterly results
- ✅ High contrast mode support
- ✅ Color-blind safe visualization (blue, orange, gray palette)
- ✅ Focus indicators on all interactive elements

**Features (v1.4.0):**
- Tooltip system: Hover/focus on underlined terms (VOD, baseline) for definitions
- Summary dashboard: Review all decisions before exporting
- Restart button: Replay simulation with different strategy
- Export button: "Download Summary (TXT)" for portfolio documentation

---

### Element 3A: Details - Tool Instructions (Expandable)

**Details Element Title:** `Need help? How to use this simulator`

```
This simulator lets you configure a streaming platform and see 5-year financial projections — the same strategic planning real executives at DAZN, Rogers, and Apple perform.

**Step 1: Build Your Content Portfolio**

Choose which sports rights to acquire from your $100M annual budget:
- **NHL Hockey** ($40M base / $100M exclusive) — Highest appeal, strongest churn reduction
- **NBA Basketball** ($25M base / $62.5M exclusive) — Strong appeal, good retention
- **MLS/EPL Soccer** ($15M base / $37.5M exclusive) — Moderate appeal, decent value
- **Emerging Sports** ($5M base / $12.5M exclusive) — Lower appeal but cheap differentiation

For each property, choose: **Skip** (don't acquire), **Shared** (base cost), or **Exclusive** (2.5x cost but only you have it).

**Step 2: Set Your Subscription Price**

Slide between $9.99/month (mass market) and $29.99/month (premium):
- Lower prices → More subscribers, lower churn, but less revenue per sub
- Higher prices → Fewer subscribers, higher churn, but more revenue per sub

Watch the "Strategy Preview" panel to see how your choices affect content appeal, expected churn, and market positioning.

**Step 3: Launch & Analyze Results**

Click "Launch Platform" to see 5-year projections. Toggle between scenarios:
- **Base Case:** Normal market conditions
- **Streaming Boom:** Cord-cutting accelerates, subscriber growth surges
- **Market Downturn:** Economic pressure increases churn, slows growth

Review metrics: Year 5 Subscribers, Cumulative Profit/Loss, Break-Even Year, Final Churn Rate.

**What to notice:**
- Exclusive rights cost 2.5x more — is the differentiation worth it?
- High content costs are fixed; you pay the same whether you have 100K or 1M subscribers
- Churn compounds: 5% monthly = 46% annual subscriber loss
- The same strategy performs very differently in boom vs. downturn scenarios

**Key insight:** There's no single "right" answer. The goal is to understand trade-offs and how market conditions affect outcomes.
```

---

## Element 4: Reflection Prompt

### Text Content (Reflection Prompt):
```
After completing the Streaming Wars Strategy simulation:

Strategic Reflection Questions:
• What was your path to profitability? How many years did it take?
• Which sports properties delivered the best ROI? Which were too expensive?
• How did you balance content costs vs. subscriber acquisition?
• What surprised you about the economics of streaming vs. expectations?

This simulation prepares you to analyze the Rogers/NHL deal in The Rogers Challenge. Rogers
essentially made these same strategic decisions—but with $5.2 billion at stake.
Consider: Would you have made the Rogers deal using the insights from this simulation?
```

---

## Element 5: AI Coach - Platform Strategy Assistant

### AI Coach Configuration:
- **Name:** "Platform Strategy Assistant"
- **System Prompt:** "You are a helpful strategy advisor for MBA students learning about streaming platform economics. Provide guidance for the Streaming Wars Strategy simulation. Don't give direct answers, but ask Socratic questions to help students think through their platform strategy decisions. Focus on: content portfolio diversification, subscriber lifetime value, churn management, pricing psychology, and rights cost vs. subscriber growth trade-offs."
- **Welcome Message:** "Working through your platform strategy? I can help you think through your rights acquisition and pricing decisions. What aspect of your strategy are you considering?"
- **Show System Prompt:** No

---

## Element 6: Strategic Considerations (Hints)

### Details Content:
```
Title: ◆ Strategic Considerations (Open if you're stuck)

Not sure how to approach this simulation? Here are some frameworks:

**Customer Lifetime Value (LTV):**
How long will subscribers stay? If average subscriber stays 18 months at $19.99/month,
their LTV is ~$360. How much can you spend to acquire them? How much on content to
retain them?

**Content Portfolio Strategy:**
• Anchor Properties: High-cost, broad appeal (e.g., NHL, NBA) - drive subscriptions
• Niche Properties: Lower-cost, targeted appeal (e.g., esports, rugby) - reduce churn
• Emerging Properties: Speculative bets (e.g., women's sports, new leagues) - differentiation

**The Streaming Profitability Paradox:**
Growth requires spending on content AND customer acquisition. Profitability requires
reducing both. Most streaming services lose money for 3-5 years building scale.

**Pricing Strategy:**
• Too low: Can't cover content costs, perceived as low-quality
• Too high: Small addressable market, high churn risk
• Sweet spot: Premium enough to signal quality, accessible enough for mass market

**Rights Negotiation:**
• Exclusive rights cost 2-3x more than non-exclusive
• Multi-year deals lock in costs but reduce flexibility
• Regional rights (Canada-only) cheaper than global but smaller audience

**Engagement Investments:**
Beyond just streaming games, consider: interactive features, fantasy integration,
social viewing, original content (documentaries, shoulder programming).
These reduce churn but add costs.

**Key Question:**
What is your differentiation? Why do subscribers choose YOU over competitors?
```

**Design Rationale:**
- **iFrame tool** provides experiential learning of complex economics (UDL engagement, Application level)
- **Infobox** clearly frames task and connects to WLOs (QM clarity)
- **Reflection prompt** encourages metacognition and case study preparation (transfer)
- **AI Chat** offers adaptive support for struggling students (UDL scaffolding)
- **Details** provides strategic frameworks without prescribing answers (progressive disclosure)
- Multiple paths to profitability - no single "right" strategy (UDL choice)
- Directly prepares students to evaluate Rogers deal critically (WLO 2.4)

---

## Element 7: Discussion Prompt - Share Your Strategy

## 💬 REFLECTION PROMPT #2: Share Your Streaming Wars Strategy

**Submit Reflection** (⬤ Required - 5 points)

**Prompt:**
Reflect on your Streaming Wars simulation results. Did you achieve profitability? What key decisions led to your outcome?

**Requirements:**
- **Screenshot:** Upload an image of your final simulation dashboard (profitability timeline, subscriber count, etc.)
- **Reflection:** 75 words minimum explaining your strategy, what worked, what didn't, and what you learned
- **Deadline:** Before starting The Rogers Challenge case study

**Example Response:**
"[Screenshot attached] I achieved profitability in Year 4 by [strategy]. My biggest lesson was [insight]. If I could replay, I would [alternative approach] because [reasoning]."

**Why This Matters:**
Articulating your strategy reveals your understanding of how different approaches to rights acquisition, pricing, and engagement affect profitability—directly preparing you to evaluate Rogers' actual decisions in the case study.

**Grading:** 5 participation points (included in Week 2's 40% weekly engagement grade)
- 5 points: Screenshot + thoughtful 75-word reflection with strategic insight

---

## Element 8: Mental Break - Prepare for Case Analysis

## 🌟 MENTAL BREAK #3: Prepare for Case Analysis

**You've completed:** Framework learning + strategic simulation
**Coming next:** Rogers $5.2B NHL case study (23-25 minutes)

**Take a moment to:**
- Stand and do 5 shoulder rolls backward, 5 forward
- Get fresh water or coffee
- Step outside for 60 seconds if possible (fresh air resets focus)

**Progress:** You're 70% through Week 2 content! The simulation showed you platform strategy in action. Now you'll analyze a real mega-deal to see where theory meets reality. This case has 4 interactive data tools—it's fascinating but dense.

*This is your most important break. The case study requires critical thinking and synthesis. Take 3-5 minutes to truly reset before diving into the Rogers deal.*

---


## Streaming Wars Simulation Complete - Transition to The Rogers Challenge

**Simulation Complete!** You've simulated the strategic decisions that media companies face when building streaming platforms. You experienced firsthand the tension between content costs, pricing, and subscriber growth—the same calculus that shaped Rogers' $5.2 billion NHL deal.

**Key Insights from Your Simulation:**
- Streaming profitability requires 3-5 year horizons (not immediate ROI like linear TV)
- Content portfolio balance matters (anchor properties + niche content for retention)
- Pricing psychology affects both acquisition and churn

---
