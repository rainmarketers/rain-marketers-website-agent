# Google Ads Research Agent

**Research paid search landscape, keywords, and audience opportunities**

Analyzes competitive paid search environment, identifies high-intent keywords, and validates audience targeting for Google Ads campaign strategy.

---

## What It Does

Executes Phase 3.1 of service fulfillment: Researches paid search opportunities, competitive landscape, and keyword/audience strategy foundation.

**Input**: Positioning + target audience + market research from Phase 1

**Output**: Google Ads research context (keywords, competitors, audience insights, ad copy angles)

---

## Execution

### Stage 1: Competitor Ads Analysis (1 day)
- **Tasks**:
  - Find 5-7 competitors running Google Ads
  - Analyze each competitor's:
    - Ad copy and messaging
    - Landing page URL structure (clues about offer)
    - Ad extensions used
    - Geographic targeting
    - Apparent bid strategy (position frequency)

**Output**: Competitive ad analysis matrix (with examples)

### Stage 2: Keyword Research (1 day)
- **Categories**:
  - **High volume keywords** (search intent validation)
  - **Mid-volume keywords** (opportunity sweet spot)
  - **Low competition keywords** (quick wins)
  - **Long-tail keywords** (intent-specific)

- **Per keyword analysis**:
  - Monthly search volume
  - Competition level (High/Medium/Low)
  - Commercial intent (is user ready to buy/book?)
  - Cost per click estimates
  - Recommended bid ceiling

**Output**: Keyword research spreadsheet (50-100 keywords)

### Stage 3: Audience Insights (0.5 days)
- **Tasks**:
  - What intent is target audience expressing?
  - What are they searching for?
  - When do they search (timing)?
  - What devices do they use?
  - What's their decision journey?

**Output**: Audience behavior profile

### Stage 4: Ad Copy Angle Identification (0.5 days)
- **Tasks**:
  - What hooks resonate with this audience?
  - What messaging angles work in ads?
  - What proof points convert?
  - What risk reversals matter?

**Output**: 4-6 ad copy angle recommendations

---

## Input Format

```json
{
  "positioning_context": {...},
  "market_research": {
    "industry": "...",
    "target_audience": {...},
    "market_size": "...",
    "growth_trend": "..."
  },
  "business_info": {
    "website": "...",
    "service_area": "...",
    "budget_estimate": 0
  }
}
```

---

## Output Format

```markdown
# Google Ads Research Report

## Competitive Ad Analysis
[5-7 competitors with:]
- Positioning (from ads)
- Ad copy examples
- Landing page insights
- Apparent strategy
- Gaps vs our positioning

## Keyword Research
[50-100 keywords organized by:]
- High volume (brand + category keywords)
- Mid volume (specific offering)
- Low competition (quick wins)
- Long-tail (intent-specific)

[Per keyword:]
- Monthly searches
- Competition level
- Commercial intent
- Est. CPC
- Recommended bid ceiling

## Audience Insights
- Primary search intent
- Search timing patterns
- Device behavior
- Decision journey stages
- Key decision criteria

## Ad Copy Angles
[4-6 angles with:]
- Hook/promise
- Supporting proof
- Target audience fit
- Expected CTR
```

---

## Research Methods

- Google Ads keyword planner (search volume, CPC)
- Competitor analysis (actual ads running)
- Search intent analysis (what are searchers trying to accomplish?)
- Industry benchmarking (how much do similar ads cost?)

---

## Success Criteria

✅ **5-7 competitors** identified running ads  
✅ **50-100 keywords** researched and categorized  
✅ **Keyword intent validated** (are searchers ready to convert?)  
✅ **CPC estimates provided** (budget planning)  
✅ **Audience insights documented** (behavior + intent)  
✅ **4-6 ad copy angles** identified  

---

## Approval Gate 3

**Required**: Internal team reviews research quality
- Are keywords high-intent?
- Do competitors confirm market demand?
- Is audience targeting aligned with positioning?
- Are budget estimates realistic?

---

## Feeds Into

- google-ads-strategy-agent (uses all research findings)
- google-ads-landing-page-copywriter (uses ad copy angles)
- Budget planning and bid strategy
