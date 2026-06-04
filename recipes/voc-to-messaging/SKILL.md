---
name: voc-to-messaging
description: >-
  Turn recurring customer language, objections, and praise from tickets into
  marketing angles, FAQ content, and on-site or ad copy — written in your
  customers' own words. The best copy you'll write is already in your inbox.
  Read-only.
---

# Voice of Customer → Messaging

The best marketing copy is your customers' own words — and they hand them to you in every ticket: the objection that almost lost the sale, the thing they loved, the confusion that made them hesitate. This recipe mines that language and turns it into angles, FAQ content, and copy you can ship. Read-only.

## When to use it

- Briefing creative, a landing page, or an ad set
- Writing or refreshing a PDP FAQ section
- Finding the real objections to pre-empt in email and ads
- Messaging for a launch or a repositioning

## Customize before you run

| Variable | Example |
|---|---|
| `{{TOPIC_OR_PRODUCT}}` | "our hero serum" or "shipping & returns" |
| `{{WINDOW}}` | "the last 6 months" |
| `{{OUTPUT}}` | "5 ad angles", "a PDP FAQ", "landing-page bullets", "email subject lines" |

## The workflow

> Using the **Gorgias MCP**, mine customer language about **{{TOPIC_OR_PRODUCT}}** over **{{WINDOW}}** and turn it into **{{OUTPUT}}**.
>
> 1. Pull pre-sales and post-purchase conversations on this topic/product.
> 2. Extract: the **objections and hesitations** that came up *before* buying; what **delighted** buyers after; and the **recurring confusion** that almost cost a sale.
> 3. Pull a handful of short verbatim quotes that capture each — **redact all PII** (names, emails, order numbers).
> 4. Turn it into **{{OUTPUT}}**, grounded in the real language — no invented benefits. Label anything inferred from keyword matching (heuristic).
> 5. Rank the angles by how often the underlying theme actually showed up.

## What it writes

Nothing — read-only.

## Tips

- Objections you surface here should be answered in two places: pre-emptively in your copy, *and* on the page via [`pdp-gap-finder`](../pdp-gap-finder/).
- Praise quotes are review/UGC gold — pair them with your reviews program.
- Always keep quotes PII-redacted before anything goes public, even internally — it's the customer's words you want, not their identity.
