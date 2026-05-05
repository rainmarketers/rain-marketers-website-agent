# Complete Workflow Documentation

Detailed breakdown of the Rain Marketers service fulfillment workflow, including phase timelines, stage descriptions, and execution logic.

---

## Overview

The orchestrator manages a 4-phase service delivery spanning 8+ weeks, from initial client onboarding through ongoing optimization. Each phase has distinct objectives, deliverables, and decision gates.

---

## Phase 1: Discovery & Strategy (Weeks 1-2)

**Objective**: Understand client business, market, and positioning

### Stage 1.1: Client Onboarding
- **Agent**: website-post-onboarding-agent
- **Input**: Client name, website URL, business type, target customer, pain points
- **Duration**: 1-2 days
- **Output**: 
  - Website brief document
  - Positioning statement
  - Messaging pillars (3-4 core claims)
  - Recommended sitemap
  - Content templates
  - Asana project structure

### Stage 1.2: Market & Competitive Research
- **Agent**: onboarding-research-agent
- **Input**: Positioning from Stage 1.1
- **Duration**: 2-3 days
- **Output**:
  - Competitor analysis (5-7 direct competitors)
  - Market landscape overview
  - Audience research depth
  - Messaging validation
  - Industry trends summary

**Approval Gate 1**: Client reviews positioning + messaging pillars
- **Required approval**: Client agrees positioning is defensible and aligned with business
- **Blocks**: All downstream work
- **Typical decision time**: 1-2 days

---

## Phase 2: Website Creation (Weeks 3-6)

**Objective**: Build and launch the website

### Stage 2.1: Website Copywriting
- **Agent**: website-copywriting-agent
- **Input**: Website brief + positioning + messaging pillars from Phase 1
- **Duration**: 3-4 days
- **Output**:
  - Homepage copy (hero, value props, social proof, CTA)
  - Inner page copy (services, about, process, testimonials, FAQ)
  - Landing page copy (if needed for ads)
  - CTA strategies
  - Copy hierarchy and prominence guidelines

**Parallel Activity**: Design phase begins based on sitemap
- **Duration**: 2-3 weeks
- **Input**: Website brief + sitemap recommendations
- **Output**: High-fidelity wireframes and design system

**Approval Gate 2**: Client/team reviews copy tone and messaging
- **Required approval**: Copy aligns with brand voice and positioning
- **Blocks**: Design hand-off and content finalization
- **Typical decision time**: 1-2 days

### Stage 2.2: Site Development
- **Duration**: 2-3 weeks
- **Input**: Final copy + approved design
- **Output**: Fully functional website with:
  - All pages implemented
  - CTA forms/booking integration
  - Mobile-responsive design
  - Analytics tracking setup
  - Google Business integration

---

## Phase 3: Paid Advertising (Weeks 5-8, overlaps with website)

**Objective**: Set up Google Ads campaign for immediate lead generation

### Stage 3.1: Google Ads Research
- **Agent**: google-ads-research-agent
- **Input**: Positioning, target audience, market research from Phase 1
- **Duration**: 2-3 days
- **Output**:
  - Competitor ad analysis
  - Keyword research and opportunities
  - Audience segment insights
  - Ad copy angle recommendations
  - Budget benchmarking

**Approval Gate 3**: Internal team reviews strategy
- **Required approval**: Research validates audience targeting and keyword strategy
- **Blocks**: Campaign creation phase
- **Typical decision time**: 1 day

### Stage 3.2: Ads Offer & Landing Page Strategy
- **Agent Phase A**: google-ads-strategy-agent
  - **Input**: Research output + business goals + pricing
  - **Duration**: 1-2 days
  - **Output**: Offer structure, messaging angles, audience segments, bid strategy

- **Agent Phase B**: google-ads-landing-page-copywriter
  - **Input**: Offer strategy + messaging angles
  - **Duration**: 1-2 days
  - **Output**: High-converting landing page copy

**Parallel Activity**: Design & development of landing pages
- **Duration**: 2-3 days
- **Input**: Final landing page copy
- **Output**: Designed and developed landing page(s)

### Stage 3.3: Campaign Prep & Launch
- **Agent**: google-ads-campaign-prep-agent
- **Input**: Landing pages (designed) + offer strategy
- **Duration**: 1-2 days
- **Output**:
  - Campaign structure (ad groups, keywords, audiences)
  - Bidding recommendations
  - Ad copy variants (3+ per ad group)
  - Conversion tracking setup
  - Performance targets

**Launch**: Campaign goes live
- Monitoring for first 48 hours
- Quality Score optimization
- Bid adjustments as needed

---

## Phase 4: SEO & Organic (Weeks 6+, ongoing)

**Objective**: Build long-term organic traffic through SEO and content

### Stage 4.1: SEO Research
- **Agent**: seo-research-agent
- **Input**: Website brief, positioning, business goals
- **Duration**: 2-3 days
- **Output**:
  - Keyword research and opportunity analysis
  - Content gap analysis (what competitors rank for)
  - SEO audit of current site
  - Topic cluster recommendations
  - Quick wins (easy-to-rank opportunities)

### Stage 4.2: Content Calendar & Planning
- **Agent**: seo-content-planner-agent
- **Input**: SEO research + messaging pillars + business goals
- **Duration**: 2-3 days
- **Output**:
  - 12-month content calendar
  - Topic clusters (pillar + supporting content)
  - Publishing schedule
  - Keyword targeting by article
  - Internal linking map

**Approval Gate 4**: Client reviews content plan + topics
- **Required approval**: Content plan aligns with business strategy
- **Blocks**: Monthly content creation
- **Typical decision time**: 1-2 days

### Stage 4.3: Monthly Content Creation (Recurring)
- **Agent**: seo-content-creator-agent
- **Input**: Content plan for current month + previous month's performance
- **Duration**: 3-5 days per month (4-6 articles)
- **Output**:
  - 4-6 fully optimized blog posts/content pieces
  - Internal linking implementation
  - Metadata (titles, meta descriptions)
  - Related content recommendations

**Cadence**: 1st week of each month

### Stage 4.4: Monthly Performance Reporting
- **Agent**: monthly-reporting-agent
- **Input**: Analytics data + Google Ads + SEO rankings + conversions
- **Duration**: 1-2 days per month
- **Output**:
  - Traffic report (organic, paid, total)
  - Lead generation trends
  - Cost per lead analysis
  - Conversion rate trends
  - Page-level performance analysis
  - Competitor benchmarking

**Cadence**: 2nd week of each month

### Stage 4.5: Conversion Rate Optimization (Recurring)
- **Agent**: cro-analysis-agent
- **Input**: Conversion data + user behavior + traffic sources + performance trends
- **Duration**: 1-2 days per month
- **Output**:
  - CRO recommendations (A/B test ideas)
  - Landing page optimization priorities
  - Form optimization suggestions
  - User experience improvements
  - Quick wins

**Cadence**: 3rd week of each month (post-reporting)

---

## Timeline Summary

```
Week 1-2:   Phase 1 (Discovery) + Gate 1 approval
Week 2-3:   Phase 1 completion + Phase 2/3 kickoff
Week 3-5:   Phase 2 (Website) + Phase 3 (Ads) in parallel
Week 4-6:   Copy approval (Gate 2) + Design/Dev
Week 5-6:   Phase 3 ads strategy + landing page prep
Week 6-7:   Website launch + Ads campaign launch
Week 6+:    Phase 4 (SEO) monthly cadence begins
Ongoing:    Monthly content, reporting, optimization
```

---

## Success Criteria by Phase

**Phase 1**: 
- ✅ Positioning statement client-approved
- ✅ Messaging pillars documented
- ✅ Competitive advantage clearly articulated

**Phase 2**:
- ✅ Website launched and live
- ✅ All pages populated with copy
- ✅ Analytics tracking verified
- ✅ CTA forms working

**Phase 3**:
- ✅ Google Ads campaign live
- ✅ Quality Score 6+
- ✅ Initial performance baseline established
- ✅ Conversion tracking working

**Phase 4**:
- ✅ Content calendar approved
- ✅ Monthly content published on schedule
- ✅ Organic traffic trending upward
- ✅ Monthly reporting delivered
