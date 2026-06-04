---
name: backlog-triage
description: >-
  Clear a ticket backlog faster by drafting replies in bulk for your oldest
  unresolved tickets, grouped by type, for you to review and send. Use after a
  spike, a holiday, or any time the queue got away from you.
---

# Backlog Triage & Draft

When the queue blows up, every hour it sits is a CSAT hit and an SLA breach — and the slowest part isn't typing, it's context-switching across dozens of half-similar tickets. This recipe reads your oldest open tickets, groups them, and drafts a reply for each so you and your agents can review and send in batches. Drafts only — nothing sends without you.

## When to use it

- After a demand spike, outage, or holiday backlog
- Monday-morning cleanup of the weekend queue
- Any time "oldest unresolved" has crept past your SLA

## Customize before you run

| Variable | Example |
|---|---|
| `{{AGE_THRESHOLD}}` | "open and untouched for more than 3 days" |
| `{{SCOPE}}` | "tickets tagged 'shipping-delay'" (or leave open for all) |
| `{{TONE}}` | "warm, concise, apologetic where we're late" |
| `{{EXCLUDE}}` | "skip anything that looks like it needs a refund decision" |

## The workflow

> Help me clear my backlog. Scope: **{{SCOPE}}**, **{{AGE_THRESHOLD}}**.
>
> 1. Pull those tickets and **group them** by what the customer actually needs (status update, return, where-is-my-order, etc.).
> 2. For each group, tell me how many there are and the common ask.
> 3. Draft a reply for each ticket in a **{{TONE}}** tone. Pull real order/customer context where the MCP can see it, so replies aren't generic.
> 4. **{{EXCLUDE}}** — flag those separately for me to handle manually instead of drafting.
> 5. Show me the drafts grouped. I'll review, edit, and approve which ones to send.

## What it writes

- **Reply drafts.** Nothing sends until you approve each batch.
- Optionally closes tickets *after* a reply, only if you ask (e.g. *"send and close the where-is-my-order group"*).

## Tips

- Start narrow with `{{SCOPE}}` — one ticket type — to build trust before going broad.
- Always keep `{{EXCLUDE}}` honest: refunds, complaints, and anything emotional deserve a human.
- For recurring backlog types, the real fix is upstream — feed them into [`intent-gap-guidance`](../intent-gap-guidance/) so your AI Agent handles them next time.
