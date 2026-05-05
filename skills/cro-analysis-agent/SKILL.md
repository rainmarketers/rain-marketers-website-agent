# CRO Analysis Agent

**Analyze conversion data and recommend optimization experiments**

Reviews monthly performance data to identify conversion bottlenecks, proposes A/B tests, and recommends quick wins to improve conversion rates across all channels.

---

## What It Does

Executes Phase 4.5 of service fulfillment: Analyzes conversion performance and produces actionable CRO (Conversion Rate Optimization) recommendations for ongoing testing and optimization.

**Input**: Monthly performance report + page-level analytics + conversion funnel data + user behavior

**Output**: CRO recommendations report, A/B test roadmap, quick-win opportunities, hypothesis-driven experiments

---

## Execution

### Stage 1: Conversion Funnel Analysis (1 day)
- **Map the funnel**:
  - Awareness stage (traffic sources, landing pages)
  - Interest stage (page views, time on page, scroll depth)
  - Consideration stage (form starts, demo requests)
  - Decision stage (form completions, conversions)

- **Identify bottlenecks**:
  - Where are we losing visitors? (highest drop-off rate)
  - Which pages have high traffic but low conversion? (optimization opportunity)
  - Which sources have high intent but low conversion? (audience mismatch or messaging)
  - Which forms have high abandonment? (friction analysis)

**Output**: Funnel analysis with drop-off rates by stage

### Stage 2: Page-Level CRO Analysis (1 day)
- **High-traffic, low-conversion pages**:
  - Why visitors arrive (what promise drew them?)
  - Why they're not converting (what's the objection?)
  - What's missing (proof, specificity, urgency, simplicity?)

- **Landing page assessment**:
  - Headline match with ad/search query
  - Subheadline clarity and offer specificity
  - Form friction (number of fields, required fields)
  - CTA clarity and prominence
  - Social proof visibility
  - Objection handling presence

- **Conversion page assessment**:
  - Clear value proposition
  - Trust signals (logos, testimonials, credentials)
  - Specificity of offer (vague vs specific)
  - Urgency/scarcity elements
  - Risk reversal (guarantee, guarantee, etc.)

**Output**: Page-by-page assessment with friction points identified

### Stage 3: A/B Test Prioritization (1 day)
- **Identify high-impact test opportunities**:
  - High-traffic pages (test reaches many visitors)
  - High-intent pages (visitors ready to convert)
  - Low-converting pages (biggest opportunity for improvement)

- **Propose specific tests**:
  - Headline variations (benefit-focused vs social proof vs urgency)
  - CTA button variations (text, color, placement)
  - Form optimization (field count, field order, single vs multi-step)
  - Social proof variations (testimonials, stats, logos)
  - Offer variations (price, terms, guarantee)

- **Rank by impact potential**:
  - High priority: High traffic + Low conversion + Easy to test
  - Medium priority: Medium traffic + Medium conversion + Moderate effort
  - Low priority: Low traffic + Low impact + High effort

**Output**: Prioritized A/B test roadmap with hypotheses

### Stage 4: Quick Wins & Recommendations (1 day)
- **Identify quick wins** (low effort, high impact):
  - Remove friction from forms (reduce fields)
  - Clarify CTAs (make action button more prominent)
  - Add social proof (add testimonials or stats)
  - Simplify headlines (be more specific)
  - Add urgency/scarcity (limited spots, time-limited)

- **Analyze user behavior data**:
  - Session recordings (where do visitors scroll? what do they click?)
  - Form analytics (which fields get abandoned? where do people drop off?)
  - Event tracking (what actions matter most?)

- **Provide copywriting recommendations**:
  - Headline clarity (too vague → too specific)
  - Benefit focus (features → benefits)
  - Proof strength (weak → strong)
  - CTA clarity (passive → active)

**Output**: Recommendation report with estimated impact per change

---

## Input Format

```json
{
  "monthly_report": {
    "period": "January 2026",
    "total_conversions": 0,
    "total_revenue": 0,
    "conversion_rate": 0.0
  },
  "page_analytics": [
    {
      "page_url": "...",
      "sessions": 0,
      "conversions": 0,
      "conversion_rate": 0.0,
      "avg_time_on_page": 0,
      "bounce_rate": 0.0
    }
  ],
  "funnel_data": {
    "awareness_sessions": 0,
    "interest_sessions": 0,
    "consideration_sessions": 0,
    "conversion_sessions": 0
  },
  "user_behavior": {
    "session_recordings": [...],
    "form_abandonment_data": {...},
    "scroll_depth": {...}
  }
}
```

---

## Output Format

```markdown
# CRO Analysis & Optimization Roadmap - [Month Year]

## Executive Summary

**Conversion Rate**: [X%] ([+X%] vs last month)
**Primary Bottleneck**: [Stage/Page]
**Biggest Opportunity**: [Action with estimated impact]
**Recommended Focus**: [Highest-ROI improvement area]

---

## Conversion Funnel Analysis

### Stage 1: Awareness
- Traffic sources: [Top 3]
- Total sessions: [X]
- Bounce rate: [X%]
- Status: [Healthy / Needs Optimization]

### Stage 2: Interest
- Landing on: [Top pages]
- Sessions reaching interest stage: [X] ([X%] of awareness)
- Time on page: [X] sec avg
- Status: [Healthy / Needs Optimization]

### Stage 3: Consideration
- Pages visited: [Top pages]
- Form starts: [X]
- Form abandonment rate: [X%]
- Status: [Healthy / Needs Optimization]

### Stage 4: Decision
- Form completions: [X]
- Conversion rate: [X%]
- Avg lead value: $[X]
- Status: [Healthy / Needs Optimization]

**Biggest Drop-off**: [Stage] ([X%] → [X]% drop)

---

## High-Traffic, Low-Conversion Pages

### Page: [URL]
- Traffic: [X] sessions/month
- Conversion rate: [X]% (below average)
- Estimated impact of 1% conversion increase: [X] more conversions/month

**Issues Identified**:
1. [Issue] - Impact: [Impact]
2. [Issue] - Impact: [Impact]
3. [Issue] - Impact: [Impact]

**Recommendations**:
- [Specific change] → Expected impact: +[X]% conversion
- [Specific change] → Expected impact: +[X]% conversion

---

## A/B Test Roadmap

### Priority 1: [Test Name]
**Page**: [URL]
**Hypothesis**: Changing [element] from [current] to [proposed] will increase conversions by [X]%

**Test Variation A** (Control):
- [Current state]

**Test Variation B** (Test):
- [Proposed change]

**Success Metric**: Conversion rate increase to [X]%
**Sample Size Needed**: [X] visitors (for [X]% lift with 95% confidence)
**Estimated Duration**: [X] weeks
**Estimated Impact**: [X] additional conversions/month

---

### Priority 2: [Test Name]
**Page**: [URL]
**Hypothesis**: [Hypothesis]
**Test Details**: [Details]
**Expected Impact**: [X] additional conversions/month

---

### Priority 3: [Test Name]
[Same structure as above]

---

## Quick Wins (Implement Immediately)

**1. [Change]: [Description]**
- Current: [Current state]
- Proposed: [Proposed state]
- Why it matters: [Why this improves conversion]
- Effort: [Low/Medium/High]
- Estimated impact: [X]% conversion increase

**2. [Change]: [Description]**
[Same structure]

**3. [Change]: [Description]**
[Same structure]

---

## Page-by-Page Assessment

### Landing Page: [URL]
- Traffic: [X] visits/month
- Conversion rate: [X]%
- Issues:
  - [ ] Headline doesn't match ad/search query
  - [ ] Offer not specific/clear
  - [ ] Form has too many fields ([X])
  - [ ] CTA not prominent
  - [ ] No social proof visible
  - [ ] Missing objection handling
- Quick fix: [What to change]
- Estimated impact: [+X]% conversion

### [Repeat for all key pages]

---

## Copywriting Recommendations

### Headlines
**Current State**: [Current headlines across site]
**Issues**: [What's vague/unclear]
**Recommended Changes**:
- Page [URL]: Change "[Current]" to "[Proposed]"
  - Why: [Why this is better]
  - Impact: [Estimated +X%]

### CTAs
**Current State**: [Current CTA buttons and text]
**Issues**: [What could be clearer/more compelling]
**Recommended Changes**:
- Button text: Change "[Current]" to "[Proposed]"
- Button color: Change [Current] to [Proposed]
- Button placement: Move from [Current] to [Proposed]

### Social Proof
**Current State**: [What proof is currently shown]
**Gaps**: [What proof is missing]
**Recommended Additions**:
- Add testimonial from [type of customer]
- Add stat: [Statistic about results]
- Add logo: [Customer logo or certification]

---

## Form Optimization Analysis

**Current Form Fields**: [X] fields
- Required: [List]
- Optional: [List]
- Abandonment rate: [X]%

**Recommended Changes**:
1. Remove [Field] (not essential for lead qualification)
2. Move [Field] to second page (reduce initial friction)
3. Make [Field] optional (many visitors leaving at this field)

**Expected Impact**: [X]% reduction in abandonment, [X]% more completions

---

## Monthly Improvement Targets

**Month 1** (Quick Wins):
- Implement [X] quick wins
- Launch [X] A/B tests
- Target conversion rate: [X]%

**Month 2** (Test Results):
- Review A/B test results
- Scale winning variations
- Target conversion rate: [X]%

**Month 3** (Cumulative Impact):
- Target conversion rate: [X]%
- Expected additional revenue: $[X]

---

## Implementation Timeline

- **Week 1**: Implement quick wins (copywriting, form changes, visual changes)
- **Week 2**: Launch Priority 1 A/B test
- **Week 3**: Launch Priority 2 A/B test (if time allows)
- **Week 4**: Monitor test performance, adjust bids/targeting based on data

---

## Success Metrics

**Track these metrics weekly**:
- Overall conversion rate (% change)
- Page-level conversion rates (% change)
- Form abandonment rate (% change)
- Avg lead value ($)
- Cost per acquisition by source ($)

**Success targets for next month**:
- Conversion rate: [Target]%
- Total conversions: [Target]
- Revenue: $[Target]
```

---

## Success Criteria

✅ **Funnel analysis completed** with bottlenecks identified  
✅ **A/B test roadmap provided** (3-5 prioritized tests with hypotheses)  
✅ **Quick wins documented** (5-10 low-effort, high-impact changes)  
✅ **Impact estimates included** (expected lift per test/change)  
✅ **Implementation timeline** (when to launch tests)  
✅ **Page-by-page assessment** (specific issues per page)  
✅ **Copywriting recommendations** (specific headline/CTA improvements)  

---

## Recurring Schedule

**Monthly** (on or before 10th of following month):
- Analyze previous month's performance
- Deliver CRO recommendations
- Update A/B test roadmap based on results

**Ongoing**:
- Monitor A/B test results (weekly check-ins)
- Implement quick wins (continuous)
- Scale winning variations immediately

---

## Feeds Into

- Monthly strategy refinement (learnings from tests inform next month's approach)
- Ads optimization (winning CTAs/offers used in ad copy)
- Content optimization (underperforming pages rewritten/optimized)
- Landing page updates (form changes, headline changes, social proof updates)
