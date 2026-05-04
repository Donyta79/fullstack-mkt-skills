# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

### Added
- Dynamic badges (stars, issues, last commit, contributors) in README
- CHANGELOG.md following Keep a Changelog format
- CODE_OF_CONDUCT.md (Contributor Covenant 2.1)
- SECURITY.md with vulnerability disclosure policy
- `.github/FUNDING.yml` sponsor button
- `.github/workflows/validate.yml` — CI auto-validates PRs
- `docs/getting-started.md` — full onboarding guide
- `docs/best-practices.md` — skill authoring & usage patterns
- GitHub topics (20 SEO-optimized tags)
- SEO-optimized English repo description

---

## [2.3.0] — 2026-05-03

### Added
- Meta Official MCP endpoint confirmed: `https://mcp.facebook.com/ads` — 29 tools, 3 permission tiers (read-only / read-write / read-write-financial)
- Full 29-tool reference in `mcp-ads-integration.md`: Campaign Management (5), Product Catalog (10), Accounts & Pages (3), Datasets & Tracking (4), Insights & Benchmarks (7)
- 8-step MCP audit workflow in `21-audit-ads-performance` using official tools (anomaly signal → industry benchmark → opportunity score → dataset quality)
- MCP diagnostic + benchmark workflow in `03-danh-gia-hieu-suat` (performance trend → anomaly signal → industry benchmark → opportunity score)
- Dual-source competitor research in `08-nghien-cuu-doi-thu`: Ads Library MCP (observe) + Meta Official MCP (measure) → gap analysis

### Changed
- `21-audit-ads-performance` 1.1.0 → 1.2.0: Expanded MCP section with 11 prioritized official tools + step-by-step audit workflow
- `03-danh-gia-hieu-suat` 2.1.0 → 2.2.0: Added 7 official MCP diagnostic/benchmark tools + 4-step quick assessment workflow
- `08-nghien-cuu-doi-thu` 2.1.0 → 2.2.0: Added Meta Official MCP benchmarks (advertiser context, industry benchmark, auction ranking) alongside Ads Library
- `references/mcp-ads-integration.md` — Major update: confirmed endpoint, full tool list, permission tiers, setup via claude.ai, write warnings, AdKit + Pipeboard CLI additions

---

## [2.2.0] — 2026-05-02

### Added
- **New reference:** `references/hook-formulas-vn.md` — 6 hook types (Con so, Nguoc doi, Bien doi, Muon uy tin, Thu nhan, Khan cap) with VN examples, funnel mapping, platform char limits, anti-patterns
- Content Matrix section in `01-lich-noi-dung` — 8 content formats × pillars = auto-generated ideas (adapted from Justin Welsh method)
- Niche Research section in `15-social-listening` — 20 trending topics in 7 days from 6 VN channels (FB Groups, TikTok Discover, Google News VN, Zalo Communities, Forums, KOL feeds)
- 6 hook formulas + reverse-engineer viral video process + QA Score gate (85/100) in `04-script-video`
- 6 hook types for ads + Copy Scoring system (35/50 gate) in `05-copy-quang-cao`
- Brand Voice analysis with voice signals + absence signals in `product-marketing-context` section 10b

### Changed
- `04-script-video` 2.0.0 → 2.1.0: Hook formulas, viral reverse-engineering, QA scoring
- `05-copy-quang-cao` 2.1.0 → 2.2.0: Ad hook types, copy scoring system
- `01-lich-noi-dung` 2.0.0 → 2.1.0: Content Matrix for idea generation
- `15-social-listening` 2.0.0 → 2.1.0: Niche Research for trending topics
- `product-marketing-context` 1.0.0 → 1.1.0: Enhanced Brand Voice section

### Credits
- Adapted from [charlie947/social-media-skills](https://github.com/charlie947/social-media-skills) (Charlie Hills, 350K+ followers, 100M+ views/year) — hook generator, content matrix, voice builder, post scorer, niche research patterns

---

## [2.1.0] — 2026-05-01

### Added
- **New skill:** `20-brief-client-intake` — 20-industry client intake form for agencies
- **New skill:** `21-audit-ads-performance` — 84-checkpoint ads health audit with scoring
- **New reference:** `references/mcp-ads-integration.md` — 8 MCP servers (Meta/Google/TikTok/Cross-platform)
- **New reference:** `references/copy-frameworks-vn.md` — 6 professional copy frameworks (AIDA, PAS, BAB, 4P, FAB, SSS)
- **New reference:** `references/quality-gates-vn.md` — 10 hard rules for ads quality control
- **New docs:** `docs/skill-map.md` — full system visualization with decision tree
- **New docs:** `docs/mcp-setup-guide.md` — step-by-step MCP setup for Meta/Google/TikTok
- **New docs:** `docs/workflow-guide.md` — unified workflow selection guide
- **New docs:** `docs/update-guide.md` — maintenance and versioning guide
- **New docs:** `docs/faq.md` — FAQ + troubleshooting (20+ Q&As)
- **New workflow:** `workflows/client-onboard.md` — agency client onboarding (5-7 days, 7 skills)
- UML sequence diagrams added to all 4 workflow files
- MCP Ads Integration section added to `CLAUDE.md`

### Changed
- `03-danh-gia-hieu-suat` 2.0.0 → 2.1.0: Health Score system (0-100, grades A-F) + 10 Quality Gates quick-reference + MCP auto-pull data
- `05-copy-quang-cao` 2.0.0 → 2.1.0: 6 copy frameworks with audience temperature selection + Andromeda creative similarity warning
- `08-nghien-cuu-doi-thu` 2.0.0 → 2.1.0: Facebook Ads Library MCP integration for automated competitor ad research
- `21-audit-ads-performance` 1.0.0 → 1.1.0: MCP auto-pull section with GAQL examples

---

## [2.0.0] — 2026-04-24

### BREAKING
- Restructured skills: `skills/name.md` → `skills/name/SKILL.md`
- Frontmatter `name` field now matches directory (includes numeric prefix)
- Compliant with [Agent Skills Spec](https://agentskills.io)

### Added
- **Foundation skill:** `product-marketing-context` — all skills read `.agents/product-marketing-context.md` first. Saves ~70% time per conversation.
- **Plugin manifest:** `.claude-plugin/marketplace.json` — install via `/plugin install minhnv0807/fullstack-mkt-skills`
- `AGENTS.md` — universal agent compatibility spec
- `VERSIONS.md` — per-skill version tracking
- `validate-skills.sh` + `validate-skills.ps1` — spec validators
- `CONTRIBUTING.md` — contribution guide
- `.github/ISSUE_TEMPLATE/` + `.github/PULL_REQUEST_TEMPLATE/`
- Bilingual docs: `README.md` (English) + `README.vi.md` (Vietnamese)

### New Skills (4)
- `16-marketing-psychology` — 7 Cialdini principles + Vietnam cultural adaptation
- `17-pricing-strategy` — Pricing tiers, charm/anchor/bundle pricing, break-even analysis
- `18-referral-program` — 1-way/2-way/affiliate models + VN channels + anti-fraud
- `19-ab-test-setup` — Sample size calculation + 8 elements to test + statistical significance

### Changed
- All 16 existing skills bumped from 1.0.0 → 2.0.0
- README redesigned with plugin install, foundation skill section, 20-skill table
- Project structure in README reflects new folder-per-skill layout

### Credits
- Inspired by [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) — foundation skill concept + plugin spec structure

---

## [1.1.0] — 2026-04-23

### Changed
- Rebrand: "Run By Linh" → "Over Powers Agency"
- Redesigned README with badges, diagrams, visual tables
- Added star history chart

---

## [1.0.0] — 2026-04-23

### Added
- Initial release with 16 marketing skills:
  - **Strategy (4):** 00-ke-hoach-mkt, 02-brief-chien-dich, 08-nghien-cuu-doi-thu, 09-insight-khach-hang
  - **Content (5):** 01-lich-noi-dung, 04-script-video, 05-copy-quang-cao, 06-brief-ugc-egc, 15-social-listening
  - **Performance (3):** 03-danh-gia-hieu-suat, 07-bao-cao-marketing, 10-tinh-kpi-nguoc
  - **Operations (4):** 11-thiet-lap-kenh, 12-brief-landing-page, 13-phan-tich-du-lieu, 14-email-marketing
- 5 reference files (benchmarks, channel system, KPI formulas, content angles, tool stack)
- 3 workflows (campaign-launch, monthly-cycle, content-production)
- 4 agent personas (mkt-strategist, content-producer, performance-analyst, channel-operator)
- 2 example outputs (spa-beauty, ecommerce-fashion)
- `install.sh` (macOS/Linux) + `install.ps1` (Windows)
- MIT License

---

## Version Guide

- **Major (X.0.0):** Breaking changes (frontmatter spec, folder structure, removed skills)
- **Minor (1.X.0):** New skill added, new major feature
- **Patch (1.0.X):** Bug fixes, benchmark updates, syntax corrections

[Unreleased]: https://github.com/minhnv0807/fullstack-mkt-skills/compare/v2.3.0...HEAD
[2.3.0]: https://github.com/minhnv0807/fullstack-mkt-skills/compare/v2.2.0...v2.3.0
[2.2.0]: https://github.com/minhnv0807/fullstack-mkt-skills/compare/v2.1.0...v2.2.0
[2.1.0]: https://github.com/minhnv0807/fullstack-mkt-skills/compare/v2.0.0...v2.1.0
[2.0.0]: https://github.com/minhnv0807/fullstack-mkt-skills/releases/tag/v2.0.0
[1.1.0]: https://github.com/minhnv0807/fullstack-mkt-skills/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/minhnv0807/fullstack-mkt-skills/releases/tag/v1.0.0
