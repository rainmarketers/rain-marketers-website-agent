# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-05-04

### Added

**Core Skill**
- Website Post-Onboarding Agent (`/website-post-onboarding-agent`)
  - Analyzes client websites and current positioning
  - Research 5-7 direct competitors
  - Identifies defensible positioning gaps
  - Develops 3 core messaging pillars
  - Creates strategic website brief
  - Generates content templates for all page types
  - Recommends industry-appropriate sitemaps
  - Sets measurable success KPIs

**Reference Materials** (7 documents)
- `example-website-brief.md` – Real output example (Clean Cut Gutters)
- `page-content-templates.md` – Copy templates for all page types
- `sitemap-builder.md` – Industry-specific website structures
- `onboarding-form-fields.md` – Client intake questionnaire
- `competitor-analysis.md` – Competitor research methodology
- `agent-prompt-guide.md` – How the agent operates
- `quality-standards.md` – Output quality evaluation checklist

**Documentation**
- `README.md` – Project overview and quick start
- `docs/SETUP.md` – Installation and configuration guide
- `docs/USAGE.md` – How to use the agent walkthrough
- `docs/ARCHITECTURE.md` – Repository structure and extension guide
- `CONTRIBUTORS.md` – Team and contribution guidelines
- `CHANGELOG.md` – This file

**Examples**
- `examples/sample-client-brief/` – Complete example (Clean Cut Gutters)
  - Full positioning brief
  - Competitive analysis
  - Content templates
  - Sitemap recommendations
  - Asana task structure

**Project Foundation**
- MIT License
- .gitignore with standard exclusions
- Project instructions for Claude Code (`.claude/CLAUDE.md`)

### Features

- **Market Research**: Analyze client website and identify market positioning
- **Competitive Analysis**: Research 5-7 direct competitors and map positioning claims
- **Positioning Strategy**: Develop defensible positioning with proof points
- **Website Brief**: Recommend structure, messaging, CTAs, and KPIs
- **Content Templates**: Ready-to-customize copy for homepage, services, about, testimonials, FAQ, contact pages
- **Sitemap Recommendations**: Industry-specific page structures for 6+ industries
- **Asana Integration**: Auto-create project tasks for tracking brief execution (optional)
- **Quality Standards**: Evaluation checklist to ensure brief meets quality bar

### Industry Support

Out of the box, the agent can analyze and recommend for:
- B2C Services (home services, salons, fitness)
- B2B Services (agencies, consulting, outsourcing)
- B2B SaaS (software as a service)
- E-commerce (physical products)
- Local Services (retail, restaurants, professional services)
- Publishers (blogs, news, content)

### Integrations

- **Asana** (optional) – Auto-creates tasks and project structure

### Documentation Structure

Organized for different audiences:
- **Team**: README, SETUP, USAGE
- **Designers/Copywriters**: USAGE, example-website-brief, page-content-templates
- **Developers**: ARCHITECTURE
- **Contributors**: CONTRIBUTORS

---

## Future Releases

### [1.1.0] - Planned

- [ ] Website Copywriting Agent – Write final copy from brief
- [ ] Design System Generator – Create design patterns from positioning
- [ ] Enhanced competitor analysis with local SEO signals

### [1.2.0] - Planned

- [ ] SEO Optimization Agent – Technical and content SEO recommendations
- [ ] Performance Auditor – Page speed and Core Web Vitals analysis

### [2.0.0] - Planned

- [ ] Multi-language support
- [ ] Industry-specific templates expansion
- [ ] Advanced analytics integration

---

## Release Notes by Version

### Version 1.0.0 (Current)

**Stability**: Production-ready

**What works**:
- ✅ Website analysis and positioning development
- ✅ Competitive research and gap analysis
- ✅ Positioning statement generation
- ✅ Content template generation
- ✅ Sitemap recommendations
- ✅ Asana integration for task creation

**Known Limitations**:
- Analysis limited to English-language websites
- Competitor research works best in established industries (5-7+ competitors exist)
- Asana integration requires exact project name match
- Content templates are frameworks (require customization for brand voice)

**Tested Scenarios**:
- ✅ Local services (gutter cleaning, plumbing, HVAC)
- ✅ Salons and fitness studios
- ✅ Professional services (accounting, consulting)
- ✅ Home service contractors

---

## How to Report Issues

Found a bug? Have a suggestion? Open an issue on GitHub or contact the team.

**Include**:
- Client name/industry (if shareable)
- Website URL analyzed
- What you expected
- What actually happened
- Steps to reproduce

---

## How to Contribute

Want to improve this project? See [CONTRIBUTORS.md](./CONTRIBUTORS.md) for guidelines.

---

## Semantic Versioning

This project follows semantic versioning:

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backwards compatible manner
- **PATCH** version when you make backwards compatible bug fixes

---

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).

---

**Last updated**: May 4, 2026

For current project status and upcoming features, see [ARCHITECTURE.md](./docs/ARCHITECTURE.md#future-structure).
