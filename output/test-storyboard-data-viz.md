# MODULE 3: Core Content - Data Storytelling Framework (⭐ INTERACTIVE FOCUS)
**Version:** 1.0.0 | **Last Updated:** 2026-02-10

### Version 1.0.0 Changes
- **INITIAL:** First draft generated using exemplar-based approach

**Purpose:** Learn the data storytelling framework and practice creating narrative-driven visualizations (measures WLOs 3.1, 3.3)

**Uplimit Structure:** Third module in Unit 3

| Order | Element | Content/Purpose | Source | Implementation Notes |
|-------|---------|----------------|--------|---------------------|
| 1 | **▬ Text** ⬤ Required | Connecting intro from Module 2 | Type directly | Sets context for storytelling |
| 2 | **Video** ⬤ Required | Data Storytelling 101 (2 min) | Upload MP4 | Explains narrative arc in data |
| 2A | **▬ Text** ⬤ Required | Widget Introduction - Chart Type Selector | Type directly | Structured intro |
| 3 | **Interactive Widget** ⬤ Required | Chart Type Selector | Embed iframe | Match data to visualization type |
| 4 | **▬ Text** ◐ Recommended | The Narrative Arc (150 words) | Type directly | Setup → Tension → Resolution |
| 4A | **▬ Text** ⬤ Required | Widget Introduction - Story Builder | Type directly | Structured intro |
| 5 | **Interactive Widget** ⬤ Required | Data Story Builder | Embed iframe | Construct narrative from dataset |
| 6 | **Infobox (Insight)** ◐ Recommended | The 5-Second Rule | Type directly | Yellow variant |
| 6A | **📝 Practice Quiz** ⬤ Required | Storytelling Fundamentals Check (4 questions) | Configure in Uplift | Tests narrative concepts |
| 7 | **▬ Text** ◐ Recommended | Audience Analysis Framework (150 words) | Type directly | Know your audience |
| 7A | **▬ Text** ⬤ Required | Widget Introduction - Audience Analyzer | Type directly | Structured intro |
| 8 | **Interactive Widget** ⬤ Required | Audience Analyzer | Embed iframe | Tailor message to stakeholder |
| 9 | **Table** ◐ Recommended | Chart Type Decision Matrix | Type directly | When to use which chart |
| 9A | **📝 Practice Quiz** ⬤ Required | Chart Selection Check (3 questions) | Configure in Uplift | Tests chart-data matching |
| 10 | **Details** ○ Optional | Advanced: Animation in Data Stories | Type directly | Accordion - optional depth |

---

## Element 1: From Data to Story - The Visualization Value Proposition

**Copy this markdown directly into Uplimit:**

```markdown
**Connecting to Weeks 1-2:** In Week 1, you learned that 65% of people are visual learners—data without visualization is data without impact. In Week 2, you mastered the technical foundations: chart types, color theory, and accessibility requirements. This week, we bridge technique and communication: how do you transform accurate charts into compelling stories that drive decisions?

You've seen examples of visualizations that changed minds and moved markets. Now let's build the framework.

Data storytelling isn't decoration—it's a strategic communication discipline. The best visualizations deliver three things that raw data can't: immediate comprehension (the 5-second rule), emotional resonance (humans remember stories, not statistics), and clear action (what should the audience DO with this insight?).

This module teaches you the industry framework for constructing data narratives. By the end, you'll identify the right chart for your data, structure a narrative arc, and tailor your message to different stakeholders.
```

---

## Element 2: Instructional Video - Data Storytelling 101

**Video Specifications:**
- **Length:** 2 minutes
- **Topic:** "The Narrative Arc in Data Visualization"
- **Key Points:** Setup, tension, resolution applied to data; the 5-second test
- **Accessibility:** Captions required, transcript provided

**Video Script (2 minutes):**
```
[0:00-0:15] Hook
"The most viral chart of 2024 wasn't the prettiest—it was the one that made you feel something. That's the difference between data visualization and data storytelling."

[0:15-0:45] The Problem
"Most analysts make the same mistake: they show ALL the data. But your audience doesn't want all the data—they want the answer. Every great data story has three acts: Setup (here's the context), Tension (here's the problem or surprise), Resolution (here's what it means)."

[0:45-1:15] The 5-Second Rule
"Your visualization has 5 seconds to communicate its main point. If the audience can't grasp your message in 5 seconds, you've lost them. This doesn't mean dumbing down—it means focusing. One chart, one message. The title should state the insight, not describe the axes."

[1:15-1:45] Audience Matters
"A chart for your CEO looks different than a chart for your data team. Executives want the 'so what'—the decision it informs. Analysts want the methodology—how you got there. Same data, different stories. We'll practice tailoring in the Audience Analyzer exercise."

[1:45-2:00] Transition
"Next, you'll use the Chart Type Selector to match your data to the right visualization. Get this wrong, and no amount of storytelling can save you."
```

---

### Element 2A: Widget Introduction - Chart Type Selector

**Copy this markdown directly into Uplimit:**

```markdown
# Practice: Match Data to Visualization

Now that you understand the storytelling framework, let's start with the foundation: choosing the right chart for your data.

## Your Challenge

You're a data analyst presenting quarterly results. Your manager asks: "Should this be a bar chart or a line chart?" You need a systematic way to answer this question for ANY dataset.

## What You'll Practice

- Identifying relationship types in data (comparison, composition, distribution, relationship)
- Matching data characteristics to appropriate chart types
- Recognizing when common charts (pie, bar, line) are wrong for your data
- Applying the "chart chooser" decision framework

## How the Selector Works

1. **Describe Your Data:** Number of variables, data type (categorical, continuous, time-series), comparison goal
2. **Answer Decision Questions:** Are you showing change over time? Comparing categories? Showing parts of a whole?
3. **Get Recommendations:** Widget suggests 2-3 appropriate chart types with explanations
4. **See Examples:** Real visualizations using each recommended type

## Strategic Considerations

- **Pie charts are rarely the answer:** They're only appropriate for parts-of-whole with 2-5 categories. If you have more, use a bar chart.
- **Line charts need continuous data:** Using lines for categorical data implies false continuity
- **Bar vs. Column:** Horizontal bars are better for long category names; vertical columns are better for time comparisons

## After the Widget

Note your recommended chart type. You'll use this in the Data Story Builder to construct a complete narrative.
```

---

## Element 3: Interactive Widget - Chart Type Selector

### ⚙ Interactive Activity: Chart Type Selector

**Practice: WLO 3.1 (Select appropriate visualization for data type)**

You're now ready to use the systematic approach that data professionals use to match visualizations to data. In this interactive selector, you'll describe your dataset's characteristics and receive evidence-based chart recommendations.

**What you'll discover:**

- How data relationship type (comparison, composition, distribution, trend) determines chart family
- Why the most common choice (pie chart) is usually wrong
- When to break conventional rules for storytelling impact
- How the same data can support multiple valid visualizations depending on your message

**Time commitment:** 5-7 minutes
**Learning outcomes practiced:** WLO 3.1 (Select appropriate visualization for data type)

---

**🎮 Widget Purpose:** Guide users through chart selection decision tree based on data characteristics.

**Inputs:**
- Data relationship type: Dropdown (Comparison/Composition/Distribution/Trend)
- Number of categories: Slider 2-20
- Time component: Yes/No
- Primary message: Text field (what insight to emphasize)

**Outputs:**
- Top 3 recommended chart types with confidence scores
- Example visualization for each recommendation
- "Why this works" explanation
- "When to avoid" warnings

**Embed Code:**
```html
<iframe
  src="widgets/chart-type-selector.html"
  width="100%"
  height="600"
  style="border: none; border-radius: 8px;"
  title="Chart Type Selector - Match your data to the right visualization"
  aria-label="Interactive chart selector where you describe your data characteristics and receive recommendations for appropriate visualization types"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 4: The Narrative Arc - Setup, Tension, Resolution

**Copy this markdown directly into Uplimit:**

```markdown
## Every Data Story Has Three Acts

A common misconception: data visualization is about showing data accurately. **Wrong.**

Accurate visualization is table stakes. The goal is **communication**—changing how your audience thinks or acts. Every effective data story follows the same structure used in journalism, film, and literature:

**Act 1: Setup** (Where are we?)
Establish context. What's the baseline? What does "normal" look like? Your audience needs a reference point before they can appreciate the insight.

**Act 2: Tension** (What's surprising?)
Reveal the conflict. What changed? What's unexpected? What's at risk? This is your chart's reason for existing. If there's no tension, there's no story.

**Act 3: Resolution** (So what?)
Deliver the meaning. What should the audience conclude? What action should they take? Never leave interpretation to chance—state your insight explicitly.

**Your Data Story Builder exercise:** You'll practice constructing all three acts from a real dataset, then see how rearranging the narrative changes audience perception.
```

---

### Element 4A: Widget Introduction - Data Story Builder

**Copy this markdown directly into Uplimit:**

```markdown
# Practice: Construct a Data Narrative

You've chosen the right chart type. Now you need to wrap it in a story that lands with your audience.

## Your Challenge

You have sales data showing a concerning trend. Your task: construct a narrative that gets executive attention and drives action. Same data can be presented as "steady decline requiring intervention" or "normal seasonal variation." Your framing determines the response.

## What You'll Practice

- Writing insight-driven titles (not axis descriptions)
- Structuring the setup-tension-resolution arc
- Adding annotations that guide interpretation
- Choosing what to emphasize and what to minimize

## How the Story Builder Works

1. **Load Dataset:** Choose from 5 real-world datasets (sales, engagement, NPS, churn, conversion)
2. **Define Your Message:** What action do you want the audience to take?
3. **Build the Arc:** Write your setup (context), identify the tension (surprise), craft the resolution (recommendation)
4. **See the Result:** Widget generates a complete data story with your narrative elements
5. **Compare Framings:** Toggle between "urgent" and "reassuring" versions of the same data

## Strategic Considerations

- **Titles should state insights:** "Sales dropped 23% in Q3" not "Q3 Sales Performance"
- **Annotations beat legends:** Label directly on the chart, don't make readers decode colors
- **Highlight the tension:** Use color, size, or position to draw eyes to the key insight

## After the Widget

Export your data story. You'll present it in the Week 3 peer review activity.
```

---

## Element 5: Interactive Widget - Data Story Builder

### ⚙ Interactive Activity: Data Story Builder

**Practice: WLO 3.3 (Construct narrative-driven visualizations)**

You've chosen your chart type. Now it's time to transform that chart into a story that changes minds. This builder walks you through constructing each element of an effective data narrative—from insight-driven titles to strategic annotations.

**What you'll discover:**

- How the same data supports radically different narratives depending on framing
- Why "neutral" presentation is a myth—every choice communicates something
- The power of annotation placement in guiding audience interpretation
- How to stress-test your narrative against skeptical audiences

**Time commitment:** 10-12 minutes
**Learning outcomes practiced:** WLO 3.3 (Construct narrative-driven visualizations)

---

**Embed Code:**
```html
<iframe
  src="widgets/data-story-builder.html"
  width="100%"
  height="700"
  style="border: none; border-radius: 8px;"
  title="Data Story Builder - Construct narrative-driven visualizations"
  aria-label="Interactive story builder where you construct data narratives using setup, tension, and resolution framework with real datasets"
  allowfullscreen
  loading="lazy">
</iframe>
```

---

## Element 6: Infobox - The 5-Second Rule

```
Title: ▶ Key Insight: The 5-Second Rule

Your audience decides whether to engage with your visualization in 5 seconds. In that window, they should grasp: (1) what the chart shows, (2) why it matters, and (3) what's surprising. If your title describes axes instead of insights ("Q3 Revenue by Region"), you've wasted your 5 seconds. Insight-driven titles ("Southeast revenue collapsed 34% after competitor entry") earn attention. Test every visualization: cover the data, read only the title—does it tell the story?
```

---

### Element 6A: Practice Quiz - Storytelling Fundamentals Check

**Question 1: Narrative Arc**

A data story has three acts. Which correctly describes the "Tension" act?

A) Establishing baseline context so the audience understands normal
B) Revealing what's surprising, unexpected, or at risk ✅
C) Recommending specific actions based on the data
D) Explaining the methodology behind the analysis

**Feedback (Correct):** Correct! Tension is the conflict—the reason your visualization exists. Without something surprising or concerning, there's no story worth telling. Setup provides context, Resolution delivers meaning.

**Feedback (Incorrect):** Think about storytelling structure: Setup establishes normal, Tension disrupts it, Resolution makes sense of the disruption. Which describes the "disruption" moment?

---

**Question 2: The 5-Second Rule**

Why do effective visualizations need to communicate their main point within 5 seconds?

A) Human attention spans have decreased due to social media
B) Executives are too busy to spend more than 5 seconds on charts
C) Audiences decide whether to engage in the first 5 seconds—unclear charts get ignored ✅
D) 5 seconds is the optimal time for visual processing

**Feedback (Correct):** Correct! The 5-second window is when audiences decide "is this worth my attention?" If your main insight isn't immediately clear, they'll move on—not struggle to decode your chart.

**Feedback (Incorrect):** Consider what happens when you encounter a confusing chart. Do you invest time deciphering it, or move on? The 5-second rule reflects this reality.

---

**Question 3: Insight-Driven Titles**

Which title better follows data storytelling best practices?

A) "Monthly Active Users, January-December 2024"
B) "User growth stalled in Q3 after algorithm change" ✅
C) "MAU Trend Analysis with Seasonal Adjustment"
D) "Figure 3: User Engagement Metrics"

**Feedback (Correct):** Correct! This title states the insight (stalled growth), identifies the timing (Q3), and hints at causation (algorithm change). Readers immediately know what they're looking at and why it matters.

**Feedback (Incorrect):** Compare the titles: which one tells you something meaningful without looking at the chart? Effective titles state insights, not just describe what axes show.

---

**Question 4: Same Data, Different Stories**

You have data showing sales declined 15% year-over-year, but increased 3% quarter-over-quarter. Your CEO wants good news for the board. Which framing is ethically appropriate?

A) Only show the quarterly improvement, hide the yearly decline
B) Present both metrics with context explaining the recovery trajectory ✅
C) Use a truncated y-axis to make the quarterly gain look larger
D) Focus on a single product line that showed growth

**Feedback (Correct):** Correct! Ethical data storytelling means presenting the full picture while emphasizing genuine positives. "We're down 15% YoY but recovering—up 3% QoQ and trending toward breakeven by Q2" is honest framing.

**Feedback (Incorrect):** Data storytelling isn't about manipulation—it's about emphasis. Hiding negative data or distorting scales crosses ethical lines. How can you highlight genuine positives while acknowledging challenges?

---

## Element 9: Table - Chart Type Decision Matrix

```
Title: Chart Selection Decision Matrix

| Your Goal | Data Type | Recommended Chart | Avoid |
|-----------|-----------|-------------------|-------|
| **Compare categories** | Categorical | Bar chart (horizontal for long names) | Pie chart (>5 categories) |
| **Show trend over time** | Time-series | Line chart | Bar chart (implies discrete) |
| **Parts of a whole** | Composition | Stacked bar, treemap | Pie chart (>5 slices) |
| **Show distribution** | Continuous | Histogram, box plot | Bar chart (bins matter) |
| **Correlation** | Two variables | Scatter plot | Line chart (implies causation) |
| **Geographic patterns** | Location data | Choropleth map | Bar chart (loses spatial) |
| **Highlight single value** | KPI | Big number + sparkline | Complex chart |

**Key Takeaway:** The "right" chart depends on your message, not just your data. A trend story needs a line chart; a comparison story needs bars—even with the same underlying data.
```

---

## Module 3 Complete - Transition to Module 4

**Completion Badge:** 🏆 Data Storytelling Framework Mastered

**What You've Accomplished:**
You've learned how to select appropriate visualizations using a systematic decision framework, construct narrative arcs that engage audiences, and tailor your message for different stakeholders. You've practiced with three interactive tools that simulate real data communication challenges.

**Key Takeaways:**
- Chart selection follows data type: comparison (bars), trend (lines), composition (stacked), distribution (histogram)
- Every data story needs three acts: Setup (context), Tension (surprise), Resolution (action)
- The 5-second rule: your title and main insight must be graspable immediately
- Same data, different stories—framing determines audience response

**Up Next: Module 4 - Audience Analysis & Stakeholder Communication**
Now that you can construct data stories, let's learn how to adapt them for different audiences. An executive dashboard looks nothing like an analyst deep-dive—even with identical data. You'll practice building stakeholder personas and tailoring visualizations to their decision-making needs.

Ready to master audience adaptation? Let's dive in.
