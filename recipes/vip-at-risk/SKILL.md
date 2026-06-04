---
name: vip-at-risk
description: >-
  Surface your high-value customers who had a poor support experience this period
  — low CSAT, long waits, repeat contacts, or unresolved issues — so you can make
  it right before they churn. Read-only.
---

# VIP-at-Risk Detection

Not every unhappy customer is worth a personal save — but your best ones are. This recipe cross-references support experience with customer value to surface the people you most don't want to lose, while there's still time to act. Read-only.

## When to use it

- A weekly or monthly retention ritual
- After a known bad stretch (shipping issue, defect, outage)
- Before a CSM or founder reaches out personally

## Customize before you run

| Variable | Example |
|---|---|
| `{{VIP_DEFINITION}}` | "customers who've spent over $500 lifetime" or "tagged 'VIP'" |
| `{{BAD_EXPERIENCE}}` | "left CSAT ≤ 2, contacted us 3+ times, or has a ticket open >5 days" |
| `{{WINDOW}}` | "this month" |

## The workflow

> Find my high-value customers who had a bad support experience in **{{WINDOW}}**.
>
> 1. Define value as: **{{VIP_DEFINITION}}**. Use whatever signals the MCP can see (Shopify spend via the connected store, VIP tags, order count).
> 2. Define a bad experience as: **{{BAD_EXPERIENCE}}**.
> 3. Return the customers who match **both**. For each: name, why they're flagged as VIP, what went wrong, and the ticket(s) involved.
> 4. Rank by value × severity — who should we reach out to first.
> 5. For the top few, draft a short, personal apology/recovery note I can send or adapt. **Draft only.**

## What it writes

- Read-only by default. Any recovery notes are **drafts** you choose to send.

## Tips

- Keep `{{VIP_DEFINITION}}` honest to your business — lifetime spend, subscription status, or a manual VIP tag all work.
- Pair the outreach with a real gesture (discount, expedited replacement) — an apology alone rarely saves a churning VIP.
- If the same root cause keeps hitting VIPs, that's a [`weekly-voc-digest`](../weekly-voc-digest/) headline, not a one-off.
