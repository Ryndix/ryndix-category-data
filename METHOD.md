# Method

## What is measured, and how

For each category we take a **snapshot of the live Amazon US marketplace**, not a
secondary database:

1. **Category frame.** Build the category from its actual top listings rather than from
   a keyword-tool taxonomy — for the mold test kit review, only 18 of the top 100
   "indoor air quality meter" listings are mold tests at all. Treating the tool's
   category total as the market overstates it by roughly double.
2. **Volume and price.** Pull units sold, revenue, review counts and listed prices for
   the top listings; take medians and volume-weighted prices, never the mean alone.
3. **Demand.** Keyword demand is read from more than one phrasing. Where two
   near-synonyms of the same concept disagree by orders of magnitude
   (168,228 vs 85), the disagreement is reported as a finding about the data source.
4. **Unit economics.** Referral fee, fulfilment fee, freight, storage and return rate
   are applied to the median price to get a pre-ad contribution per unit. Assumed
   inputs (product cost, freight, conversion) are labelled wherever they appear.
5. **Break-even advertising.** Cost per click is divided into the pre-ad contribution to
   get the conversion rate that advertising would need just to break even.
6. **Rules and recalls.** Any regulatory claim is sourced to the primary document
   (US EPA, US CPSC, NIH/PMC, US Copyright Office) and linked from the review.

## Why the verdict is published with the data

A category can have enormous demand and still be unenterable — the walking pad
category moves $19.5M a month and leaves $15.16 a unit before advertising. Publishing
the metrics without the conclusion invites the data to be quoted as an opportunity.

## Known limits

- Snapshot data ages. Each file records its `temporalCoverage`; do not read a 2026-09
  snapshot as current without re-measuring.
- Amazon fee schedules change; the fee inputs are the ones in force at snapshot time.
- Cost per click is a marketplace-reported figure and is volatile within a week.
- Sub-segment shares are computed on the sub-segment of the top 100, not the whole
  category, wherever the file says so.

## Corrections

Open an issue with the category, metric and source. Corrections are dated.
