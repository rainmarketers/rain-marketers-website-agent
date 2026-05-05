# Google Ads Strategy Agent

**Build offer structure, messaging angles, and audience segments**

Synthesizes research into campaign strategy: defines what offer to make, how to position it, which audiences to target, and bidding approach.

---

## What It Does

Executes Phase 3.2a of service fulfillment: Transforms research into a concrete ads strategy before any creative is written.

**Input**: Google Ads research context + business goals + pricing + budget

**Output**: Offer structure, messaging angles, audience segments, bid strategy

---

## Execution

### Stage 1: Define the Offer (0.5 days)
- **Tasks**:
  - What is the core offer? (Free inspection, discount, demo, etc.)
  - What makes it unique vs competitors?
  - What's the risk-reversal element?
  - What's the offer-specific value prop?
  - What objections does this overcome?

**Output**: Offer definition document

### Stage 2: Create Audience Segments (0.5 days)
- **Tasks**:
  - Primary audience segment (highest intent, best ROI)
  - Secondary segments (lower intent, higher volume)
  - Audience targeting approach (keywords, placement, interests)
  - Bid allocation per segment

**Output**: Audience segment definitions + targeting strategy

### Stage 3: Map Messaging Angles to Offer (0.5 days)
- **Tasks**:
  - Which ad copy angles resonate with which audience?
  - How does each angle address a customer pain point?
  - What proof points support each angle?
  - How do angles differentiate from competitors?

**Output**: Messaging angle matrix (audience × angle × proof)

### Stage 4: Bid Strategy & Budget (0.5 days)
- **Tasks**:
  - Recommended bid strategy (maximize conversions, maximize clicks, etc.)
  - Bid ceiling recommendations per keyword
  - Budget allocation across audiences
  - Cost per acquisition targets
  - Expected ROAS

**Output**: Bid strategy document

---

## Input Format

```json
{
  "google_ads_research": {
    "keyword_opportunities": [...],
    "audience_insights": {...},
    "ad_copy_angles": [...]
  },
  "business_goals": {
    "target_cpa": 0,
    "monthly_lead_target": 0,
    "budget_ceiling": 0
  },
  "offer_options": [
    {
      "name": "Free inspection",
      "value": "...",
      "differentiation": "..."
    }
  ]
}
```

---

## Output Format

```markdown
# Google Ads Campaign Strategy

## Offer Definition

**Primary Offer**: [What we're offering]

**Offer Unique Value**:
- [Differentiator 1]
- [Differentiator 2]
- [Differentiator 3]

**Risk Reversal**: [How we eliminate customer risk]

**Objection Handled**: [What customer concern does this solve?]

## Audience Segments

**Segment 1: [Name]**
- Target keywords: [...]
- Audience size: [...]
- Intent level: [High/Medium/Low]
- Est. conversion rate: [...]
- Bid allocation: [% of budget]

[Repeat for 2-3 additional segments]

## Messaging Angles by Audience

[Matrix showing:]
- Which angle resonates with which audience
- What proof points support each angle
- How it differentiates from competitors

**Example**:
- Segment: Busy professionals
- Angle: Same-day guarantee
- Proof: 95% within 24 hours
- Diff: Pro Gutter Pros claims same-day, we add lifetime guarantee

## Bid Strategy

**Bidding Approach**: [Maximize Clicks / Maximize Conversions / ROAS target]

**Keyword bid ceiling**: [By category]
- High volume keywords: $[X]
- Mid volume keywords: $[X]
- Low competition keywords: $[X]

**Expected metrics**:
- Average CPC: $[X]
- Expected conversion rate: [X%]
- Target CPA: $[X]
- Expected ROAS: [X:1]

## Budget Allocation

- Monthly budget: $[X]
- Segment 1 allocation: $[X] ([X]%)
- Segment 2 allocation: $[X] ([X]%)
- Expected monthly leads: [X]
```

---

## Success Criteria

✅ **Offer is differentiated** vs competitors  
✅ **2-3 audience segments defined** with targeting  
✅ **Messaging angles mapped** to audiences  
✅ **Bid strategy is realistic** (CPC estimates validated)  
✅ **Budget allocation is logical** (best ROI segment gets most budget)  
✅ **Expected metrics documented** (CPA, ROAS targets)  

---

## Feeds Into

- google-ads-landing-page-copywriter (uses offer + messaging angles)
- google-ads-campaign-prep-agent (uses segments + bid strategy)
