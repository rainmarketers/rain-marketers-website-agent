# Setup & Installation

Get the Website Post-Onboarding Agent running in 5 minutes.

---

## Prerequisites

- Claude Code (Claude 3.7+)
- Access to the skill in your Claude workspace
- Asana account with appropriate API permissions (optional, for task automation)
- A client website URL to analyze

---

## Quick Start

### 1. Verify the Skill is Installed

The skill should be available in your Claude workspace at:

```
/website-post-onboarding-agent "Client Name" "https://client-website.com"
```

If you don't see it, contact your workspace admin or check [CONTRIBUTORS.md](../CONTRIBUTORS.md) for installation help.

### 2. Prepare Client Information

Gather basic info about the client before running the agent:

- **Client Name** (e.g., "Clean Cut Gutters")
- **Website URL** (current website to analyze)
- **Industry** (what they do)
- **Target Customer** (who they sell to)
- **Main Pain Points** (what problems they solve)

Optional but helpful:
- **Known Competitors** (names if available)
- **Current Tagline/Positioning** (what they currently say about themselves)
- **Success Metrics** (how they measure website success)

See [onboarding-form-fields.md](../skills/website-post-onboarding-agent/references/onboarding-form-fields.md) for the full form structure.

### 3. Create an Asana Project (Optional)

If you want the agent to automatically create Asana tasks:

1. Create a new Asana project named exactly as the client name (e.g., "Clean Cut Gutters")
2. Get your Asana workspace ID from your Asana account settings
3. The agent will detect the project and create tasks automatically

If you skip this step, the agent still runs but won't create Asana tasks.

### 4. Run the Agent

In Claude Code:

```bash
/website-post-onboarding-agent "Client Name" "https://website.com"
```

**Example:**
```bash
/website-post-onboarding-agent "Clean Cut Gutters" "https://cleancutgutters.com"
```

The agent will:
- Analyze the client's website
- Research competitors
- Develop positioning strategy
- Create messaging pillars
- Generate content templates
- Recommend sitemap structure
- Create Asana tasks (if project exists)

### 5. Review the Output

The agent generates:

✅ **Website Brief** – Positioning, messaging, CTAs, KPIs  
✅ **Competitive Analysis** – 5-7 competitors mapped  
✅ **Content Templates** – Ready-to-customize copy for all pages  
✅ **Sitemap Recommendations** – Industry-appropriate page structure  
✅ **Asana Tasks** – Automatically created if Asana project exists  

---

## Configuration

### Asana Integration (Optional)

To enable automatic Asana task creation:

1. Get your Asana Personal Access Token:
   - Go to Asana → Settings → Apps → Personal Access Tokens
   - Create a new token
   - Save it securely

2. Get your Workspace ID:
   - Go to any Asana project URL
   - Workspace ID is in the URL: `app.asana.com/0/WORKSPACE_ID/...`

3. When running the agent, make sure:
   - An Asana project exists with the exact client name
   - Your token is configured in your Claude environment

### Customizing the Agent

The agent can be customized by editing:

**Location**: `skills/website-post-onboarding-agent/SKILL.md`

**What you can customize:**
- Default competitor analysis depth (currently 5-7)
- Content template styles
- Asana task templates
- Positioning framework

See [ARCHITECTURE.md](./ARCHITECTURE.md) for how to extend the agent.

---

## Troubleshooting

### Agent says "Website not found"

- ✅ Verify the URL is correct and publicly accessible
- ✅ Try adding `https://` if it's missing
- ✅ Check if the website blocks automated access

### Asana tasks not created

- ✅ Verify the Asana project name matches the client name exactly
- ✅ Check that your Asana token is valid (hasn't expired)
- ✅ Ensure you have permission to create tasks in that project

### Competitor analysis seems incomplete

- ✅ This is normal for niche industries with few competitors
- ✅ The agent finds 5-7 direct competitors; if fewer exist, it analyzes what's available
- ✅ You can manually add competitors by editing the agent output

### Output looks too generic

- ✅ Provide more detail in the client info (pain points, differentiators)
- ✅ Fill out the [onboarding form](../skills/website-post-onboarding-agent/references/onboarding-form-fields.md) completely
- ✅ The agent uses your input to customize analysis

---

## Next Steps

1. **Review the Brief** → Check positioning and messaging pillars
2. **Validate with Client** → Does the positioning resonate with them?
3. **Customize Templates** → Edit content templates for brand voice
4. **Hand Off to Design** → Share brief + templates with design team
5. **Track in Asana** → Use auto-created tasks to track progress

---

## Getting Help

- **How do I use this?** → See [USAGE.md](./USAGE.md)
- **How is it organized?** → See [ARCHITECTURE.md](./ARCHITECTURE.md)
- **What are the quality standards?** → See [quality-standards.md](../skills/website-post-onboarding-agent/references/quality-standards.md)
- **What makes good output?** → See [example-website-brief.md](../skills/website-post-onboarding-agent/references/example-website-brief.md)

---

**Ready?** Run your first agent: `/website-post-onboarding-agent "Your Client" "https://their-website.com"`
