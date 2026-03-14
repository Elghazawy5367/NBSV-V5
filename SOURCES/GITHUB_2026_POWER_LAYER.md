# NBSV — GitHub 2026 Power Layer
## Multi-Agent Orchestration · GitHub Models · Elite Open Source · Agentic Workflows
### March 2026 — Not 2024

---

## THE 2026 SHIFT: GitHub is an Agentic Platform

In 2024, GitHub was a code host you pushed files to.

In 2026, GitHub is a **free autonomous operating system** where:
- **Workflows are agents** — they run on schedule, respond to events, make AI calls, update your repo
- **GitHub Models** — call GPT-4o, Claude, Llama directly FROM workflows using your GitHub token (free with GitHub account, no separate API key)
- **Issues are live records** — not static markdown. Agents read them, comment on them, label them, move them
- **GitHub Projects V2** — a full GraphQL API that your dashboard reads in real-time
- **GitHub Copilot Workspace** — multi-step agentic task execution from a single natural language prompt
- **GitHub Spark** — build and deploy AI micro-apps directly from a repo
- **GitHub MCP** — Claude and other AI tools connect directly to your repo as a live data source

Your NBSV repo is not a document store. It is a **living multi-agent system** where 5 agents run autonomously while you sleep.

---

## YOUR 5 ACTIVE AGENTS

| Agent | File | Trigger | What It Does |
|---|---|---|---|
| **Gap Sentinel** | `gap-sentinel.yml` | Daily 09:00 Egypt | Posts verification links for every open candidate. Auto-flags stale ones. |
| **Season Pulse** | `season-pulse.yml` | Every Monday | Calculates all 8 season countdowns. Labels urgent candidates. Creates weekly briefing issue. |
| **Pattern Brain** | `pattern-brain.yml` | 1st of every month | Reads all rejections, calls AI (GitHub Models GPT-4o), posts intelligence brief issue. |
| **Brief Forge** | `brief-forge.yml` | When issue labeled `principle-3-pass` | Instantly calls AI, generates WhatsApp workshop brief, posts as comment. |
| **Presell Sentinel** | `presell-sentinel.yml` | Wed + Sat / on label | Tracks stalled pre-sells, posts nudges, activates production on deposit confirmation. |

**Total cost: zero.** GitHub Actions free tier: 2,000 minutes/month. These 5 agents use under 50 minutes/month combined.

---

## GITHUB MODELS — FREE AI IN YOUR WORKFLOWS

GitHub Models (`models.inference.ai.azure.com`) gives you access to:
- GPT-4o
- GPT-4o mini
- Phi-4
- Llama 3.3 70B
- Mistral Large
- And more — check `github.com/marketplace/models`

**Authorization:** your existing `${{ secrets.GITHUB_TOKEN }}` — automatically available in every workflow. No extra setup, no credit card, no API key.

**How it's used in NBSV:**
- Pattern Brain calls GPT-4o monthly with your full failure log → intelligence brief
- Brief Forge calls GPT-4o when you label `principle-3-pass` → instant workshop brief
- Both work with zero manual effort

**Rate limits (free):** 15 requests/minute, 150 requests/day per model. More than enough for NBSV's usage pattern.

---

## GITHUB COPILOT WORKSPACE (2026)

Copilot Workspace is an agentic coding environment built into GitHub. Open any issue → click "Open in Copilot Workspace" → describe a multi-step change → Copilot executes it across multiple files.

**NBSV uses:**
- "Update all season dates in `season-pulse.yml` for the new Islamic calendar year"
- "Add a new kill signal category to the failure log template and update the label list in setup.md"
- "Refactor the candidate-scan.md template to add a COGS estimate field"

This is not autocomplete. It is an autonomous multi-file editor that reads your repo context and makes coordinated changes.

**Access:** github.com → any issue → "Open in Workspace" button (requires GitHub Copilot subscription or free trial)

---

## GITHUB MCP INTEGRATION (2026)

GitHub now has a native MCP server: `github.com/github/github-mcp-server`

This lets Claude (and other MCP-compatible tools) connect directly to your repo as a **live tool**, not just a document source.

**What this means for NBSV:**

Instead of copy-pasting issue URLs into Claude, you connect Claude to your repo once via MCP. Then:
- "Run the 3-question filter on Issue #23" → Claude reads the issue, applies filter, posts verdict as comment
- "List all issues with `source-asian-viral` label sorted by creation date" → instant answer
- "What kill signal appears most in my rejected issues this month?" → Claude queries GitHub and answers
- "Generate a workshop brief for Issue #31 and post it as a comment" → Claude reads, generates, posts

**Setup (browser only):**
1. `github.com/github/github-mcp-server` → read the README
2. In Claude.ai → Settings → Integrations → Add MCP server
3. Authorize with your GitHub PAT
4. Claude now has live read/write access to your repo

**Result:** Claude becomes a live operator of your GitHub repo, not just a text assistant.

---

## GITHUB PROJECTS V2 — REAL API KANBAN

GitHub Projects V2 uses GraphQL API. Your dashboard reads it in real-time.

**What's different from V1:** Full API access, custom fields, automation rules, real-time sync.

**Custom fields to add to your NBSV project:**
- `Source Channel` — single select: Asian Viral / Concept Mine / Concept Library / AI Ideation / GitHub Intel
- `Production Path` — single select: Standard / Semi-DIY
- `COGS Estimate` — number field (EGP)
- `Shop Deposits` — number field (count)
- `Season` — single select: Continuous / Ramadan / Eid / etc.
- `Kill Signal` — text field (for failed items)

**Automation rules (built into Projects V2, no code):**
- Issue labeled `principle-1-pass` → move to "Market Verified" column
- Issue labeled `principle-3-pass` → move to "Filter Pass" column
- Issue labeled `pre-sell-confirmed` → move to "Pre-Sell" column
- Issue labeled `in-production` → move to "Production" column
- Issue labeled `closed-won` → move to "Closed Won" column
- Issue labeled `rejected` → move to "Closed Lost" column

**Setup (browser only):**
1. Your repo → Projects → New Project → Board
2. Add the columns above
3. Settings → Workflows → enable each automation rule
4. Done. Every label change moves cards automatically.

---

## GITHUB DISCUSSIONS — ASYNC KNOWLEDGE ACCUMULATION

GitHub Discussions is a structured forum built into your repo. Unlike Issues (which close), Discussions accumulate permanently.

**NBSV Discussion categories to create:**

| Category | Purpose | Compounds Over Time |
|---|---|---|
| `📊 Cycle Retrospectives` | Post-mortem after each completed cycle | After 8 cycles: pattern library of what sells |
| `🇪🇬 Egyptian Market Intel` | Any observation about Egyptian consumer behavior | Behavioral heuristics that sharpen the AHA filter |
| `🔍 Source Channel Reports` | Weekly scan session notes | Which channel is yielding signal this season |
| `🔨 Workshop Network` | Notes on workshop types and capabilities (no names) | Capability database by area |
| `🧠 Filter Edge Cases` | Borderline candidates and how the filter was applied | Sharpens judgment on ambiguous cases |

**AI summary feature (2026):** GitHub now summarizes Discussion threads with AI on demand. A 6-month Discussions thread → "Summarize" → instant pattern extraction.

---

## ELITE OPEN SOURCE REPOS — 2026 ACTIVE TARGETS

### Tier 1 — Design File Goldmines (Fork These)

| Repo | Stars | Why It Matters |
|---|---|---|
| `makers-mark/laser-cut-library` type repos | 500–2000 | Production-ready DXF/SVG, community-tested |
| OpenDesk platform repos | 1000+ | Professional furniture and storage — open license |
| Fab Foundation community repos | varies | Fab lab community — tested in actual workshops globally |
| `awesome-laser-cutting` awesome list | 800+ | Curated directory of every laser design resource on earth |
| `dxf-library` type repos | 100–400 | Raw DXF files, no abstraction |

**How to find them now:**
```
github.com/topics/laser-cutting → sort by Stars
github.com/topics/cnc-files → sort by Recently Updated
github.com/topics/flat-pack → scroll for storage/organizer designs
Search: "organizer" "dxf" OR "svg" stars:>50 pushed:>2025-01-01
Search: "storage" "laser cut" "files" stars:>30
```

### Tier 2 — Trend Intelligence (Watch These)

| Signal Type | How to Find | What You Capture |
|---|---|---|
| Kickstarter scrapers | Search `kickstarter scraper results` → read output files | Campaign data published as CSV/JSON — no code |
| AliExpress trending | Search `aliexpress trending products 2026` | Published trend reports |
| Product research repos | Search `"product opportunity" analysis stars:>20` | Gap analyses with no manufacturing solution |
| r/somebodymakethis aggregators | Search `somebodymakethis top posts` | Aggregated top-voted unmet needs |
| Yanko Design scrapers | Search `yanko design rss` | Auto-collected design posts |

### Tier 3 — AI Orchestration Repos (Study and Adapt)

These repos contain patterns you adapt to NBSV's multi-agent system:

| Repo Type | GitHub Search | What to Extract |
|---|---|---|
| GitHub Actions AI workflows | `github actions openai` OR `github actions anthropic` stars:>100 | Patterns for calling AI from workflows |
| Issue automation repos | `github issue automation ai` stars:>50 | Patterns for AI-generated issue comments |
| Multi-agent GitHub systems | `multi agent github actions` stars:>30 | Orchestration architectures |
| GitHub Models examples | `github models examples` OR `github.com/Azure-Samples/github-models` | Official GitHub Models usage patterns |

### Tier 4 — The GitHub Models Marketplace

`github.com/marketplace/models` — browse all available models, test them in the playground, get code snippets.

**For NBSV specifically:**
- Use the playground to test your filter prompts before putting them in workflows
- Test Pattern Brain's analysis prompt against sample failure data
- Compare GPT-4o vs Llama vs Mistral for Brief Forge output quality
- All free in the playground

---

## GITHUB COPILOT EXTENSIONS (2026)

Copilot Extensions let third-party services integrate directly into GitHub Copilot Chat.

**Currently useful for NBSV:**
- `@perplexity` extension in Copilot Chat: ask "what's trending on Douyin this week" while inside your repo
- `@web` extension: real-time web lookup without leaving GitHub
- Custom extension (advanced): build a Copilot Extension that reads your `egyptian-behaviors.json` and answers "does this product have an Egyptian behavior match?"

**Access:** github.com/marketplace → filter by Copilot Extensions → install free ones

---

## GITHUB SPARK — AI MICRO-APPS FROM YOUR REPO (2026)

GitHub Spark lets you build and deploy AI-powered micro-apps with a natural language prompt. They run on GitHub's infrastructure. Zero deployment cost.

**NBSV Spark app ideas:**
- "A tool that takes a product description and returns the 3-question filter result" — one-screen app, shareable URL, no hosting
- "A seasonal countdown display for Egypt's 8 demand windows" — embed in your repo README
- "A workshop COGS calculator with Standard/Semi-DIY toggle" — works on mobile, send to workshops

**Access:** spark.github.com (requires GitHub account)

---

## THE MULTI-AGENT ORCHESTRATION ARCHITECTURE

```
═══════════════════════════════════════════════════════
NBSV MULTI-AGENT SYSTEM — MARCH 2026
═══════════════════════════════════════════════════════

EXTERNAL WORLD                    GITHUB REPO (YOUR OPERATING SYSTEM)
─────────────────                 ─────────────────────────────────────
                                  
You scan Douyin/                  ┌──────────────────────────────────┐
Kickstarter/Yanko  ──────────────▶│  ISSUE CREATED (candidate label) │
                                  └──────────────┬───────────────────┘
                                                 │
                    ┌────────────────────────────▼────────────────┐
                    │  GAP SENTINEL (daily)                        │
                    │  Posts verification links → you check        │
                    │  Auto-flags stale → auto-labels result       │
                    └────────────────────────────┬────────────────┘
                                                 │ principle-1-pass label
                    ┌────────────────────────────▼────────────────┐
                    │  YOU apply Q2 + Q3 filter                    │
                    │  (in Issue, via Claude Project, or dashboard)│
                    └────────────────────────────┬────────────────┘
                                                 │ principle-3-pass label
                    ┌────────────────────────────▼────────────────┐
                    │  BRIEF FORGE (instant trigger)               │
                    │  Calls GitHub Models → generates brief       │
                    │  Posts WhatsApp spec as Issue comment        │
                    └────────────────────────────┬────────────────┘
                                                 │ brief-ready label
                    ┌────────────────────────────▼────────────────┐
                    │  PRESELL SENTINEL (Wed + Sat)                │
                    │  Tracks stall → posts nudge at day 7        │
                    │  Flags at day 14 → presell-stalled label    │
                    └────────────────────────────┬────────────────┘
                                                 │ pre-sell-confirmed label
                    ┌────────────────────────────▼────────────────┐
                    │  PRODUCTION ACTIVATED                        │
                    │  Shop deposits fund workshop deposit         │
                    │  Zero personal capital                       │
                    └────────────────────────────┬────────────────┘
                                                 │ closed-won label
                    ┌────────────────────────────▼────────────────┐
                    │  PATTERN BRAIN (monthly)                     │
                    │  Reads all rejections → GitHub Models AI     │
                    │  Posts intelligence brief → Wiki             │
                    └─────────────────────────────────────────────┘

PARALLEL AGENTS (always running in background):
  SEASON PULSE (Mondays) → watches all 8 seasons → labels urgent candidates
  
═══════════════════════════════════════════════════════
```

**The net effect:** The system runs itself. You scan. You filter. You visit shops. The infrastructure tracks, nudges, generates, and learns autonomously.

---

## WEEKLY OPERATING RHYTHM

| Day | Your Actions | Agents Running |
|---|---|---|
| Daily | Scan 35 min. Log candidates via Issue or dashboard. | Gap Sentinel posts verification links at 09:00 |
| Monday | Review Season Pulse issue. Check urgent labels. | Season Pulse posts weekly season briefing |
| Wednesday | Check Presell Sentinel nudges. Visit shops if needed. | Presell Sentinel checks stalled pre-sells |
| Saturday | Review pipeline. Check any stalled issues. | Presell Sentinel second weekly check |
| 1st of month | Read Pattern Brain intelligence brief. Update scan focus. | Pattern Brain posts monthly AI analysis |

**Your daily active time: 35–45 minutes.** Everything else runs automatically.

---

## GITHUB CLI (TABLET SHORTCUT — OPTIONAL)

For power users who want terminal access from a tablet browser:

GitHub Codespaces gives you a full Linux terminal inside your browser — no installation. Open your repo → green Code button → Codespaces → New codespace.

Then use GitHub CLI (`gh`) for rapid operations:
```bash
gh issue create --label candidate --title "Desk organizer" --body "..."
gh issue list --label candidate --state open
gh issue close 23 --comment "Market blocked - found on Noon"
gh workflow run gap-sentinel.yml
```

This is optional. The dashboard and browser-based GitHub UI cover everything the founder needs without any terminal.

---

*NBSV GitHub 2026 Power Layer — v1.0 — March 2026*
*This is not a 2024 code repository. It is a 2026 agentic operating system.*
