# 2026 Annual Meeting — Financial Update

The treasurer's financial presentation for the 34 Plaza Owners Corp. 2026 Annual Shareholder Meeting: an 8-slide deck that takes a non-financial audience from the prior year's results through the year ahead and out to the five-year capital horizon, with every figure traced back to the audited financials or the board-approved budget.

## The story it tells

The deck is built around a three-act arc:

1. **2025 — we got ahead of capital needs.** Operations ran slightly hot, but a board-approved two-year assessment more than doubled the reserve fund (from $500K to $1.14M), and the audit closed with a clean, unmodified opinion.
2. **2026 — a 5.5% maintenance increase holds operations at breakeven** while absorbing real cost pressure: insurance up 10%, payroll up 6.2% ahead of the 32BJ contract, and taxes up 2%. The increase is in line with the building's long-run norm, not an outlier.
3. **2027–2030 — the five-year capital plan, and the one variable that actually matters.** ~$2.19M of capital work, dominated by the elevator modernization, with reserves holding at or above the three-month operating benchmark through 2028. The real risk isn't the capital plan — it's the $5.618M mortgage maturing December 2028.

## The analytical calls behind it

The presentation isn't just a reporting exercise; it makes and defends two judgment calls that a skeptical shareholder could push on:

- **Sidewalks — targeted tile repair, not full replacement.** Full replacement would have cost ~$300K in 2026; the targeted repair runs ~$35K. The deck frames the ~$265K difference as a deliberate, reversible board decision that preserves reserve capacity ahead of the elevator project — not a deferral of needed work. The sidewalks are structurally sound, and the repair carries no compliance penalty.
- **No new assessment is required to execute the plan.** Modeling the reserve trajectory under the targeted-repair scenario shows the existing $262.5K/yr capital contribution (escalating ~5%) is correctly sized. Reserves stay at or above the three-month benchmark through 2028, dip ~$88K at the 2029 trough, and recover by 2030. Naming the 2028 refinancing — not the capital cadence — as the variable to watch is the central message of the closing slides.

Every chart is driven off a single source-data workbook, one tab per slide, so the numbers behind the narrative stay reproducible and any input can be changed without rebuilding the deck.

## Files in this folder

| File | What it is |
|---|---|
| `2026 Annual Meeting - Financial Update.pptx` | The 8-slide deck (modern minimal — navy + amber accents). |
| `Financial Update - Source Data.xlsx` | Every figure behind every chart, one tab per slide. Blue-text cells are inputs. |
| `Financial Update - Outline & Plan.md` | The treasurer's pre-build slide plan and the consolidated table of key numbers — the narrative spine and the talk track. |
| `34_Plaza_Capital_Plan_-_Updated_March_2026.xlsx` | Project-level capital plan (Targeted Tile Repair scenario in use). |
| `capital plan 2026+.gsheet` | Pointer to the live capital plan in Google Sheets. |

The historical source documents (audited financials, 2026 budget) remain untouched in their original form.

---

## Appendix — working with the deck

<details>
<summary>Converting to Google Slides + Sheets and keeping charts linked</summary>

**Convert each file.** Upload the `.xlsx` and `.pptx` to Google Drive, open each with Google Sheets / Google Slides, and save as the Google-native format.

**Re-link each chart.** In Slides, delete the embedded chart, then **Insert → Chart → From Sheets**, point to the converted source workbook, and check **"Link to spreadsheet."** After that, edits to blue input cells propagate to the deck via the chart's "Update" button.

| Slide | Chart | Source tab | Range |
|---|---|---|---|
| 3 | Income / expense donuts | `Slide3_BudgetMix` | `A5:B15`, `A20:B28` |
| 4 | Maintenance history bars | `Slide4_MaintHistory` | `A5:C17` (Year + % Increase) |
| 5 | Reserve waterfall | `Slide5_ReserveWaterfall` | `A5:C13` (Step + Running Balance) |
| 6 | Capital plan stacked column | `Slide6_CapitalPlan` | `A21:F29` |
| 7 | Reserves vs. benchmark | `Slide7_ReserveProj` | `A12:F13`, `A20:F20`, `A22:F22` |

Tip: pre-style one chart per tab inside the Sheet, then embed via Insert → Chart → From Sheets so styling lives with the data.

</details>

<details>
<summary>Where the inputs live</summary>

| Tab | Cells to edit |
|---|---|
| `Headlines` | All blue cells — feed Slide 2 tiles and Slide 8 takeaways |
| `Slide3_BudgetMix` | Column B (income/expense lines); % shares recalculate |
| `Slide4_MaintHistory` | Column C (% increase); rows 24–26 for driver tiles |
| `Slide5_ReserveWaterfall` | Column B (each step); running balance auto-updates |
| `Slide6_CapitalPlan` | Columns B–F (project × year); totals roll up via SUMIF |
| `Slide7_ReserveProj` | Yellow assumption cells B5–B9 drive the 5-year projection |

</details>

<details>
<summary>Swapping the sidewalk scenario back to full replacement</summary>

1. In `Slide6_CapitalPlan`, change the **Sidewalks (Targeted Tile Repair)** 2026 cell from `$35,000` to `$300,000`.
2. In `Slide7_ReserveProj`, change row 17 (Project Spending) 2026 from `-279000` to `-544000`.
3. The reserve trajectory and coverage % recalculate automatically.
4. The board-decision callout text on Slide 6 of the deck is hardcoded — edit those text boxes by hand.

</details>

<details>
<summary>Style reference</summary>

- **Fonts:** Georgia bold (headers), Calibri (body)
- **Palette:** Navy `#1E5A8C` · Amber `#D97706` (callouts) · Green `#10804A` (positives) · Gray `#6B7280` (secondary) · Charcoal `#1F2328` (body)
- **Layout:** 16:9, 0.6" margin, hairline rule under each title, page number bottom-right, footer bottom-left.

</details>

---

*Prepared by the treasurer of 34 Plaza Owners Corp. Working analysis — not an official statement of the corporation.*
