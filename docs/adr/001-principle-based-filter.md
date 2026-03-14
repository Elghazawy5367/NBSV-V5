# ADR 001 — Principle-Based Filter Over Category Gates

**Status:** Accepted
**Date:** March 2026
**Author:** Pattern Brain (based on v3.0→v4.0 transition)

---

## Context

NBSV v3.0 used a 6-category hard gate: candidates were only evaluated if they fell into one of six pre-defined product categories (Small Space Storage, Gifting Systems, Car Organizers, Desk/Study, Children's Educational, Ramadan/Eid Hosting).

The 6-category gate created two observable problems:

1. **False negatives**: Products outside the 6 categories that would pass all three principles were rejected before evaluation. The category was acting as a filter but it was not a proxy for the actual business criteria.

2. **Seasonal hard gate**: Seasons were treated as mandatory filters, blocking evaluation of a Christmas product in July even if Egyptian market was clean and production was feasible.

Founder feedback: *"The only clear rule is Never Before Seen + AHA + Workshop Feasible + Egyptian WTP."*

---

## Decision

Replace the 6-category hard gate with a 3-question principle-based filter:

1. **Never Before Seen in Egypt** — 5-platform verification (Jumia, Noon, Facebook Marketplace, Instagram, Google Lens)
2. **AHA in 3 seconds without explanation** — Stranger picks it up unprompted from shelf. Two of four involuntary reactions must be present.
3. **Egyptian workshop producible from local materials at target margin** — Green-list materials only, zero electronics, ≤6 steps, COGS ≤80/120 EGP.

The 6 scanning zones are retained as **orientation tools** (high-yield search headings) — not as mandatory criteria. A product outside all 6 zones that passes the 3-question filter advances. Always.

Seasons are repositioned as **demand amplifiers**, not gates. Continuous demand products (gifting, car, desk, storage, education) sell year-round. Season-amplified products use the timing window check only.

---

## Consequences

**Positive:**
- Increased candidate diversity without reducing filter rigor
- Reduced false negatives from over-constrained scanning
- Filter is now grounded in business logic, not product taxonomy

**Negative / Watch:**
- Requires stronger Egyptian behavior mapping in Q2 — without the category gate, the behavior answer becomes the primary cultural relevance check
- Agent prompts must explicitly emphasize the behavior question quality as a proxy for what the category gate was doing

---

## Implementation

- Filter logic updated in `orchestrator.yml` (Orchestrator AI prompt)
- Scanning zones documented in `KB/NBSV_MASTER_KB_v4.md` Part 6 as "High-Yield Zones"
- `egyptian-behaviors.json` expanded with behavior examples per zone (not gates — examples)

---

*ADR 001 — NBSV v4.0 — Accepted*
