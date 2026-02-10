# MODULE 4: Advanced Interactive Simulations (BOPPPS: Practice)
**Version:** 1.5.0 | **Last Updated:** 2026-01-13

### Version 1.5.0 Changes
- **NEW:** Added pre-widget contextual introductions for Post-Career Wealth Simulator and Athlete Decision Tree
- **NEW:** Each widget now has student-facing setup explaining purpose, what they'll discover, and time commitment
- **REMOVED:** Element 5 ("Why 78% of Athletes Go Broke") - content redundant with simulator's built-in context

**Purpose:** Apply athlete brand frameworks to complex scenarios and strategic trade-offs

**Uplimit Structure:** Fifth module in Unit 4 (Week 4)

| Order | Element | Content/Purpose | Source | Implementation Notes |
|-------|---------|----------------|--------|---------------------|
| 1 | **▬ Text** ⬤ Required | Module intro from Module 3 | Type directly | Bridge from experimentation to application |
| 2 | **⚙ iFrame Widget** ⬤ Required | **Post-Career Wealth Simulator** | Embed widget | Simulate retirement scenarios, see wealth preservation  |
| 3 | **▬ Text** ◐ Recommended | Reflection prompt | Type directly | Process insights from simulation |
| 4 | **⚙ iFrame Widget** ◐ Recommended | **Athlete Decision Tree** | Embed widget | Navigate endorsement vs. equity trade-offs |

---

## Element 1: From Theory to Practice: Complex Strategic Scenarios

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
# From Theory to Practice: Complex Strategic Scenarios

You've experimented with building athlete brand portfolios and evaluating emerging sports investments. You understand why equity beats fees and why women's sports offer superior returns.

Now it's time to apply these frameworks to the hardest problems athletes face:

- **Post-career transition:** How to preserve wealth when brand value declines 60-80% after retirement
- **Strategic trade-offs:** When to take the guaranteed $10M endorsement vs. risky $2M equity investment
- **Career-stage decisions:** Different strategies for rookies (need cash flow) vs. peak athletes (build equity) vs. retirement transition (preserve wealth)

This module features advanced simulations that force difficult decisions with incomplete information—just like real strategic planning.
```

---

## Element 2: Post-Career Wealth Simulator Widget `[v1.3.0]`

**Widget Purpose:** Simulate how different career decisions create dramatically different retirement wealth outcomes

**File:** `post-career-wealth-simulator.html`

### Pre-Widget Context (Copy to Uplimit as Text element BEFORE widget):

```markdown
## Practice: WLO 4.1 & 4.2 (Career-Stage Wealth Building)

You're about to make 30 years of financial decisions in 10 minutes.

This simulator puts you in control of an elite athlete's career—from rookie years ($2-5M salary) through peak earnings ($10-25M) to the post-career transition when income drops 60-80%. At each phase, you'll make critical decisions about lifestyle spending, savings rates, endorsement deals vs. equity investments, and wealth preservation strategy.

**The stakes are real:** 78% of NFL players are broke within 3 years of retirement. 60% of NBA players face the same fate within 5 years. These athletes earned millions—but made career decisions that destroyed their wealth. You'll see exactly how those decisions compound over decades.

**What you'll discover:**
- Which career phase has the BIGGEST impact on retirement wealth (hint: it's not what you'd expect)
- The minimum savings rate during peak years to avoid going broke
- Why Magic Johnson turned $48M in career earnings into a $1.2 billion empire—and why Allen Iverson turned $200M into bankruptcy
- How lifestyle spending choices (30% vs. 80% of income) create 10x wealth differences at age 65

**Try the preset scenarios** to see how different strategies play out:
- **Lifestyle Trap:** High spending, low investing → Broke at 45
- **Conservative Builder:** Steady savings → $334M at 65
- **Magic Johnson-style:** Equity investments → $1.2B+

*Time commitment: 10-15 minutes*
*Learning outcomes practiced: WLO 4.1 (Five revenue streams), WLO 4.2 (Owned assets vs. endorsements)*
```

---

### Widget Functionality:

**Interface:** Three career phases with strategic decisions at each stage

**Phase 1: Rookie Years (Ages 22-26)**
- Salary: $2M-5M/year
- Decisions:
  - Lifestyle spending level (frugal 30% / moderate 50% / lavish 80% of income)
  - Savings rate (0-70%)
  - Investment strategy (conservative bonds / balanced / aggressive growth)

**Phase 2: Peak Career (Ages 27-32)**
- Salary: $10M-25M/year
- Decisions:
  - Accept $10M endorsement OR invest $3M in owned business
  - Allocate windfall across 5 revenue streams
  - Risk tolerance for equity investments

**Phase 3: Retirement Transition (Ages 33-40)**
- Income declines 60-80% (no salary, endorsements expire)
- Decisions:
  - Sell businesses now or hold for growth
  - Transition to post-career ventures (media, coaching, business)
  - Draw down savings vs. let assets compound

**Output Visualization:**
- Wealth trajectory chart (ages 22-65)
- Peak net worth vs. retirement net worth
- Comparison to other simulation paths
- "Wealth Preservation Score" (0-100)

**Preset Scenarios:**
- **Lifestyle Trap:** High spending, low savings → Broke at 45
- **Conservative Builder:** Frugal living, steady investments → $50M at 65
- **Equity Maximizer:** Aggressive equity investing → $200M+ at 65 (but risky)
- **Historical Athletes:** MJ, Magic Johnson, Allen Iverson paths

**Uplimit Embed Code:**
```html
<iframe
  src="https://jkruckivey.github.io/business-of-sports-marketing/widgets/post-career-wealth-simulator.html"
  width="100%"
  height="700"
  style="border: none; border-radius: 8px;"
  title="Post-Career Wealth Simulator - See how career decisions affect retirement wealth"
  aria-label="Interactive multi-phase simulator where you make strategic decisions across rookie years, peak career, and retirement transition to see how choices affect retirement wealth at age sixty-five"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 3: Reflection Prompt

```markdown
### What Does Wealth Preservation Require?

After simulating career paths:

**1. Critical Decisions**
- Which phase had the BIGGEST impact on retirement wealth? (Rookie savings? Peak investing? Transition strategy?)
- What's the minimum savings rate during peak years to avoid going broke?
- When should athletes transition from "building wealth" to "preserving wealth"?

**2. Lifestyle vs. Wealth Trade-offs**
- How does lifestyle spending (30% vs. 80% of income) affect 40-year outcomes?
- Can athletes live lavishly AND build wealth? Or must they choose?

**3. Lessons for Your Project**
- If advising an athlete, what's your #1 recommendation?
- How does post-career planning apply to business longevity in your Anchor Project?
```

---

## Element 4: Athlete Decision Tree Widget `[v1.3.0]`

**Widget Purpose:** Interactive decision tree navigating endorsement vs. equity trade-offs

### Pre-Widget Context (Copy to Uplimit as Text element BEFORE widget):

```markdown
## Practice: WLO 4.2 (Owned Assets vs. Endorsements Strategic Trade-offs)

You're a sports agent advising an elite athlete who just received two competing offers:
- **(A)** $10 million per year to endorse Nike for three years (guaranteed $30M)
- **(B)** Invest $2 million to launch their own athletic wear brand (risky but potentially worth $100M+)

Which do you recommend?

This interactive decision tree guides you through the strategic trade-offs athletes face when choosing between guaranteed endorsement fees and risky equity investments.

Unlike the calculators that show you the math, this tool walks you through the **decision-making process** step by step. You'll answer five strategic questions about career stage, brand strength, risk tolerance, capital availability, and time horizon—then receive a personalized recommendation with 20-year wealth projections, risk assessments, and real athlete examples who followed similar paths. It's like having a strategic conversation with a financial advisor.

**What you'll discover:**
- How career stage (rookie vs. peak vs. veteran) fundamentally changes the endorsement vs. equity calculation
- Why even a conservative athlete at peak earnings should consider equity (risk is manageable when you have capital buffer)
- Strategic decision paths: When to take the guaranteed $10M endorsement vs. when to invest in owned businesses
- Real recommendations: See how LeBron, Serena, and Magic Johnson navigated similar decisions—with 20-year outcome data

*Time commitment: 10-15 minutes*
*Learning outcomes practiced: WLO 4.2 (Owned assets vs. endorsement strategy and trade-off evaluation)*
```

---

**Uplimit Embed Code:**
```html
<iframe
  src="https://jkruckivey.github.io/business-of-sports-marketing/widgets/athlete-decision-tree.html"
  width="100%"
  height="700"
  style="border: none; border-radius: 8px;"
  title="Athlete Decision Tree - Navigate endorsement vs equity strategic trade-offs"
  aria-label="Interactive decision tree where you answer five strategic questions about career stage, brand strength, and risk tolerance to receive personalized recommendations on endorsement versus equity investment decisions"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## MODULE 4 Complete - Transition to Module 5

**Key Insights:**
- Wealth preservation requires building equity DURING playing career when brand value is highest
- Lifestyle discipline (living on 30-40% of income) is non-negotiable for long-term wealth
- Post-career brand value declines 60-80% unless sustained by owned assets
- Magic Johnson's $1.2B wealth came from businesses built during career, not playing salary

**Up Next: Module 5 - Serena Williams Case Study**

You've built frameworks, experimented with simulations, and analyzed why athletes succeed or fail at wealth building. Now you'll apply everything to analyze Serena Williams' actual brand strategy:

- How she built substantial net worth far exceeding her $95M prize money
- Why she prioritized owned businesses over endorsements
- How Serena Ventures creates post-career value
- Strategic decisions you would replicate—and what you'd change

Ready to analyze a real case? Let's dive in.
