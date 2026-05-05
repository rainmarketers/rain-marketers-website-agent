# Rain Marketers Website Agent

A comprehensive AI-powered skill for creating strategic website briefs and content strategies for small business clients. Handles market research, competitive analysis, positioning strategy, and content planning.

## 🎯 What It Does

The Website Post-Onboarding Agent helps Rain Marketers:
- **Analyze client websites** to understand current positioning
- **Research competitors** to identify market gaps
- **Create strategic website briefs** with positioning, messaging, and structure recommendations
- **Generate content templates** ready for copywriters to customize
- **Design sitemaps** tailored to industry best practices

---

## 🚀 Quick Start

### Run the Agent

```bash
/website-post-onboarding-agent "Client Name" "https://client-website.com"
```

### What You Get

✅ **Market Research** – Trends, competitor analysis, positioning gaps  
✅ **Positioning Strategy** – Defensible positioning based on market data  
✅ **Website Brief** – Executive summary, messaging pillars, CTAs, KPIs  
✅ **Content Templates** – Homepage, services, FAQ, about us copy  
✅ **Sitemap Recommendations** – Industry-appropriate page structure  
✅ **Asana Tasks** – Automatically created and assigned  

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
│   └── website-post-onboarding-agent/
│       ├── SKILL.md
│       └── references/                (7 reference docs)
│
├── agents/                            (future subagents)
├── scripts/                           (future automation)
├── templates/                         (future templates)
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

## 🔧 The Skill

### `website-post-onboarding-agent`

**Location**: `skills/website-post-onboarding-agent/`

**Core Definition**: `SKILL.md`

**Reference Materials** (7 docs in `references/`):
1. **example-website-brief.md** – Real example output (Clean Cut Gutters)
2. **page-content-templates.md** – Copy templates for all page types
3. **sitemap-builder.md** – Industry-specific website structures
4. **onboarding-form-fields.md** – Client intake form
5. **competitor-analysis.md** – How to analyze competitors
6. **agent-prompt-guide.md** – How the agent operates
7. **quality-standards.md** – Output quality checklist

---

## 👥 For the Team

### Client Onboarding Workflow

1. **Collect Info** → Use [onboarding form](./skills/website-post-onboarding-agent/references/onboarding-form-fields.md)
2. **Create Asana Project** → Name = client name (e.g., "Clean Cut Gutters")
3. **Run Agent** → `/website-post-onboarding-agent "Client Name" "https://website.com"`
4. **Review Output** → Check Asana tasks + brief
5. **Handoff** → Pass to design/development team

### Understanding the Output

- **Website Brief** – What to say, how to structure, proof points
- **Content Templates** – Ready-to-customize copy for each page
- **Competitor Analysis** – Who's claiming what, where are gaps
- **Success Metrics** – What "winning" looks like for this client

See [docs/USAGE.md](./docs/USAGE.md) for detailed walkthrough.

---

## 🧠 How It Works

The agent:
1. Analyzes your client's current website
2. Researches 5-7 direct competitors
3. Maps their positioning claims
4. Identifies defensible positioning gaps
5. Develops 3 core messaging pillars
6. Creates templates for all major pages
7. Recommends site structure by industry
8. Sets measurable KPIs

**All based on proven research methodology** stored in the reference docs.

---

## 📖 Example Output

See `examples/sample-client-brief/` for a complete real example (Clean Cut Gutters gutter cleaning service).

---

## 🔮 Future Growth

This repo is structured to scale. You can add:

- **More Skills** – Copy the skill folder structure for new agents
- **Subagents** – Define specialized agents in `agents/`
- **Scripts** – Add automation in `scripts/`
- **Templates** – Store reusable templates in `templates/`

See [docs/ARCHITECTURE.md](./docs/ARCHITECTURE.md) for how to extend.

---

## ❓ Questions?

- **"How do I use this?"** → [docs/USAGE.md](./docs/USAGE.md)
- **"How is it organized?"** → [docs/ARCHITECTURE.md](./docs/ARCHITECTURE.md)
- **"What do I need to set up?"** → [docs/SETUP.md](./docs/SETUP.md)
- **"What makes good output?"** → [Quality Standards](./skills/website-post-onboarding-agent/references/quality-standards.md)
- **"How does it analyze competitors?"** → [Competitor Analysis](./skills/website-post-onboarding-agent/references/competitor-analysis.md)

---

## 📄 License

MIT License – See [LICENSE](./LICENSE) file.

## 👨‍💻 Contributors

Built by Rain Marketers team. See [CONTRIBUTORS.md](./CONTRIBUTORS.md).

---

**Ready to create your first client brief?** Start with [docs/SETUP.md](./docs/SETUP.md)
