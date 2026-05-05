# Google Ads Campaign Prep Agent

**Prepare Google Ads campaign structure, audiences, keywords, and ad copy**

Translates strategy and copy into a ready-to-launch Google Ads campaign: campaign structure, ad groups, keywords, audiences, and ad copy variants.

---

## What It Does

Executes Phase 3.3 of service fulfillment: Takes all strategy and copy work and produces a complete campaign configuration ready to launch.

**Input**: Landing pages (designed) + offer strategy + messaging angles + keyword research

**Output**: Campaign structure, audiences, keywords, bidding, ad copy variants, conversion tracking setup

---

## Execution

### Stage 1: Campaign Structure (0.5 days)
- **Campaign-level setup**:
  - Campaign name and type (Search)
  - Geographic targeting
  - Language
  - Device preferences
  - Bidding strategy selection

- **Ad group structure** (typically 3-5 groups):
  - Ad Group 1: Brand keywords
  - Ad Group 2: Service category keywords
  - Ad Group 3: Long-tail intent keywords
  - (Additional groups as needed)

**Output**: Campaign + Ad Group definitions

### Stage 2: Keyword & Audience Assignment (1 day)
- **Per Ad Group**:
  - 10-20 keywords at appropriate match types
  - Negative keywords (prevent irrelevant clicks)
  - Audience targeting if demographic/interest targeting
  - Bid adjustments per keyword

**Output**: Keyword assignments by ad group + match types + negative keywords

### Stage 3: Ad Copy Creation (1 day)
- **Per Ad Group**: 2-3 ad variants with:
  - Headline 1, Headline 2, Headline 3
  - Description Line 1, Description Line 2
  - Display URL
  - Final URL (landing page destination)
  - Ad extensions (sitelink, callout, promotion)

**Approach**: Use messaging angles + landing page copy as foundation

### Stage 4: Conversion Tracking Setup (0.5 days)
- **Tracking requirements**:
  - Conversion action definition (form submission, call, booking)
  - Conversion tag implementation
  - Value assignment (for ROAS tracking)
  - Cross-domain tracking (if applicable)

**Output**: Conversion tracking specification

---

## Input Format

```json
{
  "offer_strategy": {...},
  "keyword_research": {
    "keywords_by_group": [...]
  },
  "landing_pages": {
    "primary_page": "...",
    "url": "..."
  },
  "audience_segments": [...]
}
```

---

## Output Format

```markdown
# Google Ads Campaign Configuration

## Campaign Setup

**Campaign Name**: [Client Name] - [Service] - [Year]

**Settings**:
- Type: Search
- Geographic target: [Location]
- Language: [Language]
- Device: [All / Mobile priority]
- Bidding: [Strategy chosen]
- Budget: $[X] daily

## Ad Group Structure

### Ad Group 1: [Category] - Brand Keywords
**Bid**: $[X]
**Keywords** (10-15):
- [Exact match keywords]
- [Phrase match keywords]
- [Broad match modifiers]

**Negative keywords** (5-10):
- -[Irrelevant terms]

### [Repeat for 3-5 ad groups]

## Ad Copy Variants

### Ad Group 1 - Ad Variant 1
**Headlines**:
1. [30 chars] - Primary benefit
2. [30 chars] - Proof/urgency
3. [30 chars] - CTA/risk reversal

**Descriptions**:
1. [90 chars] - Address objection
2. [90 chars] - How it works/timeline

**Display URL**: [domain.com/service]

**Final URL**: [landing page URL]

**Ad Extensions**:
- Sitelink 1: [Link + description]
- Callout: [Key proof point]
- Promotion: [Time-limited offer]

### [Additional variants per group]

## Conversion Tracking

**Conversion Action**: [Lead submission / Phone call / Booking]

**Tracking type**: [Form submission / Phone number click / API conversion]

**Conversion value**: $[X] (estimated customer value)

**Attribution model**: [First click / Linear / Time decay]

## Expected Performance

**Estimated metrics** (based on benchmarks):
- Average CPC: $[X]
- Expected CTR: [X%]
- Expected conversion rate: [X%]
- Target CPA: $[X]
- Expected ROAS: [X:1]

**First 30 days** (estimated):
- Budget: $[X]
- Expected clicks: [X]
- Expected conversions: [X]
- Expected cost per conversion: $[X]

## Launch Checklist

- [ ] Campaign structure approved
- [ ] All keywords added with proper match types
- [ ] Negative keywords set
- [ ] Ad copy approved for brand compliance
- [ ] Landing page reviewed for QA
- [ ] Conversion tracking implemented
- [ ] Ad extensions added
- [ ] Budget and daily bid limits set
- [ ] Campaign scheduled to start
- [ ] GA4 cross-domain tracking confirmed
```

---

## Success Criteria

✅ **3-5 Ad Groups created** with logical structure  
✅ **50-100 keywords** assigned at correct match types  
✅ **Negative keywords documented** (prevent wasted spend)  
✅ **2-3 ad variants per group** (ready to A/B test)  
✅ **Conversion tracking specified** (how we measure success)  
✅ **Ad extensions configured** (increase CTR)  
✅ **Landing page URL matches** (no broken links)  

---

## Ready for Launch

This agent produces everything needed to:
- Input campaign config into Google Ads manager
- Set budgets and bid adjustments
- Launch the campaign
- Begin monitoring performance

---

## Next Phase

After launch:
- Monitor Quality Score (target 6+)
- Watch CTR and conversion rate
- Adjust bids based on performance
- A/B test ad copy variants
- Optimize landing page for conversion
