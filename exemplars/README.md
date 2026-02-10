# Exemplar Library

Production-quality examples for exemplar-based content generation. These files serve as the "training data" for Bitter Lesson-style agents that learn from patterns rather than explicit rules.

## Philosophy

Instead of encoding 50+ explicit rules about colors, fonts, spacing, and structure, we show agents 3-5 high-quality exemplars and let them discover the patterns implicitly.

> "The bitter lesson is based on the historical observations that AI researchers have often tried to build knowledge into their agents... but breakthrough progress eventually arrives by an opposing approach based on scaling computation by search and learning."
> — Rich Sutton, "The Bitter Lesson" (2019)

## Widget Exemplars

### calculators/ (6 files)
Interactive tools for financial/business calculations with inputs, calculations, and results.
- `sponsorship-roi-calculator.html` - ROI analysis with investment/return breakdown
- `media-rights-calculator.html` - Media deal valuation
- `audience-size-calculator.html` - Reach estimation
- `brand-risk-calculator.html` - Risk assessment scoring
- `engagement-multiplier-calculator.html` - Engagement impact
- `athlete-brand-calculator.html` - Brand value estimation

### explorers/ (5 files)
Click-to-explore visualizations with concept cards and detail panels.
- `revenue-streams-explorer.html` - 5-stream revenue breakdown with pie chart
- `betting-basics-explorer.html` - Betting concepts explanation
- `dynamic-pricing-explorer.html` - Pricing strategy visualization
- `media-rights-explorer.html` - Rights deal components
- `engagement-strategy-explorer.html` - Fan engagement tactics

### quizzes/ (5 files)
Pre-assessments with multiple-choice questions, feedback, and scoring.
- `revenue-strategy-pre-assessment.html` - Week 1 diagnostic
- `media-rights-pre-assessment.html` - Week 2 diagnostic
- `sponsorship-roi-pre-assessment.html` - Week 3 diagnostic
- `athlete-brand-pre-assessment.html` - Week 4 diagnostic
- `heritage-strategy-pre-assessment.html` - Week 5 diagnostic

### simulators/ (5 files)
Interactive decision-making tools with dynamic outcomes.
- `betting-market-simulator.html` - Betting market dynamics
- `dynamic-pricing-simulator.html` - Price optimization
- `ecosystem-cascade-simulator.html` - Ripple effect visualization
- `exclusivity-bidding-simulator.html` - Auction mechanics
- `post-career-wealth-simulator.html` - Financial planning

### infographics/ (4 files)
Static or lightly interactive visual explainers.
- `ecosystem-cascade-infographic.html` - Revenue ecosystem visual
- `learning-outcomes-week.html` - Week outcomes template
- `serena-williams-comic.html` - Case study narrative
- `week4-concept-map.html` - Concept relationships

## Storyboard Exemplars

### cohort/ (4 files)
Weekly deadline format with WLOs, peer activities, and PAIRR methodology.
- `week1-storyboard-overview.md` - Revenue fundamentals
- `week3-storyboard-overview.md` - Sponsorship & betting
- `week4-storyboard-overview.md` - Athlete branding
- `week5-storyboard-overview.md` - Heritage & innovation

### self-paced/ (0 files)
Flexible module format with MLOs and independent pacing.
*(Needs examples - create from future self-paced courses)*

## Usage

### For Exemplar-Based Agents

```markdown
1. Identify widget type needed (calculator, explorer, quiz, etc.)
2. Read 3-5 exemplars from the matching category
3. Generate new content that "matches the patterns"
4. Self-evaluate against exemplars
5. Iterate until quality score > 8/10
```

### Adding New Exemplars

Only add files that meet ALL criteria:
- [ ] Used in a live, production course
- [ ] Passed accessibility audit (WCAG 2.2 AA)
- [ ] Represents "gold standard" for its type
- [ ] Not a draft, experiment, or archived version

## Curation Log

| Date | Action | Files |
|------|--------|-------|
| 2025-02-10 | Initial population | 25 widgets, 4 storyboards |

---

*This library powers the `/build-widget-adaptive` and future exemplar-based generation commands.*
