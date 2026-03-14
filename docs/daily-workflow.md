# NBSV Daily Workflow
## Browser-Only. Tablet-Optimized. No Technical Knowledge Required.
### Everything runs in a browser tab. Nothing to install.

---

## Before You Start Any Session

Open two browser tabs:
1. **Your scan platform** (Douyin / Kickstarter / Yanko / etc.)
2. **Your GitHub repo** (`github.com/[your-username]/nbsv-engine`)

That's all you need.

---

## Session Type A — Scanning Session (35 Minutes)

### Minutes 0–25: Scan

Open the right SOURCES/ file for today's platform before starting:
- `SOURCES/CHINESE_PLATFORMS.md` → for Douyin or Xiaohongshu
- `SOURCES/KOREAN_PLATFORMS.md` → for Naver or Korean Instagram
- `SOURCES/CONCEPT_MINES.md` → for Kickstarter or Makuake
- `SOURCES/CONCEPT_LIBRARIES.md` → for Yanko, Core77, Behance, r/somebodymakethis
- `SOURCES/AI_IDEATION.md` → for a Claude or Qwen ideation session
- `SOURCES/GITHUB_INTELLIGENCE.md` → for GitHub design files or research repos

Follow the session guide in the file. Screenshot anything that stops your scroll.

**Target: 0–1 candidates per session. Zero is correct most days.**

---

### Minutes 25–35: Filter

For each screenshot you captured, run the 3-question filter from memory (or open `PROMPTS/FILTER_QUICKCHECK.md`):

**Question 1:** Is the Egyptian market clean?
- Search Jumia Egypt, Noon Egypt, Facebook Marketplace Egypt, Instagram Egypt, Google Lens
- All clean → continue. Found anywhere → stop.

**Question 2:** Does the AHA happen in 3 seconds without a word?
- YES → continue. UNSURE → stop.

**Question 3:** Can I make this in Egypt at real margin?
- One sentence to workshop owner. Green-list materials only. COGS under 80/120 EGP.
- All pass → advance. Any NO → stop.

---

### If a Candidate Passes All 3 Questions:

1. Go to GitHub repo → Issues tab → **New Issue**
2. Select: **🎯 NBSV Candidate — New Product**
3. Fill in the template (most fields you've already checked)
4. Attach your screenshot (drag and drop into the Issue)
5. Submit the Issue
6. Copy the Issue URL
7. Open Claude Project → paste the URL + describe what you saw
8. Claude returns: PASS / FAIL / INVESTIGATE + next action
9. Go back to the Issue → update the labels based on verdict

---

### If a Candidate Fails Any Question:

1. Go to GitHub repo → Issues → **New Issue**
2. Select: **🗑️ NBSV Failure Log — Rejected Candidate**
3. Fill in: description + kill signal + why it seemed promising
4. Apply the correct label (e.g., `fail-electronics`, `on-jumia`)
5. Submit and move on

**Never skip the failure log.** After 20 entries it starts paying back.

---

### Session End — Log One Line

Open `SESSIONS/SESSION_LOG.md` → add one line:

```
[DATE] | [SOURCE] | [PRODUCT — 5 words] | [VERDICT] | [KILL SIGNAL or NEXT STEP]
```

Close both tabs. Done.

---

## Session Type B — Pre-Sell Session (Field Visit)

Before leaving the house:
1. Open the candidate's GitHub Issue on your tablet
2. Confirm the video is saved locally and playable without internet
3. Open `PROMPTS/PRESELL_SCRIPT.md` — read the exact words once

At each shop:
1. Enter. Place product/tablet on counter. Show the video. Say nothing.
2. Script: *"This has [X] million views. Nobody in Egypt has it yet. I can make it locally. Do you want to be the first shop in [area] to carry it?"*
3. Record the response in the GitHub Issue as a comment.

After 2 shops confirm + pay deposit:
1. Go back to the Issue → add label `pre-sell-confirmed`
2. Projects board → move card to **PRE-SELL** column
3. Open GitHub Issues → New Issue → **🏭 Workshop Brief**
4. Fill in the production spec
5. Copy the WhatsApp message from the brief → send to workshop

---

## Session Type C — Production Monitoring

While waiting for the workshop batch:

**Day of order:**
- Move the Issue card to **PRODUCTION** column in Projects board
- Note the deadline in the Issue as a comment

**When workshop sends first 3 unit photos:**
- Inspect via WhatsApp: clean cuts, correct dimensions, smooth edges
- If approved: reply to workshop → proceed full batch → comment on Issue "QC APPROVED"
- If rejected: describe issue to workshop → get corrected units → add comment to Issue

**If Semi-DIY path:**
- Do NOT start finishing until QC is approved
- Log finishing start in Issue: "Finishing started — batch of [N]"
- Note actual finish time per unit

---

## Session Type D — Distribution Day

Day of delivery:

1. Update Issue card → move to **DISTRIBUTED** column
2. Deliver to each shop
3. At each counter: place product. Say nothing. Watch.
4. Record shop owner's reaction as Issue comment
5. Post reveal video on TikTok/Facebook same day
6. Note post URLs in Issue

**7 days later:**
- Check sell-through with each shop
- Record in Issue: units sold / units remaining
- Decide: reorder OR close the cycle

**Closing the cycle:**
- Move Issue card to **CLOSED-WON**
- Fill in the outcome section of the Issue
- Create a `CANDIDATES/PASSED/` file using `TEMPLATE_RESULT.md`
- Note real learnings — one paragraph, honest

---

## GitHub Projects Board — Your Visual Pipeline

Set up once in GitHub (no code — browser only):

**Column structure:**
```
🔍 SCANNED
→ ✅ FILTER-PASS
→ 📞 PRE-SELL
→ 🏭 PRODUCTION
   ↳ [Standard] or [Semi-DIY]
→ 🚚 DISTRIBUTED
→ 📊 CLOSED-WON
→ 🗑️ CLOSED-LOST
```

Every candidate Issue lives on this board. Labels move it between columns.

**Setup steps (3 minutes, browser only):**
1. Go to your repo → Projects tab → New Project
2. Select: Board view
3. Create the columns above
4. For each new Issue: drag it to the correct column

---

## Label System — Your Failure Pattern Engine

Apply these labels to every Issue as it moves through the system:

**Status labels:**
- `candidate` — newly submitted
- `principle-1-pass` — Egyptian market verified clean
- `principle-2-pass` — AHA confirmed
- `principle-3-pass` — producible at margin
- `pre-sell-confirmed` — 2+ shop deposits collected
- `in-production` — workshop order placed
- `distributed` — delivered to shops
- `closed-won` — completed cycle
- `rejected` — failed at any stage

**Source labels:**
- `source-asian-viral`
- `source-concept-mine`
- `source-concept-library`
- `source-ai-ideation`
- `source-github-intel`

**Production labels:**
- `standard-path`
- `semi-diy`

**Context labels:**
- `season-amplified` — demand spikes at specific season
- `urgent` — timing window closing within 3 weeks
- `continuous-demand` — year-round Egyptian behavior

**Failure labels (apply to rejected Issues):**
- `fail-electronics`
- `fail-injection-mold`
- `fail-imported-component`
- `fail-no-aha`
- `fail-needs-explanation`
- `fail-intellectual-aha`
- `fail-assembly-complex`
- `fail-cogs-high`
- `on-jumia`
- `on-noon`
- `on-facebook`
- `on-instagram`
- `in-shops`
- `fail-no-egyptian-fit`
- `fail-chinese-context`
- `presell-fail`

**After 20 rejected Issues:** Go to Issues → filter by `fail-electronics` → see how many times this appeared. That's your most common kill signal. Scan less of that source type or apply that filter earlier.

**Feed to Claude monthly:**
> "Here are my last [N] rejected Issues and their labels. What kill signal appears most often? What should I stop scanning for? What passed that I should look for more of?"

---

## GitHub Pages — Your Free HTML Tracker (Phase 2)

When the HTML Tracker is built:
1. Repo Settings → Pages → Source: Deploy from branch → `main` → `/tracker`
2. Your tracker is live at: `https://[username].github.io/nbsv-engine`
3. Bookmark this on your tablet — accessible offline after first load

No hosting cost. No third-party service. Zero technical setup beyond the 3 settings clicks.

---

## Weekly Review (Friday — 15 Minutes)

1. Open Issues → filter by `candidate` → review what moved and what stalled
2. Check Projects board — any card stuck in one column for more than 5 days?
3. Look at failure labels — any signal appearing 3+ times this week?
4. Update `SESSIONS/SESSION_LOG.md` with weekly summary row
5. If any season is within 8 weeks — check if any candidate in pipeline is season-amplified and move it to `urgent`

---

*NBSV Docs — Daily Workflow — v1.0 — March 2026*
*Browser-only. Tablet-optimized. No terminal. No code. No paid tools.*
