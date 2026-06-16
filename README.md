# 2026 Annual Meeting — Financial Update Deck

Two files were generated together:

| File | What it is |
|---|---|
| `2026 Annual Meeting - Financial Update.pptx` | The 8-slide deck (modern minimal, navy + amber accents). |
| `Financial Update - Source Data.xlsx` | All numbers behind every chart, organized one tab per slide. Edit the **blue-text** cells to update inputs. |

The outline (`Financial Update - Outline & Plan.md`) is the narrative/planning doc — useful for the talk track.

---

## How to convert these to Google Slides + Google Sheets (and link the charts)

### Step 1 — Convert each file to Google format

1. Open **Google Drive** → upload `Financial Update - Source Data.xlsx`.
2. Right-click the uploaded file → **Open with → Google Sheets**.
3. Once opened, **File → Save as Google Sheets** (or the duplicate auto-converts). Keep the converted version.
4. Repeat for `2026 Annual Meeting - Financial Update.pptx` → open with Google Slides → save as Google Slides.

### Step 2 — Replace each embedded chart with a linked chart from the Sheet

For each chart slide listed below:

1. In Google Slides, click the existing chart and **Delete** it.
2. Click where the chart was → **Insert → Chart → From Sheets**.
3. Pick the Google Sheets version of `Financial Update - Source Data`.
4. Select the chart range from the matching tab (see table below).
5. Make sure **"Link to spreadsheet"** is checked, then **Import**.
6. Resize to fit. From now on, edits to blue cells in the Sheet propagate to the deck via the "Update" button on the chart.

| Slide | Chart | Source tab | Range to select |
|---|---|---|---|
| 3 | Income donut | `Slide3_BudgetMix` | `A5:B15` |
| 3 | Expense donut | `Slide3_BudgetMix` | `A20:B28` |
| 4 | 12-yr maintenance bars | `Slide4_MaintHistory` | `A5:C17` (use Year + % Increase columns) |
| 5 | Reserve waterfall | `Slide5_ReserveWaterfall` | `A5:C13` (use Step + Running Balance) |
| 6 | Capital plan stacked column | `Slide6_CapitalPlan` | `A21:F29` |
| 7 | Reserves vs benchmark | `Slide7_ReserveProj` | `A12:F13`, `A20:F20`, `A22:F22` (the three rows for chart) |

> Tip: it's often easier to first set up a clean chart **inside the Google Sheet** (one chart per tab, pre-styled), then use Insert → Chart → From Sheets and point to the existing chart rather than a range. That way the styling lives with the Sheet and the deck just embeds it.

---

## Where the inputs live (the cells you'll edit most often)

| Tab | Cells you'll touch |
|---|---|
| `Headlines` | All blue cells — flow into Slide 2 tiles and Slide 8 takeaways |
| `Slide3_BudgetMix` | Column B (income lines & expense lines) — % shares recalculate |
| `Slide4_MaintHistory` | Column C (% increase) for the bar chart; rows 24–26 for the driver tiles |
| `Slide5_ReserveWaterfall` | Column B (each waterfall step). Running balance auto-updates. |
| `Slide6_CapitalPlan` | Columns B–F (project × year). Category totals auto-roll up via SUMIF. |
| `Slide7_ReserveProj` | Yellow-highlighted assumption cells in B5–B9 (opening reserve, contribution, growth rates) drive the full 5-year projection. Project spending row is hardcoded to the targeted-tile-repair scenario. |

---

## Scenario flexibility (e.g., to test a different sidewalk option)

To swap the sidewalks scenario back to full replacement:
1. Go to `Slide6_CapitalPlan` tab.
2. In the **Sidewalks (Targeted Tile Repair)** row, change the **2026** cell from `$35,000` to `$300,000`.
3. Update the **Sidewalk decision callout** at the bottom of the tab if needed.
4. Then in `Slide7_ReserveProj`, update row 17 (Project Spending) for 2026: change from `-279000` to `-544000` to match the new total.
5. The reserve trajectory and coverage % will recalculate automatically.

The board decision callout on Slide 6 of the deck is hardcoded text — you'll want to edit those text boxes manually if you change the scenario.

---

## Style reference

- **Header font:** Georgia, bold
- **Body font:** Calibri
- **Palette:**
  - Navy `#1E5A8C` (primary)
  - Amber `#D97706` (callouts & "watch this" items)
  - Green `#10804A` (positive outcomes)
  - Muted gray `#6B7280` (secondary text)
  - Charcoal `#1F2328` (body text)
- **Layout:** 16:9, 0.6" margin, hairline rule under each title, page number bottom-right, footer bottom-left.

---

## Files in this folder

- `2026 Annual Meeting - Financial Update.pptx` — the deck (this is what you import to Google Slides)
- `Financial Update - Source Data.xlsx` — the source workbook (this is what you import to Google Sheets)
- `Financial Update - Outline & Plan.md` — the narrative outline used to build the deck
- `Financial Update - README.md` — this file
- The historical source documents (audited financials PDF, 2026 budget PDF, capital plan gsheet) remain untouched.
