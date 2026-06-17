# Commercial Lease NPV Comparison Model

A net-present-value model for evaluating competing lease offers on a building's commercial space from the **landlord's perspective**. The model compares two lease proposals side by side over a common time horizon, accounting for rent income, upfront tenant-improvement costs borne by the building, annual rent escalation, vacancy between lease cycles, and time-value discounting.

## The decision

The building received two offers for the same commercial unit:

| | Lease A | Lease B |
|---|---|---|
| Monthly rent | $4,500 | $4,800 |
| Term | 1 year | 5 years |
| Building investment required | $0 | $35,000 (tenant improvements) |

On the surface Lease B collects more rent per month, but the building must spend $35K to prepare the space. Lease A requires no investment but exposes the building to annual turnover and vacancy risk. The question: **which offer generates more value for the building over time?**

## What the model does

Both leases are evaluated over the same time horizon (the longer of the two terms) so the comparison is apples-to-apples. For shorter-term leases, the model cycles through lease periods and vacancy gaps to project realistic cash flows across the full horizon.

The key inputs — all toggleable in the spreadsheet — are: monthly rent, lease term, upfront investment, annual rent escalation, vacancy between leases, and discount rate. The model computes total rent income, NPV of that income stream, net NPV after subtracting the building's investment, and a per-month net return for direct comparison.

The **Cash Flows** tab shows month-by-month detail: each month's rent income (or $0 during vacancy), the discount factor, and the present value of that payment.

## How the inputs interact

The vacancy assumption is the swing factor. With default inputs (3 months vacancy between annual leases), Lease A only collects rent in 48 of 60 months while Lease B collects all 60. That lost income from turnover outweighs Lease A's lower cost basis, and Lease B wins. Set vacancy to zero — assuming seamless back-to-back renewals — and Lease A's no-investment advantage takes over.

This lets the board frame the decision around a concrete question: *how confident are we that we can re-lease this unit within X months each year?*

## How the model was built

This model went through several iterations to get the framing right:

1. **First pass — tenant perspective.** The initial build treated both rent and investment as costs, producing a "lowest cost" comparison. This was backwards for a building owner evaluating income-generating assets.

2. **Second pass — landlord perspective, total NPV.** Flipped rent to income and investment to cost. But comparing total NPV across different lease lengths always favored the shorter lease (less total obligation), which made the longer lease impossible to justify regardless of inputs.

3. **Third pass — per-month NPV.** Switched the comparison metric to NPV per month to normalize across different terms. Better, but still no scenario existed where the 5-year lease won, because the model didn't account for what happens when the 1-year lease expires.

4. **Final model — common horizon with vacancy cycling.** Both leases evaluated over the same 5-year window. Shorter leases cycle through lease + vacancy periods. This correctly captures the real trade-off: guaranteed long-term income vs. turnover risk. The vacancy toggle is now the decisive input, which matches how the board actually thinks about the decision.

## Files in this folder

| File | What it is |
|---|---|
| `Lease_NPV_Comparison.xlsx` | The interactive NPV model. Toggle the blue/yellow input cells to run scenarios. |
| `README.md` | This file — model documentation and iteration history. |

## Spreadsheet conventions

The workbook follows standard financial modeling conventions: blue text on yellow background marks input cells the user should toggle, black text marks formulas, and green text marks cross-sheet references. All calculations use Excel formulas (no hardcoded values), so changing any input recalculates the entire model.

---

*Built for the board of 34 Plaza Owners Corp. to support a commercial lease decision.*
