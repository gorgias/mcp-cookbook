---
name: intent-gap-guidance
description: >-
  Find the high-volume customer intents your AI Agent has no Guidance for, then
  draft Guidance to close each gap. Use to systematically raise AI Agent coverage
  by aiming new knowledge at what customers actually ask most.
---

# Intent-Gap → Guidance

The fastest way to raise AI Agent coverage isn't writing more Guidance — it's writing the *right* Guidance. This recipe finds the topics customers ask about most that your AI Agent currently has no answer for, and drafts Guidance for each, ranked by impact. Drafts only; you review and publish.

## When to use it

- Your AI Agent is live but coverage or automation rate is plateauing
- After a [`weekly-voc-digest`](../weekly-voc-digest/) surfaces a theme with no AI answer
- A recurring optimization loop (monthly) to keep coverage climbing

## Customize before you run

| Variable | Example |
|---|---|
| `{{MIN_VOLUME}}` | "at least 20 tickets in the last 90 days" |
| `{{TOP_N}}` | "the top 5 gaps" — how many to draft this round |
| `{{WINDOW}}` | "the last 90 days" |

## The workflow

> Help me close my AI Agent's biggest knowledge gaps.
>
> 1. Look at my ticket intents over **{{WINDOW}}**. Identify high-volume topics (**{{MIN_VOLUME}}**) where my AI Agent has **no matching Guidance**, or where it's handing these over instead of resolving them.
> 2. Rank the gaps by volume — biggest impact first.
> 3. For **{{TOP_N}}** gaps, draft a Guidance for each. Ground each draft in how my team *actually* answers these tickets today (use real resolved tickets as the source of truth, not generic advice).
> 4. Create them as **drafts**. List what you created so I can review and publish.

## What it writes

- **Guidance drafts** only. Nothing is published until you say so.

## Tips

- Before publishing, preview each one: *"Simulate how my AI Agent would answer [the customer question] with this new Guidance enabled."*
- If your team already encoded logic in **Flows**, ask it to convert those instead of writing from scratch: *"Is there a Flow covering this gap I should convert to Guidance?"*
- Run it monthly with a small `{{TOP_N}}` — steady gains beat one giant batch nobody reviews.
