---
name: pdp-gap-finder
description: >-
  Find the products generating the most pre-sales questions and post-purchase
  confusion, and get a concrete list of what to add to each product page. Turns
  support tickets into PDP improvements that lift conversion and cut returns.
  Read-only.
---

# PDP Gap Finder

Every pre-sales question your team answers is a question your product page failed to answer first — and every one of those is a shopper who hesitated, bounced, or bought the wrong thing and returned it. Your support queue is the cheapest PDP research you'll ever get. This recipe finds the products customers ask about most, tells you exactly what's missing from each page, and ranks the fixes by impact. Read-only.

## When to use it

- Planning a PDP or storefront refresh and you want it driven by real shopper confusion
- Conversion on a category is soft and you don't know why
- Returns are creeping up and you suspect expectation gaps
- Quarterly merchandising review

## Customize before you run

| Variable | Example |
|---|---|
| `{{WINDOW}}` | "the last 90 days" |
| `{{SCOPE}}` | "the apparel category" or a specific product (optional — omit for all) |
| `{{TOP_N}}` | "the top 10 products" |

## The workflow

> Using the **Gorgias MCP**, find where my product pages are failing shoppers, based on **{{SCOPE}}** over **{{WINDOW}}**.
>
> 1. Look at pre-sales conversations and tickets that reference specific products — both *before* purchase (questions, hesitations) and *after* (confusion, "this wasn't what I expected", returns).
> 2. Group by product and rank by how much support volume each one generates. Focus on **{{TOP_N}}**.
> 3. For each product, identify the specific thing shoppers keep asking or getting wrong — sizing, materials, compatibility, dimensions, care, what's in the box.
> 4. Output a table: **Product | What shoppers ask or get wrong | What to add to the PDP | Priority**. Populate it only from products actually referenced in real conversations — no generic advice.
> 5. Call out the single highest-leverage page to fix first, and why.

## What it writes

Nothing — read-only. Hand the table to whoever owns the storefront.

## Tips

- Pair with [`returns-reduction`](../returns-reduction/): products with the worst PDP gaps are usually the worst return offenders too — fix the page, cut the returns.
- Re-run after you ship the PDP changes to see if the question volume actually dropped — that's your proof the fix worked.
- The same gaps are great [`intent-gap-skills`](../intent-gap-skills/) candidates: if shoppers keep asking it, your AI Agent should answer it too.
