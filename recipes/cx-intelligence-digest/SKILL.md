---
name: cx-intelligence-digest
description: >-
  Turn the last 7 days of Gorgias tickets into an executive-ready weekly CX
  digest — analyzed across five business functions (Product, Marketing,
  Ecommerce/Revenue, Product Marketing, Leadership) with a TLDR, signal-status
  tagging, a PDP-gap table, and owner-tagged actions. Read-only; optionally
  publishes to Notion.
---

# CX Intelligence Digest Generator

Your support queue is the highest-signal feedback loop in the business — but the insight is scattered across hundreds of tickets and never reaches the teams who could act on it. This recipe compresses a week of tickets into one structured, executive-ready digest, read through five functional lenses, with owner-tagged actions so it doesn't die in someone's inbox.

It's the heavyweight sibling of [`weekly-voc-digest`](../weekly-voc-digest/): that one is a quick VoC pulse; this is the full cross-functional readout you'd send to leadership. Read-only on Gorgias — it can optionally publish straight to Notion.

> **Heads up:** the volume, automation, and resolution figures rely on Gorgias MCP analytics, which are in **beta** and directional. The prompt's built-in rules (no invented data, `(heuristic)` labels, small-sample caveats) keep it honest — cross-check exact numbers in your Statistics dashboard before reporting them up.

## When to use it

- A weekly leadership/cross-functional CX readout
- Feeding Product, Marketing, and Ecommerce real customer evidence on a cadence
- Replacing the manual "what did support hear this week" doc someone writes by hand

## Customize before you run

| Variable | Example |
|---|---|
| `{{BRAND_NAME}}` | "Acme" |
| `{{START_DATE}}` | "2026-05-22" |
| `{{END_DATE}}` | "2026-05-28" |
| `{{PARENT_PAGE}}` | a Notion page/database to publish under (optional — omit to get markdown back) |

The **five lenses** (Product / Marketing / Ecommerce / Product Marketing / Leadership) are tuned for a DTC e-commerce brand — rename or swap them to match your org.

## The workflow

Fill in the placeholders and paste this into your connected AI client:

```text
You are a CX Intelligence Analyst. Generate a weekly CX Intelligence Digest for
{{BRAND_NAME}} using support data from our connected Gorgias helpdesk. [If a Notion
connector is available: publish the result as a new Notion page under {{PARENT_PAGE}};
otherwise return it as formatted markdown.]

Data scope & rules
- Window: the last 7 days ({{START_DATE}} → {{END_DATE}}). State the window explicitly.
- Source of truth: Gorgias only. Pull non-spam tickets, intents/tags, channel, AI Agent
  handover vs. resolution status, sentiment tags, and CSAT responses.
- No invented data. Every number must trace to Gorgias. Where a figure comes from keyword
  or tag matching rather than a structured field, label it (heuristic).
- Redact PII in all customer quotes (names, emails, order numbers, addresses).
- Note any metric with too small a sample to be reliable (e.g. CSAT under ~30 responses)
  instead of reporting it as fact.
- Classify every signal with a status emoji so trends are visible at a glance:
  🟢 emerging (new or accelerating this week), 🔵 existing (recurring / tracked),
  🟡 fading (declining vs. recent weeks). If only a single week of data is available,
  infer status directionally from this week's volume and language, and say so.

Structure to produce (keep this exact skeleton)
1. Top callout — "TLDR: top 5 learnings this week (all functions)": a highlighted callout
   with exactly 5 bullets synthesizing the single most important learning across every
   function. Lead each bullet with a bolded takeaway, then the supporting number.
   Prioritize risk, revenue, and the AI automation gap.
2. "Week at a glance" — short bulleted overview: Volume (total non-spam + top 5 intents
   with counts); Channels (volume per channel + % AI-handled); AI Agent (tickets touched,
   # and % handed to human, # and % fully resolved); Sentiment flags (negative/urgent tag
   counts; CSAT note); #1 risk signal of the week.
3. Five department sections, each a collapsible toggle:
   🛠️ 1. Product — Recurring customer pain report
   📣 2. Marketing — Voice of customer insights
   🛒 3. Ecommerce / Revenue — Shopper friction report
   📚 4. Product Marketing — Feature confusion & enablement gaps
   🧭 5. Leadership — Weekly CX intelligence summary
   Inside each section, use these blocks in order:
   - What we learned — 4–6 tight bullets with key signals and figures (labeled (heuristic)
     where relevant). Prefix each bullet with its status emoji (🟢 / 🔵 / 🟡) and add a
     one-line status key under the heading. End with an italic one-line volume/impact summary.
   - What we should do — action items as to-do checkboxes (- [ ]), each a bolded action +
     one line of rationale.
   - What customers said & source tickets (redacted) — 3–5 representative verbatim quotes,
     each under ~25 words, with the source Gorgias ticket linked inline at the end of each
     quote. If two quotes share a ticket, link both; if a relevant ticket has no quote, list
     it as an italic "Also relevant:" line.
4. Two section-specific additions:
   - In Ecommerce / Revenue, after "What we should do," add a table titled "Products needing
     better PDP descriptions" with columns: Product | Gap in current PDP | What to add |
     Priority. Populate only from products actually referenced in this week's conversations.
   - In Leadership, lead with a signal status legend (🟢 emerging · 🔵 existing · 🟡 fading),
     then split signals into three labeled lists — "Emerging signals" 🟢, "Existing signals" 🔵,
     and "Fading signals" 🟡 — each bullet prefixed with its emoji.
5. Footer — "✅ Top cross-functional actions for this week": a collapsible toggle with the 5
   highest-priority actions across all functions, each with a named Owner (e.g. CX Leadership,
   Product/Engineering, Ecommerce, Product Marketing, AI Agent Ops). Close with an italic
   methodology note explaining (heuristic) figures, the CSAT caveat, spam exclusion, and the
   date window.

Tone & formatting
- Crisp and executive. Bullets over paragraphs. No filler.
- Bold the takeaway in each bullet; keep supporting detail to one clause.
- Spell out terms in full (e.g. "success rate," not abbreviations).
- Make department sections collapsible toggles so the page scans top-to-bottom from the callout.
```

## What it writes

- **Gorgias:** nothing — read-only.
- **Notion (optional):** if you provide `{{PARENT_PAGE}}` and have the Notion connector enabled, it publishes the digest as a new page. Otherwise it returns formatted markdown you can paste anywhere.

## Tips

- **Run it weekly.** Save it as a scheduled task and only update the date window each run.
- **The trust rules are load-bearing.** "No invented data" and the `(heuristic)` labels are what make leadership believe the numbers — keep them in any variant.
- **Single-week caveat:** the 🟢/🟡 status calls are directional until you feed it multi-week data. For true trends, run it against several weeks and ask it to compare.
- Pair with [`intent-gap-guidance`](../intent-gap-guidance/): the recurring pains this surfaces are exactly what your AI Agent should learn to handle next.
