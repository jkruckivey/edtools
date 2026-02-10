# MODULE 3: Core Content - Compound Interest & Time Value of Money
**Version:** 1.0.0 | **Last Updated:** 2026-02-10

### Version 1.0.0 Changes
- **INITIAL:** First draft generated using exemplar-based approach

**Purpose:** Understand compound interest fundamentals and apply time value of money calculations (measures WLOs 3.1, 3.3)

**Uplimit Structure:** Third module in Unit 3

| Order | Element | Content/Purpose | Source | Implementation Notes |
|-------|---------|----------------|--------|---------------------|
| 1 | **▬ Text** ⬤ Required | Connecting intro from Module 2 | Type directly | Sets context for compound interest |
| 2 | **Video** ⬤ Required | The Magic of Compound Interest (2 min) | Upload MP4 | Einstein quote, exponential growth |
| 2A | **▬ Text** ⬤ Required | Widget Introduction - Compound Interest Calculator | Type directly | Structured intro |
| 3 | **Interactive Widget** ⬤ Required | Compound Interest Calculator | Embed iframe | Calculate future value, see growth |
| 4 | **▬ Text** ◐ Recommended | The Rule of 72 (150 words) | Type directly | Quick mental math for doubling |
| 4A | **▬ Text** ⬤ Required | Widget Introduction - Retirement Planner | Type directly | Structured intro |
| 5 | **Interactive Widget** ⬤ Required | Retirement Goal Planner | Embed iframe | Work backwards from retirement goal |
| 6 | **Infobox (Insight)** ◐ Recommended | Time > Money | Type directly | Yellow variant |
| 6A | **📝 Practice Quiz** ⬤ Required | Compound Interest Check (4 questions) | Configure in Uplimit | Tests core concepts |
| 7 | **▬ Text** ◐ Recommended | Inflation: The Silent Thief (150 words) | Type directly | Real vs nominal returns |
| 8 | **Table** ◐ Recommended | Investment Vehicle Comparison | Type directly | 401k, IRA, brokerage differences |
| 9 | **▬ Text** ⬤ Required | Module complete + transition | Type directly | Module 4 preview |

---

## Element 1: Why Starting Early Matters More Than Starting Big

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
**Connecting to Modules 1-2:** In Module 1, you learned why personal finance matters—the gap between financial literacy and financial outcomes. In Module 2, you explored budgeting and cash flow management. Now we tackle the most powerful concept in finance: compound interest.

Albert Einstein allegedly called compound interest "the eighth wonder of the world." Whether he said it or not, the math proves the point.

Here's the uncomfortable truth: **a 22-year-old investing $200/month will retire wealthier than a 35-year-old investing $400/month**—despite contributing half as much per month. The difference? Time. Compound interest rewards patience, not just effort.

This module teaches you the math behind that claim. By the end, you'll calculate future values, understand the Rule of 72, and see exactly why every financial advisor says "start now."
```

---

## Element 2: Instructional Video - The Magic of Compound Interest

**Video Specifications:**
- **Length:** 2 minutes
- **Topic:** "The Magic of Compound Interest"
- **Key Points:** Exponential vs. linear growth, time as multiplier, real examples
- **Accessibility:** Captions required, transcript provided

**Video Script (2 minutes):**
```
[0:00-0:15] Hook
"Would you rather have $1 million today or a penny that doubles every day for 30 days? Most people take the million. They shouldn't."

[0:15-0:45] The Penny Example
"A penny doubling daily seems trivial. Day 10: $5.12. Day 20: $5,242. But by Day 30? $5.4 million. That's compound growth—small gains multiplying on themselves until they explode. This isn't magic. It's math."

[0:45-1:15] Your Money Works the Same Way
"Your investments follow the same pattern. $10,000 at 7% becomes $20,000 in 10 years. Another 10 years? $40,000. Then $80,000. Each decade, your money doubles—but you didn't add anything. The growth generated the growth."

[1:15-1:45] Time Is the Variable
"Here's what most people miss: the rate of return matters less than time. Someone earning 7% for 40 years beats someone earning 10% for 20 years. Starting at 22 vs. 32 can mean a $500,000 difference at retirement—even with identical contributions."

[1:45-2:00] Transition
"Next, you'll use the Compound Interest Calculator to see exactly how your money grows. Input your numbers and watch the curve go exponential."
```

---

### Element 2A: Widget Introduction - Compound Interest Calculator

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
## Practice: See Your Money Grow

Now that you understand why compound interest is so powerful, let's make it personal.

### Your Challenge

You're a recent graduate deciding whether to start investing now or wait until you've paid off student loans. Your question: **How much does waiting 5 years actually cost me?** The calculator will show you the exact dollar difference.

### What You'll Practice

- Calculating future value with different contribution amounts
- Comparing scenarios (start now vs. start later)
- Understanding how return rates affect long-term outcomes
- Visualizing the exponential growth curve

### How the Calculator Works

1. **Input Your Numbers:** Initial investment, monthly contribution, time horizon, expected return
2. **See the Math:** Future value, total contributions, interest earned
3. **Visualize Growth:** Chart showing contributions vs. compound growth
4. **Get Insights:** Personalized analysis of your scenario

### Strategic Considerations

- **7% is the inflation-adjusted S&P 500 average**—use this for realistic projections
- **Monthly compounding** is standard for most investment accounts
- **Tax-advantaged accounts** (401k, IRA) let all gains compound without annual tax drag

### After the Widget

Note your future value. You'll use this in the Retirement Planner to work backwards from your goal.

*Time commitment: 5-7 minutes*
*Learning outcomes practiced: WLO 3.1, WLO 3.3*
```

---

## Element 3: Interactive Widget - Compound Interest Calculator

### ⚙ Interactive Activity: Compound Interest Calculator

**Practice: WLO 3.1 (Explain time value of money concepts)**

You're now ready to see compound interest in action with your own numbers. This calculator lets you input your starting amount, monthly contribution, time horizon, and expected return—then watch the exponential growth curve unfold.

**What you'll discover:**

- How the growth curve stays flat for years, then explodes upward (the "hockey stick")
- Why the last 10 years of a 40-year investment generate more than the first 30 combined
- The exact dollar cost of waiting 5 years to start investing
- How small increases in monthly contributions compound into massive differences

**Time commitment:** 5-7 minutes
**Learning outcomes practiced:** WLO 3.1 (Time value of money)

---

**Embed Code:**
```html
<iframe
  src="widgets/compound-interest-calculator.html"
  width="100%"
  height="700"
  style="border: none; border-radius: 8px;"
  title="Compound Interest Calculator - See how your money grows over time"
  aria-label="Interactive calculator where you input initial investment, monthly contributions, time horizon, and expected return to see future value with compound interest visualized on a growth chart"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 4: The Rule of 72 - Mental Math for Investors

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
## The Rule of 72: Quick Math for Doubling Time

You don't need a calculator for every compound interest question. The Rule of 72 gives you instant estimates.

**The formula:** 72 ÷ annual return = years to double

- At 6% return: 72 ÷ 6 = **12 years to double**
- At 8% return: 72 ÷ 8 = **9 years to double**
- At 12% return: 72 ÷ 12 = **6 years to double**

**Why this matters:** When someone offers you an investment, you can instantly estimate growth. A 4% savings account doubles in 18 years. A 10% stock portfolio doubles in 7.2 years. That's a decade difference.

**The inverse works too:** If you want to double your money in 10 years, you need 72 ÷ 10 = **7.2% annual return**.
```

---

### Element 4A: Widget Introduction - Retirement Planner

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
## Practice: Work Backwards from Your Goal

The Compound Interest Calculator showed you where your current savings will end up. Now let's flip the question: **How much do you need to save to reach your retirement goal?**

### Your Challenge

You want $1 million at age 65. You're currently 25. How much do you need to invest monthly to get there? What if you're 35? The Retirement Planner works backwards from your goal to show the required monthly contribution.

### What You'll Practice

- Setting realistic retirement targets based on lifestyle goals
- Calculating required monthly savings at different starting ages
- Understanding how employer matches accelerate progress
- Comparing different return scenarios (conservative vs. aggressive)

### How the Planner Works

1. **Set Your Goal:** Target retirement amount and age
2. **Input Your Situation:** Current age, current savings, expected return
3. **See Required Savings:** Monthly contribution needed to reach goal
4. **Test Scenarios:** What if you start 5 years later? Need 50% more? See the difference.

*Time commitment: 5-7 minutes*
*Learning outcomes practiced: WLO 3.3*
```

---

## Element 5: Interactive Widget - Retirement Goal Planner

**Embed Code:**
```html
<iframe
  src="widgets/retirement-goal-planner.html"
  width="100%"
  height="700"
  style="border: none; border-radius: 8px;"
  title="Retirement Goal Planner - Calculate required monthly savings"
  aria-label="Interactive planner where you set a retirement goal amount and age, then calculate the required monthly contribution based on current age, savings, and expected return"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 6: Infobox - Time Beats Money

**Uplimit Implementation:**
1. Select **Infobox** element (Insight variant, yellow)
2. Copy markdown below:

```markdown
Title: ▶ Key Insight: Time Beats Money

Starting at 22 with $200/month beats starting at 32 with $400/month—even though the late starter contributes twice as much per month. By age 65, the early starter has $525,000 while the late starter has $440,000. Those extra 10 years of compounding matter more than doubling contributions. This is why every financial advisor says "start now, even if it's small." The math is unforgiving: you cannot out-contribute lost time.
```

---

### Element 6A: Practice Quiz - Compound Interest Check

**Question 1: Doubling Time**

Using the Rule of 72, approximately how long does it take to double your money at 9% annual return?

A) 6 years
B) 8 years ✅
C) 12 years
D) 18 years

**Feedback (Correct):** Correct! 72 ÷ 9 = 8 years. The Rule of 72 gives you quick mental math for any return rate.

**Feedback (Incorrect):** Apply the Rule of 72: divide 72 by the return rate. 72 ÷ 9 = ?

---

**Question 2: Starting Age Impact**

Why does a 22-year-old investing $200/month typically end up wealthier than a 35-year-old investing $400/month?

A) Younger people earn higher returns
B) Compound interest has more time to work ✅
C) Inflation is lower for younger investors
D) Tax rates favor early starters

**Feedback (Correct):** Correct! The 22-year-old has 13 extra years of compounding. That additional time allows interest to earn interest repeatedly, eventually overtaking higher contributions.

**Feedback (Incorrect):** Think about what compound interest needs to work: time. More years = more compounding cycles.

---

**Question 3: Real vs. Nominal Returns**

The S&P 500 has historically returned ~10% annually. Why do financial planners often use 7% for projections?

A) They're being conservative about future performance
B) 7% accounts for inflation (real return) ✅
C) Taxes reduce returns to 7%
D) Fees average 3% annually

**Feedback (Correct):** Correct! The 10% is nominal return. After ~3% average inflation, the "real" return—what your money actually buys—is closer to 7%.

**Feedback (Incorrect):** Consider what erodes purchasing power over time. If investments grow 10% but prices rise 3%, your actual gain is...

---

**Question 4: Investment Vehicle Selection**

Which account type offers the best compound growth potential for long-term retirement savings?

A) Regular savings account (1% interest)
B) Taxable brokerage account (S&P 500 index fund)
C) Tax-advantaged 401(k) with employer match ✅
D) Cryptocurrency wallet

**Feedback (Correct):** Correct! The 401(k) combines tax-deferred growth (no annual taxes on gains) with employer matching (free money). Both accelerate compounding compared to taxable accounts.

**Feedback (Incorrect):** Consider which option gives you (1) market returns, (2) tax-deferred growth, AND (3) additional contributions you didn't earn.

---

## Element 7: Inflation - The Silent Thief

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
## Real vs. Nominal: What Your Money Actually Buys

Compound interest grows your wealth. Inflation erodes it. Understanding both is essential.

**Nominal return:** What your account statement shows (10% S&P 500 average)
**Real return:** What you can actually buy (7% after 3% inflation)

A million dollars in 1980 had the purchasing power of $3.7 million today. So when you project "$1M at retirement," ask: in today's dollars or future dollars?

**The planning rule:** Use 7% (real return) for retirement projections. This automatically adjusts for inflation, so your target represents actual purchasing power.

**The danger:** Savings accounts paying 1% while inflation runs 3% mean you're losing 2% purchasing power annually. Your balance grows, but your wealth shrinks. Cash is not a long-term investment.
```

---

## Element 8: Investment Vehicle Comparison

**Uplimit Implementation:**
1. Select **Table** element
2. Copy content below:

```
| Account Type | Tax Treatment | Contribution Limit (2024) | Best For |
|--------------|---------------|---------------------------|----------|
| **401(k)** | Pre-tax contributions, tax-deferred growth | $23,000 (+$7,500 catch-up if 50+) | Employer match, high earners |
| **Roth IRA** | After-tax contributions, tax-free growth | $7,000 (+$1,000 catch-up) | Young savers, expect higher future taxes |
| **Traditional IRA** | Pre-tax contributions, tax-deferred growth | $7,000 (+$1,000 catch-up) | No employer plan, want tax deduction now |
| **Taxable Brokerage** | After-tax, capital gains on sale | Unlimited | Already maxed retirement accounts |
| **HSA** | Pre-tax in, tax-free growth, tax-free out | $4,150 individual / $8,300 family | Triple tax advantage for medical costs |

**Priority order:** 401(k) up to match → Roth IRA → 401(k) to max → HSA → Taxable brokerage
```

---

## Element 9: Module Complete - Transition to Module 4

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
## Module 3 Complete: Compound Interest Mastered

You now understand the most powerful concept in personal finance. Compound interest rewards time over money—starting early matters more than starting big. The Rule of 72 gives you instant mental math for doubling time, and you've seen exactly how different scenarios play out in the calculators.

**Key Insights:**
- Time beats money: 10 extra years of compounding > doubling contributions
- Use 7% for projections (real return after inflation)
- Tax-advantaged accounts accelerate compounding (no annual tax drag)
- The Rule of 72: divide 72 by return rate to estimate doubling time

**Up Next: Module 4 - Debt Management & Optimization**

You've learned how to grow wealth. Now learn how to destroy the enemy of wealth: high-interest debt. Module 4 covers the debt avalanche vs. snowball methods, when to invest vs. pay off loans, and how to optimize your debt payoff strategy.

Ready to tackle debt strategically? Let's dive in.
```
