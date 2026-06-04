---
name: winback-list-builder
description: >-
  Build a targeted win-back segment from support signal — customers who hit a
  problem, left low CSAT, or went quiet after a bad experience — as a list you
  can hand to your email/SMS tool. The most qualified re-engagement audience you
  have is in your tickets. Read-only.
---

# Win-Back List Builder

Your support history knows exactly which customers wobbled: who hit a problem, who left a low score, who hasn't ordered since a rough experience. That's the most qualified win-back audience you'll ever build — and it's sitting in Gorgias, not your ESP. This recipe turns it into a clean segment you can drop into Klaviyo, Postscript, or wherever your flows live. Read-only.

## When to use it

- Building or refreshing a win-back / re-engagement flow
- After a rough patch (shipping delay, defect, stockout) you want to make right at scale
- A quarterly retention push
- Before a sale, to re-approach lapsed-but-recoverable customers

## Customize before you run

| Variable | Example |
|---|---|
| `{{SEGMENT_CRITERIA}}` | "left CSAT ≤ 3 in the last 90 days on a now-resolved ticket" |
| `{{WINDOW}}` | "the last 90 days" |
| `{{FIELDS}}` | "email, first name, order count, last issue" |

## The workflow

> Using the **Gorgias MCP**, build a win-back segment from my support data over **{{WINDOW}}**.
>
> 1. Find customers matching: **{{SEGMENT_CRITERIA}}**.
> 2. Return them as an export-ready list with these fields: **{{FIELDS}}**.
> 3. Group them by *why* they're on the list (had a defect, slow shipping, low CSAT, abandoned after a question) — the reason should drive the message.
> 4. For each group, suggest a win-back angle and offer that actually addresses what went wrong.
> 5. **Exclude anyone with an open ticket** — don't re-market to someone you're still resolving.

## What it writes

Nothing in Gorgias — read-only. It produces a list of *your own* customers' contact details for you to load into your own email/SMS tool. Handle it like any customer export.

## Tips

- Prioritize your highest-value customers in the list — they deserve a richer offer or a personal note, not a bulk blast.
- Match the gesture to the reason: a defect win-back needs a replacement or credit, not 10% off.
- Suppress anyone who's still unhappy or mid-conversation — re-marketing to an open complaint backfires.
