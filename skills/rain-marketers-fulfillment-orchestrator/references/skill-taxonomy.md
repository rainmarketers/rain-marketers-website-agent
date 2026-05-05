# Skill Taxonomy

Complete inventory of all AI skills in the Rain Marketers fulfillment system, organized by function and phase.

---

## Organizational Model

**3 Skill Categories**:
- 🔍 **Research Skills**: Analyze market, competition, audience, opportunities
- ✍️ **Creation Skills**: Write copy, build plans, create content
- 📊 **Analysis Skills**: Report performance, identify optimization, measure impact

---

## By Phase

### Phase 1: Discovery & Strategy

#### Research Skills
- **website-post-onboarding-agent** 🔍
  - **Purpose**: Initial client analysis and positioning development
  - **Input**: Client name, website, business type, target customer, pain points
  - **Output**: Website brief, positioning statement, messaging pillars, sitemap, content templates
  - **Duration**: 1-2 days
  - **Category**: Foundation research

- **onboarding-research-agent** 🔍
  - **Purpose**: Deep market, competitive, and audience research
  - **Input**: Positioning statement, target audience definition
  - **Output**: Competitive analysis, market trends, audience validation, messaging angles
  - **Duration**: 2-3 days
  - **Category**: Supporting research

---

### Phase 2: Website Creation

#### Creation Skills
- **website-copywriting-agent** ✍️
  - **Purpose**: Write all website copy aligned with positioning
  - **Input**: Website brief, messaging pillars, positioning, target audience
  - **Output**: Homepage copy, services copy, about/why-us copy, testimonial structures, FAQ
  - **Duration**: 3-4 days
  - **Category**: Website content creation
  - **Deliverables**: All page copy ready for design implementation

---

### Phase 3: Paid Advertising

#### Research Skills
- **google-ads-research-agent** 🔍
  - **Purpose**: Analyze paid search landscape and opportunities
  - **Input**: Positioning, target audience, market research
  - **Output**: Competitor ad analysis, keyword research, audience segments, CPC benchmarks
  - **Duration**: 2-3 days
  - **Category**: Ads research
  - **Feeds into**: Google Ads strategy

#### Strategy & Creation Skills
- **google-ads-strategy-agent** ✍️
  - **Purpose**: Build Google Ads campaign strategy
  - **Input**: Research output, business goals, pricing, budget
  - **Output**: Offer structure, messaging angles, audience segments, bid recommendations
  - **Duration**: 1-2 days
  - **Category**: Ads strategy
  - **Feeds into**: Landing page copywriting

- **google-ads-landing-page-copywriter** ✍️
  - **Purpose**: Write high-converting landing page copy
  - **Input**: Offer strategy, messaging angles, conversion objectives
  - **Output**: Landing page headline, subheadline, body copy, form copy, CTA variants
  - **Duration**: 1-2 days
  - **Category**: Landing page content
  - **Feeds into**: Design and campaign prep

- **google-ads-campaign-prep-agent** ✍️
  - **Purpose**: Prepare Google Ads campaign for launch
  - **Input**: Landing pages (designed), offer strategy, audience data
  - **Output**: Campaign structure, ad groups, keywords, audiences, bidding strategy, ad copy variants
  - **Duration**: 1-2 days
  - **Category**: Campaign preparation
  - **Deliverables**: Ready-to-launch campaign configuration

---

### Phase 4: SEO & Organic

#### Research Skills
- **seo-research-agent** 🔍
  - **Purpose**: Identify SEO opportunities and content gaps
  - **Input**: Website brief, positioning, business goals
  - **Output**: Keyword research, topic clusters, content gaps, quick-win opportunities
  - **Duration**: 2-3 days
  - **Category**: SEO research
  - **Feeds into**: Content planning

#### Strategy & Planning Skills
- **seo-content-planner-agent** ✍️
  - **Purpose**: Build 12-month content calendar
  - **Input**: SEO research, messaging pillars, business goals
  - **Output**: Content calendar (12 months), topic clusters, publishing schedule, keyword assignments
  - **Duration**: 2-3 days
  - **Category**: Content strategy
  - **Delivers**: 12-month roadmap for content creation

#### Creation Skills (Recurring Monthly)
- **seo-content-creator-agent** ✍️
  - **Purpose**: Create monthly optimized content
  - **Input**: Content plan for current month, previous month's performance
  - **Output**: 4-6 fully optimized blog posts/content pieces, metadata, internal linking
  - **Duration**: 3-5 days per month
  - **Cadence**: Monthly (Week 1)
  - **Category**: Content creation
  - **Deliverables**: Blog-ready content pieces

---

### Phase 4: Ongoing Optimization (Recurring Monthly)

#### Analysis Skills
- **monthly-reporting-agent** 📊
  - **Purpose**: Track and report monthly performance
  - **Input**: Website analytics, Google Ads data, SEO rankings, conversion data
  - **Output**: Performance report (traffic, leads, conversion rate, cost per lead), trends, insights
  - **Duration**: 1-2 days per month
  - **Cadence**: Monthly (Week 2)
  - **Category**: Performance reporting
  - **Feeds into**: CRO analysis

- **cro-analysis-agent** 📊
  - **Purpose**: Identify conversion optimization opportunities
  - **Input**: Performance data, user behavior, traffic sources, conversion bottlenecks
  - **Output**: CRO recommendations, A/B test ideas, landing page optimizations, quick wins
  - **Duration**: 1-2 days per month
  - **Cadence**: Monthly (Week 3)
  - **Category**: Conversion optimization
  - **Deliverables**: Actionable optimization roadmap

---

## By Function

### 🔍 Research Skills (Analyze market/competitors/audience)

| Skill | Phase | Input | Output |
|-------|-------|-------|--------|
| website-post-onboarding-agent | 1 | Business basics | Positioning + brief |
| onboarding-research-agent | 1 | Positioning | Market analysis + validation |
| google-ads-research-agent | 3 | Audience + positioning | Ads research + keywords |
| seo-research-agent | 4 | Business + goals | SEO opportunities + gaps |

**Total**: 4 research skills

---

### ✍️ Creation Skills (Write/plan content)

| Skill | Phase | Input | Output | Frequency |
|-------|-------|-------|--------|-----------|
| website-copywriting-agent | 2 | Website brief | All website copy | Once |
| google-ads-strategy-agent | 3 | Ads research | Campaign strategy | Once |
| google-ads-landing-page-copywriter | 3 | Ads strategy | Landing page copy | Once |
| google-ads-campaign-prep-agent | 3 | Landing pages + strategy | Campaign config | Once |
| seo-content-planner-agent | 4 | SEO research | 12-month calendar | Once |
| seo-content-creator-agent | 4 | Content plan + performance | Monthly content | Recurring (monthly) |

**Total**: 6 creation skills (1 recurring)

---

### 📊 Analysis Skills (Measure/optimize performance)

| Skill | Phase | Input | Output | Frequency |
|--------|-------|-------|--------|-----------|
| monthly-reporting-agent | 4+ | Analytics data | Performance report | Recurring (monthly) |
| cro-analysis-agent | 4+ | Performance + behavior | Optimization ideas | Recurring (monthly) |

**Total**: 2 analysis skills (both recurring)

---

## By Input/Output Type

### Input Types

**Web/Business Data**:
- Client website URL (website-post-onboarding-agent)
- Business basics (name, type, target, pain points)
- Analytics data (monthly-reporting-agent)

**Positioning/Strategy Data**:
- Positioning statement (all Phase 2-4 skills)
- Messaging pillars (content/ads/SEO skills)
- Market research (feeds into downstream skills)

**Performance Data**:
- Previous month's performance (seo-content-creator-agent, cro-analysis-agent)
- Conversion data (cro-analysis-agent)
- Traffic metrics (reporting and optimization)

### Output Types

**Strategic Documents**:
- Website brief (with positioning, messaging, sitemap)
- Google Ads strategy (offer + messaging angles)
- SEO strategy (keyword + topic roadmap)

**Copy/Content**:
- Website copy (homepage, services, about, etc.)
- Landing page copy
- Blog posts (4-6 per month)
- Campaign ad copy variants

**Analysis Reports**:
- Competitive analysis
- Market research
- Performance reports (monthly)
- CRO recommendations

**Configuration/Plans**:
- Content calendar (12 months)
- Campaign structure (audiences, keywords, bids)
- A/B test roadmap

---

## Skill Dependency Graph

```
website-post-onboarding-agent (FOUNDATION)
    ├─→ website-copywriting-agent
    ├─→ google-ads-research-agent
    │   └─→ google-ads-strategy-agent
    │       └─→ google-ads-landing-page-copywriter
    │           └─→ google-ads-campaign-prep-agent
    │
    └─→ seo-research-agent
        └─→ seo-content-planner-agent
            └─→ seo-content-creator-agent (recurring monthly)
                ├─→ monthly-reporting-agent
                │   └─→ cro-analysis-agent
                │
                └─→ cro-analysis-agent (consumes previous month data)
```

**Key observations**:
- 1 foundation skill (website-post-onboarding-agent) feeds all downstream skills
- 3 parallel research/strategy branches (website, ads, SEO)
- 2 recurring analysis skills that loop monthly
- Positioning context flows from top to bottom unchanged

---

## Skill Maturity & Status

### Core Skills (Fully Implemented)
✅ website-post-onboarding-agent
✅ onboarding-research-agent  
✅ website-copywriting-agent
✅ google-ads-research-agent
✅ google-ads-strategy-agent
✅ google-ads-landing-page-copywriter
✅ google-ads-campaign-prep-agent
✅ seo-research-agent
✅ seo-content-planner-agent
✅ seo-content-creator-agent
✅ monthly-reporting-agent
✅ cro-analysis-agent

### Extension Skills (Future Implementation)
- 🔄 email-outreach-agent (Phase 5: nurture sequences)
- 🔄 social-media-strategy-agent (Phase 5: organic social)
- 🔄 video-strategy-agent (Phase 5: video content)
- 🔄 partnership-development-agent (Phase 5: strategic partnerships)

---

## Skill Selection by Service Package

### Package 1: Website Only
Skills invoked:
- website-post-onboarding-agent
- onboarding-research-agent
- website-copywriting-agent

Deliverables: Website brief + live website

### Package 2: Website + Paid Ads
Skills invoked:
- website-post-onboarding-agent
- onboarding-research-agent
- website-copywriting-agent
- google-ads-research-agent
- google-ads-strategy-agent
- google-ads-landing-page-copywriter
- google-ads-campaign-prep-agent

Deliverables: Website + Google Ads campaign

### Package 3: Full Service (Website + Ads + SEO)
Skills invoked:
- All 12 core skills listed above

Deliverables: Website + Google Ads + Monthly SEO/reporting (ongoing)

---

## Total Skill Inventory

- **Total Core Skills**: 12
- **One-time Skills**: 10
- **Recurring Skills**: 2 (monthly cadence)
- **Expected Future Extensions**: 4

**Total Person-Hours per Service**:
- Website only: ~40-60 hours
- Website + Ads: ~60-100 hours
- Full service: ~100-150 hours (first month) + 30-40 hours monthly (recurring)
