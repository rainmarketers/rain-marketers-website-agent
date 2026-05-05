# SEO Content Planner Agent

**Build 12-month SEO content calendar**

Translates SEO research into a structured, long-term content plan with topics, keywords, publishing schedule, and internal linking strategy.

---

## What It Does

Executes Phase 4.2 of service fulfillment: Creates 12-month content roadmap that guides ongoing content creation and ensures strategic coverage of keyword opportunities.

**Input**: SEO research + messaging pillars + business goals

**Output**: 12-month content calendar, topic clusters, publishing schedule, keyword assignments, internal link map

---

## Execution

### Stage 1: Build Content Calendar (1 day)
- **Map content across 12 months** with:
  - Publication date
  - Topic and keyword target
  - Content type (blog post, guide, case study, etc.)
  - Expected word count
  - Internal linking targets

- **Distribute strategically**:
  - Weeks 1-2: Quick wins (easy-to-rank content)
  - Weeks 3-8: Core pillar content
  - Weeks 9-52: Ongoing supporting content
  - Seasonal/timely topics at appropriate months

**Output**: 12-month calendar (40-60 articles planned)

### Stage 2: Topic Cluster Mapping (0.5 days)
- **Define pillar pages** (broad topics)
- **Assign supporting content** to clusters
- **Plan internal linking** (how pages connect)

**Output**: Topic cluster diagram with internal link map

### Stage 3: Keyword Assignment (1 day)
- **Per article**:
  - Primary keyword (target keyword)
  - Secondary keywords (related terms)
  - LSI keywords (semantic variations)

**Output**: Keyword assignment spreadsheet

### Stage 4: Content Sequencing (0.5 days)
- **Determine optimal order**:
  - What content supports conversion (pillar pages first)
  - What content builds topical authority (cluster building)
  - What seasonal content runs when
  - Dependencies (which articles should come first)

**Output**: Sequenced content plan with rationale

---

## Input Format

```json
{
  "seo_research": {
    "keyword_opportunities": [...],
    "topic_clusters": [...],
    "quick_wins": [...],
    "content_gaps": [...]
  },
  "messaging_pillars": [...],
  "business_goals": {
    "target_leads_monthly": 0,
    "growth_targets": "..."
  }
}
```

---

## Output Format

```markdown
# SEO Content Calendar - 12 Month Plan

## Overview
- Total articles planned: [X]
- Content types: [Blog, Guides, Case studies, etc.]
- Focus areas: [Topic clusters]
- Expected organic traffic impact: [Target]

## Content Calendar

### Month 1: [Month Name]
**Week 1-2** (Quick wins - Easy to rank)
- **Article 1**: [Title]
  - Primary keyword: [Keyword]
  - Word count: [X]
  - Internal links: [Links to]
  - Expected ranking difficulty: Low
  - Publication date: [Date]

- **Article 2**: [Title]
  - [Details]

**Week 3-4** (Core content)
- **Article 3**: [Title]
  - [Details]

### [Repeat for all 12 months]

## Topic Cluster Map

```
Pillar: Gutter Cleaning Guide
├─ Supporting: When to Clean Gutters → Links to Pillar
├─ Supporting: Signs Your Gutters Need Cleaning → Links to Pillar
├─ Supporting: DIY vs Professional → Links to Pillar
└─ Supporting: How Often to Clean → Links to Pillar
```

## Publishing Schedule

**Monthly cadence**:
- **Week 1**: Quick-win articles (2-3 posts)
- **Week 2**: Cluster-building articles (1-2 posts)
- **Week 3**: Seasonal/timely content (1-2 posts)
- **Week 4**: Internal linking optimization (updates)

**Monthly totals**: 4-6 articles per month = 48-72 articles/year

## Keyword Assignment by Month

| Month | Article | Primary Keyword | Difficulty | Expected Ranking Time |
|-------|---------|-----------------|------------|----------------------|
| Month 1 | Article 1 | [Keyword] | Low | 4-8 weeks |
| Month 1 | Article 2 | [Keyword] | Medium | 8-12 weeks |

## Internal Linking Strategy

**Strategy**:
- Each article links to 2-3 related articles
- Pillar pages receive 3-5 internal links from cluster articles
- Cross-cluster linking for broader topical authority

**Example**:
- Article: "When to Clean Gutters" links to:
  - Pillar: "Gutter Cleaning Guide"
  - Related: "Signs Your Gutters Need Cleaning"
  - Conversion: "Schedule Your Free Inspection"

## Expected Outcomes

**By Month 3**:
- 10-15 articles published
- Quick-win articles ranking (positions 5-10)
- Topical authority building

**By Month 6**:
- 25-30 articles published
- Core pillar pages ranking (positions 1-5 for main keywords)
- 20-30% organic traffic increase expected

**By Month 12**:
- 48-72 articles published
- Strong topical authority established
- 50-100% organic traffic increase expected
- Monthly organic conversions trending up

## Content Maintenance Notes

**Every month**:
- Review previous month's performance
- Adjust strategy based on what's working
- Backlink prospecting for top-performing articles
- Update older content with latest information
```

---

## Success Criteria

✅ **12-month calendar created** (40-60+ articles planned)  
✅ **Topic clusters defined** with internal linking  
✅ **Keywords assigned** to each article  
✅ **Content sequenced** strategically  
✅ **Realistic publishing cadence** (4-6 articles/month)  
✅ **Mix of content types** (blog, guides, case studies)  

---

## Approval Gate 4

**Required**: Client reviews content plan + topics
- Does content plan align with business goals?
- Are topics relevant to their offerings?
- Is publishing cadence realistic for their team?
- Any topics they'd like to add/remove?

---

## Feeds Into

- seo-content-creator-agent (executes content plan monthly)
- Monthly content production
- Long-term SEO strategy success
