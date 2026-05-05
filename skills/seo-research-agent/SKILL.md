# SEO Research Agent

**Identify SEO opportunities, keywords, and content gaps**

Analyzes search landscape to identify keyword opportunities, topic clusters, and content gaps where the site can rank.

---

## What It Does

Executes Phase 4.1 of service fulfillment: Researches long-term organic search opportunities and creates foundation for content strategy.

**Input**: Website brief + positioning + business goals

**Output**: Keyword opportunities, topic clusters, content gap analysis, quick-win opportunities

---

## Execution

### Stage 1: Keyword Research (1 day)
- **Identify 50-100 relevant keywords** across intent levels:
  - High-intent keywords (ready to buy/book)
  - Mid-intent keywords (considering)
  - Educational keywords (learning/researching)

- **Per keyword analyze**:
  - Monthly search volume
  - Keyword difficulty (how hard to rank)
  - Commercial value (will lead convert?)
  - Current ranking position (if any)
  - Recommended page type

**Output**: Comprehensive keyword research spreadsheet

### Stage 2: Competitor Content Analysis (0.5 days)
- **Tasks**:
  - Who ranks for target keywords?
  - What content do they have?
  - What gaps exist in their content?
  - What topics do they avoid?

**Output**: Competitor content matrix

### Stage 3: Topic Clustering (1 day)
- **Define pillar pages** (broad topics covering a subject)
- **Identify supporting content** (specific subtopics)
- **Map internal linking structure** (how pages relate)

**Example**:
```
Pillar: "Gutter Cleaning Guide"
  ├─ When to clean gutters
  ├─ Signs your gutters need cleaning
  ├─ DIY vs professional
  └─ How often to clean
```

**Output**: Topic cluster map (3-5 clusters)

### Stage 4: Content Gap Analysis (0.5 days)
- **Identify opportunities**:
  - What competitors rank for that we don't
  - What topics have high search volume but weak competition
  - What educational content would support conversion pages
  - What local/specific content would help

**Output**: Priority content opportunities ranked by impact

---

## Input Format

```json
{
  "website_brief": {...},
  "positioning": {...},
  "business_goals": {
    "target_leads_monthly": 0,
    "service_area": "..."
  },
  "industry": "..."
}
```

---

## Output Format

```markdown
# SEO Research & Strategy

## Keyword Opportunities (50-100 keywords)

**High-Intent Keywords** (ready to book/buy):
- [Keyword 1]: [Vol] searches/month, [Difficulty], [Ranking potential]
- [Keyword 2]: [Vol] searches/month, [Difficulty], [Ranking potential]

**Mid-Intent Keywords** (considering):
- [Keyword]: [Vol], [Difficulty]

**Educational Keywords** (learning):
- [Keyword]: [Vol], [Difficulty]

## Topic Clusters (3-5)

### Cluster 1: [Main Topic]
**Pillar Page**: [Main topic content page]
**Supporting Content**:
- Subtopic 1
- Subtopic 2
- Subtopic 3
(Internal links show relationships)

## Competitor Analysis

**Top Ranking Competitors**:
- [Competitor 1]: Ranks for [keywords], has [content types]
- [Competitor 2]: Strong on [topics], weak on [topics]

**Content Gaps**:
- No one ranks for [keyword] → opportunity
- Weak competition on [topic] → quick win
- High search volume, weak content → high impact opportunity

## Content Gap Opportunities

**High Priority** (high volume + low competition):
1. [Topic] - [Monthly searches], [Why it's a gap]
2. [Topic] - [Monthly searches], [Why it's a gap]

**Medium Priority** (medium volume + moderate competition):
1. [Topic]
2. [Topic]

**Quick Wins** (easy to execute, high impact):
1. FAQ content
2. Seasonal guide
3. Local service pages

## SEO Audit Results

**Current state**:
- [X] pages indexed
- [Y] pages ranking (top 100)
- [Z] pages ranking (top 10)

**Opportunities**:
- Fix on-page SEO for [pages]
- Add internal links to [pages]
- Improve page speed (currently [X ms])
- Mobile optimization needed on [pages]
```

---

## Research Methods

- Keyword planner tools (search volume, CPC data)
- SERP analysis (who ranks, what content they have)
- Competitor analysis (what topics they cover)
- Search intent analysis (what do searchers want?)
- Industry trend research

---

## Success Criteria

✅ **50-100 relevant keywords** researched  
✅ **Content gaps identified** vs competitors  
✅ **3-5 topic clusters defined** with pillar pages  
✅ **Quick wins identified** (easy, high-impact content)  
✅ **Priority ranked** (what to tackle first)  
✅ **Difficulty assessed** (difficulty per keyword)  

---

## Feeds Into

- seo-content-planner-agent (uses keyword + cluster data)
- Content strategy for entire site
- Blog topic prioritization
