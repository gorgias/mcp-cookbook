# Contributing a recipe

Found a Gorgias MCP workflow that saved you real time? Share it. The best recipes here come from people running actual support operations, not from us guessing.

## What makes a good recipe

A recipe is a **playbook you adapt**, not a feature of the product. Before you write one, check it fits:

- ✅ **It's a process.** Multiple steps, or something you run on a cadence.
- ✅ **It has variables.** Things the next person must swap in — their tags, thresholds, policies. If there's nothing to customize, it's probably just a prompt (add it to the README's "What can I just ask it?" list instead).
- ✅ **It leans on the MCP, doesn't re-explain it.** Don't document how Guidance or Macros work — the MCP already knows. Show *what to do* with them.
- ❌ **Not a product mechanic or a one-liner.** Single questions like *"summarize my low-CSAT tickets"* belong in the README prompt list, not as a recipe.

## How to add one

1. Copy [`recipes/_template/SKILL.md`](recipes/_template/SKILL.md) to `recipes/your-recipe-name/SKILL.md`.
2. Fill in every section. Mark customizable values clearly with `{{DOUBLE_BRACES}}`.
3. Be explicit about **what it writes** to the account. If it creates or changes anything, say so — and make sure the workflow creates **drafts** or asks for confirmation. Never write a recipe that publishes or sends without a human in the loop.
4. Add a row to the recipe table in [`README.md`](README.md).
5. Open a pull request describing the problem it solves and roughly how much time it saves.

## Style

- Write to a busy merchant, not a developer.
- Lead with the outcome, not the mechanism.
- Keep it skimmable — short sections, a clear workflow block they can paste.
- Cross-link related recipes where it helps (`[name](../name/)`).

## A note on safety

Everything here can run against a live production account. Recipes that write **must** keep the user in control: drafts over publishes, confirmation over silent action, narrow scope over "all tickets." When in doubt, make it read-only and let the user opt into writes.
