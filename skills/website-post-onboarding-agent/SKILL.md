---
name: website-post-onboarding
description: "Market research, competitive positioning, strategic website brief, and homepage copy generation for new clients. Conducts deep market analysis, identifies positioning opportunity, creates concise website brief, and generates homepage copy. Integrates findings into Asana project as assigned tasks. Use when onboarding a new client to Rain Marketers."
user-invokable: true
argument-hint: "[client_name] [client_website_url]"
license: MIT
metadata:
  author: Rain Marketers
  version: "1.0.0"
  category: agency-workflow
---

# Website Post-Onboarding: Market Research + Positioning + Brief + Copy

## Process

1. **Gather Client Context & Locate Asana Project**
   - Client name, website URL
   - Search for Asana project by name (exact match or variation of client_name)
   - Extract business model, industry, target audience from website + onboarding form if available
   
2. **Market Research** (delegate to agent or run inline)
   - **Market Analysis**: Industry trends, market size, growth drivers, customer pain points
   - **Competitor Research**: Identify 5-7 direct competitors, analyze positioning, messaging, differentiators, pricing
   - **Customer Landscape**: Target audience segmentation, buying journey, decision-making criteria
   
3. **Positioning Strategy**
   - Analyze competitor positioning gaps
   - Identify client's unique value proposition
   - Find 2-3 positioning angles that differentiate from competitors
   - Recommend best-fit positioning based on market data
   
4. **Strategic Website Brief** (concise, efficient, not text-heavy)
   - Executive Summary: Recommended positioning, target audience, key differentiators
   - Messaging Pillars: 3-4 core messages based on positioning research
   - Brand Voice & Tone: Recommended voice based on industry + audience
   - Homepage Structure: Wireframe/outline of recommended sections
   - Call-to-Action Strategy: Primary + secondary CTAs based on conversion funnel
   - Success Metrics: 3-5 KPIs to track post-launch
   
5. **Homepage Copy**
   - Hero Section: Headline, subheadline, CTA (based on positioning)
   - Value Propositions: 3-4 key benefits with supporting copy
   - Social Proof / Credibility: Suggested proof elements
   - Final CTA: Bottom-of-page conversion prompt
   - Notes: SEO + conversion optimization tips
   
6. **Create Asana Tasks**
   - Task 1: "[Client] Market Research Findings" – Assign to Stevie
   - Task 2: "[Client] Website Brief" – Assign to Stevie
   - Task 3: "[Client] Homepage Copy (Draft)" – Assign to Stevie
   - Task 4: "[Client] Design & Development Kickoff" – Unassigned, awaiting design review
   - Add all research findings, brief, and copy to task descriptions
   
7. **Deliver Output**
   - Generate markdown report with all sections
   - Optionally generate PDF report for client presentation
   - Confirm tasks created in Asana

## Research Methodology

### Market Analysis
- Google Trends: Industry keyword trends + seasonality
- Industry reports: SaaS review sites, G2, Capterra, industry analysts
- Search behavior: Top-ranked pages in Google for industry keywords
- Market gaps: Which niches/segments are underserved?

### Competitor Analysis (5-7 competitors)
For each competitor:
- Website homepage messaging
- Positioning statement (explicit or inferred)
- Target audience (persona from messaging)
- Pricing model + price points
- Key differentiators mentioned
- Unique value props vs. generic competitors
- Website structure / CTAs

**Competitive Matrix**:
| Competitor | Target | Positioning | Price | Differentiator |
|------------|--------|-------------|-------|----------------|
| A | Enterprise | Speed + reliability | $X/mo | Custom integrations |
| B | SMB | Ease of use | $Y/mo | Free tier |
| C | ... | ... | ... | ... |

### Positioning Gaps
- What customer pain points are competitors addressing?
- Which segments are over-served vs. under-served?
- Where can the client own a unique positioning?

### Recommended Positioning Framework
- **Market Segment**: Who is the primary target?
- **Problem**: What pain point do they face?
- **Solution**: How does the client solve it?
- **Differentiation**: Why is the client better than alternatives?
- **Proof**: What evidence supports this claim?

## Output Files

- `MARKET-RESEARCH-FINDINGS.md` – Detailed market analysis, competitor matrix, positioning gaps
- `POSITIONING-STRATEGY.md` – Recommended positioning, audience, key messages
- `WEBSITE-BRIEF.md` – Strategic brief (executive summary, messaging, structure, KPIs)
- `HOMEPAGE-COPY.md` – Hero section + value props + copy
- `ASANA-TASKS.json` – Task details ready for import (or auto-created via Asana API)

## Asana Integration

**Trigger**: Pass `asana_project_gid` to automatically create tasks
**Tasks Created**:
1. Market Research Findings (with full research)
2. Website Brief (with brief document)
3. Homepage Copy - Draft (with copy)
4. Design & Development Kickoff (placeholder for design team)

**Assignee**: All research/content tasks assigned to `assignee_gid` for Stevie (configured at invocation)

**Dependencies**: (Optional) Link Homepage Copy → Brief → Market Research to show workflow

## Data Sources

- **Web Scraping**: Homepage analysis for competitors + client website
- **Google**: Trends, search behavior, SERP analysis
- **Public Databases**: G2, Capterra, Crunchbase, industry analyst reports
- **Social Proof**: LinkedIn, Twitter, reviews (if applicable)
- **Domain Research**: Whois, domain age, similar domains (optional)

## Configuration

```
client_name: "Clean Cut Gutters" (from input)
client_website: "https://cleancutgutters.com" (from input)
asana_project_lookup: "Clean Cut Gutters" or "Clean Cut Gutter..." (searches by name, auto-resolves to GID)
asana_assignee: "stevie@rainmarketers.com" (configured once)
research_depth: "deep" (5-7 competitors, full market analysis)
brief_format: "concise" (300-400 words, structured sections)
```

## Success Criteria

- ✅ Market research identifies 3+ positioning gaps
- ✅ Competitor analysis covers 5-7 relevant competitors
- ✅ Positioning strategy is defensible (based on market data)
- ✅ Website brief is concise (<1 page formatted, efficient structure)
- ✅ Homepage copy is conversion-focused with clear CTAs
- ✅ Asana tasks created and assigned within 1 hour of invocation
- ✅ All deliverables ready for handoff to design team

## Error Handling

| Scenario | Action |
|----------|--------|
| Client website unreachable | Use onboarding form data; note limitation in research |
| Asana project not found (invalid GID) | Report error, provide research/brief as downloadable files instead |
| Insufficient market data (niche industry) | Use available sources; acknowledge limitations in report |
| Too many competitors (crowded market) | Focus on top 7 by market share / relevance; note market saturation |

## PDF Report (Optional)

Use `/website-post-onboarding generate-report <project_gid>` to create a professional A4 PDF:
- Title page: Client name, positioning statement, date
- Market Analysis: Trends, market size, customer pain points
- Competitor Matrix: Comparison table with positioning
- Positioning Recommendation: Strategy with supporting evidence
- Website Brief: Executive summary + messaging pillars
- Homepage Copy: Ready-to-use copy blocks
- Appendix: Full competitor profiles

---

## Invocation

```bash
/website-post-onboarding "Clean Cut Gutters" "https://cleancutgutter.com"
```

**How it works:**
1. Uses client name to find Asana project (searches for exact match or variation)
2. Conducts market research, competitor analysis, positioning strategy
3. Generates website brief and homepage copy
4. Automatically creates Asana tasks assigned to Stevie with all findings

**Optional: Generate PDF Report**
```bash
/website-post-onboarding generate-report "Clean Cut Gutters"
```
Creates a professional A4 PDF with market analysis, positioning recommendation, brief, and copy.
