# CLAUDE.md — Commercial Lease NPV Comparison

A net-present-value model comparing two competing lease offers on the building's commercial space, from the **landlord's perspective**. See [README.md](README.md) for the decision context, model logic, and iteration history.

## What's here

- **`Lease_NPV_Comparison.xlsx`** — the interactive model. Two lease proposals (A: $4,500/mo, 1-yr, no investment · B: $4,800/mo, 5-yr, $35K tenant improvements) evaluated over a common horizon.
- **`README.md`** — model documentation and the build history (four iterations from a naive cost comparison to the final landlord-perspective model).

## How the model works

- Both leases are evaluated over the **same time horizon** (the longer term) so the comparison is apples-to-apples. Shorter leases cycle through lease + vacancy periods.
- Key metric is **NPV per month**, which normalizes across different lease lengths — total NPV alone always favors the shorter lease and is misleading.
- **Vacancy is the swing input.** With the default 3-month vacancy between annual leases, Lease B wins; set vacancy to zero and Lease A's no-investment advantage takes over.

## Working rules

- **Spreadsheet conventions:** blue text on yellow background = input cells the user toggles; black text = formulas; green text = cross-sheet references. **All calculations are Excel formulas — no hardcoded values.** Edit inputs, not computed cells.
- **Keep the landlord framing.** Rent is income, the tenant-improvement spend is the only cost. An earlier iteration treated both as costs (tenant perspective) — that's the bug the final model fixed; don't reintroduce it.
- **Keep the common-horizon + vacancy-cycling logic.** Comparing raw total NPV across unequal terms is the framing error documented in the README; per-month NPV over a shared horizon is the correct comparison.
- When changing inputs, recompute and report which lease wins and why — the point of the model is to frame the board's decision around re-leasing confidence (the vacancy assumption).
