# Architecture & Organization

How the repo is structured and how to extend it with new skills.

---

## Directory Structure

```
rain-marketing-website-agent/
├── README.md                                # Main entry point
├── CONTRIBUTORS.md                          # Team credits
├── CHANGELOG.md                             # Release notes
├── LICENSE                                  # MIT License
├── WEBSITE_AGENT_DOCUMENTATION.md           # Technical deep-dive (legacy)
│
├── skills/                                  # Skill definitions (auto-discovered)
│   └── website-post-onboarding-agent/      # Main skill
│       ├── SKILL.md                         # Skill definition (entry point)
│       └── references/                      # Knowledge base (on-demand docs)
│           ├── example-website-brief.md     # Real output example
│           ├── page-content-templates.md    # Copy templates
│           ├── sitemap-builder.md           # Page structure recommendations
│           ├── onboarding-form-fields.md    # Client intake form
│           ├── competitor-analysis.md       # Competitor research methodology
│           ├── agent-prompt-guide.md        # How the agent operates
│           └── quality-standards.md         # Output quality checklist
│
├── docs/                                    # Documentation (this layer)
│   ├── SETUP.md                             # Installation & configuration
│   ├── USAGE.md                             # How to use the agent
│   └── ARCHITECTURE.md                      # This file
│
├── examples/                                # Example outputs & workflows
│   └── sample-client-brief/                 # Complete real example
│       ├── README.md                        # Project context
│       ├── brief.md                         # The actual brief output
│       └── asana-tasks.json                 # Auto-created tasks
│
├── .claude/                                 # Claude Code project files
│   └── CLAUDE.md                            # Project instructions for Claude
│
├── .gitignore                               # Git ignore rules
└── LICENSE                                  # MIT License text
```

---

## Layer 1: Skill Definition

**Location**: `skills/website-post-onboarding-agent/SKILL.md`

**Purpose**: Defines the skill behavior, input/output, and execution flow.

**Key sections**:
- Skill name and description
- Input parameters (client name, website URL)
- Processing steps (analysis, research, synthesis)
- Output format
- Integration points (Asana, etc.)

**When to edit**: If you want to change how the skill operates (e.g., different competitor count, new output sections).

---

## Layer 2: Reference Documents

**Location**: `skills/website-post-onboarding-agent/references/`

**Purpose**: Knowledge base that the skill references. These are on-demand documents loaded during execution.

### Each reference document:

| Document | Purpose | Owner | When to Edit |
|----------|---------|-------|-------------|
| `example-website-brief.md` | Real output from a complete brief | Strategy | Update with new examples |
| `page-content-templates.md` | Copy frameworks for all page types | Copywriting | When copy guidelines change |
| `sitemap-builder.md` | Industry-specific page structures | IA | When adding new industries |
| `onboarding-form-fields.md` | Client intake questionnaire | Strategy | When needing new client data |
| `competitor-analysis.md` | Competitor research methodology | Research | When refining analysis approach |
| `agent-prompt-guide.md` | Instructions for how agent operates | Engineering | When changing agent logic |
| `quality-standards.md` | Output evaluation criteria | QA | When refining quality bars |

**Design principle**: Each reference is **self-contained** and **reusable**. Copywriters can use `page-content-templates.md` without reading SKILL.md. Designers can use `sitemap-builder.md` independently.

---

## Layer 3: Documentation

**Location**: `docs/`

**Purpose**: User-facing guides for different audiences.

### SETUP.md
- **Audience**: Anyone installing or configuring
- **Content**: Prerequisites, quick start, configuration, troubleshooting
- **When to update**: When setup process changes

### USAGE.md
- **Audience**: Strategy team, designers, copywriters
- **Content**: How to use the agent, understanding output, customization
- **When to update**: When workflows change

### ARCHITECTURE.md
- **Audience**: Developers extending the system
- **Content**: This file. How the repo is organized, how to add new skills
- **When to update**: When adding new skills or restructuring

---

## Layer 4: Examples

**Location**: `examples/sample-client-brief/`

**Purpose**: Real, complete example of the agent's output.

**Contains**:
- `README.md` – Context about the example client
- `brief.md` – The actual brief output (real)
- `asana-tasks.json` – Auto-created task structure (sample)

**When to update**: When you want to add new examples or update with latest real client work.

---

## How It Works: The 4-Layer Flow

```
1. USER INPUT
   /website-post-onboarding-agent "Client" "https://website.com"
   
   ↓
   
2. SKILL LAYER (SKILL.md)
   • Parses input
   • Routes to reference docs
   • Executes analysis steps
   • Synthesizes output
   
   ↓
   
3. REFERENCE LAYER (references/)
   • competitor-analysis.md → guides competitor research
   • page-content-templates.md → structures copy
   • sitemap-builder.md → guides site structure
   • onboarding-form-fields.md → informs questions to ask
   • quality-standards.md → validates output
   
   ↓
   
4. OUTPUT
   Website Brief:
   • Executive summary
   • Market research
   • Positioning strategy
   • Website brief
   • Content templates
   • Sitemap recommendations
   • Asana tasks (if enabled)
```

---

## Extending the System: Adding a New Skill

### Scenario: You want to add a "Website Copywriting Agent"

Here's how you'd structure it:

#### Step 1: Create the skill directory

```bash
mkdir -p skills/website-copywriting-agent/references
```

#### Step 2: Create SKILL.md

**Location**: `skills/website-copywriting-agent/SKILL.md`

**Template**:
```markdown
# Website Copywriting Agent

**Purpose**: Write final website copy based on a positioning brief.

**Inputs**:
- Website brief (from post-onboarding agent)
- Brand voice guidelines (optional)
- Target audience details

**Process**:
1. Parse the positioning brief
2. Apply [copy-guidelines.md reference]
3. Customize templates per page type
4. Validate against [quality-standards.md]
5. Create final copy deliverable

**Outputs**:
- Homepage copy (final)
- Services page copy (final)
- About Us copy (final)
- [etc.]
```

#### Step 3: Create reference documents

Create supporting docs in `references/`:

```
skills/website-copywriting-agent/references/
├── copy-guidelines.md          # Brand voice, tone, style rules
├── copywriting-framework.md    # How-to for writing compelling copy
├── example-copy-output.md      # Real example of final copy
└── qa-checklist.md             # How to evaluate final copy
```

#### Step 4: Add to the ecosystem

Update the main README to link to it:

```markdown
| `/website-copywriting-agent` | Takes a brief and writes final website copy | [SKILL.md](./skills/website-copywriting-agent/SKILL.md) |
```

#### Step 5: Document in ARCHITECTURE.md

Update this file with the new skill in the registry.

---

## Naming Conventions

- **Skill directories**: `kebab-case` (e.g., `website-copywriting-agent`)
- **SKILL.md files**: Always named `SKILL.md`
- **Reference docs**: `kebab-case` (e.g., `copy-guidelines.md`)
- **Commands**: `/skill-name [subcommand] [args]`

---

## Design Principles

### 1. Progressive Disclosure

Only load the knowledge you need:
- SKILL.md is the entry point
- Reference docs are on-demand (loaded during execution)
- Documentation is user-focused (SETUP, USAGE, ARCHITECTURE)

### 2. Modularity

Each skill is independent:
- Can be used standalone
- References are self-contained
- No circular dependencies

### 3. Reusability

Documentation serves multiple purposes:
- Quality checklist is used by skill AND team review
- Example brief is used for onboarding AND for QA training
- Competitor analysis doc is used by agent AND for manual research

### 4. Scalability

Adding new skills doesn't require code:
- Just create `/skills/new-skill-name/` directory
- Add SKILL.md and reference docs
- Update main README
- Done

---

## File Size Guidelines

- **SKILL.md**: Keep under 500 lines / 5,000 tokens
- **Reference docs**: 100-300 lines each
- **Documentation (docs/)**: 200-500 lines each
- **Examples**: Reasonable size (this is real output)

If a file gets too large:
- Split into multiple reference docs
- Link between them
- Keep each focused

---

## Future Structure

When you add skills, the structure evolves:

```
rain-marketing-website-agent/
├── skills/
│   ├── website-post-onboarding-agent/    [Current]
│   ├── website-copywriting-agent/        [Future]
│   ├── website-design-system-agent/      [Future]
│   ├── seo-optimization-agent/           [Future]
│   └── performance-audit-agent/          [Future]
├── docs/
│   └── (same structure)
├── examples/
│   ├── sample-client-brief/              [Current]
│   ├── sample-copy-output/               [Future]
│   └── sample-design-system/             [Future]
└── README.md                             [Updates to link all skills]
```

---

## Maintenance

### Regular Updates

- **Reference docs**: Update when methodology changes (quarterly review)
- **Examples**: Add new real examples when good outputs exist (monthly)
- **Documentation**: Update when workflows change (ad-hoc)
- **SKILL.md**: Update when agent behavior changes (ad-hoc)

### Quality Gates

Before merging any changes:
- [ ] Reference docs are up-to-date
- [ ] Example is current/accurate
- [ ] SKILL.md reflects actual behavior
- [ ] README is accurate
- [ ] No broken links in documentation

---

## CI/CD Integration (Future)

When you scale, consider automation:

- **Linting**: Validate SKILL.md format
- **Links**: Check all documentation links work
- **Examples**: Validate example outputs pass quality checklist
- **Versioning**: Tag releases, auto-generate CHANGELOG

For now: manual review before merge.

---

## Key Files to Know

| File | Purpose | Edit Frequency |
|------|---------|-----------------|
| `skills/website-post-onboarding-agent/SKILL.md` | Agent behavior | Low (design changes) |
| `skills/website-post-onboarding-agent/references/*` | Knowledge base | Medium (quarterly updates) |
| `README.md` | Project overview | Low (major releases) |
| `docs/SETUP.md` | Installation guide | Low (config changes) |
| `docs/USAGE.md` | How-to guide | Medium (workflow changes) |
| `docs/ARCHITECTURE.md` | Structure guide | Medium (new skills) |
| `CHANGELOG.md` | Release notes | Every release |

---

## Getting Started

**If you want to...**

- ✅ **Use the skill** → Start with [SETUP.md](./SETUP.md)
- ✅ **Understand output** → Read [USAGE.md](./USAGE.md)
- ✅ **Add a new skill** → Read this file (ARCHITECTURE.md), then create `skills/new-skill/`
- ✅ **Understand the brief** → See `examples/sample-client-brief/`
- ✅ **Evaluate quality** → Use [quality-standards.md](../skills/website-post-onboarding-agent/references/quality-standards.md)

---

## Questions?

- Structure questions → This file (ARCHITECTURE.md)
- Usage questions → [USAGE.md](./USAGE.md)
- Setup questions → [SETUP.md](./SETUP.md)
- Contributor questions → [CONTRIBUTORS.md](../CONTRIBUTORS.md)
