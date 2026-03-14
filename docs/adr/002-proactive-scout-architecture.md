# ADR 002 — Proactive Scout Architecture Over Reactive Processing

**Status:** Accepted
**Date:** March 2026
**Author:** NBSV System Analysis (Claude + Qwen synthesis)

---

## Context

NBSV v4.0 agent system was reactive: every agent waited for the founder to submit a candidate via Issue form. The architecture flow was:

```
You find product → You submit Issue → Agents process → You decide
```

This created a structural dependency: the system's output quality was bounded by the founder's scanning time and energy. On low-energy days, the pipeline went empty. On high-energy days, manual scanning produced raw candidates with no pre-filtering.

Two observable inefficiencies:
1. The founder spent 35 minutes per day scanning across channels — roughly 40% of that time was discovering things that would be instantly killed by the AI filter
2. The Step 3 market verification (5-platform check) consumed 4-6 minutes per candidate manually, regardless of how likely the market was to be clear

---

## Decision

Introduce three outward-facing Scout Agents that operate proactively on a schedule:

| Agent | Schedule | Source | Model |
|---|---|---|---|
| `scout-reddit.yml` | Every Wednesday 08:00 Egypt | r/somebodymakethis (Reddit JSON API) | GPT-4o-mini |
| `scout-rss.yml` | Daily 08:30 Egypt | Yanko Design + Core77 RSS feeds | GPT-4o-mini |
| `scout-kickstarter.yml` | Every Sunday 09:00 Egypt | Kickstarter search API | GPT-4o-mini |

Each Scout:
1. Fetches from its source using real public APIs (no auth required)
2. Deduplicates against already-scouted Issues (prevents repeat processing)
3. Runs GPT-4o-mini triage on all new items simultaneously
4. Creates GitHub Issues only for PASS and INVESTIGATE verdicts
5. Discards FAILs silently — no noise in the Issue tracker

The new architecture flow:
```
Agents scan external sources → Issues auto-created (pre-triaged) → Gap Sentinel pre-assesses → You decide
```

Additionally, Gap Sentinel v5.0 adds GPT-4o pre-assessment of Q1 market presence (reasoning-based, not scraping-based). This reduces manual verification to ~20-30% of candidates (UNCERTAIN verdicts only).

---

## Model Selection Rationale

**GPT-4o-mini** for scouts: scouts run high-volume, low-nuance triage (instant kill detection). Speed and cost efficiency matter more than reasoning depth. At 15 req/min free tier rate, scouts process 15 items in one batch comfortably.

**GPT-4o** for Gap Sentinel pre-assessment and Orchestrator filter: nuanced evaluation required. AHA quality, behavioral specificity, COGS reasoning all require deeper inference. GPT-4o is the correct model here.

**Mistral-large** for Brief Forge: manufacturing vocabulary and material sourcing context. Mistral's training distribution includes more European/industrial technical data, producing more precise workshop specs.

---

## Consequences

**Positive:**
- Founder's 35-minute scan session becomes a 10-minute decision session on a pre-filtered pile
- Pipeline runs even on zero-scan days (scouts run automatically)
- Instant kills are removed before the founder ever sees them
- Q1 verification time reduced ~70-80%

**Negative / Watch:**
- Scout agents can create false positives (INVESTIGATE verdicts that are clearly wrong to the founder on inspection). The founder's judgment is the final gate — scout labels are suggestions, not verdicts.
- Kickstarter API availability is not guaranteed (rate limits, schema changes). `scout-kickstarter.yml` has a manual fallback notice built in.
- Scout-created Issues require the founder to fill in the Egyptian Behavior Answer before the full Orchestrator filter runs. This is intentional: the behavior answer cannot be automated — it requires the founder's market knowledge.

---

## Implementation

- `scout-reddit.yml`, `scout-rss.yml`, `scout-kickstarter.yml` — new proactive agents
- `gap-sentinel.yml` v5.0 — upgraded with GPT-4o reasoning-based pre-assessment
- `bootstrap-labels.yml` v5.0 — new scout labels: `scout-reddit`, `scout-yanko`, `scout-core77`, `scout-kickstarter`, `needs-human-review`, `ai-likely-clear`, `ai-flagged-found`
- `orchestrator.yml` v5.0 — added routing for scout-created issue activation (triggers filter when founder fills behavior field)

---

*ADR 002 — NBSV v5.0 — Accepted*
