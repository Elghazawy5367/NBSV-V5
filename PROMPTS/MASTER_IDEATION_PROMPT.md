# NBSV Master Ideation Prompt
## Copy-Paste This Entire Block at the Start of Every AI Ideation Session
### Works with: Claude, Qwen, ChatGPT, Gemini — any capable AI

---

## HOW TO USE THIS FILE

1. Fill in the `[BUYER]` and `[PAIN]` sections below before copying
2. Replace `[N]` with the number of concepts you want (recommend 5)
3. Copy the entire block from the `---START---` line to the `---END---` line
4. Paste into your AI session
5. After receiving concepts — run the 3-question filter from `FILTER_QUICKCHECK.md` on each

---

## BUYER DESCRIPTION BANK
### Use these as starting points — customize to be more specific

**Small Space Storage Buyer:**
> Cairo mother of 2–3 children in a 65–80sqm apartment in [Nasr City / Heliopolis / Maadi] managing school bags, sports equipment, cleaning supplies, and daily household items with no dedicated storage room

**Car Organizer Buyer:**
> Cairo male professional aged 28–45 spending 2–3 hours daily in his car, managing phone charger cables, sunglasses, car registration papers, tissues, water bottles, and receipts creating visible dashboard and back-seat chaos

**Gift Packaging Buyer:**
> Egyptian woman aged 25–45 who gives gifts 15–20 times per year for Eid visits, weddings, births, Ramadan visits, and graduations, currently using whatever plastic bags and cardboard boxes are available

**Children's Education Buyer:**
> Egyptian parent of a child aged 7–14 where education is the household's top spending priority, managing textbooks, notebooks, colored pencils, ruler sets, and activity materials for 3+ subjects spread across a small shared bedroom

**Desk Organization Buyer:**
> Egyptian university student aged 18–24 studying at home on a small desk that also holds a phone, charger, water bottle, snacks, and personal items alongside study materials

---

## THE MASTER PROMPT

---START---

I am a solo Egyptian founder running a physical product business.
I need product concepts that can be locally manufactured and sold 
in Egypt with zero personal capital at risk.

Generate [N] product concepts for:

BUYER: [Paste your specific buyer description here]

PAIN: [Describe a specific daily frustration this person 
experiences — be as concrete and behavioral as possible]

EVERY concept must satisfy ALL of the following constraints 
with absolutely zero exceptions:

─── PRODUCTION CONSTRAINTS ────────────────────────────────────
Made ONLY from these materials (Egyptian workshop sources):
• MDF / plywood / solid wood
• Acrylic / perspex sheet
• Aluminum sheet (locally produced in Egypt)
• Standard fabric / textile / canvas
• Foam / sponge / EVA sheet
• Standard hardware (screws, hinges, brackets, tubes, knobs)
• Heat press / screen print on standard blanks
• Basic resin or epoxy poured elements
• Finish materials: sandpaper, wood stain, felt, paint, ribbon

ZERO electronics of any kind
(no LED, no battery, no USB, no sensor, no motor — nothing powered)
ZERO injection molding
ZERO imported core components
Maximum 6 assembly steps
Producible by a small Egyptian workshop with basic tools in 1–2 days

─── ECONOMICS CONSTRAINTS ─────────────────────────────────────
COGS under 80 EGP at batch 30 (standard workshop path)
OR under 120 EGP if a home finish layer (sanding, staining,
felt lining, painting, hardware addition) adds 30%+ perceived
value and takes 20 minutes or less per unit to apply

─── AHA CONSTRAINTS ────────────────────────────────────────────
A stranger must stop and pick this up within 3 seconds
of seeing it sitting on a shop counter with zero signage
Zero explanation needed — the value is instantly visible
AHA must be emotional and visual:
"I need this" / "I want one" / "I know who to give this to"
NOT intellectual: "that's clever" without wanting it is insufficient
The product must self-sell on a shelf — no demo, no description

─── MARKET CONSTRAINTS ─────────────────────────────────────────
Must NOT exist anywhere in Egypt currently:
not on Jumia, not on Noon, not on Facebook Marketplace,
not on Instagram Egypt, not in any physical shop

─── EGYPTIAN FIT CONSTRAINT ────────────────────────────────────
Must replace or enhance a SPECIFIC Egyptian daily behavior
Not globally generic — must connect to Egyptian reality:
• Cairo apartment sizes (average 60–90 sqm)
• Cairo traffic (2–4 hours daily for many residents)
• Egyptian gifting culture (mandatory gifts for weddings, 
  Eid, births, visits — 15–25 gifting occasions per year)
• Egyptian hosting culture (receiving guests is a regular 
  obligation with strong presentation expectations)
• Egyptian investment in children's education 
  (top household spending priority)

─── OUTPUT FORMAT ──────────────────────────────────────────────
For EACH concept output EXACTLY this structure — no variations:

**Product Name:** (3 words maximum)

**What it is:** (One sentence only — no jargon, no technical terms)

**How it is made:** (One sentence — as you would say it to a 
workshop owner who has never seen or heard of this product)

**The AHA moment:** (Describe what a stranger sees and feels 
in the first 3 seconds of encountering this product)

**Specific Egyptian behavior it replaces or enhances:**
(Name the exact daily behavior — not a category, a behavior)

**Materials:** (List every material — Egyptian local sources only)

**COGS estimate at batch 30:** (in EGP)

**Production path:** Standard Workshop Model / Semi-DIY Finish Model
(Semi-DIY = workshop makes the base structure, founder adds finish 
layer at home: sanding + staining + felt + hardware in ≤20 min/unit)

**Why no Egyptian has seen this before:**
(Explain specifically — not "it's new" but why it hasn't arrived yet)

─── SELF-FILTER INSTRUCTION ────────────────────────────────────
Before outputting any concept, check it against every constraint.
If it fails any single constraint — discard it silently and 
generate a replacement concept.
Only output concepts that pass every constraint completely.
Do not mention discarded concepts — just output the passing ones.
Do not apologize for meeting the constraints — just meet them.

---END---

---

## AFTER THE SESSION

For every concept received — run this immediately:

**3-Question Filter** (from `FILTER_QUICKCHECK.md`):

1. Has anyone in Egypt seen this before? → Verify: Jumia, Noon, Facebook, Instagram
2. Does the AHA happen in 3 seconds without a word being said?
3. Can I make this in Egypt, from Egyptian materials, at a price that leaves real margin?

**For any concept surviving all 3:**
→ Create a file in `CANDIDATES/ACTIVE/`
→ Use `TEMPLATE_CANDIDATE.md` as the structure

**For every rejected concept:**
→ Add one line to `CANDIDATES/FAILED/FAILURE_LOG.md`
→ Record: Date | Concept name | Kill signal | Which constraint it failed

---

*NBSV Prompts — Master Ideation Prompt — v1.0 — March 2026*
