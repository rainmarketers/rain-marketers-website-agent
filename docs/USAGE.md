# Usage Guide

Complete walkthrough of how to use the Website Post-Onboarding Agent.

---

## The Complete Workflow

### Step 1: Gather Client Information

Before running the agent, collect:

**Essential:**
- Client name
- Current website URL
- Industry/business type
- Primary target customer
- Top 3-5 customer pain points

**Helpful:**
- Years in business
- Current positioning/tagline
- Known competitors
- Website goals
- Budget/timeline

Use the [onboarding form](../skills/website-post-onboarding-agent/references/onboarding-form-fields.md) as your checklist.

**Example:**
> **Company**: Clean Cut Gutters  
> **Website**: https://cleancutgutters.com  
> **Industry**: Gutter cleaning (B2C services)  
> **Target**: Homeowners age 40-65 in Chicago suburbs  
> **Pain Points**: Don't remember to clean gutters, fear of ladders, don't trust unfamiliar contractors, need reliable local service

### Step 2: Create an Asana Project (Optional)

If using Asana integration:

1. Click "New Project" in Asana
2. Name it **exactly** as the client name (e.g., "Clean Cut Gutters")
3. Set it to "List" view
4. You're ready — the agent will auto-detect it

If you skip this, the agent still runs but won't create tasks.

### Step 3: Run the Agent

In your Claude Code editor:

```bash
/website-post-onboarding-agent "Client Name" "https://website-url.com"
```

**Example:**
```bash
/website-post-onboarding-agent "Clean Cut Gutters" "https://cleancutgutters.com"
```

The agent will take 2-5 minutes depending on:
- Website complexity
- Number of competitors
- Asana task creation (if enabled)

---

## Understanding the Output

The agent generates a structured brief with these sections:

### 1. Executive Summary

**What it is**: One-page overview of positioning and strategy  
**Who uses it**: Everyone (clients, designers, copywriters)

**Includes**:
- Client name and industry
- Target customer snapshot
- Positioning statement
- 3 core messaging pillars
- Quick competitive context

**Example**:
> **Target**: Homeowners age 40-65 in Chicago suburbs  
> **Positioning**: "The gutter service for property managers who demand reliability and scale"  
> **Pillars**: Same-day service, licensed & insured, lifetime guarantee

### 2. Market Research

**What it is**: Competitor and market landscape analysis  
**Who uses it**: Strategy team, designers, copywriters

**Includes**:
- 5-7 direct competitors analyzed
- Positioning map (who's claiming what)
- Market gaps identified
- Audience segments underserved
- Industry trends

**Example**:
> - **Competitor 1 (Pro Gutter Pros)**: "Same-day convenience" positioning
> - **Competitor 2 (Local Gutters Co)**: "Family trust and local presence" positioning  
> - **Gap**: No one targets commercial/multi-family properties
> - **Recommendation**: Position for property managers (B2B angle)

### 3. Positioning Strategy

**What it is**: Recommended positioning with proof points  
**Who uses it**: Decision makers, copywriters

**Includes**:
- Positioning statement
- Why it's defensible (backed by competitors analyzed)
- Target audience definition
- Key differentiators
- Proof points (what proof exists)
- Messaging pillars (3-4 core claims)

**Example**:
> **Positioning**: "Same-day gutter service for busy professionals"  
> **Defensible because**: Competitors split between speed-focused OR family-trust-focused, but not both  
> **Target**: Working professionals, age 35-55, value convenience  
> **Pillars**:  
> 1. Speed: Same-day or next-day (95% of calls)  
> 2. Reliability: Licensed, insured, guaranteed  
> 3. Transparency: Free inspection with photo report

### 4. Website Brief

**What it is**: High-level recommendations for website structure and messaging  
**Who uses it**: Design and development team

**Includes**:
- Homepage messaging (headline, subheadline, CTAs)
- Value propositions (3-4 key benefits)
- Recommended sitemap (page structure)
- Call-to-action strategy
- Key conversion metrics

**Example**:
```
HOMEPAGE HEADLINE: "Never Climb a Ladder Again"
SUBHEADLINE: "Same-day gutter cleaning you can trust"
HERO CTA: "Schedule Your Free Inspection"

VALUE PROPS:
1. Same-Day Service (95% within 24 hours)
2. Licensed & Insured (Full coverage)
3. Lifetime Guarantee (Clog-free for life)

RECOMMENDED SITEMAP:
- Homepage (Problem, solution, trust)
- Services (With pricing)
- Why Choose Us (Differentiators + proof)
- Customer Testimonials (Social proof)
- Service Area Map (Local coverage)
- Contact / Book Now
```

### 5. Content Templates

**What it is**: Ready-to-customize copy for every page type  
**Who uses it**: Copywriter, content creator

**Includes**:
- Homepage copy template
- Services page template
- About Us template
- Testimonials/case studies template
- FAQ template
- Contact page template

Each template:
- Follows the messaging pillars from the brief
- Is benefit-focused (not feature-heavy)
- Includes placeholder guidance `[in brackets]`
- Shows copy examples

**How to use**:
1. Copy the relevant template
2. Replace `[brackets]` with your content
3. Adjust tone/voice to match your brand
4. Review against [quality standards](../skills/website-post-onboarding-agent/references/quality-standards.md)

**Example template block**:
```
HERO SECTION
Headline: "Never Clean Gutters Again"

Subheadline: "Our [service name] means you'll never climb a ladder again. 
[Key benefit] guaranteed."

Hero Image: [Visual of the benefit in action]

Primary CTA: "Schedule Your Free [Inspection/Estimate]"
```

### 6. Sitemap Recommendations

**What it is**: Recommended page structure based on industry best practices  
**Who uses it**: Information architect, design team

**Includes**:
- Recommended navigation structure
- Page hierarchy
- Key pages and their purpose
- Conversion funnel flow

**Example**:
```
Homepage
├── Services (with pricing)
├── Why Choose Us (differentiators)
├── Our Process (4-step flow)
├── Customer Testimonials
├── Service Area Map
├── FAQ
└── Contact / Book Now
```

### 7. Asana Tasks (if Asana enabled)

**What it is**: Auto-created project tasks tracking the brief execution  
**Who uses it**: Project manager, team leads

**Includes**:
- Design tasks
- Content tasks
- Development tasks
- Launch tasks
- Success tracking tasks

Each task includes:
- Clear title and description
- Assigned team member (if specified)
- Due date estimates
- Links to relevant sections of the brief

---

## Customizing the Output

The output is a **starting point**, not final copy. Customize it:

### For Messaging

1. Review positioning statement with client
2. If they don't agree, adjust messaging pillars
3. Re-run content templates with new pillars
4. Validate new messaging resonates

### For Design

1. Use recommended sitemap as starting point
2. Adjust page structure for unique needs
3. Add/remove pages based on goals
4. Reorder for better conversion flow

### For Copy

1. Use templates as frameworks
2. Inject brand voice (more casual? more formal?)
3. Add specific numbers/proof points from client
4. Review against quality standards

### For Asana Workflow

1. Assign tasks to team members
2. Adjust due dates to match project timeline
3. Add any additional tasks specific to this client
4. Use task descriptions to brief team on strategy

---

## Quality Checklist

Before handing off the brief to the next team:

**Positioning**
- [ ] Does positioning fill an identified market gap?
- [ ] Can the client credibly deliver on this positioning?
- [ ] Is it differentiated from 5-7 competitors?
- [ ] Does it address customer pain points?

**Website Brief**
- [ ] Does homepage messaging flow logically?
- [ ] Are CTAs clear and action-oriented?
- [ ] Is sitemap logical for customer journey?
- [ ] Are success metrics measurable?

**Content Templates**
- [ ] Are they benefit-focused (not feature-heavy)?
- [ ] Do they follow positioning pillars?
- [ ] Are CTAs specific and clear?
- [ ] Is copy scannable (short paragraphs, strong subheads)?

**Asana Tasks**
- [ ] Are tasks specific and actionable?
- [ ] Are due dates realistic?
- [ ] Is assignment clear (who's responsible)?
- [ ] Are tasks linked to brief sections?

See [quality-standards.md](../skills/website-post-onboarding-agent/references/quality-standards.md) for the full checklist.

---

## Common Use Cases

### Scenario 1: Client Doesn't Agree with Positioning

1. Show them the competitive analysis
2. Walk through the positioning gap analysis
3. Explain why the gap exists (what's missing in market)
4. Ask: "Is this positioning something you can credibly deliver?"
5. If not, re-run with adjusted input or different positioning angle

### Scenario 2: Designer Asks "Why This Sitemap?"

1. Point to the recommended sitemap section
2. Explain the conversion funnel logic
3. Show how it addresses customer journey
4. Let them adjust for unique business needs

### Scenario 3: Copywriter Asks "How Do I Use the Templates?"

1. Share the [page-content-templates.md](../skills/website-post-onboarding-agent/references/page-content-templates.md) file
2. Show example of template + customized version
3. Point to [quality-standards.md](../skills/website-post-onboarding-agent/references/quality-standards.md) for evaluation
4. Have them review first draft against positioning pillars

### Scenario 4: Client Wants to Know Success Metrics

1. Show the KPIs section of the brief
2. Explain why these metrics were chosen
3. Show how they align with website goals
4. Set baseline metrics before launch
5. Track against metrics post-launch

---

## Next Steps After Brief

1. **Review with Client** (2-3 hours)
   - Walk through positioning and messaging
   - Get buy-in on differentiators and claims
   - Validate target customer understanding

2. **Design Phase** (1-2 weeks)
   - Use sitemap and templates as design brief
   - Create wireframes following recommended structure
   - Build design system aligned with positioning

3. **Content Creation** (1-2 weeks)
   - Copywriter customizes templates with brand voice
   - Create final copy for all pages
   - Collect/optimize images and testimonials

4. **Development** (1-3 weeks)
   - Build website from design
   - Implement messaging and CTAs
   - Set up analytics and conversion tracking

5. **Launch & Optimize** (Ongoing)
   - Monitor KPIs against targets
   - Adjust copy/CTAs based on performance
   - Gather customer feedback
   - Iterate positioning if needed

---

## Getting Help

- **Something in the output doesn't make sense?** → Review [agent-prompt-guide.md](../skills/website-post-onboarding-agent/references/agent-prompt-guide.md)
- **How do I customize the agent?** → See [ARCHITECTURE.md](./ARCHITECTURE.md)
- **Is my output good quality?** → Check [quality-standards.md](../skills/website-post-onboarding-agent/references/quality-standards.md)
- **Need an example?** → See [example-website-brief.md](../skills/website-post-onboarding-agent/references/example-website-brief.md)

---

**Ready for your next client?** Start with [SETUP.md](./SETUP.md) or jump to the full [README](../README.md).
