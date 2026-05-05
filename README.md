# Rain Marketers Service Fulfillment Orchestrator

A complete AI-powered multi-skill orchestration system that coordinates 11 specialized agents across 4 service delivery phases: Discovery & Strategy → Website Creation → Paid Advertising → SEO/Organic.

## 🎯 What It Does

The Service Fulfillment Orchestrator automates the complete Rain Marketers service delivery workflow:

**Phase 1: Discovery & Strategy** (Weeks 1-2)
- Market research, competitive analysis, positioning strategy
- Customer interviews & audience validation
- Website brief creation with messaging pillars

**Phase 2: Website Creation** (Weeks 3-6)
- Homepage, services, about, testimonials copywriting
- Website design direction & user flows
- SEO-optimized page structure

**Phase 3: Paid Advertising** (Weeks 5-8, overlapping)
- Google Ads keyword research & competitive analysis
- Campaign strategy, offers, messaging angles
- Landing page copy optimization
- Campaign configuration ready to launch

**Phase 4: SEO/Organic** (Weeks 6+, ongoing)
- SEO keyword research & content gap analysis
- 12-month content calendar planning
- Monthly article creation & publishing (4-6/month)
- Monthly performance reporting across all channels
- Conversion rate optimization recommendations

---

## 🚀 Quick Start

### Run the Orchestrator

```bash
/rain-marketers-fulfillment-orchestrator
```

### What You Get

The orchestrator coordinates 11 specialized AI skills across 4 phases:

**Phase 1: Discovery & Strategy** (4 skills)
✅ **Onboarding Research** – Market landscape, competitive analysis, positioning validation  
✅ **Website Brief** – Strategic direction, messaging pillars, success KPIs  

**Phase 2: Website Creation**
✅ **Website Copywriting** – All website pages (homepage, services, about, testimonials, FAQ)  

**Phase 3: Paid Advertising** (3 skills)
✅ **Google Ads Research** – Keyword opportunities, audience insights, competitor ad analysis  
✅ **Ads Strategy** – Offer structure, messaging angles, audience segments, bidding  
✅ **Campaign Preparation** – Campaign structure, ad groups, keywords, conversions tracking  

**Phase 4: SEO/Organic** (3 skills, recurring monthly)
✅ **SEO Research** – Keyword opportunities, topic clusters, content gaps  
✅ **Content Planning** – 12-month content calendar (40-60 articles)  
✅ **Content Creation** – Monthly article production (4-6 articles/month)  

**Ongoing Optimization** (2 skills, recurring monthly)
✅ **Monthly Reporting** – Performance across all channels  
✅ **CRO Analysis** – Conversion optimization recommendations & A/B test roadmap  

✅ **Approval Gates** – Human decision points at critical stages  
✅ **Asana Integration** – Project created with phase-based task structure  

---

## 📚 Documentation

| Document | Purpose |
|----------|---------|
| **[SETUP.md](./docs/SETUP.md)** | Installation & configuration |
| **[USAGE.md](./docs/USAGE.md)** | How to use the agent |
| **[ARCHITECTURE.md](./docs/ARCHITECTURE.md)** | How the repo is organized |
| **[WEBSITE_AGENT_DOCUMENTATION.md](./WEBSITE_AGENT_DOCUMENTATION.md)** | Technical details |

---

## 📁 Project Structure

```
rain-marketing-website-agent/
├── skills/
│   ├── rain-marketers-fulfillment-orchestrator/     (Main orchestrator "brain")
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── fulfillment-workflow.md
│   │       ├── integration-patterns.md
│   │       ├── skill-taxonomy.md
│   │       └── context-models.md
│   │
│   ├── onboarding-research-agent/                   (Phase 1.2)
│   ├── website-copywriting-agent/                   (Phase 2.1)
│   ├── google-ads-research-agent/                   (Phase 3.1)
│   ├── google-ads-strategy-agent/                   (Phase 3.2a)
│   ├── google-ads-landing-page-copywriter/          (Phase 3.2b)
│   ├── google-ads-campaign-prep-agent/              (Phase 3.3)
│   ├── seo-research-agent/                          (Phase 4.1)
│   ├── seo-content-planner-agent/                   (Phase 4.2)
│   ├── seo-content-creator-agent/                   (Phase 4.3, recurring)
│   ├── monthly-reporting-agent/                     (Phase 4.4, recurring)
│   └── cro-analysis-agent/                          (Phase 4.5, recurring)
│
├── docs/
│   ├── SETUP.md
│   ├── USAGE.md
│   └── ARCHITECTURE.md
│
├── examples/
│   └── sample-client-brief/
│
└── README.md (this file)
```

See [docs/ARCHITECTURE.md](./docs/ARCHITECTURE.md) for the complete structure.

---

## 🧠 The Orchestrator System

### `rain-marketers-fulfillment-orchestrator`

**Location**: `skills/rain-marketers-fulfillment-orchestrator/`

**Core Definition**: `SKILL.md` – Main orchestrator that routes work through 4 phases and coordinates approval gates

**Reference Architecture** (4 docs in `references/`):
1. **fulfillment-workflow.md** – Complete 4-phase workflow with timeline, approval gates, success criteria
2. **integration-patterns.md** – How skills communicate, context passing, error handling
3. **skill-taxonomy.md** – Complete inventory of 11 core skills by phase/function
4. **context-models.md** – 6 structured JSON data models for context flow between skills

### 11 Specialized Skills

| Phase | Skill | Days | Purpose |
|-------|-------|------|---------|
| 1.2 | onboarding-research-agent | 2-3 | Market research, competitor analysis, positioning validation |
| 2.1 | website-copywriting-agent | 3-4 | All website page copy (homepage, services, about, testimonials, FAQ) |
| 3.1 | google-ads-research-agent | 2-3 | Keyword research (50-100), audience insights, competitor ads analysis |
| 3.2a | google-ads-strategy-agent | 2 | Offer structure, messaging angles, audience segments, bidding strategy |
| 3.2b | google-ads-landing-page-copywriter | 1-2 | High-converting landing page copy with social proof & objection handling |
| 3.3 | google-ads-campaign-prep-agent | 2.5 | Campaign structure, keywords by ad group, ad copy variants, conversion tracking |
| 4.1 | seo-research-agent | 2 | Keyword opportunities (50-100), topic clusters (3-5), content gaps, quick wins |
| 4.2 | seo-content-planner-agent | 2 | 12-month content calendar (40-60 articles), keyword assignment, internal linking |
| 4.3 | seo-content-creator-agent | Monthly | Monthly content production (4-6 articles/month) with full optimization |
| 4.4 | monthly-reporting-agent | Monthly | Performance aggregation across Ads, SEO, conversions, budget ROI |
| 4.5 | cro-analysis-agent | Monthly | Conversion optimization analysis, A/B test roadmap, quick wins |

---

## 👥 For the Team

### Complete Service Delivery Workflow

**Phase 1: Discovery & Strategy** (Weeks 1-2)
1. **Collect info** from client (industry, goals, current state)
2. **Run orchestrator** → `/rain-marketers-fulfillment-orchestrator`
3. **Onboarding research** → Market analysis, positioning strategy
4. **Approval Gate 1** → Client reviews & approves positioning
5. **Website brief** → Strategic direction ready for all downstream work

**Phase 2: Website Creation** (Weeks 3-6)
6. **Website copywriting** → All pages (homepage, services, about, etc.)
7. **Design & development** → Copy becomes website structure/pages
8. **Approval Gate 2** → Client reviews website design
9. **Publish website** → Live and optimized for SEO

**Phase 3: Paid Advertising** (Weeks 5-8, overlapping)
10. **Google Ads research** → Keyword opportunities, audience insights
11. **Campaign strategy** → Offer, messaging angles, audience segments
12. **Landing page copywriting** → High-converting page optimized for ads
13. **Campaign preparation** → Structure, keywords, ad copy, tracking
14. **Approval Gate 3** → Client reviews campaign configuration
15. **Launch campaign** → Ads live and tracking conversions

**Phase 4: SEO/Organic** (Weeks 6+, ongoing)
16. **SEO research** → Keyword opportunities, content gaps, clusters
17. **Content planning** → 12-month calendar with 40-60 article topics
18. **Approval Gate 4** → Client reviews content plan
19. **Monthly content creation** → 4-6 articles/month published & optimized
20. **Monthly reporting** → Performance across all channels
21. **CRO optimization** → Conversion rate improvements & A/B tests

See [docs/USAGE.md](./docs/USAGE.md) for detailed walkthrough and [skills/rain-marketers-fulfillment-orchestrator/references/fulfillment-workflow.md](./skills/rain-marketers-fulfillment-orchestrator/references/fulfillment-workflow.md) for phase details.

---

## 🏗️ How The Orchestrator Works

The orchestrator is a **coordinating "brain"** that manages context flow between specialized skills:

1. **Phase 1: Discovery** → Outputs positioning context (used by website + ads + SEO)
2. **Phase 2: Website** → Outputs website brief context (messaging, structure, KPIs)
3. **Phase 3: Ads** → Takes positioning + brief, outputs campaign ready to launch
4. **Phase 4: SEO** → Takes positioning + brief, outputs 12-month content plan
5. **Ongoing**: Monthly skills (content creation, reporting, CRO) process performance data

**Key Features**:
- **Context Passing** – JSON data flows between skills (no manual re-entry)
- **Approval Gates** – Human decision points at critical stages block downstream work
- **Parallel Execution** – Ads (Phase 3) runs alongside website (Phase 2)
- **Recurring Cycles** – Monthly content, reporting, and optimization continue indefinitely
- **Asana Integration** – Project auto-created with phase-based task structure
- **Data Consistency** – Shared context prevents messaging conflicts

**All based on proven service delivery methodology** documented in reference files.

---

## 📖 Example Output

See `examples/sample-client-brief/` for a complete real example (Clean Cut Gutters gutter cleaning service).

---

## 🔮 Extending The System

This orchestrator is built to scale. You can add new skills by:

1. **Create new skill folder** under `skills/` with the standard structure:
   - `SKILL.md` – Core definition (What it does, Input, Output, Execution stages)
   - `references/` – Supporting documentation (optional)

2. **Define the skill** following the established pattern:
   - Input format (what context it receives)
   - Output format (what context it produces)
   - Execution stages (2-4 concrete stages)
   - Success criteria (how to know it worked)
   - Feeds into (which downstream skills use its output)

3. **Update the orchestrator** to route to your new skill:
   - Add to the appropriate phase
   - Define input/output context flow
   - Integrate with Asana task structure

4. **Document relationships**:
   - Skill taxonomy (in orchestrator references)
   - Context models (in context-models.md)
   - Integration patterns (in integration-patterns.md)

See [docs/ARCHITECTURE.md](./docs/ARCHITECTURE.md) for detailed extension guide and skill development standards.

---

## ❓ Questions?

- **"How do I run the complete workflow?"** → [docs/USAGE.md](./docs/USAGE.md)
- **"How is it organized & how do I extend it?"** → [docs/ARCHITECTURE.md](./docs/ARCHITECTURE.md)
- **"What do I need to set up?"** → [docs/SETUP.md](./docs/SETUP.md)
- **"How do skills coordinate?"** → [Integration Patterns](./skills/rain-marketers-fulfillment-orchestrator/references/integration-patterns.md)
- **"What context flows between skills?"** → [Context Models](./skills/rain-marketers-fulfillment-orchestrator/references/context-models.md)
- **"What's the complete workflow?"** → [Fulfillment Workflow](./skills/rain-marketers-fulfillment-orchestrator/references/fulfillment-workflow.md)
- **"What are all the skills?"** → [Skill Taxonomy](./skills/rain-marketers-fulfillment-orchestrator/references/skill-taxonomy.md)

---

## 📄 License

MIT License – See [LICENSE](./LICENSE) file.

## 👨‍💻 Contributors

Built by Rain Marketers team. See [CONTRIBUTORS.md](./CONTRIBUTORS.md).

---

**Ready to run your first complete service delivery workflow?** Start with [docs/SETUP.md](./docs/SETUP.md)
