# CLAUDE.md — 2026 Financial Presentation

The treasurer's financial update for the 34 Plaza Owners Corp. 2026 Annual Shareholder Meeting: an 8-slide deck plus the source workbook and narrative outline that back it. See [README.md](README.md) for the polished summary and [`Financial Update - Outline & Plan.md`](Financial%20Update%20-%20Outline%20%26%20Plan.md) for the slide-by-slide plan and the consolidated key-numbers table.

## How this folder is structured

- **`2026 Annual Meeting - Financial Update.pptx`** — the deck. Charts are meant to be linked to the source workbook, not hardcoded.
- **`Financial Update - Source Data.xlsx`** — one tab per slide. **Blue-text cells are inputs; everything else is formula-driven.** Change inputs, never the computed cells.
- **`Financial Update - Outline & Plan.md`** — the narrative spine and talk track; the single source for what each slide says and why.
- **`34_Plaza_Capital_Plan_-_Updated_March_2026.xlsx`** and **`capital plan 2026+.gsheet`** — project-level capital plan; the **Targeted Tile Repair** scenario is the one in use.

## Working rules

- **Source of truth:** every shareholder-facing figure traces back to the audited FY2025 financials or the board-approved 2026 budget. Don't introduce numbers that can't be sourced to one of those.
- **Scenario in use is Targeted Tile Repair** (sidewalks ~$35K, not the ~$300K full replacement). If asked to model full replacement, follow the swap steps in the README appendix — change `Slide6_CapitalPlan` and the matching `Slide7_ReserveProj` project-spending row together, and flag that the Slide 6 callout text is hardcoded.
- **Keep the two key analytical calls intact** when editing narrative: (1) targeted repair is a deliberate, reversible board decision, not a deferral; (2) no new assessment is required — the $262.5K/yr escalating capital contribution funds the plan, with the 2028 mortgage refi as the variable to watch.
- **Don't touch the original audited financials / budget PDFs** if present — they're reference, not working files.

## When asked to change numbers

Trace the figure to its tab and input cell first, edit the blue input, and let the formulas recalculate. If a change affects the narrative (e.g. reserve coverage dropping below the 3-month benchmark), call that out — the outline and deck text may need to follow.
