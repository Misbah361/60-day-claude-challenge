# Day 16 — Custom Skill: Stock Fundamental Research

## Task
Build a Custom Skill in Claude that analyzes Indian listed stocks using fundamentals only, test it on a real stock, and observe how the skill can be reused across prompts without re-entering instructions.

## Skill Setup
- **Skill name:** `stock-fundamental-research`
- **Description:** Analyzes Indian and global listed companies using fundamentals, financial statements, business quality, competitive advantages, valuation, risks, and growth prospects. Generates evidence-based research reports and investor-friendly summaries. Never provides direct buy/sell/hold recommendations.
- **Key rules encoded in the skill:**
  - Live data first, sourced with priority: Screener > Tickertape > Moneycontrol > NSE > BSE > Annual Reports > Earnings Calls
  - Never fabricate data — flag 🚩 when unavailable or unverifiable
  - Cite a source beside every key figure
  - Never give buy/sell/hold calls or price targets
  - No predictions — only illustrative historical trend continuation
  - Multiple output modes: Quick Take, Deep Dive, Compare, Pros & Cons, Portfolio Fit

## Test 1 — Deep Dive: HDFC Bank
Ran a full Deep Dive on **HDFC Bank Ltd (NSE: HDFCBANK)**, rendered as an interactive tabbed HTML report (Snapshot / Valuation / Growth / Health / Returns / Peers / Ownership / View).

**Key findings:**
- CMP ₹720, Market Cap ₹11,10,063 Cr, P/E 14.0x — fair to mildly cheap vs. own 10-year history
- ROE has structurally declined from 20% (FY15) to 14% (FY26) — now below ICICI Bank and SBI
- FII holding fell from ~52% (Sep 2023) to ~42% (Jun 2026) while DII holding rose from ~30% to ~42% over the same period
- CEO Sashidhar Jagdishan announced retirement effective October 2026 — a near-term governance/transition watch-point
- Strong recent cash generation: CFO/Operating Profit ratio hit 94–98% in FY25–FY26

**Screenshot:** `screenshots/hdfc_bank_deep_dive.png`

## Test 2 — Quick Take: TCS (Reusability Test)
To test Step 14 — reusing the skill without re-entering the prompt — I simply asked for a different stock ("TCS") in the same conversation, with no re-statement of the skill's rules or output format.

**Result:** The skill auto-applied identically — same sourcing discipline, same 🚩 data-flagging behavior, same "no recommendation" disclaimer — to a completely different company and sector (IT services vs. banking), confirming the skill persists as reusable context rather than a one-off instruction.

**Key findings:**
- CMP ₹2,342, Market Cap ₹8,47,356 Cr, P/E 15.8x, ROE 51.8%, ROCE 63.0%
- Screener directly flagged poor 5-year sales growth (10.2%) — a real growth deceleration signal
- Strong capital efficiency but margin pressure from AI investment and reduced variable pay

**Screenshot:** `screenshots/tcs_quick_take.png`

## Key Learnings
1. **Skills persist across prompts** — once loaded, a skill applies its full rule set (sourcing priority, output format, safety constraints) to any relevant new request in the session, without re-explaining the methodology each time. This is a big efficiency gain for repeated workflows like stock research.
2. **Guardrails matter more than raw output** — the most valuable behavior wasn't the numbers themselves, but the skill's discipline in flagging 🚩 conflicting or unverifiable data (e.g., peer P/E and peer ROE figures) instead of confidently picking one number. That's the difference between a research tool and a hallucination risk.
3. **Domain-specific interpretation rules are essential** — the skill correctly treated bank-specific metrics (low interest coverage, large contingent liabilities, ROCE) differently from how it would for a non-financial company like TCS, since deposits/leverage are structural to banking rather than red flags.
4. **A skill is not a one-time template — it's reusable infrastructure.** This is the core insight the whole 60-day challenge keeps reinforcing: build the capability once, reuse it indefinitely.

## Disclaimer
All outputs above are educational fundamentals-based views only — not investment advice, not buy/sell/hold recommendations. Figures verified against Screener.in where possible; a few peer-comparison figures came from secondary sources and are flagged for independent verification.

---
*Part of the [60 Days of AI Challenge](https://www.abtalks.in) — Day 16*
