# 34 Plaza Owners Corp. — Treasurer's Working Repo

Financial work for **34 Plaza Owners Corp.**, a residential co-op (111 residential units, 9 professional units, 52,803 shares). I keep the treasurer's analysis, source data, and shareholder-facing materials here so each year's numbers are reproducible and the decisions behind them are written down.

## How I use Claude as treasurer

I treat Claude as an analyst and drafting partner — I bring the raw co-op documents, Claude helps me turn them into a defensible story for the board and shareholders. The workflow:

1. **Ingest the source documents.** I drop in the audited financial statements, the approved operating budget, and the capital plan workbook. Claude reads them and pulls the numbers that matter (P&L, reserve roll-forward, maintenance history, mortgage terms, compliance obligations).
2. **Reconcile and cross-check.** Claude cross-references figures across documents — e.g. confirming the capital plan total against the budget, or tying the reserve closing balance to the audit schedule — and flags anything that doesn't foot.
3. **Model scenarios.** For board decisions (like targeted sidewalk tile repair vs. full replacement), Claude builds the reserve trajectory under each scenario so I can show the funding impact through the plan horizon, not just the first-year cost.
4. **Draft the shareholder materials.** Claude turns the analysis into the annual-meeting outline and the financial-update deck + linked source workbook, written for a non-financial audience.
5. **Keep the reasoning on the record.** The outline and READMEs capture *why* each call was made (e.g. why 5.5% maintenance is in line with the long-run norm, why the targeted repair is a deliberate board call and not a deferral), so next year's treasurer — or a skeptical shareholder — can follow the logic.

What I do **not** outsource: every number is sourced back to an audited or board-approved document, and I review the deck before it's presented. Claude accelerates the analysis and drafting; the fiduciary judgment stays with me and the board.

## What's in this repo

| Path | What it is |
|---|---|
| [2026_financial_presentation/](2026_financial_presentation/) | The 2026 Annual Meeting financial update — deck, source-data workbook, narrative outline, and capital plan. See its own [README](2026_financial_presentation/README.md) for the build/handoff details. |

### `2026_financial_presentation/`

- **`Financial Update - Outline & Plan.md`** — the treasurer's slide-by-slide plan and the single consolidated table of key numbers. This is the narrative spine of the presentation.
- **`Financial Update - Source Data.xlsx`** — every figure behind every chart, one tab per slide. Blue cells are inputs; edit those to update the deck.
- **`34_Plaza_Capital_Plan_-_Updated_March_2026.xlsx`** — project-level capital plan (the Targeted Tile Repair scenario is the one in use).
- **`capital plan 2026+.gsheet`** — Google Sheets pointer to the live capital plan.
- **`README.md`** — how to convert the deck/workbook to Google Slides + Sheets and keep the charts linked.

## Conventions

- **Source of truth:** audited financials and the board-approved budget. Anything presented to shareholders traces back to one of those.
- **Scenario discipline:** when a decision has alternatives, both are kept in the workbook so the trade-off is visible, not just the chosen path.
- **By year:** each annual cycle gets its own top-level folder (`YYYY_financial_presentation`) so prior years stay frozen as presented.

---

*Maintained by the treasurer of 34 Plaza Owners Corp. Internal working repo — figures here are working analysis, not an official statement of the corporation.*
