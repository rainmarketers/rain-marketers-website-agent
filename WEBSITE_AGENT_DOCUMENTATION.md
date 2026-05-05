# Website Post-Onboarding Agent – Complete Documentation

## Overview

The Website Post-Onboarding Agent is the first step in Rain Marketers' service fulfillment workflow. It handles deep market research, competitive analysis, positioning strategy, website brief creation, and homepage copy generation for new clients.

**Purpose**: Provide strategic website planning grounded in real market data before design/development begins.

**Timeline**: ~2-3 hours per client (research + brief + copy)

**Output**: Research findings, positioning strategy, website brief, homepage copy, and Asana tasks ready for design handoff

---

## Process Flow

```
Client Onboarding Form
        ↓
Create Asana Project (client name)
        ↓
Run Agent: /website-post-onboarding-agent "Client" "URL"
        ↓
[Agent Steps]:
  1. Gather context (website, onboarding form, industry)
  2. Market research (trends, market size, pain points)
  3. Competitor analysis (5-7 competitors)
  4. Positioning gaps analysis
  5. Recommended positioning strategy
  6. Create website brief (strategic, concise)
  7. Write homepage copy (hero, value props, CTAs)
  8. Create Asana tasks (assign to Stevie)
        ↓
Research Findings + Brief + Copy
        ↓
Asana Tasks Created (Stevie reviews)
        ↓
Handoff to Design Team
```

---

## Agent Inputs

### Required
- **client_name**: Client company name (e.g., "Clean Cut Gutters")
- **client_website**: Client website URL (e.g., "https://cleancutgutters.com")

### Auto-Detected
- **Asana project GID**: Agent searches for project by client name
- **Industry**: Agent infers from website + onboarding form
- **Target audience**: Agent infers from website messaging + form

### Optional (from onboarding form)
- Business model (B2B, B2C, hybrid)
- Service area / geography
- Key differentiators (claimed by client)
- Pricing model
- Current marketing channels
- Biggest pain points

---

## Agent Outputs

### 1. Market Research Findings
**File**: `MARKET-RESEARCH-FINDINGS.md`

Contents:
- **Industry Overview**: Market size, growth rate, key trends
- **Market Dynamics**: Customer pain points, buying behavior, decision criteria
- **Competitive Landscape**: 5-7 competitor analysis with matrix
- **Positioning Gaps**: Where competitors are clustering and where whitespace exists
- **Customer Segments**: Recommended target audience based on market data

### 2. Positioning Strategy
**File**: `POSITIONING-STRATEGY.md`

Contents:
- **Recommended Positioning**: Market segment + problem + solution + differentiation + proof
- **Supporting Evidence**: Data from market research justifying the positioning
- **Competitive Advantage**: Why this positioning wins vs. alternatives
- **Audience Profile**: Who should the website target
- **Key Messages**: 3-4 core messages derived from positioning

### 3. Website Brief
**File**: `WEBSITE-BRIEF.md`

Contents (concise, ~400 words formatted):
- **Executive Summary**: Client name, recommended positioning, target audience
- **Messaging Pillars**: 3-4 core messages
- **Brand Voice & Tone**: How the brand should sound
- **Homepage Structure**: Recommended sections (hero, value props, social proof, CTA)
- **Call-to-Action Strategy**: Primary + secondary CTAs
- **Success Metrics**: 3-5 KPIs to track post-launch
- **Sitemap**: Recommended page structure

### 4. Homepage Copy
**File**: `HOMEPAGE-COPY.md`

Contents:
- **Hero Section**: Headline, subheadline, CTA (conversion-focused)
- **Value Propositions**: 3-4 benefits with supporting copy
- **Social Proof / Credibility**: Suggested proof elements
- **Final CTA**: Bottom-of-page conversion prompt
- **Technical Notes**: SEO + conversion optimization tips

### 5. Asana Tasks
**Created automatically in Asana**:

1. **[Client] Market Research Findings**
   - Assignee: Stevie
   - Description: Full market research, competitor matrix
   - Status: Ready for review

2. **[Client] Website Brief**
   - Assignee: Stevie
   - Description: Strategic brief document
   - Status: Ready for review

3. **[Client] Homepage Copy - Draft**
   - Assignee: Stevie
   - Description: Copy ready for editing/refinement
   - Status: Ready for review

4. **[Client] Design & Development Kickoff**
   - Assignee: Unassigned (for design team)
   - Description: Design brief + approved homepage copy
   - Status: Awaiting design review

---

## Data Sources & Methodology

### Market Research
- **Google Trends**: Keyword trends, seasonality, growth
- **Industry Reports**: Analyst reports, SaaS benchmarks, industry publications
- **SERP Analysis**: Top-ranking content for industry keywords
- **Social Signals**: LinkedIn, Twitter, industry forums

### Competitor Analysis (5-7 competitors)
For each competitor, the agent analyzes:
- Homepage messaging + positioning statement
- Target audience (inferred from messaging)
- Pricing model + price points
- Claimed differentiators
- Website structure and CTAs
- Industry reputation

**Competitive Matrix Output**:
| Competitor | Segment | Positioning | Price | Differentiator |
|------------|---------|-------------|-------|----------------|
| A | Enterprise | Reliability + scale | $X/mo | Custom integrations |
| B | SMB | Ease of use | $Y/mo | Free tier |
| C | ... | ... | ... | ... |

### Positioning Framework
The agent uses this framework to recommend positioning:

1. **Market Segment**: Who is the primary target?
2. **Problem**: What pain point do they face?
3. **Solution**: How does the client solve it?
4. **Differentiation**: Why is the client better?
5. **Proof**: What evidence supports the claim?

---

## Quality Standards

See [Quality Standards](./skills/website-post-onboarding-agent/references/quality-standards.md) for:
- What constitutes good market research
- Standards for positioning strategy
- Brief structure and conciseness guidelines
- Copy quality expectations

---

## Example Output

See [Example Website Brief](./skills/website-post-onboarding-agent/references/example-website-brief.md) for a complete real-world example showing market research, positioning, brief, and copy.

---

## Configuration & Setup

### Asana Integration
The agent creates tasks in the client's Asana project. Requirements:
- **Project must exist** with client name (or variation)
- **Assignee**: Stevie (configured as default)
- **Custom fields** (optional): Priority, Status, Due Date

### Credentials
No API credentials required for basic operation. Optional:
- **Asana PAT** (for task creation with detailed descriptions)
- **Google Trends API** (for more precise trend data)

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| "Asana project not found" | Verify project exists with client name in Asana |
| "Website unreachable" | Check URL format; use full HTTPS URL |
| "Insufficient market data" | Industry may be niche; agent uses available sources |
| "Too many competitors" | Agent focuses on top 7 by relevance |

---

## Future Enhancements

Planned additions to the system:
- **Pricing Strategy Agent** – Recommend pricing model based on market data
- **Competitive Brief Agent** – Deep-dive on specific competitor for positioning defense
- **Content Strategy Agent** – Blog planning based on positioning + SEO keywords
- **Visual Brand Agent** – Color, typography, imagery recommendations
- **Conversion Optimization Agent** – CTA testing + funnel strategy

---

## Best Practices

1. **Use complete onboarding forms**: More data = better positioning strategy
2. **Review Asana tasks before design**: Brief and copy should be reviewed/approved
3. **Validate assumptions with client**: Position should align with client's market knowledge
4. **Reference quality standards**: Use [Quality Standards](./skills/website-post-onboarding-agent/references/quality-standards.md) when reviewing output
5. **Iterate if needed**: Position can be refined if market data suggests different approach

---

## Related Documentation

- [Agent Prompt Guide](./skills/website-post-onboarding-agent/references/agent-prompt-guide.md) – How the agent processes information
- [Competitor Analysis Methodology](./skills/website-post-onboarding-agent/references/competitor-analysis.md) – Detailed analysis framework
- [Onboarding Form Fields](./skills/website-post-onboarding-agent/references/onboarding-form-fields.md) – What to ask new clients
- [Sitemap Builder](./skills/website-post-onboarding-agent/references/sitemap-builder.md) – Recommended page structures
- [Page Content Templates](./skills/website-post-onboarding-agent/references/page-content-templates.md) – Copy frameworks for common pages
