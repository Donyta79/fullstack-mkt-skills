# Versions

> Theo doi phien ban cua tat ca skills. Agent co the so sanh voi ban local de biet can cap nhat.

## Current versions

| Skill | Version | Last Updated | Category |
|-------|---------|--------------|----------|
| product-marketing-context | 1.0.0 | 2026-04-24 | foundation |
| 00-ke-hoach-mkt | 2.0.0 | 2026-04-24 | strategy |
| 01-lich-noi-dung | 2.0.0 | 2026-04-24 | content |
| 02-brief-chien-dich | 2.0.0 | 2026-04-24 | strategy |
| 03-danh-gia-hieu-suat | 2.0.0 | 2026-04-24 | performance |
| 04-script-video | 2.0.0 | 2026-04-24 | content |
| 05-copy-quang-cao | 2.0.0 | 2026-04-24 | content |
| 06-brief-ugc-egc | 2.0.0 | 2026-04-24 | content |
| 07-bao-cao-marketing | 2.0.0 | 2026-04-24 | performance |
| 08-nghien-cuu-doi-thu | 2.0.0 | 2026-04-24 | strategy |
| 09-insight-khach-hang | 2.0.0 | 2026-04-24 | strategy |
| 10-tinh-kpi-nguoc | 2.0.0 | 2026-04-24 | performance |
| 11-thiet-lap-kenh | 2.0.0 | 2026-04-24 | operations |
| 12-brief-landing-page | 2.0.0 | 2026-04-24 | operations |
| 13-phan-tich-du-lieu | 2.0.0 | 2026-04-24 | operations |
| 14-email-marketing | 2.0.0 | 2026-04-24 | operations |
| 15-social-listening | 2.0.0 | 2026-04-24 | content |
| 16-marketing-psychology | 1.0.0 | 2026-04-24 | strategy |
| 17-pricing-strategy | 1.0.0 | 2026-04-24 | strategy |
| 18-referral-program | 1.0.0 | 2026-04-24 | operations |
| 19-ab-test-setup | 1.0.0 | 2026-04-24 | performance |

## Changelog

### 2026-04-24 — v2.0.0 (Major release)

**BREAKING CHANGES:**
- Restructure skills: `skills/name.md` → `skills/name/SKILL.md`
- Update frontmatter spec to match [agentskills.io](https://agentskills.io)
- Path migration: references moved into per-skill folders (where applicable)

**New features:**
- Added foundation skill `product-marketing-context` — every skill reads this first
- Added `.claude-plugin/marketplace.json` — install via `/plugin install`
- Added `AGENTS.md` — universal agent compatibility spec
- Added `VERSIONS.md` — version tracking
- Added `validate-skills.sh` + `validate-skills.ps1` — spec validators
- Added `.github/` templates (issues, PRs)
- Added `CONTRIBUTING.md`

**New skills (4):**
- `16-marketing-psychology` — Nguyen ly tam ly trong marketing (Cialdini + VN cultural context)
- `17-pricing-strategy` — Chien luoc gia cho thi truong VN
- `18-referral-program` — He thong gioi thieu va hoa hong
- `19-ab-test-setup` — Thiet lap A/B test don gian

**Upgrades to existing skills:**
- Bump all 16 skills from 1.0.0 to 2.0.0
- Add `metadata.version` field to frontmatter
- Optimize descriptions for trigger phrase matching
- Add reference to `product-marketing-context` foundation

**Plugin compat:**
- Repo is now an official Claude Code Plugin Marketplace
- Install via: `/plugin install minhnv0807/fullstack-mkt-skills`

### 2026-04-23 — v1.1.0

- Rebrand: Run By Linh → Over Powers Agency
- Redesign README with badges, diagrams, visual tables
- Add star history chart

### 2026-04-23 — v1.0.0 (Initial release)

- 16 marketing skills (strategy, content, performance, operations)
- 5 reference files (benchmarks, channel system, KPI formulas, content angles, tool stack)
- 3 workflows (campaign-launch, monthly-cycle, content-production)
- 4 agents (mkt-strategist, content-producer, performance-analyst, channel-operator)
- 2 examples (spa-beauty, ecommerce-fashion)
- install.sh + install.ps1
- MIT License

## Versioning policy

- **Major** (X.0.0): Breaking change (frontmatter, folder structure, removed skill)
- **Minor** (1.X.0): New skill or new major section
- **Patch** (1.0.X): Bug fix, benchmark update, syntax correction

## How agents check for updates

```bash
# Check if local is outdated
curl -s https://raw.githubusercontent.com/minhnv0807/fullstack-mkt-skills/master/VERSIONS.md | head -30

# Update all skills
cd ~/.claude/skills/marketing && git pull
```
