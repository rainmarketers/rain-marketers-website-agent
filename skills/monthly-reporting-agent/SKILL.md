# Monthly Reporting Agent

**Produce monthly performance reports across all channels**

Aggregates analytics, ads performance, SEO results, and conversion data into unified monthly reports showing what's working, what needs optimization, and ROI across all channels.

---

## What It Does

Executes Phase 4.4 of service fulfillment: Produces monthly performance reports that track progress toward goals across Google Ads, SEO, website conversions, and overall campaign health.

**Input**: GA4 organic traffic + Google Ads performance + conversion data + SEO rankings + CMS article metrics

**Output**: Monthly performance report with KPI dashboard, channel performance breakdown, budget ROI, and trend analysis

---

## Execution

### Stage 1: Data Collection & Aggregation (1 day)
- **Google Ads data**:
  - Impressions, clicks, CTR by ad group
  - Conversions, CPA, ROAS by campaign
  - Budget spent vs. daily budget
  - Quality Score trends

- **SEO data**:
  - Keywords tracked in top 100 / top 20 / top 10
  - Organic traffic (users, sessions, revenue)
  - New articles indexed and ranking progress
  - Backlinks acquired this month

- **Conversion data**:
  - Form submissions by source (Ads, Organic, Direct)
  - Phone call conversions
  - Booking conversions
  - Lead value and customer acquisition cost

- **Website data**:
  - Page views, sessions, bounce rate
  - Top performing pages (by traffic, by conversion)
  - Mobile vs desktop performance
  - Core Web Vitals scores

**Output**: Raw data compilation from all sources

### Stage 2: Performance Analysis (1 day)
- **Calculate KPIs**:
  - Total conversions by source
  - Overall ROAS (revenue / ad spend)
  - Overall CAC (cost per acquisition)
  - Conversion rate by channel
  - Average lead value
  - Traffic growth month-over-month, year-over-year

- **Trend analysis**:
  - What's trending up? What's trending down?
  - Which channels are most profitable?
  - Which campaigns/articles underperforming?
  - Seasonality patterns (if applicable)

- **Benchmark comparison**:
  - Performance vs. industry benchmarks
  - Performance vs. previous month
  - Performance vs. goal targets

**Output**: Analysis dashboard with trends and insights

### Stage 3: Report Generation (1 day)
- **Create professional report**:
  - Executive summary (1 page)
  - Key metrics dashboard (visuals)
  - Channel performance breakdown (Ads, SEO, Direct)
  - Conversion funnel analysis
  - Budget & ROI summary
  - Top performers (articles, ads, keywords)
  - Issues & risks (underperforming campaigns)
  - Month-over-month comparison

- **Include visualizations**:
  - Revenue by channel (pie chart)
  - Traffic trends (line chart)
  - Conversion funnel (waterfall)
  - Cost per acquisition by channel
  - Keyword performance matrix

**Output**: PDF report (15-20 pages)

### Stage 4: Insights & Recommendations (1 day)
- **Identify quick wins**:
  - Top-performing ads (scale budget)
  - High-traffic, low-conversion pages (optimize)
  - Underperforming keywords (pause or improve)
  - Articles ranking positions 5-15 (build links to push to top 3)

- **Flag risks**:
  - Declining trends (investigate cause)
  - Low Quality Score ads (improve copy/landing page)
  - Articles not ranking after 2 months (rewrite or backlink)

- **Recommend actions** for next month

**Output**: Executive summary + action items list

---

## Input Format

```json
{
  "reporting_period": {
    "start_date": "2026-01-01",
    "end_date": "2026-01-31",
    "month": "January"
  },
  "google_ads_data": {
    "campaigns": [...],
    "total_spend": 0,
    "total_conversions": 0,
    "total_revenue": 0
  },
  "seo_data": {
    "organic_traffic": 0,
    "new_keywords_top100": 0,
    "articles_published": 0,
    "top_keywords": [...]
  },
  "conversion_data": {
    "form_submissions": 0,
    "phone_calls": 0,
    "booking_conversions": 0,
    "total_lead_value": 0
  },
  "website_data": {
    "total_sessions": 0,
    "bounce_rate": 0,
    "conversion_rate": 0
  }
}
```

---

## Output Format

```markdown
# Monthly Performance Report - [Month Year]

## Executive Summary

**Reporting Period**: [Date Range]

**Key Metrics**:
- Total conversions: [X]
- Total revenue: $[X]
- Total spend: $[X]
- Overall ROAS: [X:1]
- Cost per acquisition: $[X]
- Traffic: [X] sessions ([+X%] vs last month)

**Month Status**: [On Track / At Risk / Off Track]

---

## Performance by Channel

### Google Ads
**Budget**: $[X] ([+X%] vs last month)
**Conversions**: [X] ([+X%] vs last month)
**ROAS**: [X:1]
**Quality Score**: [X] avg
**Status**: [Performing / Needs Optimization]

**Top Performing**:
- Campaign: [Name] → ROAS [X:1]
- Ad group: [Name] → CTR [X%]

**Needs Optimization**:
- [Campaign] → Quality Score [X] (improve landing page)
- [Keyword] → CPC $[X] (consider pausing)

### Organic (SEO)
**Organic traffic**: [X] users ([+X%] vs last month)
**Conversions**: [X] ([+X%] vs last month)
**Articles published**: [X]
**New keywords top 100**: [X]
**New keywords top 20**: [X]

**Top Performers**:
- Article: "[Title]" → [X] users, [X] conversions
- Keyword: "[Keyword]" → Position [X], [X] clicks

**Underperformers**:
- Article: "[Title]" → Position [X+], no conversions (Action: build links or rewrite)
- Keyword: "[Keyword]" → Position [X+] (Action: update article)

### Direct & Other
**Sessions**: [X] ([+X%] vs last month)
**Conversions**: [X] ([+X%] vs last month)

---

## Conversion Analysis

**Total Conversions**: [X]
- From Ads: [X] ([X]%)
- From Organic: [X] ([X]%)
- From Direct/Other: [X] ([X]%)

**Conversion by Type**:
- Form submissions: [X]
- Phone calls: [X]
- Bookings: [X]

**Average Lead Value**: $[X]
**Best Performing Lead Source**: [Ads / Organic / Direct]
**CAC by Source**:
- Ads: $[X]
- Organic: $[X]
- Direct: $[X]

---

## Budget & ROI Summary

**Total Spend**: $[X]
- Google Ads: $[X] ([X]%)
- SEO (monthly execution): $[X] ([X]%)

**Total Revenue Generated**: $[X]
**Net ROI**: [X%] ([X:1])
**Payback Period**: [X] days

**Monthly Recurring Revenue**: $[X]

---

## Traffic & Engagement

**Total Sessions**: [X] ([+X%] vs last month)
**Total Users**: [X] ([+X%] vs last month)
**Pages/Session**: [X]
**Avg Session Duration**: [X] sec
**Bounce Rate**: [X]%

**Top Pages** (by traffic):
1. [Page] - [X] sessions ([X]% conversion)
2. [Page] - [X] sessions ([X]% conversion)
3. [Page] - [X] sessions ([X]% conversion)

**Top Pages** (by conversion):
1. [Page] - [X] conversions
2. [Page] - [X] conversions
3. [Page] - [X] conversions

---

## Issues & Risks

**Red Flags** 🚩:
- [Issue]: [Impact] → Recommended action: [Action]
- [Issue]: [Impact] → Recommended action: [Action]

**Yellow Flags** ⚠️:
- [Issue]: [Impact] → Monitor and review next month

---

## Recommendations for Next Month

**High Priority** (do immediately):
1. [Action] - Expected impact: [Metric] +[X%]
2. [Action] - Expected impact: [Metric] +[X%]

**Medium Priority** (do if time allows):
1. [Action]
2. [Action]

**To Investigate**:
1. [Trend or anomaly]
2. [Trend or anomaly]

---

## Looking Ahead

**Goals for Next Month**:
- Conversions: [Target]
- Revenue: $[Target]
- Organic traffic: [Target]
- Ads ROAS: [Target]

**Content Planned**:
- [X] articles to publish (targeting [X] keywords)
- Topics: [List]

**Ads Tests Planned**:
- [Test description]
- [Test description]
```

---

## Success Criteria

✅ **Report delivered by 5th of following month** (timely reporting)  
✅ **All data sources verified** (Ads, SEO, GA4, conversions accurate)  
✅ **Executive summary included** (one-page quick reference)  
✅ **Visualizations included** (charts, dashboards)  
✅ **Trend analysis included** (month-over-month, what's trending)  
✅ **Action items documented** (clear recommendations for next month)  
✅ **ROI calculated** (spend vs. revenue/conversions)  

---

## Recurring Schedule

**Monthly** (on or before 5th of following month):
- Month 1-12: Generate full report with all channels
- Month 3, 6, 9, 12: Include quarterly analysis

---

## Feeds Into

- CRO analysis (cro-analysis-agent uses performance data to identify optimization opportunities)
- Client communication (report sent to client for monthly review)
- Budget reallocation (underperforming channels adjusted)
- Strategy refinement (next month's strategy adjusted based on results)
