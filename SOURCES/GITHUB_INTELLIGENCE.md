# NBSV Source Intelligence — GitHub Exploitation
## Source Channel 5 — Technical Intelligence Layer
### No coding required. GitHub is a library. You are a reader.

---

## WHAT GITHUB IS FOR THIS SYSTEM

GitHub is not a code platform for NBSV purposes. It is a publicly accessible intelligence layer containing:

- **Awesome Lists** — community-curated directories of every scanning platform, tool, and resource in any domain
- **Product research repositories** — publicly shared market research, product gap analyses, trend data
- **Trend analysis outputs** — developers build scrapers, you read the results they publish
- **Design file repositories** — producible designs shared publicly, never manufactured commercially
- **Gists** — informal public lists of ideas, concepts, and unmet needs

**Access:** Every file in every public repository is readable in a browser. Navigate → click file → read. No account required for reading. No technical knowledge required.

---

## SECTION 1 — AWESOME LISTS

Awesome Lists are community-maintained directories of resources, organized by category. A single relevant Awesome List can surface 20–50 scanning sources you've never encountered.

### How to Search for Awesome Lists

Go to `github.com` and use the search bar:

```
awesome product design
awesome industrial design
awesome manufacturing
awesome crowdfunding
awesome laser cutting
awesome open source hardware
awesome design tools
awesome maker
```

### What to Look For in an Awesome List
- Sections titled: "Platforms" / "Resources" / "Communities" / "Tools"
- Any platform name you haven't heard of
- Any community or forum focused on product design, manufacturing, or unmet needs

### What to Do With What You Find
Every new platform in a relevant Awesome List is a potential new scanning source. Add the most relevant ones to the appropriate SOURCES/ file and add the platform to your rotation schedule.

---

## SECTION 2 — PRODUCT RESEARCH REPOSITORIES

Researchers, students, and product developers publish market research and product gap analyses as public GitHub repositories.

### Search Queries to Run

```
"product opportunity" "market research" stars:>10
"product gap" "physical product" stars:>20
"unmet needs" consumer product stars:>15
"product ideas" "home organization" stars:>10
"trending products" analysis 2024 stars:>20
"product design" "Egyptian market" stars:>5
```

### What These Repositories Contain
- Market size analyses with product gap identification
- Consumer research summaries (sometimes from MBA projects or consulting work)
- Product category trend analyses
- Lists of products people want that don't yet exist

The researcher had the analysis. You have the manufacturing and distribution path. That is the combination.

---

## SECTION 3 — TREND ANALYSIS OUTPUTS

Developers build tools that automatically track trending products on AliExpress, Amazon, Taobao, and other platforms. They publish the output data publicly.

### Search Queries

```
trending products scraper results
aliexpress trending products list
taobao trending analysis
amazon bestseller tracker
product trend data
```

### How to Use
- Navigate to the repository
- Look for data files: `.csv` `.json` `.md` files containing product lists
- Read the files directly in your browser — no code needed
- These outputs contain products you may not have seen yet on Douyin or 1688

---

## SECTION 4 — DESIGN FILE REPOSITORIES

Designers publish parametric design files for products they've designed but never manufactured commercially. These are ready-to-produce files — hand one to an Egyptian laser cutting workshop and they can produce it the same day.

### Search Queries

```
"laser cut" "design files" "organizer" stars:>30
"flat pack" "furniture" design files stars:>50
parametric furniture design SVG stars:>40
laser cut storage SVG DXF stars:>20
CNC furniture plans free stars:>30
"open source" "furniture" design files stars:>25
modular shelf design files stars:>20
```

### File Formats to Look For
- `.svg` — Scalable Vector Graphic — directly usable by laser cutting workshops
- `.dxf` — Drawing Exchange Format — standard for CNC and laser cutting
- `.ai` — Adobe Illustrator — most Egyptian laser workshops can open

### What 100+ Stars Means
A design file with 100+ GitHub stars has been validated as interesting by hundreds of other designers globally. That is a proxy for AHA potential — designers collectively stopped and said "this is good." Your job: check if it translates to Egyptian demand.

### Important Check Before Advancing
Search the design on AliExpress and Amazon to verify it hasn't been mass-manufactured. High-star design files sometimes get picked up by manufacturers. Verify the Egyptian market is clean before spending further time.

---

## SECTION 5 — GITHUB GISTS

Gists are short, informal public notes — lists someone made for themselves and shared publicly. More raw and genuinely original than polished repository content.

### Search at `gist.github.com`

```
product ideas
invention concepts
things that should exist
product gaps
products I wish existed
home organization ideas
```

### What to Look For
Lists of product ideas written informally by someone who had the idea but no path to execute it. The informal format often produces more original and honest need statements than polished platforms.

---

## SECTION 6 — GITHUB TOPICS TO FOLLOW

Navigate to `github.com/topics/[topic-name]` and click "Watch" to receive notifications when new repositories are published. This is a completely passive scan.

### Topics to Follow

```
github.com/topics/product-design
github.com/topics/industrial-design
github.com/topics/laser-cutting
github.com/topics/cnc
github.com/topics/flat-pack-furniture
github.com/topics/parametric-design
github.com/topics/open-source-hardware
github.com/topics/maker
```

Watching these topics means GitHub emails you when a new repository in your domain is published — no active scanning required.

---

## GITHUB SEARCH OPERATORS REFERENCE

These operators sharpen your searches on GitHub:

| Operator | What It Does | Example |
|---|---|---|
| `stars:>N` | Only repos with more than N stars | `stars:>50` |
| `language:markdown` | Only repos where main files are Markdown (lists, docs) | `"product ideas" language:markdown` |
| `pushed:>YYYY-MM-DD` | Only repos updated recently | `pushed:>2025-01-01` |
| `topic:X` | Only repos tagged with topic X | `topic:laser-cutting` |

**Combined example:**
```
"product design" "concept" language:markdown stars:>30 pushed:>2025-01-01
```
This finds recently updated, well-starred Markdown repositories about product design concepts.

---

## SECTION 7 — GITHUB AS YOUR OPERATING SYSTEM

Beyond using GitHub to find external intelligence, your own NBSV repository uses GitHub's built-in features as a zero-code, browser-based operating platform. No technical knowledge required.

### Issues — Your Live Candidate Pipeline

Every candidate that passes the initial AHA check becomes a GitHub Issue. Every rejection becomes a Failure Log Issue. This replaces static markdown files in `CANDIDATES/ACTIVE/` as the live pipeline.

**Why Issues beat static files:**
- Searchable by label, date, source channel, and kill signal
- Filterable — see all `source-asian-viral` candidates in one click
- Commentable — add Claude verdicts, shop reactions, QC results as comments
- Linkable — paste Issue URL into Claude for full context in one step
- Automatic audit trail — every change is timestamped

**The three Issue templates:**
- **🎯 Candidate Scan** — for every product that passes the 3-question filter
- **🗑️ Failure Log** — for every rejection (log the kill signal)
- **🏭 Workshop Brief** — production spec for pre-sell-confirmed candidates

**Daily workflow:**
```
Spot candidate → fill Candidate template → submit Issue
                                          ↓
                        Paste Issue URL + screenshot into Claude
                                          ↓
                      Claude returns PASS/FAIL/INVESTIGATE
                                          ↓
                        Update Issue labels → move on Projects board
```

### Projects Board — 7-Step Cycle Visualized

One Kanban board with columns aligned to the 7-step operational cycle:

```
🔍 SCANNED → ✅ FILTER-PASS → 📞 PRE-SELL → 🏭 PRODUCTION → 🚚 DISTRIBUTED → 📊 CLOSED-WON
                                                                              → 🗑️ CLOSED-LOST
```

Every candidate Issue lives on this board. Drag cards between columns as the product moves. The board shows you at a glance: what's active, what's stalled, and what closed.

**Setup:** Repo → Projects → New Project → Board → create columns above. (3 minutes, no code.)

### Labels — Your Failure Pattern Engine

Every Issue carries labels that become searchable over time. After 20+ rejected Issues with labels like `fail-electronics` and `on-jumia`, you can filter by label and instantly see your most common kill signals.

**The failure label taxonomy** (full list in `docs/daily-workflow.md`):
- Kill signal labels: `fail-electronics`, `fail-no-aha`, `on-jumia`, `fail-no-egyptian-fit`...
- Source labels: `source-asian-viral`, `source-concept-mine`, `source-ai-ideation`...
- Status labels: `principle-1-pass`, `pre-sell-confirmed`, `in-production`...
- Context labels: `season-amplified`, `urgent`, `continuous-demand`...

**Monthly pattern check:** Filter Issues by `rejected` → sort by most common label → feed to Claude:
> "Here are my last 30 rejections and their labels. What kill signal appears most? What should I stop scanning for?"

### Wiki — Long-Term Pattern Recognition

GitHub Wiki (repo → Wiki tab) is version-controlled documentation for patterns that accumulate over time.

**What to track in Wiki:**
- **Failure Pattern Catalog** — after 2–3 cycles, document what kill signals cluster together. "Egyptian market has caught up with Chinese [category] — no longer viable for NBSV."
- **Cultural Fit Heuristics Library** — Egyptian behaviors that produced AHA vs. behaviors that didn't. Compounds with every cycle.
- **Workshop Notes** — general patterns across workshops (no names — area + capability only).
- **Seasonal Retrospectives** — "Ramadan 2026: what amplified demand, what didn't, what arrived too late."

Wiki entries are permanent institutional memory that makes every future cycle faster.

---

```
nbsv/
│
├── README.md                     ← System description + index
│
├── SOURCES/
│   ├── CHINESE_PLATFORMS.md      ← This document's equivalent
│   ├── KOREAN_PLATFORMS.md
│   ├── CONCEPT_MINES.md
│   ├── CONCEPT_LIBRARIES.md
│   ├── AI_IDEATION.md
│   └── GITHUB_INTELLIGENCE.md   ← This file
│
├── PROMPTS/
│   ├── MASTER_IDEATION_PROMPT.md
│   ├── DAILY_SCAN_SUBMISSION.md
│   ├── FILTER_QUICKCHECK.md
│   └── PRESELL_SCRIPT.md
│
├── KB/
│   ├── NBSV_MASTER_KB_v3.md     ← Authoritative. Read only.
│   ├── NBSV_PRODUCT_SOURCES_v1.md
│   └── CHANGELOG.md
│
├── CANDIDATES/
│   ├── ACTIVE/
│   ├── PASSED/
│   └── FAILED/
│       └── FAILURE_LOG.md       ← Most valuable file over time
│
├── INTELLIGENCE/
│   ├── WORKSHOP_ROSTER.md
│   ├── SHOP_NETWORK.md
│   └── MARKET_VERIFICATION_LOG.md
│
└── SESSIONS/
    └── SESSION_LOG.md
```

### The Four Functions of Your Repo

**Source Memory** — `SOURCES/` folder contains every platform, hashtag, search term, and signal indicator. Open the right file before any session. Nothing held in your head.

**Pattern Recognition Engine** — `CANDIDATES/FAILED/FAILURE_LOG.md` accumulates every rejection. After 20 entries it shows patterns. After 50 it becomes the fastest filter you have. Feed it to Claude periodically.

**Intelligence Protection** — `INTELLIGENCE/` files are private. The workshop knows their part. The shop knows their part. Only you see the full map.

**Prompt Library** — `PROMPTS/` contains every prompt and script you use repeatedly. Evolves with every session. Compounds in value exactly like the scanning skill.

### Repository Privacy Setting
Set the repository to **Private** on GitHub. All the intelligence in `INTELLIGENCE/` (workshop names, shop contacts, zone exclusivity agreements) must remain private. `SOURCES/`, `PROMPTS/`, and `KB/` files could be public — but keeping the entire repo private is simpler and protects everything.

---

## GITHUB SCAN SESSION GUIDE

**Time required:** 15–20 minutes per session

**Recommended frequency:** Once every 2 weeks is sufficient — GitHub doesn't change daily

**Session flow:**
1. Run 2–3 of the design file search queries (5 min)
2. Browse the latest repos in your followed topics (5 min)
3. Run 1 product research search query (5 min)
4. Check if any Awesome List you bookmarked has been updated (5 min)

**What to record:**
- Any new platform found → add to appropriate SOURCES/ file
- Any design file that passes initial check → add to CANDIDATES/ACTIVE/
- Any research repository with useful product gap data → link in SESSION_LOG.md

---

*NBSV Sources — GitHub Intelligence — v1.0 — March 2026*
