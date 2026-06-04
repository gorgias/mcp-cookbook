# Gorgias MCP Cookbook

> Ready-to-fork recipes for the [Gorgias MCP](https://mcp.gorgias.com) — automate your helpdesk and AI Agent from Claude, ChatGPT, or Cursor.

A collection of playbooks for getting more out of the Gorgias MCP. Each recipe is a **starting point, not a finished product** — copy it, swap in your own policies, tags, and thresholds, and run it. Connect once, then automate the support work you'd otherwise do by hand.

These recipes don't re-explain how Gorgias works — the MCP already knows that. They show you *what to do with it*.

---

## What is the Gorgias MCP?

The [Gorgias MCP](https://mcp.gorgias.com) is a first-party connector that plugs your Gorgias account into any AI client that speaks [MCP](https://modelcontextprotocol.io) — Claude, ChatGPT, Cursor, and more. Once connected, your AI assistant can read and act on your tickets, customers, tags, macros, knowledge (Guidance), Workflows, and AI Agent settings — all scoped to your account, via OAuth.

**Setup takes ~2 minutes.** See the [official install guide](https://docs.gorgias.com/en-US/connect-your-ai-assistant-to-gorgias-6310546).

```
https://mcp.gorgias.com/mcp
```

You'll be prompted for your subdomain, then sign in with your Gorgias credentials.

---

## Recipes

Each recipe lives in [`recipes/`](recipes/) as a self-contained `SKILL.md`. Copy the folder into your AI client's skills directory (e.g. `~/.claude/skills/`), or just paste the workflow into a chat. **Recipes are grouped by who gets the most out of them** — but many serve more than one team, so browse across.

### 🎧 For the CX / Support Lead
*Protect CSAT and SLA, automate the repetitive volume, prove CX is a value center.*

| Recipe | What it does | Writes? |
|---|---|---|
| [intent-gap-guidance](recipes/intent-gap-guidance/) | Find high-volume intents with no Guidance, and draft one for each | ✅ Drafts only |
| [monthly-helpdesk-hygiene](recipes/monthly-helpdesk-hygiene/) | Audit tags, stale macros, permissions, and rule gaps on a cadence | ❌ Suggests fixes |
| [policy-change-sweep](recipes/policy-change-sweep/) | Update every Guidance, Macro, and rule that references an old policy | ✅ You approve |
| [performance-report](recipes/performance-report/) | A shareable report of your support performance for leadership | ❌ Read-only |
| [weekly-voc-digest](recipes/weekly-voc-digest/) | A repeatable Voice-of-Customer report to feed the rest of the org | ❌ Read-only |

### 🛒 For the Ecommerce / Merchandising Lead
*Lift conversion and AOV, cut returns, and run pre-sales as a revenue channel.*

| Recipe | What it does | Writes? |
|---|---|---|
| [pdp-gap-finder](recipes/pdp-gap-finder/) | Find which products confuse shoppers and exactly what to add to each PDP | ❌ Read-only |
| [returns-reduction](recipes/returns-reduction/) | Cluster *why* customers return, by product, and fix the root cause | ❌ Read-only |
| [shopping-assistant-performance](recipes/shopping-assistant-performance/) | Read Shopping Assistant as a revenue channel — recommendations, conversion, revenue | ❌ Read-only |
| [seasonal-prep](recipes/seasonal-prep/) | Prep Guidance and Macros for a seasonal event (BFCM, holidays, sales) | ✅ Drafts only |
| [vip-at-risk](recipes/vip-at-risk/) | Surface high-value shoppers who had a bad experience, before you lose them | ❌ Read-only |

### 💌 For the Marketing / Retention Lead
*Turn support signal into segments, demand, and copy — repeat purchase, win-back, and messaging.*

| Recipe | What it does | Writes? |
|---|---|---|
| [winback-list-builder](recipes/winback-list-builder/) | Build a win-back segment from customers who hit a problem, ready for your ESP | ❌ Read-only |
| [restock-demand-list](recipes/restock-demand-list/) | Build a back-in-stock notify list, ranked by demand, from restock requests | ❌ Read-only |
| [voc-to-messaging](recipes/voc-to-messaging/) | Turn real customer language into ad angles, FAQ, and copy | ❌ Read-only |

### 🧭 For Leadership (cross-functional)
*One readout that turns support into company-wide intelligence.*

| Recipe | What it does | Writes? |
|---|---|---|
| [cx-intelligence-digest](recipes/cx-intelligence-digest/) | A weekly executive digest across 5 functions — TLDR, signal tagging, PDP-gap table, owner-tagged actions | ❌ Read-only (optional Notion publish) |

---

## What can I just *ask* it?

Most day-to-day tasks don't need a recipe — the MCP handles them from a single prompt. A few to get started:

- *"What are the top reasons customers contacted us this month? Group them by theme."*
- *"Audit my AI Agent setup and flag any handover conditions that seem too broad."*
- *"Find all open tickets tagged '[tag]' and summarize what customers are asking for."*
- *"Build a support performance recap for last month, formatted for a Slack post."*

👉 **See [PROMPTS.md](PROMPTS.md) for the full library** — 50+ questions organized by goal, from Voice-of-Customer and helpdesk ops to Shopping Assistant & revenue insights.

> **Tip:** if you have other tools connected (Shopify, a data warehouse, etc.), start your message with **"Using the Gorgias MCP, …"** so Claude knows which integration to use. The recipes already do this for you.

---

## Important

- **You're always in control.** Recipes that write to your account create **drafts** or **ask for confirmation** first. Nothing publishes or sends without your say-so. Review before you approve.
- **These are templates.** Every recipe has a *"Customize before you run"* section. Swapping in your real values (return windows, VIP thresholds, tags) is the whole point — don't run them blind.
- **Analytics are in beta.** Reporting recipes are best-effort and may differ slightly from your Statistics dashboard. Treat them as directional.

## Contributing

Got a workflow that saved you hours? We'd love to add it. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Questions & feedback

Open an [issue](https://github.com/gorgias/mcp-cookbook/issues), or reach out to your Gorgias contact.

## License

[MIT](LICENSE) — fork it, adapt it, ship it.
