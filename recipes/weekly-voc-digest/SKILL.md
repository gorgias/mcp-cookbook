---
name: weekly-voc-digest
description: >-
  A repeatable Voice-of-Customer digest from your Gorgias tickets — top contact
  reasons, recurring complaints, restock requests, and emerging themes. Use weekly
  (or on any cadence) to stay on top of what customers are actually telling you.
---

# Weekly Voice-of-Customer Digest

You're the only person in the company who hears from every customer, every day — but that signal is buried in hundreds of tickets nobody else reads. This recipe turns a week of tickets into a short, themed digest you can drop into Slack, so Product, Merch, and Ops act on what you're already seeing. Read-only — it touches nothing in your account.

## When to use it

- A weekly or biweekly ritual to spot trends before they become fires
- Before a product/ops sync, to bring real customer evidence
- After a launch or a change, to see how it landed in support

## Customize before you run

| Variable | Example |
|---|---|
| `{{WINDOW}}` | "the last 7 days" |
| `{{THEMES}}` | "shipping, product quality, sizing, returns" (or leave open) |
| `{{AUDIENCE}}` | "my ops team" — shapes tone and length |

## The workflow

> Build a Voice-of-Customer digest from my tickets over **{{WINDOW}}**, for **{{AUDIENCE}}**.
>
> 1. **Top contact reasons.** Group tickets by theme and rank them. Show volume and the week-over-week change for each.
> 2. **Complaints & frustration.** Summarize the most common complaints, especially from low-CSAT tickets. Quote real customer language, don't paraphrase into corporate.
> 3. **Restock & product asks.** What products are customers asking us to restock or carry?
> 4. **Untagged patterns.** Are there recurring themes that *aren't* captured by my current tags? Flag them — they may need a new tag.
> 5. **One thing to act on.** End with the single highest-leverage follow-up for this week.
>
> Keep it under 400 words. Lead with the headline, not the methodology.

## What it writes

Nothing. Pure read.

## Tips

- Make it a real cadence: combine with the [`schedule`](https://docs.claude.com) capability in your client, or just keep the prompt in a saved note.
- If a theme spikes, hand off to the [`intent-gap-guidance`](../intent-gap-guidance/) recipe to close the gap in your AI Agent.
- Ask it to compare two windows: *"How does this week compare to the same week last month?"*
