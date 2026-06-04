---
name: restock-demand-list
description: >-
  Build a back-in-stock demand list from customers who asked about out-of-stock
  or discontinued products — ranked by demand, with a per-product notify list —
  to drive back-in-stock campaigns and inform the next buy. Read-only.
---

# Restock Demand List

Every "when is this coming back?" ticket is a pre-qualified sale waiting on inventory. Most of that demand evaporates because nobody captures it. This recipe aggregates restock requests by product, so you can size real demand, build a back-in-stock notify list per product, and hand merch a hard signal for the next buy. Read-only.

## When to use it

- Planning a back-in-stock / notify-me campaign
- Informing the next purchase order with real demand, not gut feel
- A quarterly demand review with merch/buying
- After a sellout, to capture and convert the waitlist

## Customize before you run

| Variable | Example |
|---|---|
| `{{WINDOW}}` | "the last 90 days" |
| `{{TOP_N}}` | "the top 15 products by demand" |

## The workflow

> Using the **Gorgias MCP**, build a restock demand list from my support data over **{{WINDOW}}**.
>
> 1. Find tickets and conversations asking about out-of-stock, sold-out, discontinued, or "when will this be back" products.
> 2. Group by product and **rank by number of distinct requesters** — that's your demand signal. Show the top **{{TOP_N}}**.
> 3. For each product, return an export-ready notify list (email, first name) of the customers who asked.
> 4. Flag the products with demand far above the rest — those are the ones to prioritize restocking, not just notifying.

## What it writes

Nothing in Gorgias — read-only. It produces per-product customer lists for you to load into back-in-stock flows. Handle like any customer export.

## Tips

- The per-product lists feed straight into a back-in-stock email/SMS flow — the highest-intent campaign you can send.
- The demand ranking is a buying signal: share the top of the list with merch, and cross-check against [`returns-reduction`](../returns-reduction/) so you don't reorder a high-return product.
- If a discontinued product keeps generating demand, that's a reinstate-or-replace decision for merch.
