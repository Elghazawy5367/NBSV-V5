# NBSV Failure Log
## Every Rejected Candidate — Every Kill Signal
### The Most Valuable File in This Repository Over Time

---

## WHY THIS FILE MATTERS

After 20 entries: patterns start appearing.
After 50 entries: you recognize kill signals before running the filter.
After 100 entries: this file saves more time than any other tool in the system.

Feed this file to Claude periodically:
> "Here are my last [N] rejections and their kill signals. What product type should I stop scanning for entirely? What pattern is consistently failing? What should I look for more of?"

**Never delete entries. Every rejection is data.**

---

## HOW TO LOG AN ENTRY

One line per rejected candidate. Fill in every column.

Add new entries at the TOP of the log (most recent first).

---

## THE LOG

| Date | Source | Product Description | Kill Signal | Step Killed At | Notes |
|---|---|---|---|---|---|
| DD/MM/YYYY | [Platform] | [Brief description — 5 words max] | [Specific reason] | [1–5 or Pre-sell] | [Optional — any pattern noticed] |

---

## KILL SIGNAL REFERENCE
### Use these exact labels for consistency — patterns only emerge with consistent labels

**Filter Kill Signals (Step 2):**
- `ELECTRONICS` — contains any electronic component
- `INJECTION_MOLD` — requires injection molding
- `IMPORTED_COMPONENT` — core component must be imported
- `NO_AHA` — no AHA reaction in 3 seconds
- `NEEDS_EXPLANATION` — value requires description
- `INTELLECTUAL_AHA` — clever but not desired
- `ASSEMBLY_COMPLEX` — more than 6 precision steps
- `COGS_HIGH` — cannot reach COGS ceiling at batch 30
- `MARGIN_BROKEN` — cannot leave shop 40–60% margin at real WTP

**Market Kill Signals (Step 3):**
- `ON_JUMIA` — found on Jumia Egypt
- `ON_NOON` — found on Noon Egypt
- `ON_FACEBOOK` — found on Facebook Marketplace Egypt
- `ON_INSTAGRAM` — found on Instagram Egypt
- `IN_SHOPS` — found in physical Egyptian shops
- `ON_WHOLESALE` — found in Ataba/Mansheya/Victoria wholesale markets

**Cultural Kill Signals (Step 2):**
- `NO_EGYPTIAN_FIT` — cannot name a specific Egyptian behavior it serves
- `CHINESE_CONTEXT` — appeal depends on Chinese cultural context
- `CUTE_ONLY` — appeal is aesthetic/cute with no functional core
- `BEHAVIOR_CHANGE` — requires buyer to adopt a new behavior

**Timing Kill Signals:**
- `TOO_EARLY` — 1688 has fewer than 3 suppliers
- `WINDOW_CLOSED` — AliExpress English listings with reviews
- `SEASON_LATE` — less than 3 weeks to season

**Pre-Sell Kill Signals (Step 5):**
- `PRESELL_FAIL` — fewer than 2 shop owners committed
- `NO_SHOP_REACTION` — shop owners didn't pick it up or respond
- `FACEBOOK_SILENCE` — social validation post got no response

**Semi-DIY Kill Signals:**
- `FINISH_COMPLEX` — finish requires spray booth, kiln, or special equipment
- `FINISH_TIME` — finish exceeds 30 minutes per unit
- `FINISH_IMPORTS` — finish materials not available locally

---

## PATTERN ANALYSIS PROMPTS
### Run these in Claude after accumulating entries

**After 20 entries:**
```
Here is my NBSV failure log. What is the single most common 
kill signal? What category of product is failing most often?
```

**After 50 entries:**
```
Here is my NBSV failure log. What product type should I stop 
scanning for entirely based on consistent failure patterns? 
What source channel is producing the most kills at which step?
```

**After 100 entries:**
```
Here is my NBSV failure log. What positive pattern do you see 
in the products that survived to pre-sell? What should I be 
looking for more of based on what almost worked?
```

---

*NBSV Candidates — Failure Log — v1.0 — March 2026*
*Start logging from Day 1 of live operation.*
*Most recent entry at top. Never delete.*
