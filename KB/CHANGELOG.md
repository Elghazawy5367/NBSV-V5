# NBSV System — CHANGELOG

All significant changes to the NBSV system are documented here.
Format: [VERSION] — DATE — CHANGE TYPE — Description

---

## [5.0.0] — March 2026

### Architecture: Reactive → Proactive (Breaking Change)
- **Added** Scout agent layer: `scout-reddit.yml`, `scout-rss.yml`, `scout-kickstarter.yml`
- Agents run on schedule, discover candidates autonomously, create pre-labeled Issues
- Architecture shift: external world → scouts → Issues → founder decides (vs. founder → Issue → agents)
- See: `docs/adr/002-proactive-scout-architecture.md`

### Multi-Model Routing
- **Changed** `brief-forge.yml`: model switched from `gpt-4o` → `Mistral-large` (fallback: `gpt-4o`)
- **Changed** `scout-*.yml`: use `gpt-4o-mini` for high-volume initial triage
- **Unchanged** `orchestrator.yml` filter + `pattern-brain.yml` analysis: retain `gpt-4o`
- See: `docs/adr/003-multi-model-routing.md`

### Gap Sentinel Upgrade
- **Added** GPT-4o reasoning-based Q1 pre-assessment (replaces broken CSS-selector scraping approach)
- Pre-assessment labels: `ai-likely-clear`, `ai-flagged-found` — reduce manual verification to ~20-30%
- **Fixed** v4.0 CSS selector approach: Jumia/Noon are JS-rendered SPAs — scraping HTML returns empty shells

### Pattern Brain Upgrade
- **Added** Step 5: Config Auto-Update Loop
- Pattern Brain reads `closed-won` + `presell-stalled` outcomes monthly
- Proposes weighted updates to `egyptian-behaviors.json`
- Opens a Pull Request — founder approves in one click
- Over 12 months: config becomes a self-improving behavioral model from actual sales data

### New Labels
- Scout labels: `scout-reddit`, `scout-yanko`, `scout-core77`, `scout-kickstarter`
- AI assessment labels: `ai-likely-clear`, `ai-flagged-found`, `ai-filter-pass`, `ai-filter-fail`
- Process labels: `needs-human-review`, `scout-error`

### Architecture Documentation
- **Added** `docs/adr/` directory with 3 Architecture Decision Records
- **Added** `schema/candidate.schema.json` — JSON Schema for pipeline data validation
- **Added** `KB/CHANGELOG.md` (this file)

### Orchestrator Upgrade
- **Added** routing for scout-created Issues (activates full filter when founder fills behavior field)
- **Added** manual dispatch options for all 3 scout agents

---

## [4.0.0] — March 2026

### Filter: Category Gate → Principle-Based (Breaking Change)
- **Removed** 6-category hard gate (Small Space Storage, Gifting, Car, Desk, Children's, Ramadan/Eid)
- **Changed** categories to "High-Yield Scanning Zones" — orientation tools, not mandatory criteria
- **Added** 3-question principle filter as the sole gate
- See: `docs/adr/001-principle-based-filter.md`

### Seasonal Timing: Gate → Amplifier (Breaking Change)
- **Removed** seasonal timing as mandatory filter criterion
- Seasons are now demand multipliers — they amplify but never gate
- Continuous demand products (gifting, car, desk, storage, education) are unaffected by season calendar

### Source Channels
- **Expanded** from 3 channels (Chinese/Korean platforms) to 5:
  - Channel 1: Asian Viral (Douyin / Xiaohongshu / Korean)
  - Channel 2: Concept Mine (Kickstarter / Makuake / Indiegogo)
  - Channel 3: Concept Library (Yanko / Core77 / Behance / Reddit)
  - Channel 4: AI Ideation (Claude / Qwen / ChatGPT)
  - Channel 5: GitHub Intelligence (DXF files / design repos)

### Agent Infrastructure
- **Added** `orchestrator.yml` — master dispatcher routing all Issue events
- **Added** `brief-forge.yml` — auto-generates workshop spec on `principle-3-pass` label
- **Added** `gap-sentinel.yml` — daily verification briefing with links
- **Added** `pattern-brain.yml` — monthly AI failure analysis
- **Added** `season-pulse.yml` — weekly season countdown
- **Added** `presell-sentinel.yml` — deposit tracking

### GitHub Models Integration
- All agents use `models.inference.ai.azure.com` with `$GITHUB_TOKEN` (no external API key)
- Zero Deno/TypeScript runtime dependency — all pure `github-script@v7` JavaScript

---

## [3.0.0] — January 2026

### Filter Changes
- **Added** 6-category hard gate (subsequently removed in v4.0)
- **Added** seasonal timing as mandatory gate (subsequently removed in v4.0)

### Production
- **Added** Semi-DIY finish model as optional production path
- **Rejected** DIY kit model permanently (customer assembly violates zero-explanation rule)

---

## [2.0.0] — December 2025
- Initial GitHub repo structure
- 3-platform scanning stack (Douyin, Xiaohongshu, 1688)

## [1.0.0] — November 2025
- Initial NBSV system design
- Egyptian fast-follower model for physical products
