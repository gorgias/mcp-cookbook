---
name: monthly-helpdesk-hygiene
description: >-
  A recurring helpdesk hygiene audit — redundant or inconsistent tags, stale
  macros, mismatched agent permissions, and gaps in your rules. Use monthly or
  quarterly to keep your Gorgias setup clean as it grows.
---

# Monthly Helpdesk Hygiene Audit

Helpdesk setups rot quietly. Tags multiply, macros go unused, permissions drift, rules develop blind spots — and messy tags are exactly why your reporting stops being trustworthy. This recipe runs a structured audit so cleanup is a 20-minute monthly ritual instead of a once-a-year archaeology dig, and so the numbers you present upward actually hold up. It only *suggests* — you decide what to clean.

## When to use it

- Monthly or quarterly hygiene ritual
- Before onboarding new agents (clean permissions first)
- When your tag list or macro library has clearly sprawled

## Customize before you run

| Variable | Example |
|---|---|
| `{{STALE_DAYS}}` | "90 days" — how long unused = stale |
| `{{SECTIONS}}` | which checks to run (default: all four below) |

## The workflow

> Run a helpdesk hygiene audit on my account. For each section, give me a short list with a clear recommendation — don't change anything.
>
> 1. **Tag taxonomy.** Flag tags that are redundant, inconsistently named (e.g. `return` vs `returns` vs `Return`), or used on almost no tickets. Suggest merges and renames.
> 2. **Stale macros.** Find macros not used in the last **{{STALE_DAYS}}**. For each, tell me whether to update or retire it.
> 3. **Agent permissions.** Flag any agents whose permissions don't match their apparent role.
> 4. **Rule gaps.** Are there gaps in my helpdesk rules that could let tickets fall through the cracks (no assignment, no tag, no routing)?
>
> Prioritize the list: what would you clean up first, and why?

## What it writes

Nothing by default — it produces a cleanup plan. Approve specific items and ask it to act (e.g. *"Archive the 6 stale macros you listed"*).

## Tips

- Pair with [`weekly-voc-digest`](../weekly-voc-digest/): untagged themes it surfaces are candidates for *new* tags here.
- Keep a running doc of what you cleaned each month — the audit gets faster every time.
- Be conservative with tag merges; check volume before deleting anything customers' history relies on.
