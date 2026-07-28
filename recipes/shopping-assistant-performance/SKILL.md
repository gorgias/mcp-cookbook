---
name: shopping-assistant-performance
description: >-
  Analyze how your Shopping Assistant is performing as a revenue channel — most
  recommended products, best-converting recommendation pairs, revenue and
  time-to-purchase per conversation, and the pre-sales topics and handover
  reasons behind it. Read-only. Analytics are in beta — directional.
---

# Shopping Assistant Performance

Shopping Assistant is a revenue surface, not a support cost — it recommends products, answers pre-sales questions, and nudges shoppers toward checkout. But most teams never look at *how well* it sells. This recipe turns it into a channel you can actually manage: what it recommends, what converts, what it earns, and where pre-sales conversations break down. Read-only.

> **Heads up:** Gorgias MCP analytics are in **beta**. Revenue, conversion, and time-to-purchase figures are directional and may differ from your in-product Statistics. Use them for trends and prioritization, and cross-check exact numbers before reporting them up.

## When to use it

- A monthly read on Shopping Assistant as a revenue channel
- Deciding which products to feature or pair in recommendations
- Diagnosing why pre-sales conversations stall or hand over to a human
- Building the case for (or measuring the ROI of) pre-sales automation

## Customize before you run

| Variable | Example |
|---|---|
| `{{WINDOW}}` | "the last 30 days" |
| `{{COMPARE_TO}}` | "vs the previous 30 days" (optional) |

## The workflow

> Using the **Gorgias MCP**, give me a Shopping Assistant performance read for **{{WINDOW}}** ({{COMPARE_TO}}). Where a figure relies on beta analytics, say so.
>
> **Recommendations & conversion**
> 1. What are my most recommended products?
> 2. What products are most commonly recommended together, and which pair converts best?
> 3. What's the purchase rate per recommendation pair?
>
> **Revenue & velocity**
> 4. What's the revenue per Shopping Assistant conversation?
> 5. What's the time-to-purchase after a recommendation?
>
> **Where shoppers engage & stall**
> 6. Which product pages start the most conversations?
> 7. What pre-sales topics do shoppers ask about most frequently?
> 8. What are the biggest handover reasons for pre-sales conversations, and how often does each occur?
>
> Close with the top 3 actions: products to feature, pairings to push, and the pre-sales gap to fix first.

## What it writes

Nothing — read-only.

## Tips

- Recurring **handover reasons** are pre-sales questions the assistant couldn't close — feed them to [`intent-gap-skills`](../intent-gap-skills/) so it can next time.
- Pre-sales topics that map to specific products belong in [`pdp-gap-finder`](../pdp-gap-finder/) — answer them on the page *and* in the assistant.
- Some signals (e.g. product-link clicks / add-to-cart from a card) may not be available yet — if a number comes back empty, it's a current limitation, not a data error.
