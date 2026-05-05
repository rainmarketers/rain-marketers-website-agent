# Rain Marketers Service Fulfillment Orchestrator

**The main "brain" that coordinates all Rain Marketers service delivery.**

Orchestrates a complete workflow from client onboarding through monthly optimization, managing research, content creation, strategy, campaign execution, and reporting.

---

## What It Does

Routes client projects through a coordinated multi-skill workflow, passing context between specialized agents and managing human approval gates.

**Input**: Client name + website (triggers full service delivery)

**Output**: Integrated fulfillment plan with all deliverables, timelines, and Asana project structure

---

## Service Fulfillment Workflow

```
PHASE 1: DISCOVERY & STRATEGY (Weeks 1-2)
├─ onboarding
├─ research (AI)
└─ website brief (AI)
    ↓ [HUMAN APPROVAL]
    
PHASE 2: WEBSITE CREATION (Weeks 3-6)
├─ Homepage copy (AI)
    ├─ [DESIGN]
├─ Inner page content (AI)
    ├─ [DESIGN]
└─ Site development
    
PHASE 3: PAID ADVERTISING (Weeks 5-8)
├─ Google Ads research (AI)
├─ Google Ads offer creation (AI)
├─ Landing page copy (AI)
│   ├─ [DESIGN & DEVELOPMENT]
├─ Campaign prep (AI)
└─ Campaign launch
    
PHASE 4: SEO & ORGANIC (Ongoing, starting Week 6)
├─ SEO research (AI)
├─ Content planner setup (AI)
├─ Monthly SEO content creation (AI - recurring)
├─ Monthly reporting (AI - recurring)
└─ CRO optimization (AI - recurring)
```

---

## Workflow Stages & AI Handlers

### Stage 1: Onboarding
**Handler**: website-post-onboarding-agent  
**Input**: Client name, website URL  
**Output**: Website brief, positioning, messaging pillars, content templates, sitemap  
**Deliverable**: Website Brief document + Asana project  

---

### Stage 2: Research (Initial Market Analysis)
**Handler**: onboarding-research-agent  
**Input**: Positioning from Stage 1  
**Output**: Market analysis, competitor deep-dive, audience research, messaging validation  
**Deliverable**: Research report  
**Feeds Into**: All downstream skills

---

### Stage 3: Website Strategy & Copy
**Handler**: website-copywriting-agent  
**Input**: Website brief + messaging pillars + positioning  
**Output**: Homepage copy, inner page copy, CTA strategies  
**Deliverable**: Final copy for all website pages  
**Feeds Into**: Design phase

---

### Stage 4: Google Ads Strategy
**Handler Phase A**: google-ads-research-agent  
**Input**: Positioning, target audience, market research  
**Output**: Competitor ad analysis, keyword research, audience insights  
**Feeds Into**: Offer creation

**Handler Phase B**: google-ads-strategy-agent  
**Input**: Research output, business goals, pricing  
**Output**: Offer structure, messaging angles, audience segments, bid strategy  
**Feeds Into**: Landing page copy

**Handler Phase C**: google-ads-landing-page-copywriter  
**Input**: Offer strategy, messaging angles  
**Output**: High-converting landing page copy  
**Feeds Into**: Design & development

**Handler Phase D**: google-ads-campaign-prep-agent  
**Input**: Landing pages (designed), offer strategy  
**Output**: Campaign structure, audiences, keywords, bidding recommendations  
**Feeds Into**: Campaign launch

---

### Stage 5: SEO Strategy & Content
**Handler Phase A**: seo-research-agent  
**Input**: Website brief, positioning, business goals  
**Output**: Keyword research, content opportunity analysis, SEO audit  
**Feeds Into**: Content planning

**Handler Phase B**: seo-content-planner-agent  
**Input**: SEO research, messaging pillars, business goals  
**Output**: 12-month content calendar, topic clusters, publishing schedule  
**Feeds Into**: Monthly content creation

**Handler Phase C**: seo-content-creator-agent (recurring monthly)  
**Input**: Content plan for current month, previous month's performance  
**Output**: 4-6 optimized blog posts/content pieces  
**Feeds Into**: Publishing and monthly reporting

---

### Stage 6: Measurement & Optimization
**Handler Phase A**: monthly-reporting-agent (recurring)  
**Input**: Website analytics, Google Ads performance, SEO rankings, conversions  
**Output**: Monthly performance report with trends and insights  
**Feeds Into**: CRO optimization

**Handler Phase B**: cro-analysis-agent (recurring)  
**Input**: Conversion data, user behavior, traffic sources  
**Output**: CRO recommendations, A/B test ideas, landing page optimizations  
**Feeds Into**: Implementation queue

---

## Data Flow Between Skills

### Context Passing
Each skill passes structured context to the next:

**Positioning Context** (created in Stage 1, used everywhere):
```
{
  positioning_statement: "...",
  messaging_pillars: [...],
  target_audience: {...},
  unique_differentiators: [...],
  proof_points: [...]
}
```

**Website Brief Context** (created in Stage 1):
```
{
  positioning_context: {...},
  recommended_sitemap: {...},
  messaging_strategy: {...},
  success_metrics: {...}
}
```

**Google Ads Research Context** (Stage 4A → 4B):
```
{
  competitor_analysis: {...},
  keyword_data: {...},
  audience_insights: {...},
  ad_copy_angles: [...]
}
```

**SEO Research Context** (Stage 5A → 5B):
```
{
  keyword_opportunities: [...],
  topic_clusters: [...],
  content_gaps: [...],
  ranking_potential: {...}
}
```

**Performance Context** (Monthly → CRO):
```
{
  traffic_sources: {...},
  conversion_data: {...},
  user_behavior: {...},
  bottlenecks: [...]
}
```

---

## Approval Gates

### Gate 1: After Website Brief (Stage 1 → Stage 2)
**Required**: Client approval of positioning and messaging  
**Blocks**: All downstream work  
**Action on approval**: Proceeds to research, copy creation, Google Ads strategy  

### Gate 2: After Website Copy (Stage 3 → Design)
**Required**: Client approval of messaging and copy tone  
**Blocks**: Design phase  
**Action on approval**: Releases to design team  

### Gate 3: After Google Ads Research (Stage 4A → 4B)
**Required**: Internal approval of strategy and audience targeting  
**Blocks**: Campaign creation  
**Action on approval**: Proceeds to offer strategy and landing page copy  

### Gate 4: After Content Plan (Stage 5B → 5C)
**Required**: Client approval of topics and publishing schedule  
**Blocks**: Content creation  
**Action on approval**: Monthly content creation begins  

---

## Asana Project Structure

Auto-created with sections for each phase:

```
Rain Marketers Project: [Client Name]

DISCOVERY & STRATEGY
├─ ☐ Onboarding research
├─ ☐ Website brief creation
├─ ☐ [APPROVAL] Client reviews positioning
└─ ☐ Marketing strategy finalized

WEBSITE CREATION
├─ ☐ Homepage copy creation
├─ ☐ Inner page content creation
├─ ☐ Design phase
├─ ☐ Website development
├─ ☐ Website QA and launch
└─ ☐ Google Business Profile setup

GOOGLE ADS CAMPAIGN
├─ ☐ Google Ads market research
├─ ☐ Offer and strategy development
├─ ☐ Landing page copy creation
├─ ☐ Landing page design & development
├─ ☐ Campaign structure and setup
├─ ☐ [APPROVAL] Review and launch
└─ ☐ Campaign optimization setup

SEO & CONTENT
├─ ☐ SEO opportunity research
├─ ☐ Content calendar creation
├─ ☐ [APPROVAL] Client reviews content plan
├─ ☐ Month 1 content creation
├─ ☐ Month 2 content creation
├─ ☐ ... (monthly recurring)
└─ ☐ SEO performance monitoring

ONGOING OPTIMIZATION
├─ ☐ Month 1 performance report
├─ ☐ Month 1 CRO analysis
├─ ☐ Implement CRO changes
├─ ☐ Month 2 performance report
├─ ☐ ... (monthly recurring)
└─ ☐ Ongoing optimization and testing
```

---

## Workflow Management

### How It Works

1. **Project Initialization**: User provides client name + website
2. **Stage Router**: Orchestrator determines what stage(s) are active
3. **Skill Activation**: Routes to appropriate sub-skill(s)
4. **Context Passing**: Previous outputs fed as inputs to next skill
5. **Approval Gating**: Pauses at decision points, resumes on approval
6. **Progress Tracking**: Updates Asana automatically
7. **Output Synthesis**: Combines all deliverables into integrated plan

### Timeline Management

**Default timeline** (can be customized):
- Phase 1 (Discovery): Weeks 1-2
- Phase 2 (Website): Weeks 3-6
- Phase 3 (Ads): Weeks 5-8 (overlaps with website)
- Phase 4 (SEO): Starts Week 6, ongoing
- Phases 5 & 6 (Reporting/CRO): Ongoing from Month 2

---

## Integration Points

### Skill Dependencies
```
website-post-onboarding-agent (foundation)
    ↓
    ├─→ website-copywriting-agent
    ├─→ google-ads-research-agent
    ├─→ seo-research-agent
    ├─→ onboarding-research-agent (enrichment)
    
google-ads-research-agent
    ↓
    └─→ google-ads-strategy-agent
        ↓
        └─→ google-ads-landing-page-copywriter
            ↓
            └─→ google-ads-campaign-prep-agent

seo-research-agent
    ↓
    └─→ seo-content-planner-agent
        ↓
        └─→ seo-content-creator-agent (monthly)
            ↓
            └─→ monthly-reporting-agent
                ↓
                └─→ cro-analysis-agent
```

### Cross-Skill Data Sharing
- Positioning context is read-only, used by all downstream skills
- Research outputs enrich copy creation
- Performance data flows back to optimization
- Monthly reporting informs CRO strategy

---

## Success Metrics

**Project-level metrics** tracked in Asana:
- All phases completed on schedule
- All approval gates cleared
- All deliverables quality-approved
- Client satisfaction score

**Performance metrics** tracked monthly:
- Website traffic (vs. baseline)
- Lead generation rate
- Google Ads ROAS
- SEO rankings progress
- Conversion rate
- Customer acquisition cost

---

## Configuration

### Parameters
- **Client name** (required)
- **Website URL** (required)
- **Service package** (Website only, Website + Ads, Full service)
- **Timeline** (standard, accelerated, custom)
- **Budget allocation** (for Ads phase)
- **Content frequency** (SEO phase)

### Customization Points
- Approval gate requirements
- Timeline phase lengths
- Skill execution order (some can run in parallel)
- Reporting frequency
- CRO optimization cadence

---

## Extending the Orchestrator

To add new skills or phases:

1. Create new skill in `skills/new-skill-name/`
2. Define inputs and outputs
3. Add to this workflow document
4. Update skill dependencies diagram
5. Add to Asana task template
6. Document context passing

See [ARCHITECTURE.md](../../docs/ARCHITECTURE.md) for skill creation details.

---

## See Also

- [Complete Workflow Documentation](./references/fulfillment-workflow.md)
- [Integration Patterns Guide](./references/integration-patterns.md)
- [Skill Taxonomy](./references/skill-taxonomy.md)
- [Data Context Models](./references/context-models.md)

---

**Version**: 1.0.0  
**Last updated**: May 4, 2026  
**Status**: Foundation - ready for skill implementation
