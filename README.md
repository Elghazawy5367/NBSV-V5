# NBSV Engine v5.0
## Never Before Seen Viral Products — Egyptian Micro-Manufacturing Fast-Follower
### Multi-Agent Autonomous Discovery · Zero Budget · Browser-Only · March 2026

---

```
Never Before Seen in Egypt
+ AHA in 3 seconds without explanation
+ Egyptian workshop producible from local materials
+ Real Egyptian WTP with no import price reference
= First-mover pricing power + zero capital at risk
```

---

## What Changed in v5.0

**v4.0 was reactive.** You submitted candidates. Agents processed them.

**v5.0 is proactive.** Agents discover candidates. You decide.

```
v4.0:  You scan → You submit → Agents process → You decide
v5.0:  Agents scan → Issues auto-created → You fill one field → You decide
```

Three new Scout Agents run autonomously on a schedule:

| Scout | Runs | Source | What it does |
|---|---|---|---|
| Scout Reddit | Every Wednesday 08:00 | r/somebodymakethis | Top weekly posts → pre-triaged Issues |
| Scout RSS | Daily 08:30 | Yanko Design + Core77 | Design concept articles → pre-triaged Issues |
| Scout Kickstarter | Every Sunday 09:00 | Kickstarter product design | Live campaigns → pre-triaged Issues |

Gap Sentinel now runs **AI pre-assessment** of Q1 market presence. ~70-80% of candidates get a preliminary LIKELY_CLEAR or LIKELY_FOUND verdict before you touch them.

Pattern Brain now generates a **config update PR** monthly — proposes updates to `egyptian-behaviors.json` based on what actually sold vs. what stalled.

---

## The 8-Agent System

| Agent | File | Schedule | What It Does | Model |
|---|---|---|---|---|
| **Scout Reddit** | `scout-reddit.yml` | Wed 08:00 | r/somebodymakethis → Issues | GPT-4o-mini |
| **Scout RSS** | `scout-rss.yml` | Daily 08:30 | Yanko + Core77 → Issues | GPT-4o-mini |
| **Scout Kickstarter** | `scout-kickstarter.yml` | Sun 09:00 | Kickstarter → Issues | GPT-4o-mini |
| **Orchestrator** | `orchestrator.yml` | On Issue event | Routes → 3-question filter | GPT-4o |
| **Gap Sentinel** | `gap-sentinel.yml` | Daily 09:00 | Q1 AI pre-assessment + links | GPT-4o |
| **Brief Forge** | `brief-forge.yml` | On label event | Workshop spec + WhatsApp script | Mistral-large |
| **Season Pulse** | `season-pulse.yml` | Every Monday | Season countdowns + urgency labels | — |
| **Presell Sentinel** | `presell-sentinel.yml` | Wed + Sat | Deposit tracking + nudges | — |
| **Pattern Brain** | `pattern-brain.yml` | 1st of month | Failure analysis + config update PR | GPT-4o |

**Total cost: zero.** GitHub Actions free tier: 2,000 min/month. All 8 agents use under 80 min/month.

---

## Quick Start (30 Minutes, Browser-Only)

### Step 1: Create the repo
1. Create a new GitHub repo: `nbsv-engine` (private recommended)
2. Upload all files from this zip using GitHub's drag-and-drop upload

### Step 2: Bootstrap labels
1. Go to **Actions** tab → **Bootstrap Labels** → **Run workflow**
2. All 40+ NBSV labels are created in ~30 seconds

### Step 3: Enable GitHub Models
The `models: read` permission in each workflow YAML is already set. GitHub Models uses your `$GITHUB_TOKEN` automatically — no setup needed.

### Step 4: Enable GitHub Projects V2 (optional but recommended)
1. Repo → **Projects** → **New project** → **Board**
2. Add columns: Scanned → Market Verified → Filter Pass → Brief Ready → Pre-Sell → Production → Closed Won
3. Settings → Workflows → enable automation rules per label

### Step 5: Run scouts immediately
1. **Actions** → **Scout Reddit** → **Run workflow**
2. **Actions** → **Scout RSS** → **Run workflow**
3. **Actions** → **Scout Kickstarter** → **Run workflow**
4. Check **Issues** tab — your first pre-triaged candidates should appear within 2-3 minutes

---

## Your Daily Workflow (v5.0)

```
Morning (10 min):
  1. Check Issues tab — review any new scout-created Issues
  2. For each Issue with 'needs-human-review': open the source link
  3. Fill in "Egyptian Behavior Answer" if the product has potential
  4. Orchestrator auto-runs full 3-question filter when you fill the behavior field

Gap Sentinel check (5 min, optional):
  5. Review any 'pending-verification' Issues with 'ai-likely-clear' label
  6. Quick verify those 2 platforms (Gap Sentinel says they're probably clean)
  7. Add 'principle-1-pass' to clean ones

Decisions (5 min):
  8. For 'principle-3-pass' Issues: Brief Forge auto-generated spec is in the comments
  9. Copy the WhatsApp brief → send to workshop
  10. Use pre-sell script → show video to 3 shop owners

Monday:
  Check Season Pulse issue for timing-sensitive candidates

1st of month:
  Read Pattern Brain intelligence brief
  Review config update PR if one was created → approve or close
```

**Your active daily time: 10-20 minutes. Everything else is autonomous.**

---

## Repo Structure

```
.github/
├── workflows/
│   ├── scout-reddit.yml          # NEW v5.0 — Proactive Reddit discovery
│   ├── scout-rss.yml             # NEW v5.0 — Proactive Yanko/Core77 discovery
│   ├── scout-kickstarter.yml     # NEW v5.0 — Proactive Kickstarter discovery
│   ├── orchestrator.yml          # UPGRADED v5.0 — Scout routing added
│   ├── gap-sentinel.yml          # UPGRADED v5.0 — AI pre-assessment added
│   ├── brief-forge.yml           # UPGRADED v5.0 — Mistral-large model
│   ├── pattern-brain.yml         # UPGRADED v5.0 — Config update PR added
│   ├── season-pulse.yml          # v4.0 (unchanged)
│   ├── presell-sentinel.yml      # v4.0 (unchanged)
│   ├── github-intelligence.yml   # v4.0 (unchanged)
│   └── bootstrap-labels.yml      # UPGRADED v5.0 — New labels added
├── ISSUE_TEMPLATE/               # v4.0 (unchanged — scouts create their own format)
├── config/
│   ├── egyptian-behaviors.json   # Self-updating via Pattern Brain PR
│   ├── material-greenlist.json
│   └── source-pipelines.json
KB/
├── NBSV_MASTER_KB_v4.md         # Authoritative reference
├── NBSV_PRODUCT_SOURCES_v1.md
└── CHANGELOG.md                  # NEW v5.0 — Semantic versioning history
docs/
└── adr/
    ├── 001-principle-based-filter.md
    ├── 002-proactive-scout-architecture.md
    └── 003-multi-model-routing.md
schema/
└── candidate.schema.json         # NEW v5.0 — JSON Schema for pipeline data
SOURCES/                          # Channel intelligence files
PROMPTS/                          # AI prompt templates
CANDIDATES/                       # Active/Passed/Failed pipeline records
SESSIONS/                         # Session logs
```

---

## The 11 Rules (Non-Negotiable)

1. Never produce until 2+ shop owners confirmed via deposit
2. Never explain the product — to anyone. If it needs explaining, it failed
3. Never use personal capital for unvalidated production
4. Never produce a product found anywhere in Egyptian market
5. Never miss QC: first 3 units via WhatsApp before approving full batch
6. Semi-DIY only: never start finishing until base structure is inspected
7. Never carry inventory beyond the product's natural selling window
8. Never tell the workshop what you're selling or where
9. Never treat "interesting" as "AHA" — completely different thresholds
10. Never let a product you love override the filter
11. Never validate demand using social media polls — only shop deposits count

---

## The Monthly Learning Loop

```
Cycle completes (closed-won label) 
  ↓
Pattern Brain runs (1st of month)
  ↓
Intelligence brief: what patterns emerged, what to scan more/less
  ↓
Config update PR: proposed additions to egyptian-behaviors.json
  ↓
You review + approve in one click
  ↓
Next month's scouts and filter use improved behavioral config
  ↓
System gets smarter from your actual sales data, not generic training data
```

After 8 cycles: your `egyptian-behaviors.json` is a proprietary Egyptian consumer behavioral model that nobody else has. It's built from what actually sold at shelf level in Cairo.

---

*NBSV Engine v5.0 — March 2026*
*Aligned with NBSV_MASTER_KB_v4.0*
*GitHub as agentic operating system — not just a code host*
