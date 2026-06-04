# Prompt library — what to ask the Gorgias MCP

A browsable list of questions and tasks you can copy/paste into your connected AI client (Claude, ChatGPT, Cursor). No setup beyond [connecting the MCP](https://docs.gorgias.com/en-US/connect-your-ai-assistant-to-gorgias-6310546).

**How to use this:** find your goal below, copy a prompt, and replace anything in `[brackets]` with your own values. Start simple — these are single-shot asks. For multi-step, repeatable workflows, see the [recipes](recipes/).

> **If you have other tools connected** (Shopify, a data warehouse, etc.), Claude may not know which one to use — questions like *"what are my top products?"* are ambiguous. Start your message with **"Using the Gorgias MCP, …"** to point it at the right place.

> **A note on analytics:** sections marked _**(beta — directional)**_ rely on analytics that are still in beta. Numbers may differ slightly from your in-product Statistics dashboard — great for spotting trends, but cross-check exact figures before reporting them up.

---

## 🚀 Set up & improve your AI Agent
*For whoever owns AI Agent — CX leads, support managers.*

- "Audit my AI Agent setup and flag any handover conditions that seem too broad or likely to cause unnecessary escalations."
- "Review my AI Agent Guidance and draft improvements for the 3 weakest entries."
- "Simulate how my AI Agent would respond to this before I enable it: [paste a customer message]."
- "Are there topics my customers ask about that my AI Agent isn't configured to handle?"
- "In ticket #[number] the AI Agent didn't respond correctly — help me find why and fix it."
- "Which topics is my AI Agent handing over that it could safely handle? Adjust my handover settings."
- "Convert my existing Flows into AI Agent Guidance."
- "Generate a tone of voice for my AI Agent from the style of my website, then apply it."
- "Where am I in my AI Agent rollout, and what are the 3 highest-impact things to do next?"

## 🗣️ Understand your customers (Voice of Customer)
*For CX leads and product teams who want the signal hiding in tickets.*

- "What are the top reasons customers contacted us this month? Group them by theme."
- "Summarize the most common complaints from low-CSAT tickets in the past 30 days."
- "What products are customers asking us to restock most often?"
- "Find patterns in tickets tagged 'returns' and tell me the reasons customers give."
- "Are there recurring frustrations in tickets that aren't captured by any of my current tags?"
- "Which issues generate the most repeat contacts — where customers write in more than once?"
- "What changed in customer questions after [our launch / price change / policy update]?"
- "Pull 10 verbatim quotes that capture how customers feel about [topic]."

## 🎫 Run the helpdesk day-to-day
*For agents and team leads working the queue.*

- "Find all open tickets tagged '[tag]' and summarize what customers are asking for."
- "Post an internal note on ticket #[number] flagging it for the fulfillment team."
- "Update all tickets from the last 24h that mention [issue] to priority: urgent."
- "Reply to ticket #[number] letting the customer know their order shipped, then close it."
- "Draft a reply to ticket #[number] using the order details on the customer's account."
- "Which tickets have been open longest without a reply? Group them by what the customer needs."
- "Apply the [macro name] macro to all open tickets about [topic]."

## 🧹 Keep your helpdesk clean
*For admins keeping the setup from rotting as it grows.*

- "Review my tag taxonomy and flag tags that are redundant, inconsistently named, or rarely used."
- "Find macros that haven't been used in the last 90 days and suggest which to update or retire."
- "Check if any agents have permissions that don't match their current role."
- "Are there gaps in my helpdesk rules that could let tickets fall through the cracks?"
- "List every Macro, Guidance, and rule that mentions [old policy] so I can update them."

## 🛍️ Shopping Assistant & pre-sales _**(beta — directional)**_
*For growth, merchandising, and e-commerce owners — the revenue side of support.*

- "What are my most recommended products?"
- "Which product pages result in the most conversations started?"
- "What products are most commonly recommended together?"
- "What is the purchase rate per product recommendation pair made by Shopping Assistant?"
- "What is the revenue per Shopping Assistant conversation?"
- "What is the time-to-purchase after a recommendation?"
- "Which paired recommendation converts best?"
- "What are the biggest handover reasons for pre-sales conversations, and how often does each occur?"
- "What pre-sales topics do customers ask about most frequently?"
- "Which products generate the most pre-sales questions before customers buy?"
- "What objections or hesitations come up most often before a purchase?"
- "Are there products customers keep asking about that Shopping Assistant isn't surfacing?"

> Want this as a repeatable monthly read? See the [`shopping-assistant-performance`](recipes/shopping-assistant-performance/) recipe.

## 💸 Revenue & conversion _**(beta — directional)**_
*For owners and growth leads connecting support to the bottom line.*

- "Which support topics are most associated with customers who go on to purchase?"
- "What's the revenue impact of conversations my AI Agent handled vs. handed over?"
- "Find my highest-spending customers who had a poor support experience this month."
- "Which products drive the most post-purchase tickets relative to their sales volume?"
- "Are returns concentrated in specific products or variants? Show me the worst offenders."

## 🧵 Merchandising & catalog _(some figures heuristic)_
*For merchandising and buying teams turning support signal into better products and pages.*

- "Which products generate the most pre-sales questions, and what are shoppers unsure about?"
- "What's missing from my [product] page that customers keep asking support about?"
- "Why are customers returning [product]? Cluster the reasons."
- "Which products have the biggest gap between how they're described online and what customers expected?"
- "What sizing or fit issues come up most often, and for which products?"
- "Are there product defects or quality complaints I should flag to my buying team?"
- "Which products drive the most post-purchase tickets relative to how well they sell?"

> Want this as a repeatable workflow? See the [`pdp-gap-finder`](recipes/pdp-gap-finder/) and [`returns-reduction`](recipes/returns-reduction/) recipes.

## 📊 Reporting & team updates
*For anyone who has to report support performance up or out.*

- "Build a support performance recap for [month] vs the previous month, formatted for a Slack post."
- "What's my automation rate this month, and how is it trending?"
- "Generate a clean HTML report of this month's support KPIs I can share with my team."
- "Summarize this week in support in 5 bullets for our standup."
- "What's the one metric that moved the most this period, and why?"

---

## Don't see your use case?

These are starting points, not a fixed menu — the MCP works in natural language, so ask for what you actually need. If you build a great multi-step workflow, consider [contributing it as a recipe](CONTRIBUTING.md).
