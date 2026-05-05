# Onboarding Research Agent

**Deep market analysis, competitive research, and audience validation**

Enriches the initial positioning from the website-post-onboarding-agent with comprehensive market research, competitor deep-dive, and audience insights validation.

---

## What It Does

Executes Phase 1.2 of service fulfillment: Takes positioning strategy and validates it against real market data, competitive landscape, and audience research.

**Input**: Positioning statement + messaging pillars from website-post-onboarding-agent

**Output**: Market analysis report, competitive intelligence, validated audience personas, messaging validation framework

---

## Execution

### Stage 1: Market Landscape Analysis
- **Duration**: 1 day
- **Tasks**:
  - Industry overview and trends
  - Market size and growth trends
  - Customer acquisition channels in industry
  - Seasonal or cyclical patterns
  
**Output**: Market context document (2-3 pages)

### Stage 2: Competitive Research
- **Duration**: 1-2 days
- **Tasks**:
  - Identify 5-7 direct competitors
  - Analyze each competitor's:
    - Positioning statement
    - Messaging and claims
    - Target audience
    - Pricing model
    - Marketing channels used
    - Website structure and CTAs
    - Customer reviews/ratings
    - Apparent strengths and weaknesses

**Output**: Competitive analysis matrix and detailed profiles (3-5 pages)

### Stage 3: Positioning Validation
- **Duration**: 0.5 days
- **Tasks**:
  - Does positioning fill a real market gap?
  - Can competitors claim something similar?
  - Is positioning defensible based on client capabilities?
  - Do messaging pillars resonate with target audience?

**Output**: Validation report with recommendations (1-2 pages)

### Stage 4: Audience Deep-Dive
- **Duration**: 1 day
- **Tasks**:
  - Expand on target audience definition
  - Document secondary audience segments
  - Pain point validation (do these actually matter?)
  - Decision-making criteria research
  - Behavior patterns and search intent

**Output**: Detailed audience personas (2-3 pages)

---

## Input Format

```json
{
  "positioning_context": {
    "positioning_statement": "...",
    "messaging_pillars": [...],
    "target_audience": {...},
    "unique_differentiators": [...],
    "proof_points": [...]
  },
  "client_info": {
    "name": "...",
    "industry": "...",
    "website": "...",
    "years_in_business": 0
  }
}
```

---

## Output Format

```markdown
# Market Research & Validation Report

[Client Name] - [Industry]

## Market Overview
- Industry size and growth
- Key trends
- Customer acquisition landscape
- Seasonal patterns

## Competitive Analysis
[5-7 competitors analyzed with positioning, pricing, messaging]

## Positioning Validation
- Gap analysis vs competitors
- Defensibility assessment
- Audience fit assessment

## Audience Insights
- Demographic deep-dive
- Psychographic profiles
- Pain point validation
- Decision criteria ranking

## Recommendations
- Positioning adjustments (if needed)
- Messaging refinement ideas
- Audience segment opportunities
```

---

## Success Criteria

✅ **5-7 competitors identified** and analyzed  
✅ **Positioning gap clearly articulated** vs competition  
✅ **Audience personas expanded** with behavioral data  
✅ **Messaging pillars validated** or refined  
✅ **Actionable recommendations** provided  

---

## Feeds Into

- website-copywriting-agent (validated positioning)
- google-ads-research-agent (audience + market data)
- seo-research-agent (market/keyword opportunity data)
- Approval Gate 1 (positioned + validated)
