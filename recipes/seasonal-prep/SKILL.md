---
name: seasonal-prep
description: >-
  Get your helpdesk and AI Agent ready for a seasonal event — BFCM, holidays, a
  big sale, a product drop. Drafts the temporary Guidance and Macros you'll need
  for the surge, and flags what to revert afterward. Drafts only.
---

# Seasonal Prep (BFCM, Holidays, Sales)

Every peak season brings the same predictable surge of questions — extended return windows, shipping cutoffs, "will it arrive by [date]", sale-price adjustments. This recipe gets your AI Agent and macros ready *before* the wave hits, and reminds you what to roll back when it's over. Drafts only.

## When to use it

- 2–4 weeks before BFCM, the holidays, or a major sale/drop
- Any event with a temporary policy (extended returns, shipping deadlines, promo codes)

## Customize before you run

| Variable | Example |
|---|---|
| `{{EVENT}}` | "Black Friday / Cyber Monday 2026" |
| `{{TEMP_POLICIES}}` | "extended 90-day returns; order-by Dec 18 for Christmas delivery; code BFCM30" |
| `{{KEY_DATES}}` | "sale Nov 28–Dec 1; shipping cutoff Dec 18" |
| `{{EXPECTED_SPIKES}}` | "WISMO, discount-not-applied, return-window questions" |

## The workflow

> Help me prep for **{{EVENT}}**. Temporary policies in effect: **{{TEMP_POLICIES}}**. Key dates: **{{KEY_DATES}}**.
>
> 1. **Anticipate the surge.** Based on **{{EXPECTED_SPIKES}}** and what happened in past peak periods, list the question types likely to spike.
> 2. **Draft seasonal Guidance.** For each, draft Guidance reflecting the temporary policies — clearly marked as seasonal so it's easy to find later.
> 3. **Draft seasonal Macros.** Canned replies for the team for the same scenarios (shipping cutoffs, promo issues, extended returns).
> 4. **Flag the rollback.** List everything you created and the date/condition to revert or disable it, so temporary policy doesn't silently become permanent.
> 5. Create Guidance and Macros as **drafts** for me to review and publish.

## What it writes

- **Guidance drafts** and **Macro drafts**. You review and publish.
- A **rollback checklist** (text) so nothing temporary lingers.

## Tips

- Tag or name everything `seasonal-{{EVENT}}` so cleanup is one search later.
- After the event, run [`policy-change-sweep`](../policy-change-sweep/) in reverse to revert temporary policies cleanly.
- Preview the high-traffic ones before going live: *"Simulate how my AI Agent answers 'can I still return my Black Friday order?' with the seasonal Guidance enabled."*
