# ADR 003 — Multi-Model Routing: Right Model Per Task Type

**Status:** Accepted
**Date:** March 2026
**Author:** NBSV System Analysis

---

## Context

NBSV v4.0 used GPT-4o for all GitHub Models API calls across all agents. This was a sensible default for initial build — GPT-4o is capable and the system was proving the architecture. However, as of March 2026 the GitHub Models marketplace offers 6+ free models with meaningfully different capabilities per task type.

Using the same model for everything ignores real differences in:
- **Speed vs. depth tradeoff**: high-volume triage tasks don't need deep reasoning
- **Domain-specific vocabulary**: manufacturing specs benefit from models with stronger industrial training data
- **Rate limit management**: cheaper/faster models on high-volume tasks leave GPT-4o capacity for tasks that need it

---

## Decision

Assign the correct GitHub Models free tier model to each task type:

| Agent | Task Type | Model | Rationale |
|---|---|---|---|
| `scout-reddit.yml` | Initial triage (high volume, binary) | `gpt-4o-mini` | Instant kill detection doesn't need deep reasoning. Fast, cheap, handles 15-item batches. |
| `scout-rss.yml` | Initial triage (high volume, binary) | `gpt-4o-mini` | Same as above. |
| `scout-kickstarter.yml` | Initial triage (high volume, binary) | `gpt-4o-mini` | Same as above. |
| `gap-sentinel.yml` | Q1 market presence reasoning | `gpt-4o` | Nuanced reasoning about Egyptian market state. Wrong here = false CLEAR or false FOUND. |
| `orchestrator.yml` | Full 3-question filter | `gpt-4o` | AHA evaluation, behavior answer quality assessment, COGS reasoning. All require depth. |
| `brief-forge.yml` | Workshop production spec | `Mistral-large` | Manufacturing vocabulary. Workshop steps, material specs, cost estimates. Mistral's industrial training distribution produces cleaner specs. Fallback to `gpt-4o` if unavailable. |
| `pattern-brain.yml` | Monthly synthesis + config update | `gpt-4o` | Pattern recognition across many data points + careful config proposal. Depth needed. |

---

## Implementation Notes

Model strings for GitHub Models API (`models.inference.ai.azure.com`):
- `gpt-4o` — available, standard quota
- `gpt-4o-mini` — available, faster/cheaper
- `Mistral-large` — available, strong at structured generation

Rate limits (free tier): 15 req/min, 150 req/day per model.
NBSV's total daily AI calls (estimated): ~20-30 req/day across all agents. Well within limits.

All agents have fallback logic: if primary model returns non-200, fall back to `gpt-4o`. If `gpt-4o` also fails, fall back to human-readable notice with manual action instructions.

---

## Consequences

**Positive:**
- Meaningful improvement in Brief Forge output quality (Mistral-large workshop specs are more precise)
- Scout agents process faster with GPT-4o-mini (lower latency per item)
- GPT-4o quota preserved for high-stakes filter evaluations

**Negative / Watch:**
- `Mistral-large` model string may change as GitHub Models evolves. Monitor GitHub Models marketplace (`github.com/marketplace/models`) for current model IDs.
- If GitHub adds Claude models to GitHub Models marketplace (possible in 2026), update Brief Forge and Pattern Brain to use Claude for those tasks.

---

*ADR 003 — NBSV v5.0 — Accepted*
