# MODULE 7: Wrap-Up & Anchor Project Milestone 4
**Version:** 2.4.0 | **Last Updated:** 2026-02-05

### Version 2.4.0 Changes
- **ADDED:** Team Brand Package as required component per SME feedback (connects to Brand Package Creator widget)
- **REDISTRIBUTED:** Rubric points (still 20 pts total)
- **UPDATED:** Widget now required, not recommended

### Version 2.3.0 Changes
- **ADDED:** Founding Sponsor Partner as required component (connects to Week 3 sponsorship content)
- **RENAMED:** "Ambassador Strategy" → "Athlete Ambassador Strategy" for clarity
- **REDISTRIBUTED:** Rubric points to accommodate new sponsor partner criterion (still 20 pts total)

### Version 2.2.0 Changes
- **ADDED:** Element 6 - Recommended Readings (Serena Williams Brand Strategy)

### Version 2.1.0 Changes
- **NEW:** Element 2A - Brand Package Creator widget with bridging framing (connects athlete branding content to team brand design)

### Version 2.0.0 Changes
- **STANDARDIZED:** Minimal exit structure (Key Takeaways + Milestone + What's Next)
- **REMOVED:** Concept map widget, reflection prompts, detailed instructions, optional resources, AI chat
- **CONSOLIDATED:** Week 5 preview into single "What's Next" infobox

**Purpose:** Complete CFL Expansion Milestone 4, transition to Week 5

**Uplimit Structure:** Final module in Unit 4

| Order | Element | Content/Purpose | Source | Implementation Notes |
|-------|---------|----------------|--------|---------------------|
| 1 | **ⓘ Infobox (Callout)** ⬤ Required | Week 4 key takeaways | Type directly | 5 critical insights |
| 2 | **▬ Text** ⬤ Required | Anchor Project Milestone 4 Introduction | Type directly | Sets context for milestone |
| 2A | **▬ Text** ⬤ Required | Widget Introduction - Brand Package Creator | Type directly | Structured intro |
| 2B | **⚙ iFrame** ⬤ Required | Brand Package Creator widget | Embed widget | Interactive brand builder, export required for submission |
| 3 | **ⓘ Infobox (Assessment)** ⬤ Required | Milestone 4 Brief | Type directly | Purple variant, 20 points |
| 4 | **📤 File Response** ⬤ Required | Milestone 4 Submission | Configure in Uplimit | File upload |
| 5 | **ⓘ Infobox (Next Steps)** ⬤ Required | What's Next | Type directly | Green variant, transition to Week 5 |
| 6 | **⊞ Details** ◐ Recommended | Recommended Readings | Type directly | Accordion, external industry sources |

---

## Element 1: Infobox Content

```
Title: ◉ Week 4 Key Takeaways

You've completed your deep dive into athlete brands and emerging sports! The five critical insights: (1) athletes build wealth through five revenue streams—endorsements, owned businesses, investments, media/content, and licensing—not just prize money, (2) equity compounds while fees don't, making owned assets dramatically more valuable than endorsement deals over time, (3) women's sports and emerging markets offer first-mover opportunities with 300%+ growth rates versus established leagues, (4) post-career planning must happen during playing career when brand value is highest—78% of NFL players go broke because they didn't build equity, and (5) the Serena Williams playbook (30% endorsements / 70% equity) creates generational wealth that endorsement-heavy portfolios cannot match. This foundation prepares you for Week 5's focus on legacy properties, cultural impact, and the future of sports business—plus your final capstone presentation. Well done!

**Up Next:** CFL Expansion Milestone 4, then Week 5 preview.
```

---

## Element 2: Anchor Project Milestone 4 Introduction

**Uplimit Implementation:**
1. Select **Text** element
2. Copy markdown below:

```markdown
## CFL Expansion Project: Milestone 4 - Brand, Sponsor, Ambassador & Launch Strategy

Your CFL expansion franchise needs a compelling brand identity, a founding sponsor partner, and athlete ambassadors to build credibility before the first game. In Milestones 1-3, you analyzed the market, designed media strategy, and built a sponsorship portfolio. Now you'll design your team brand, identify your primary sponsor, recruit athlete ambassadors, and create a launch campaign.

**Your Challenge:** Design your team's brand identity, identify a founding sponsor partner, build an athlete ambassador strategy, and create a launch campaign for your CFL expansion team.

**Why This Matters:** New franchises lack the 50-year history that established teams use to build fan loyalty. A strong brand identity attracts sponsors and ambassadors. A credible founding sponsor signals market viability. Athlete ambassadors accelerate brand building by lending their personal brands to your new franchise.

**Apply Week 3 & 4 Frameworks:**
- Design a team brand that resonates with your market (use the Brand Package Creator below)
- Identify a founding sponsor partner that fits your market (Week 3 sponsorship frameworks)
- Select athlete ambassadors (current/former CFL players, local athletes, community figures)
- Apply the owned vs. endorsed analysis to your ambassador strategy
- Consider how women's sports athletes might open new fan segments
- Design a launch campaign that builds buzz before the first game
```

---

### Element 2A: Widget Introduction - Brand Package Creator

**Copy this markdown directly into Uplimit:**

```markdown
# Practice: Design Your CFL Franchise Brand

You've learned that athletes like Serena Williams carefully protect and grow their personal brands. They don't partner with just anyone—they choose brands that align with their values and amplify their image. Now flip the perspective: **What kind of team brand would attract the athletes YOU want as ambassadors?**

## Your Challenge

You're the Chief Marketing Officer for your CFL expansion franchise. Before recruiting brand ambassadors, you need a compelling team identity. Design a brand package that will attract top athletes, resonate with local fans, and appeal to sponsors. Your brand choices will directly influence which ambassadors want to partner with you.

## What You'll Practice

- Creating a team name that reflects your market's identity and culture
- Selecting primary and secondary colors that work on jerseys AND in sponsor materials
- Designing a mascot concept that could become a beloved local icon
- Building a cohesive brand identity that attracts athlete ambassadors

## How the Brand Package Creator Works

1. **Enter Team Name:** Choose a name that reflects your expansion city (Halifax Schooners? Quebec Voyageurs? Saskatoon Rush?)
2. **Select Colors:** Pick primary and secondary colors using the color picker—see hex values for sponsor consistency
3. **Design Jersey Mockup:** Watch your colors appear on a jersey template in real-time
4. **Create Mascot Concept:** Describe your mascot character and its connection to local culture
5. **Export Brand Package:** Download a text file with all your brand specifications

## Strategic Considerations

- **Name should resonate locally:** The best team names connect to regional identity (Roughriders = prairie toughness, Argonauts = Toronto's maritime history)
- **Colors matter for merchandise:** High-contrast combinations sell better. Avoid colors that clash with major local competitors.
- **Mascot = content engine:** A great mascot creates social media content, youth program opportunities, and sponsor activation options
- **Think about athlete fit:** Would Serena Williams want to be associated with your brand? Would local CFL stars be proud to represent it?

## After the Widget

**Export your brand package and paste it at the TOP of your Milestone 4 submission as a header.** Add 2-3 sentences explaining why these brand choices fit your market. This header doesn't count toward the 2-3 page limit—it's your brand identity summary that frames the rest of your strategy.

*Example rationale: "The Schooners name honors Halifax's shipbuilding heritage. Deep navy and gold evoke maritime tradition while differentiating from the Argonauts' lighter blue."*
```

---

### Element 2B: iFrame Widget - Brand Package Creator

**File:** `brand-package-creator.html`

```html
<iframe
  src="https://jkruckivey.github.io/business-of-sports-marketing/modules/week4/widgets/brand-package-creator.html"
  width="100%"
  height="800"
  style="border: none; border-radius: 8px;"
  title="CFL Brand Package Creator - Design your expansion team's identity"
  aria-label="Interactive brand builder where you design your CFL expansion team's name, colors, jersey mockups, mascot, and logo concept"
  allowfullscreen
  loading="lazy">
</iframe>
```

**Accessibility:**
- ✅ Keyboard navigation functional
- ✅ Color pickers with hex value display
- ✅ Form labels on all inputs
- ✅ Export function for brand package text file

**Note:** This tool is **required** for Milestone 4. Export your brand package and include it in your submission.

---

## Element 3: Infobox - Milestone 4 Brief

**Uplimit Implementation:**
1. Select **Infobox** element
2. Choose variant: **Assessment** (purple)
3. Copy markdown below:

```markdown
Title: ▪ Anchor Project Milestone 4: Brand, Sponsor, Ambassador & Launch Strategy (20 points)

**Deliverable:** 2-3 pages plus Brand Identity Header

**Required Components:**

**HEADER (not counted in page limit):**
- **Brand Identity Summary**: Paste your Brand Package Creator export at the top of your document, followed by 2-3 sentences explaining why these choices fit your market

**BODY (2-3 pages):**
1. **Founding Sponsor Partner** (0.5 page): Identify your primary corporate sponsor (e.g., naming rights, jersey sponsor) with strategic rationale for why this brand fits your market and team
2. **Athlete Ambassador Strategy** (0.5-1 page): 2-3 target athlete ambassadors (CFL players, local athletes, community figures) with rationale, roles, and activation plans
3. **Launch Campaign Timeline** (1 page): 18-month pre-launch to first game campaign with key milestones
4. **Community Integration** (0.5 page): Youth programs, school partnerships, and local talent pipeline

**Grading Rubric (20 points):**
- Brand Identity Header (3 pts): Cohesive brand identity with brief strategic rationale
- Founding Sponsor Partner (3 pts): Strategic sponsor selection with clear fit to market and brand
- Athlete Ambassador Selection (4 pts): Strategic athlete choices with clear rationale and fit
- Launch Campaign (5 pts): Creative, feasible timeline with measurable milestones
- Community Integration (2 pts): Authentic local connections beyond transactional sponsorship
- Professional Presentation (3 pts): Clear writing, logical organization

**Due:** End of Week 4

**Connection to Final Proposal:** Milestone 4 completes your franchise strategy. Week 5 synthesizes Milestones 1-4 into your final CFL expansion proposal.
```

---

## Element 4: File Response Question - Milestone 4 Submission

**Uplimit Implementation:**
1. Select **Exercise → File Response Question**
2. Configure the following fields:

**Question:**
```
Submit your CFL Expansion Milestone 4: Brand, Sponsor, Ambassador & Launch Strategy. Your submission should be 2-3 pages plus a Brand Identity Header at the top.
```

**Additional Instructions (optional):**
```
Your submission will be evaluated using the rubric below (20 points total):

• Brand Identity Header (3 pts) - Widget export + 2-3 sentences of rationale (doesn't count toward page limit)
• Founding Sponsor Partner (3 pts) - Strategic sponsor selection with clear fit to market and brand
• Athlete Ambassador Selection (4 pts) - Strategic athlete choices with clear rationale
• Launch Campaign (5 pts) - Creative, feasible timeline with milestones
• Community Integration (2 pts) - Authentic local connections
• Professional Presentation (3 pts) - Clear writing, logical organization

FORMAT: Start your document with your Brand Package Creator export, then add 2-3 sentences explaining your choices. This header doesn't count toward the 2-3 page limit.

Accepted formats: PDF, DOCX
Filename suggestion: LastName_M4_BrandLaunchStrategy.pdf
```

**Template:** No template required

**Rubric Configuration:**

---

**CRITERION 1: Brand Identity Header**

**Points:** 3

**Description:**
Student includes Brand Package Creator export at top of document with brief strategic rationale (2-3 sentences).

**Does not meet expectations:** 0 points
No brand package included, or brand elements feel random without any rationale. Missing widget export entirely.

**Partially meets expectations:** 1.5 points
Brand package export present but rationale missing or generic. May have good name/colors without explaining why they fit the market.

**Fully meets expectations:** 3 points
Widget export included with clear, concise rationale (2-3 sentences). Team name connects to regional identity. Brief explanation of why colors/mascot fit the market and will appeal to sponsors/fans.

---

**CRITERION 2: Founding Sponsor Partner**

**Points:** 3

**Description:**
Student identifies a primary corporate sponsor with strategic rationale for why this brand fits their market and team positioning.

**Does not meet expectations:** 0 points
No sponsor identified, or selection is unrealistic (e.g., global brands unlikely to sponsor a CFL expansion team). No rationale for why this sponsor fits the market or team brand. Doesn't demonstrate understanding of Week 3 sponsorship frameworks.

**Partially meets expectations:** 1.5 points
Sponsor identified but rationale incomplete. May select an appropriate brand without explaining strategic fit. Limited connection to market characteristics from Milestone 1 or sponsorship value proposition.

**Fully meets expectations:** 3 points
Strategic sponsor selection with clear rationale. Explains why this brand fits the market (e.g., regional headquarters, target demographics, brand values alignment). Identifies specific sponsorship assets (naming rights, jersey, in-stadium). Shows understanding of Week 3 sponsorship valuation and activation frameworks.

---

**CRITERION 3: Athlete Ambassador Selection**

**Points:** 4

**Description:**
Student selects strategic athlete ambassadors with clear rationale for how they fit the market and franchise brand positioning.

**Does not meet expectations:** 0 points
Ambassador choices missing or inappropriate (e.g., selecting global superstars unrealistic for CFL budget). No rationale for selections. No connection between ambassadors and market characteristics or brand positioning.

**Partially meets expectations:** 2 points
Ambassador choices present but rationale incomplete. May select appropriate athletes without explaining strategic fit. Limited connection to market from Milestone 1 or brand identity.

**Fully meets expectations:** 4 points
Strategic athlete ambassador choices with clear rationale. Explains why these athletes fit the market and brand. Considers local connections, CFL alumni, emerging athletes, or community figures. Shows understanding of Week 4 athlete brand frameworks.

---

**CRITERION 4: Launch Campaign**

**Points:** 5

**Description:**
Student creates a feasible launch campaign timeline with clear milestones from pre-announcement through the first game.

**Does not meet expectations:** 0 points
No campaign timeline or only vague ideas. Missing key milestones. No clear path from announcement to first game. Timeline unrealistic or not feasible.

**Partially meets expectations:** 2.5 points
Campaign timeline present but incomplete. May have good ideas without clear sequencing. Some milestones identified but missing measurable outcomes. Timeline feasible but lacks creativity.

**Fully meets expectations:** 5 points
Creative, feasible 18-month timeline from pre-launch to first game. Clear milestones with measurable outcomes. Shows understanding of how to build anticipation and convert interest to ticket sales. Campaign tactics appropriate for market size and budget.

---

**CRITERION 5: Community Integration**

**Points:** 2

**Description:**
Student develops authentic community integration strategies that build long-term relationships beyond transactional sponsorship.

**Does not meet expectations:** 0 points
No community strategy or only transactional approaches ("sponsor local events"). Doesn't demonstrate understanding of how sports franchises build authentic community connections.

**Partially meets expectations:** 1 point
Community ideas present but feel generic. May list programs without explaining how they build long-term relationships. Limited connection to specific community characteristics of chosen market.

**Fully meets expectations:** 2 points
Authentic community integration beyond transactional sponsorship. Specific programs tailored to market (youth programs, school partnerships, charitable foundation). Shows how franchise becomes part of community fabric.

---

**CRITERION 6: Professional Presentation**

**Points:** 3

**Description:**
Student delivers a clear, well-organized document with professional writing and effective use of visual elements.

**Does not meet expectations:** 0 points
Document poorly organized, contains significant errors, or exceeds page limit substantially. Missing required sections or difficult to follow.

**Partially meets expectations:** 1.5 points
Meets basic requirements but writing could be clearer. Some organizational issues or minor errors. Adequate but not polished.

**Fully meets expectations:** 3 points
Clear, professional writing. Logical organization with all required sections. Appropriate length (2-3 pages). Visual elements (timeline, diagrams) used effectively. Ready for business review.

---

## Element 5: Infobox - What's Next

**Uplimit Implementation:**
1. Select **Infobox** element
2. Choose variant: **Next Steps** (green)
3. Copy markdown below:

```
Title: ✓ What's Next: Week 5

**Week 5: Legacy, Culture & The Future of Sports**

The final week brings everything together. You'll explore how heritage properties balance tradition with innovation, analyze emerging trends shaping sports business, and synthesize all four weeks into your final CFL expansion proposal.

**Core Case:** Hockey Hall of Fame: Heritage Monetization
**Focus Areas:** Legacy vs. innovation tension, future trends (AI, VR, sustainability), cultural impact, strategic synthesis

**Milestone 5 (Final Proposal):** Synthesize Milestones 1-4 into a comprehensive CFL expansion proposal for the league's Board of Governors. This is your capstone deliverable.

See you in Week 5—the home stretch!
```

---

## Element 6: Details - Recommended Readings

**Uplimit Implementation:**
1. Select **Details** element
2. Copy content below:

```
Title: 📚 Recommended Readings

**Serena Williams Brand Strategy** (Forbes/HBR case analysis)
Analysis of how Serena Williams built a $260M+ net worth with only 30% from endorsements and 70% from equity positions. Covers the owned vs. endorsed assets framework, Serena Ventures portfolio strategy, and the playbook for building generational wealth versus fee-based income.

*Focus on:* Five athlete revenue streams, equity compounding vs. endorsement fees, women's sports investment thesis, post-career transition planning.

[Link to Forbes/HBR Coverage]
```

---

## Instructor Notes

**Module 7 Purpose:**
- Consolidate Week 4 learning through key takeaways
- Complete Milestone 4 submission
- Clean transition to Week 5 capstone

**Grading Notes:**
- Ambassador choices should fit the chosen market from Milestone 1
- Launch campaign should demonstrate understanding of athlete brand value
- Community integration should feel authentic, not performative
