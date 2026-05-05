# SEO Content Creator Agent

**Execute monthly content plan: write, optimize, publish 4-6 articles**

Executes the 12-month content calendar monthly: researches, writes, optimizes, and publishes 4-6 fully SEO-optimized articles per month based on the content plan.

---

## What It Does

Executes Phase 4.3 of service fulfillment: Produces monthly content (4-6 articles) that executes the strategic content calendar created in Phase 4.2.

**Input**: SEO content calendar (from seo-content-planner-agent) + previous month performance data + client website context

**Output**: 4-6 published blog posts, optimized for target keywords, with internal links implemented, tracked for performance monitoring

---

## Execution

### Stage 1: Content Research & Outlining (2-3 days)
- **Per article**:
  - Research target keyword and related topics
  - Analyze top 10 SERP results (what they cover, gaps, depth)
  - Identify proof points (data, case studies, expert quotes)
  - Create detailed article outline
  - Determine visual requirements (images, charts, diagrams)

**Output**: Content outlines for all 4-6 articles with research notes and SERP analysis

### Stage 2: Article Writing (3-4 days)
- **Per article**:
  - Write 2,000-5,000 word article matching outline
  - Integrate primary and secondary keywords naturally
  - Add H2/H3 headers for scanability
  - Embed social proof (stats, testimonials, case studies)
  - Include clear CTAs (links to conversion pages, offers)
  - Add internal links to pillar pages and related articles

**Approach**: Reader-focused, benefit-driven, proof-heavy copy that satisfies search intent while driving conversions

**Output**: 4-6 complete, publication-ready articles

### Stage 3: SEO Optimization (1-2 days)
- **Per article**:
  - Optimize meta title (55-60 chars) with primary keyword
  - Optimize meta description (155-160 chars) with call-to-action
  - Set internal link anchors to related articles and conversion pages
  - Ensure H1 tag present and keyword-focused
  - Validate keyword density (1-2% for primary, natural for LSI)
  - Add schema markup (Article, BreadcrumbList, FAQSchema if applicable)
  - Optimize alt text for all images

**Output**: Fully optimized articles ready for publishing platform

### Stage 4: Publishing & Promotion (0.5-1 days)
- **Per article**:
  - Publish to blog with scheduled date
  - Update sitemap with new URLs
  - Submit to Google Search Console (Indexing API)
  - Share on social channels
  - Notify subscribers (if applicable)
  - Track initial impressions

**Output**: Live articles, indexed in search, social promotion scheduled

---

## Input Format

```json
{
  "content_calendar": {
    "month": "January",
    "articles": [
      {
        "title": "Article Title",
        "primary_keyword": "keyword",
        "secondary_keywords": ["keyword2", "keyword3"],
        "word_count": 2500,
        "content_type": "blog_post",
        "publication_date": "2026-01-15",
        "internal_links": ["url1", "url2", "url3"]
      }
    ]
  },
  "previous_month_performance": {
    "top_articles": [...],
    "low_performing": [...],
    "traffic_trends": "..."
  },
  "client_context": {
    "website_url": "...",
    "target_audience": "...",
    "tone_of_voice": "..."
  }
}
```

---

## Output Format

```markdown
# Month [X] Content Production Report

## Overview
- Articles published: [X]
- Total words: [X]
- Topics covered: [List]
- Internal links created: [X]
- Estimated combined monthly searches: [X]

## Article 1: [Title]

**Publication Date**: [Date]
**Primary Keyword**: [Keyword]
**Target Difficulty**: [Low/Medium/High]
**Article Link**: [URL]

**Metrics**:
- Word count: [X]
- H2 headers: [X]
- Images: [X]
- Internal links: [X]

**Internal Linking Strategy**:
- Links to pillar: [Anchor → URL]
- Links to cluster: [Anchor → URL]
- Links from other articles: [Incoming links]

**SEO Elements**:
- Meta title: [Title]
- Meta description: [Description]
- Schema markup: Article, BreadcrumbList
- Alt text: [Sample]

---
## [Repeat for all articles published this month]

## Publishing Checklist

- [ ] All articles written and edited
- [ ] SEO optimization completed (meta, headers, keywords)
- [ ] Internal links verified (no broken links)
- [ ] Images optimized and alt text added
- [ ] Schema markup implemented
- [ ] Articles published and indexed
- [ ] Sitemap updated
- [ ] Google Search Console notified
- [ ] Social promotion scheduled
- [ ] Subscriber notification sent (if applicable)

## Performance Targets

**By end of month**:
- All articles indexed in Google
- Initial impressions tracked
- Average CTR: [X%]

**By month 3**:
- Quick-win articles ranking positions 5-10
- Cluster articles beginning to rank
- Cumulative traffic from this month's articles: [X visits]

**By month 6**:
- Articles trending toward top-20 rankings
- Contributing [X]% to overall organic traffic

## Next Steps

- Monitor article performance daily
- Track keyword rankings weekly
- Update underperforming articles monthly
- Build backlinks to top performers
- Plan next month content based on performance data
```

---

## Success Criteria

✅ **4-6 articles published** per month as scheduled  
✅ **All articles optimized** (meta, headers, keywords, schema)  
✅ **Internal linking implemented** (2-3 links per article)  
✅ **Articles indexed** in Google within 48 hours  
✅ **Images optimized** (size, alt text, format)  
✅ **Social promotion executed** (Twitter, LinkedIn, etc.)  
✅ **Performance tracked** from day 1 (impressions, CTR, rankings)  

---

## Recurring Schedule

**Monthly cadence** (every month):
- Weeks 1-2: Research & write articles
- Week 3: Optimize & publish
- Week 4: Monitor & promote

**Monitoring continues** throughout month (rankings, traffic, engagement)

---

## Feeds Into

- Monthly performance reporting (seo-monthly-reporting-agent consumes traffic data)
- CRO optimization (cro-analysis-agent uses traffic data to identify conversion opportunities)
- Backlink prospecting (top-performing articles become link-building targets)
- Long-term topical authority (cumulative articles strengthen domain expertise)
