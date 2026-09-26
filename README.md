# Ryndix Amazon category data

Point-in-time measurements of Amazon US categories, published as open data.

Each dataset is the evidence layer behind one published Ryndix category review.
Every figure is either **measured** from a marketplace snapshot or an **assumption**
that is labelled as such. Nothing here is modelled, forecast or estimated silently.

**Why this repository exists:** most "is this niche worth entering" answers online are
opinions. These are the numbers, with the method, so anyone can check the arithmetic
or reuse it under an attribution licence.

- Reviews and verdicts: <https://www.ryndix.com/cases>
- Free tools (listing score, main-image compliance): <https://www.ryndix.com/tools>
- Method: [METHOD.md](METHOD.md)
- Licence: CC BY 4.0 — reuse freely, credit required ([LICENSE](LICENSE))

---

## Categories

| Category (Amazon US) | Snapshot | Headline | Verdict |
|---|---|---|---|
| Under-desk treadmill (walking pad) | 2024-09 / 2026-08 | Top 100 move **$19.5M/month** and 150,225 units; at the **$99.99** median price one unit leaves **$15.16** before ads (18.3% gross margin) | Stop for a new seller buying traffic |
| Home mold test kit | 2026-08 | A keyword tool reports **168,228** searches against **139** listings; the near-synonym reports **85** against **17,797**; demand **-48%** YoY | Stop |
| Electric grill brush | 2026-08 | **$3.57** cost per click against a **$39.99** median price; break-even needs a **29.9%** conversion rate; **64x** peak-to-trough seasonality | Conditional above $70 |
| Affirmation cards | 2026-08 | **50.7%** gross margin at **$16.90** and a **$0.45** click, but demand is **-40%** YoY against 29,240 competing listings | Worth testing as a short-cycle position |
| Pool rafts & inflatable ride-ons (tanning sub-segment) | 2026-09 | At the leader's **$26.99** price, fees alone take **$17.05**, so the margin ceiling with **zero** goods cost is **36.8%**; at the real 1688 sourcing price, **1.8%** | Product-definition problem, not a marketing one |

## Files

```
data/categories.csv        one row per category, all metrics as columns
data/<slug>.json           full dataset per category (schema.org Dataset shape)
```

Each JSON file carries:

- `variableMeasured` — every metric, with its unit in the name
- `measurementTechnique` — how the snapshot was taken
- `temporalCoverage` — the window the data describes
- `authoritativeSources` — the primary sources (EPA, CPSC, NIH/PMC, US Copyright
  Office, Amazon, Apple) the review relies on for any regulatory or platform claim
- `headlineVerdict` — the published conclusion, so the data is not read without it

## What these numbers are not

They are **point-in-time**. Marketplace prices, fees, cost per click and demand move;
a snapshot from September 2026 is not a statement about November 2026. Cost inputs
marked as assumptions are illustrative and are replaced by real quotes in a paid
engagement. Nothing here is financial, legal or investment advice, and no figure is a
promise of profit, sales or ranking.

## Citation

```
Ryndix (Ylemos Inc). (2026). Ryndix Amazon category data [Data set].
https://github.com/joke52tan/ryndix-category-data
```

## Contributing a correction

If a number here disagrees with what you see in Seller Central or on the listing page,
open an issue with the category, the metric and the source. Corrections are published
with the date they were made.
