# Rain Marketing Website Agent

**Market research, competitive positioning, website brief, and homepage copy generation for new client onboarding.**

## Quick Start

### Basic Invocation

```bash
/website-post-onboarding-agent "Client Name" "https://client-website.com"
```

The agent automatically:
1. Finds the client's Asana project by name
2. Conducts deep market research
3. Analyzes 5-7 competitors
4. Identifies positioning gaps
5. Creates a strategic website brief
6. Writes conversion-focused homepage copy
7. Creates Asana tasks assigned to Stevie

### What You Get

- **Market Research Findings** – Trends, competitor matrix, positioning gaps
- **Positioning Strategy** – Defensible positioning based on market data
- **Website Brief** – Executive summary, messaging pillars, CTA strategy, KPIs
- **Homepage Copy** – Hero section, value props, social proof, CTAs
- **Asana Tasks** – Automatically created and assigned to Stevie

### Generate PDF Report

```bash
/website-post-onboarding-agent generate-report "Client Name"
```

Creates a professional A4 PDF with market analysis, positioning recommendation, brief, and copy.

---

## Documentation

- **[WEBSITE_AGENT_DOCUMENTATION.md](./WEBSITE_AGENT_DOCUMENTATION.md)** – Complete technical guide
- **[Quality Standards](./skills/website-post-onboarding-agent/references/quality-standards.md)** – What constitutes good research, brief, and copy
- **[Agent Prompt Guide](./skills/website-post-onboarding-agent/references/agent-prompt-guide.md)** – How the agent thinks and processes information
- **[Example Website Brief](./skills/website-post-onboarding-agent/references/example-website-brief.md)** – Real example of a strategic brief
- **[Competitor Analysis](./skills/website-post-onboarding-agent/references/competitor-analysis.md)** – Methodology for analyzing competitors

---

## For New Clients

1. **Client Onboarding**: Have client fill out onboarding form (see [Onboarding Form Fields](./skills/website-post-onboarding-agent/references/onboarding-form-fields.md))
2. **Create Asana Project**: Project name = client name (e.g., "Clean Cut Gutters")
3. **Run Agent**: `/website-post-onboarding-agent "Clean Cut Gutters" "https://cleancutgutters.com"`
4. **Review Output**: Check Asana tasks created with findings
5. **Handoff to Design**: Design team reviews brief and copy, begins design/development

---

## Support Files

- **[Sitemap Builder](./skills/website-post-onboarding-agent/references/sitemap-builder.md)** – Recommended website structure templates by industry
- **[Page Content Templates](./skills/website-post-onboarding-agent/references/page-content-templates.md)** – Copy frameworks for common pages
- **[Onboarding Form Fields](./skills/website-post-onboarding-agent/references/onboarding-form-fields.md)** – Form fields to collect from new clients

---

## Next Steps

- Review [WEBSITE_AGENT_DOCUMENTATION.md](./WEBSITE_AGENT_DOCUMENTATION.md) for technical details
- Check [Quality Standards](./skills/website-post-onboarding-agent/references/quality-standards.md) to understand output expectations
- Refer to [Example Website Brief](./skills/website-post-onboarding-agent/references/example-website-brief.md) when reviewing client briefs
