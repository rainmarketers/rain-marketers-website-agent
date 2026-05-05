# Integration Patterns Guide

How skills communicate, pass context, and coordinate with each other throughout the fulfillment workflow.

---

## Core Integration Patterns

### 1. Sequential Flow with Context Passing

**Pattern**: Upstream skill → Context object → Downstream skill

**How it works**:
- Upstream skill produces structured output
- Output is formatted as a context object (JSON)
- Context object is passed as input to next skill
- Downstream skill inherits all upstream findings

**Example**: Onboarding research → Content templates
```
website-post-onboarding-agent OUTPUT:
{
  positioning_statement: "Same-day gutter service for busy professionals",
  messaging_pillars: ["Speed", "Reliability", "Local Expertise"],
  target_audience: {...},
  recommended_sitemap: {...}
}
↓
website-copywriting-agent INPUT:
- Uses positioning_statement to inform all copy tone
- Uses messaging_pillars as copy pillars
- Uses target_audience to define copy audience
- Uses recommended_sitemap for page structure
```

### 2. Parallel Branching

**Pattern**: One skill → Multiple downstream skills (non-dependent)

**When used**:
- Phase 1 onboarding branches to 3 parallel research paths:
  - website-copywriting-agent (website content)
  - google-ads-research-agent (paid ads strategy)
  - seo-research-agent (organic search strategy)

**How it works**:
```
website-post-onboarding-agent
    ├─→ website-copywriting-agent (independent)
    ├─→ google-ads-research-agent (independent)
    └─→ seo-research-agent (independent)
```

Each downstream skill receives the SAME positioning context, but produces independent output (no waiting for others).

### 3. Multi-Stage Sequential

**Pattern**: Skill A → Skill B → Skill C → ... (chain of dependencies)

**When used**:
- Google Ads strategy (4 stages in sequence)
- SEO strategy (3 stages in sequence)

**Example**: Google Ads
```
google-ads-research-agent
    ↓ (research output feeds into)
google-ads-strategy-agent
    ↓ (strategy output feeds into)
google-ads-landing-page-copywriter
    ↓ (copy feeds into)
google-ads-campaign-prep-agent
```

Each stage depends on previous output; must execute sequentially.

### 4. Approval Gate Pattern

**Pattern**: Skill output → Human approval → Downstream continues

**When used**:
- After website brief (Gate 1)
- After website copy (Gate 2)
- After Google Ads research (Gate 3)
- After content calendar (Gate 4)

**How it works**:
```
Skill produces output
    ↓
Orchestrator pauses
    ↓
Human reviews and approves
    ↓
Orchestrator resumes downstream work
```

**If not approved**: Orchestrator waits for either:
- Approval (proceed forward)
- Rejection with feedback (loop back to skill with adjusted input)

### 5. Recurring Cycle Pattern

**Pattern**: Monthly agent runs on schedule, consuming previous month's output

**When used**:
- Monthly content creation (consumes content calendar + previous month performance)
- Monthly reporting (consumes analytics + performance baseline)
- Monthly CRO analysis (consumes current performance + historical trends)

**How it works**:
```
Month 1:
  content-planner-agent → content-calendar (ONCE)
  ↓
  content-creator-agent → Month 1 content
  ↓
  monthly-reporting-agent → Month 1 report
  ↓
  cro-analysis-agent → Month 1 recommendations

Month 2:
  content-creator-agent → Month 2 content
    (consumes: content calendar + Month 1 performance)
  ↓
  monthly-reporting-agent → Month 2 report
    (consumes: current analytics)
  ↓
  cro-analysis-agent → Month 2 recommendations
    (consumes: Month 2 performance + Month 1 baseline)
```

---

## Context Object Models

### Positioning Context (Foundation, reused everywhere)

```json
{
  "positioning_statement": "Same-day gutter service for busy professionals",
  "messaging_pillars": [
    "Speed: Same-day or next-day service",
    "Reliability: Licensed, insured, lifetime guarantee",
    "Local Expertise: 20+ years founder experience"
  ],
  "target_audience": {
    "demographics": "Homeowners age 40-65, suburban Chicago",
    "income": "$75K-150K annually",
    "psychographics": "Values time, reliability, local relationships"
  },
  "unique_differentiators": [
    "Same-day delivery (95% of calls)",
    "Local founder-led service (not franchised)",
    "Lifetime guarantee (unique claim)"
  ],
  "proof_points": [
    "20+ years founder experience",
    "4.8★ Google rating from 200+ reviews",
    "Grew from 0 to 4 employees through word-of-mouth"
  ]
}
```

**Used by**: Every downstream skill (website, ads, SEO)

### Website Brief Context

```json
{
  "positioning_context": {...},
  "website_brief": {
    "homepage_headline": "Never Climb a Ladder Again",
    "value_propositions": [...],
    "cta_primary": "Get Your Free Inspection",
    "cta_secondary": "See How We Work"
  },
  "recommended_sitemap": {
    "homepage": "Problem → Solution → Trust → CTA",
    "services": "Details + pricing",
    "why_choose_us": "Differentiators + proof",
    ...
  },
  "success_metrics": {
    "target_leads_monthly": 15,
    "conversion_rate_target": 0.20,
    "customer_satisfaction_target": 4.8
  }
}
```

**Used by**: Design team, copywriting team, development team

### Google Ads Research Context

```json
{
  "competitor_analysis": [
    {
      "name": "Pro Gutter Pros",
      "positioning": "Speed/Convenience",
      "price_range": "$150-300/visit"
    },
    {...}
  ],
  "keyword_data": {
    "high_volume": ["gutter cleaning near me", "best gutter service"],
    "low_competition": ["gutter service + same-day"],
    "cpc_range": "$2-5"
  },
  "audience_insights": {
    "primary_intent": "Local service search with immediacy",
    "decision_criteria": ["Reviews", "Speed", "Price", "Local presence"]
  },
  "ad_copy_angles": [
    "Same-day guarantee",
    "Local expert authority",
    "Risk reversal (guarantee)"
  ]
}
```

**Used by**: google-ads-strategy-agent, google-ads-landing-page-copywriter

### SEO Research Context

```json
{
  "keyword_opportunities": [
    {
      "keyword": "gutter cleaning chicago",
      "monthly_searches": 1200,
      "difficulty": "moderate",
      "intent": "local service search"
    },
    {...}
  ],
  "topic_clusters": [
    {
      "pillar": "Gutter Cleaning Guide",
      "supporting_content": ["When to clean", "DIY vs professional", "Signs of clogging"]
    },
    {...}
  ],
  "content_gaps": [
    "No one ranking for 'water damage prevention'",
    "Weak content on 'gutter protection systems'",
    "Missing local landing pages for suburbs"
  ]
}
```

**Used by**: seo-content-planner-agent, seo-content-creator-agent

### Performance Context (Monthly flow)

```json
{
  "period": "May 2026",
  "traffic_metrics": {
    "organic_sessions": 245,
    "organic_conversion_rate": 0.12,
    "paid_sessions": 890,
    "paid_conversion_rate": 0.18
  },
  "conversion_data": {
    "total_leads": 18,
    "qualified_leads": 14,
    "cost_per_lead": 28.5,
    "booking_rate": 0.22
  },
  "user_behavior": {
    "most_viewed_page": "/services/gutter-cleaning",
    "highest_ctr_cta": "Get Free Inspection",
    "form_abandonment_rate": 0.31
  },
  "bottlenecks": [
    "Contact form has high abandonment",
    "Services page needs more detail",
    "Mobile experience could be better"
  ]
}
```

**Used by**: monthly-reporting-agent, cro-analysis-agent

---

## Skill Invocation Patterns

### Direct Invocation (User-initiated)
```
User: "Create website brief for Clean Cut Gutters"
Orchestrator: Invokes website-post-onboarding-agent
Output: Website brief delivered to user
```

### Programmatic Invocation (Orchestrator-triggered)
```
Orchestrator: "Gate 1 approved, proceeding to Phase 2"
Orchestrator: Invokes website-copywriting-agent with positioning context
Orchestrator: Monitors for completion
Orchestrator: Passes output to next stage
```

### Conditional Invocation
```
IF client_selected_service == "Full service" THEN
  Invoke google-ads-research-agent
  Invoke seo-research-agent
ELSE IF client_selected_service == "Website only" THEN
  Skip Ads and SEO phases
```

---

## Error Handling & Fallback Patterns

### When Skill Output is Insufficient

**Pattern**: Loop back with adjusted input

```
Skill A produces output
Orchestrator evaluates quality
IF quality < threshold THEN
  Invoke Skill A again with:
    - Original input
    - + Quality feedback
    - + Examples of better output
ELSE
  Proceed to Skill B
```

### When Approval is Rejected

**Pattern**: Gather feedback, re-run skill, re-approve

```
Skill output → Gate (Human approval)
IF rejected THEN
  Gather feedback from approver
  Re-invoke upstream skill with:
    - Original input
    - Approval feedback/notes
  New output → Gate (re-approval cycle)
ELSE
  Proceed
```

---

## Data Consistency Rules

1. **Positioning is immutable** during Phase 1-2
   - Once approved at Gate 1, positioning flows unchanged to all downstream skills
   - Prevents mid-project strategy shifts

2. **Context is additive** but not mutative
   - Downstream skills add findings, don't modify upstream output
   - Prevents unintended cascading changes

3. **Approval gates are blocking**
   - No downstream work proceeds until gate is cleared
   - Prevents wasted effort on unvalidated strategy

4. **Performance data flows one direction**
   - Reporting and CRO analysis consume performance data
   - Performance data doesn't flow backwards to content/ads strategy
   - New month's content creation gets previous month's performance as input

---

## Integration Checklists

### Before invoking downstream skill
- [ ] Upstream skill completed successfully
- [ ] Output is in expected format (JSON or markdown)
- [ ] Required context fields are present and non-null
- [ ] Approval gates (if any) have been cleared

### After skill completion
- [ ] Output saved to project repository
- [ ] Output logged to Asana task
- [ ] Context object prepared for next skill
- [ ] Quality threshold met (or feedback loop initiated)

### At approval gates
- [ ] Output summary prepared for decision maker
- [ ] Key decisions clearly articulated
- [ ] Feedback mechanism established for rejection case
- [ ] Timeline impact understood if rejected
