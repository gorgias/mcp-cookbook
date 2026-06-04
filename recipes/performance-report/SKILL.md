---
name: performance-report
description: >-
  Generate a shareable support performance report for your team or leadership —
  volume, automation rate, top intents, CSAT, and trends — formatted for a Slack
  post or doc. Read-only. Best-effort while analytics are in beta.
---

# Shareable Performance Report

Pulling together a support recap every month is busywork. This recipe assembles the numbers and the story into something you can paste straight into Slack or a doc — no spreadsheet wrangling. Read-only.

> **Heads up:** Gorgias MCP analytics are in **beta**. Figures here are directional and may differ slightly from your in-product Statistics dashboard. Use it for narrative and trends, and cross-check exact numbers in Statistics before reporting them up.

## When to use it

- Monthly/quarterly support recap for leadership
- A weekly team pulse-check
- Building the support slide for a wider business review

## Customize before you run

| Variable | Example |
|---|---|
| `{{PERIOD}}` | "May 2026" |
| `{{COMPARE_TO}}` | "vs April 2026" |
| `{{METRICS}}` | "volume, automation rate, CSAT, first response time, top 5 intents" |
| `{{AUDIENCE}}` | "leadership" — sets tone and depth |
| `{{FORMAT}}` | "a Slack post" or "a one-page summary" |

## The workflow

> Build a support performance report for **{{PERIOD}}** ({{COMPARE_TO}}), for **{{AUDIENCE}}**, formatted as **{{FORMAT}}**.
>
> 1. **Headline metrics:** {{METRICS}}. Show each with the change vs the comparison period.
> 2. **What drove volume:** the top contact reasons, and any notable shifts.
> 3. **AI Agent impact:** automation rate and where it's helping most / struggling most.
> 4. **One win and one watch-item** for the period.
> 5. Add the disclaimer that figures are directional pending the in-product dashboard.
>
> Keep it tight and skimmable — numbers with a one-line "so what" each, not a wall of stats.

## What it writes

Nothing. Read-only.

## Tips

- Ask for an **HTML version** if you want something more visual to share — the AI Agent can produce a clean, styled report.
- Lock the structure once you like it and reuse it every period — consistency makes trends legible.
- For exact, board-ready numbers, pull from your Statistics dashboard; use this for the narrative around them.
