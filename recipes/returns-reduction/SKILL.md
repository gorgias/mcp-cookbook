---
name: returns-reduction
description: >-
  Cluster why customers actually return products — sizing, quality, expectation
  gaps — by product, from ticket and return language, so you can fix the root
  cause instead of just processing the refund. Returns are a margin killer;
  this finds where they start. Read-only.
---

# Returns Reduction Analysis

Returns are one of the biggest silent margin leaks in DTC, and the reason for each one is sitting in plain language in your tickets — "ran small," "looked different online," "stopped working after a week." This recipe clusters the *why* behind returns by product, so you can fix the source (a misleading PDP, a sizing gap, a quality issue) instead of just eating the refund again next month. Read-only.

## When to use it

- Return rate is climbing and you need to know what's driving it
- Before a buying/merch decision on a product or category
- Quarterly margin review
- Investigating a single product that's returning more than it should

## Customize before you run

| Variable | Example |
|---|---|
| `{{WINDOW}}` | "the last 90 days" |
| `{{SCOPE}}` | "all products", a category, or one SKU |

## The workflow

> Using the **Gorgias MCP**, analyze why customers are returning products in **{{SCOPE}}** over **{{WINDOW}}**.
>
> 1. Pull tickets and conversations about returns, exchanges, and "this wasn't what I expected" — use tags where they exist, and customer language where they don't (label those (heuristic)).
> 2. Cluster the **reasons** customers give: sizing/fit, quality/defect, didn't match the description or photos, shipping/damage, changed their mind, wrong item.
> 3. Break it down **by product** — which products drive the most returns, and the dominant reason for each.
> 4. For the worst offenders, name the specific expectation gap and the root-cause fix: PDP copy, a sizing guide, better photos, a QA flag for the buying team, or a packaging change.
> 5. Rank by volume × fixability — where will one change remove the most returns.

## What it writes

Nothing — read-only.

## Tips

- "Quality/defect" clusters aren't a PDP problem — route those to whoever owns buying/QA, fast. A recurring defect is a supplier conversation, not a copy edit.
- "Ran small / didn't fit / looked different" → straight into [`pdp-gap-finder`](../pdp-gap-finder/) to fix the page.
- Track return rate on the products you fixed over the next window — closing the loop is how you prove the work paid off.
