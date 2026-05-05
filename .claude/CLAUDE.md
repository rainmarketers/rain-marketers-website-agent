# Rain Marketers Website Agent

## Project Instructions for Claude Code

This file contains project-specific instructions for working with the Website Post-Onboarding Agent.

---

## Quick Start

**Main skill**: `/website-post-onboarding-agent "Client Name" "https://website.com"`

**Documentation**:
- [README.md](../README.md) – Project overview
- [docs/SETUP.md](../docs/SETUP.md) – Installation guide
- [docs/USAGE.md](../docs/USAGE.md) – How to use
- [docs/ARCHITECTURE.md](../docs/ARCHITECTURE.md) – Structure and extension

---

## Project Context

**What it does**: Analyzes client websites, researches competitors, develops positioning strategy, and generates website briefs with content templates.

**Who uses it**: Rain Marketers team for client onboarding.

**Output**: Strategic website brief, competitive analysis, content templates, sitemap recommendations, Asana tasks.

---

## Key Files

| File | Purpose |
|------|---------|
| `skills/website-post-onboarding-agent/SKILL.md` | Main skill definition |
| `skills/website-post-onboarding-agent/references/` | Knowledge base (7 documents) |
| `docs/SETUP.md` | Setup and configuration |
| `docs/USAGE.md` | Usage walkthrough |
| `docs/ARCHITECTURE.md` | Structure and extension guide |
| `examples/sample-client-brief/` | Real example output |

---

## Development Rules

### When Editing SKILL.md

- Keep under 500 lines
- Update `agent-prompt-guide.md` if behavior changes
- Test with a real client website first
- Update example brief if output format changes

### When Editing Reference Docs

- Keep each under 300 lines
- Ensure they're self-contained (can be read independently)
- Update [quality-standards.md](../skills/website-post-onboarding-agent/references/quality-standards.md) if evaluation criteria change
- Cross-reference between docs where helpful

### When Adding New Content

- Create in `skills/website-post-onboarding-agent/references/`
- Ensure it's focused on one aspect
- Link from SKILL.md and README
- Update ARCHITECTURE.md if it's a new reference layer

### When Testing

1. Run with a real client (or realistic example)
2. Check output against [quality-standards.md](../skills/website-post-onboarding-agent/references/quality-standards.md)
3. Verify Asana integration (if using Asana)
4. Test with different industries (SaaS, local services, e-commerce, etc.)

---

## Adding New Skills

To add a new skill (e.g., copywriting agent):

1. Read [docs/ARCHITECTURE.md](../docs/ARCHITECTURE.md) → "Extending the System"
2. Create `skills/your-new-skill/` directory
3. Add `SKILL.md` and reference docs
4. Update main README with new skill
5. Add to [CONTRIBUTORS.md](../CONTRIBUTORS.md) as future skill
6. Commit and update CHANGELOG.md

**Structure**:
```
skills/your-new-skill/
├── SKILL.md                          # Main definition
└── references/
    ├── example-output.md             # Real example
    ├── methodology.md                # How it works
    ├── qa-checklist.md              # Quality standards
    └── ...
```

---

## Integrations

### Asana (Optional)

If Asana project exists with exact client name:
- Agent automatically creates tasks
- Requires valid Asana token
- Tasks are created under project

To test: Create an Asana project named "Test Client" and run agent.

---

## Quality Gates

Before committing:

- [ ] All links in documentation work
- [ ] No spelling/grammar errors
- [ ] Files follow naming conventions (kebab-case)
- [ ] SKILL.md reflects actual behavior
- [ ] Example output is current and accurate
- [ ] README links are correct

---

## Common Tasks

### Update Example Brief

**When**: New client work looks like a good example

**How**:
1. Review output against quality-standards.md
2. Copy brief to `examples/sample-client-brief/brief.md`
3. Update README in that folder with client context
4. Update CHANGELOG.md with new example version

### Improve a Reference Doc

**When**: You find a better way to explain something

**How**:
1. Edit the reference doc directly
2. Test that agent still produces good output
3. Get feedback if significant change
4. Commit with clear message

### Add a New Industry Example

**When**: You want to show agent works for new industry

**How**:
1. Run agent on real (or realistic) company in that industry
2. If output is great, save to `examples/`
3. Update README example list
4. Update CHANGELOG.md

---

## Troubleshooting

**Agent produces generic output**
- Check that client info is detailed (pain points, differentiators)
- Review [onboarding-form-fields.md](../skills/website-post-onboarding-agent/references/onboarding-form-fields.md)
- Provide more context in client brief

**Competitors not found**
- Some niche industries have few competitors
- Agent finds what exists; manually add more if needed
- Check [competitor-analysis.md](../skills/website-post-onboarding-agent/references/competitor-analysis.md) methodology

**Asana tasks not created**
- Verify project name matches client name exactly
- Check Asana token is valid
- See [SETUP.md](../docs/SETUP.md) troubleshooting section

---

## Philosophy

This project follows these principles:

1. **Progressive Disclosure**: Load knowledge as needed, not upfront
2. **Modularity**: Each skill is independent, reusable
3. **Scalability**: Add skills without changing existing ones
4. **Simplicity**: Keep files focused and readable
5. **Quality First**: Output must meet standards before release

---

## Getting Help

- **How do I use this?** → [docs/USAGE.md](../docs/USAGE.md)
- **How is it organized?** → [docs/ARCHITECTURE.md](../docs/ARCHITECTURE.md)
- **How do I extend it?** → [docs/ARCHITECTURE.md](../docs/ARCHITECTURE.md#extending-the-system-adding-a-new-skill)
- **How do I contribute?** → [CONTRIBUTORS.md](../CONTRIBUTORS.md)

---

## Next Steps

1. Review [docs/SETUP.md](../docs/SETUP.md) to understand configuration
2. Read [docs/USAGE.md](../docs/USAGE.md) to understand workflow
3. Check [examples/sample-client-brief/](../examples/sample-client-brief/) for real output
4. Review [skills/website-post-onboarding-agent/references/](../skills/website-post-onboarding-agent/references/) for methodology

---

**Last updated**: May 4, 2026

For project-level decisions, see [CONTRIBUTORS.md](../CONTRIBUTORS.md).
For architectural questions, see [docs/ARCHITECTURE.md](../docs/ARCHITECTURE.md).
