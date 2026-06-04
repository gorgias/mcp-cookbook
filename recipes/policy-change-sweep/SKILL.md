---
name: policy-change-sweep
description: >-
  Find and update every place a business policy lives across your Gorgias account
  — Guidance, Macros, and helpdesk rules — when that policy changes. Use when a
  return window, shipping cutoff, warranty term, or any stated policy is updated
  and you need it reflected everywhere consistently.
---

# Policy Change Sweep

When you change a policy, the old version is usually hiding in a dozen places: an AI Agent Guidance, three Macros, a helpdesk rule. Miss one and your AI Agent contradicts your team — which means wrong answers, CSAT hits, and repeat contacts landing right back in your queue. This recipe finds every reference and updates them in one pass — with you approving each change.

This is the kind of sweep that's painful by hand and **impossible through the REST API alone** (Guidance has no bulk REST surface). The MCP is the only supported route.

## When to use it

- You changed a return/exchange window (e.g. 30 → 60 days)
- A shipping cutoff, delivery estimate, or carrier changed
- A warranty term, price, discount code, or eligibility rule changed
- Any stated policy that customers ask about and your AI Agent answers

## Customize before you run

Replace these with your real values:

| Variable | Example |
|---|---|
| `{{OLD_POLICY}}` | "30-day return window" |
| `{{NEW_POLICY}}` | "60-day return window" |
| `{{EFFECTIVE_DATE}}` | "starting June 15, 2026" (optional) |

## The workflow

Paste this into your connected AI client, with your values filled in:

> Using the **Gorgias MCP**, sweep my Gorgias account for a policy change.
> We changed our policy: **{{OLD_POLICY}} → {{NEW_POLICY}}** ({{EFFECTIVE_DATE}}).
> Sweep my whole account for the old policy and prepare updates. Specifically:
>
> 1. Search my **Guidance** for any mention of the old policy or its specifics (the old number, dates, terms). List each match with its title.
> 2. Search my **Macros** for the same — canned replies often hard-code the old wording.
> 3. Check my **helpdesk rules** for conditions or actions tied to the old policy.
> 4. For each match, show me the current text and a proposed edit side-by-side. **Don't change anything yet.**
> 5. Once I approve, apply the updates — Guidance as drafts for me to publish, Macros and rules updated directly.

## What it writes

- **Guidance** → created/updated as **drafts**. You publish.
- **Macros** → updated in place after your approval.
- **Rules** → updated in place after your approval.

Nothing changes until you've seen the before/after and said go.

## Tips

- Run it **before** the policy goes live, so everything flips on the effective date.
- Ask it to also check for *implicit* references ("a few weeks", "within a month") — not just the exact number.
- Re-run a read-only pass afterward: *"Confirm nothing still references {{OLD_POLICY}}."*
