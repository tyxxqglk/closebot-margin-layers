# white label chatbot pricing: what you actually pay per client, where markup gets eaten, and how to keep a real margin

Agencies searching for white label chatbot pricing are usually trying to answer a specific question, not a philosophical one: if I resell AI agents to ten clients, what does that cost me each month, and what's left over?

The hard part is that most platforms publish one number and hide the rest. A $89/month widget plan and a $397/month agency plan look comparable on a pricing page and end up wildly different once you add message costs, client seats, knowledge storage, and the CRM the whole thing runs on.

This piece breaks the cost layers apart, then walks through one platform's published numbers in detail — CloseBot's — because it's an agency-first product with a public pricing breakdown, including the rebilling setup that determines your margin.

## The four cost layers hiding behind one monthly price

Almost every white label chatbot quote is built from the same pieces. The order matters, because the second and third layers are where margins go to die.

1. **Platform fee** — the subscription itself. This buys you the builder, the client portal, and the right to put your logo on it.
2. **Usage** — messages, tokens, credits, or minutes. Sometimes included in the plan, sometimes metered separately.
3. **Seats** — every human who logs in, whether that's your builder or the client checking their dashboard.
4. **Storage and channels** — knowledge base files (often billed by the MB, sometimes per day), plus carrier or Meta fees if SMS and WhatsApp are involved.

Two questions separate a cheap platform from a profitable one. Does the plan let you rebill usage to your client at your own markup? And does the client portal carry your brand, or does your client see the vendor's logo the moment they log in?

A platform that's $100 cheaper per month but doesn't let you rebill usage is usually the more expensive choice by client number three.

## CloseBot's published pricing, plan by plan

CloseBot's plans page splits into two tracks: business plans for companies using agents on their own pipeline, and agency plans built around rebilling and white labeling. Same product, different commercial wrapper.

| Plan | Best for | What's included | Price | Billing | Get started |
| --- | --- | --- | --- | --- | --- |
| Free | Testing, or under 100 messages a month | 1 agent, 1 user seat, 1 MB knowledge storage, 100 monthly messages, unlimited account connections | $0 | Free forever while you stay under 100 messages/mo | [Start on the free plan](https://app.closebot.com/a?fpr=li87) |
| Core (Business) | Companies qualifying their own leads | Message costs included in the base price, 500 messages at base, 15+ templates, human support, add-on users at $5/seat, add-on storage and agents | From $64/mo monthly, from $53/mo billed annually ($640/yr) | Monthly or annual, month to month, no contract | [Check the business plans](https://app.closebot.com/a?fpr=li87) |
| Core (Agency) | Agencies reselling AI agents to clients | Unlimited agents and sources, white label client portal, rebill all costs, $0.012/message rebillable, client seats $5, storage $0.006/MB/day | $397/mo monthly, around $331/mo on annual billing | Monthly or annual, 7-day trial of the paid plan | [See the agency plan](https://app.closebot.com/a?fpr=li87) |
| Growth | High volume, regulated industries, SLAs | HIPAA compliant, quarterly audits, 99.99% priority uptime, priority support, 50+ templates | Custom quote | Custom | [Talk to sales about Growth](https://app.closebot.com/a?fpr=li87) |

The business track scales by monthly message volume rather than by agent count. Published tiers move from $64/mo at the entry level to roughly $84 at 1,000 messages, $109 at 2,000, and $176 at 5,000, with the pricing calculator on the plans page showing the exact figure for your configuration. Above that, you're into the hundreds per month.

The agency track is deliberately flat at $397/month. Unlimited agents, unlimited client accounts, and usage billed at $0.012 per message, all rebillable.

> CloseBot states plainly that there are no refunds. What you get instead is a free plan that stays free under 100 messages a month and a 7-day trial on any paid plan, with plans running month to month and no contract.

## What the $397 agency plan is really pricing

If you're already paying for a CRM, comparing a $397 agency subscription against a $89 widget plan is the wrong comparison. The agency plan buys three things that competitor plans generally don't bundle.

**A branded client portal.** Clients log in and see your name and domain, their dashboards, message counts, and charges. They don't see agent logic or instructions, which keeps your build from becoming your client's next DIY project.

**Rebilling through Stripe.** CloseBot's docs walk through connecting a Stripe account, then setting your own markup for message responses, user seats, and storage. Their example configuration rebills messages at $0.02, seats at $100, and storage at $0.05 — those are example rates, not fixed ones. You set the number.

**Rebillable costs across the board.** The $5 per client seat and the $0.006 per MB per day of knowledge storage can both be marked up. Client seats are billed hourly at $0.0069, which comes to about $5/month per user and adjusts automatically if someone is added or removed mid-month.

Run the arithmetic on a modest client: 5,000 AI messages a month costs you $60 at the $0.012 wholesale rate. Rebill the same 5,000 messages at $0.02 and the client pays $100. That's $40 of gross usage margin on one account, before you count seats or storage. Six quiet clients can cover the platform fee; six busy ones do considerably better. CloseBot's own marketing cites polled agencies billing an average of $500 per client per month, which is a vendor figure rather than an audited one, but it tells you what the pricing model is designed to support.

This is also why the business plan exists. On a business plan, message costs are baked into the subscription — no per-message charge unless you cross your included volume, at which point overages draw from a wallet. If you're the only user and the agent only works your own pipeline, paying for agency features you'll never touch is the more expensive route.

## The billing details that change the math

Three things about CloseBot's usage billing are worth reading before you quote clients, because they're the kind of details that turn a clean margin into an awkward conversation.

**A message is a segment.** One message equals one segment — unless you're using the Agent Node with unlimited potential switched on. Add a lot of tools and unlimited instruction size, and billing moves to token costs, meaning a single message can consume more than one segment. Build heavy agents and your per-message estimate needs a cushion.

**No bring-your-own API key.** CloseBot doesn't allow connecting your own OpenAI or Anthropic key, and explains the decision as a security and compliance choice. Your model spend lands inside the plan rather than on your own provider bill. Whether that's better or worse depends on your volume: it's simpler to forecast, and you can't shop around on model pricing.

**Free plan overages are $0.08 per message** on the free plan, which makes it a reasonable testing tier and a poor production tier. Which is the intended design.

CloseBot is also text-first. It takes over the messaging channels inside your CRM and, when needed, runs standalone. If a client needs voice agents, that's a separate line item from a different vendor — budget for it rather than assuming it's included.

## The subscription nobody puts in the comparison table

CloseBot integrates natively with HighLevel, HubSpot, LeadConnector, and custom CRMs, and it can also run without one. In practice, most agency deployments sit on top of a CRM the client is already paying for, but if you're bringing on a new client from scratch, the CRM is part of the total cost.

HighLevel's published plans start at $97/month for Starter, $297 for Unlimited, and $497 for Agency Pro. HubSpot's paid tiers are their own line item. So a solo business running around 1,000 AI messages a month is realistically looking at something like $84 for CloseBot plus $97 for the CRM, before any channel fees.

That's not an argument against CloseBot's pricing — the platform fee is what it is. It's an argument for quoting clients the full stack, because the moment you quote $150/month and forget the CRM underneath, the margin disappears.

## How CloseBot's platform fee compares on paper

Published list prices across the white label chatbot category vary by what "white label" means to each vendor. These are the vendors' own published starting points as of August 2026:

| Platform | Published starting point | White label depth |
| --- | --- | --- |
| Botpress Plus | $89/mo (or $79 annual), AI spend separate | Widget watermark removal; Studio and Dashboard stay branded |
| Stammer Agency | $197/mo, plus model-based message costs | Branded dashboard, domain, API, client resale |
| ConvoCore White Label | $199/mo, 60,000 credits, 20 client subaccounts | Branded dashboard, domain, client billing via Stripe |
| CloseBot Agency | $397/mo, $0.012/message rebillable | Branded client portal, rebilling, unlimited agents and sources |
| Tidio Partners (Tidio+) | Around $394/mo | White label within the partners program; Lyro AI and Flows billed separately |

Two honest notes. First, these vendors bill different units, so the headline numbers aren't direct substitutes — Stammer and ConvoCore charge model-based message costs on top, and Botpress bills AI spend at provider cost. Second, Botpress is explicit that its white label covers the end-user widget, not the builder your team works in. If a client needs to log into branded software with your logo on it, a widget-only white label doesn't solve that.

CloseBot sits at the top of the list on platform fee and near the bottom on per-message cost, which is the trade the agency plan is built around: a higher base price in exchange for rebillable usage, unlimited client accounts, and markup you control.

## Picking the right tier without overpaying

The free plan is genuinely usable for evaluation — 100 messages a month, one agent, unlimited account connections — and it's free forever at that volume. It won't support client work, but it will tell you in an afternoon whether the builder and the conversation quality fit how you sell.

Business plans make sense when the agent points at your own pipeline: one company, one or a few agents, message costs included. Pick the tier by monthly message volume, not by agent count, and remember the higher tiers unlock bulk message pricing.

The agency plan starts making sense around the point where you're handing over dashboards or invoices to someone else. Rebilling is the feature that pays for it — if you're not rebilling, you're paying $397 for capabilities you aren't using. The 7-day trial covers the agency plan specifically, which is the right way to test whether the Stripe rebilling setup and portal branding match how you invoice clients.

Growth is for the cases where "probably fine" isn't acceptable: HIPAA-covered workflows, quarterly audits, a 99.99% priority uptime commitment, and a contract with SLAs in it.

## Questions agencies ask before signing up

**Can I white label the client portal on the agency plan?**
Yes. The agency plan includes the white label client portal, and client seats see their own dashboards, message volume, and charges without access to your agent logic.

**Are message costs included or metered?**
Both exist, depending on the track. Business plans include message costs in the base price with wallet-based overage protection if you go over. Agency plans bill usage at $0.012 per message, which you rebill at your own markup.

**What happens if a heavy agent burns more than one segment per message?**
Using the Agent Node with unlimited potential switches a message to token-based billing, so one message can consume more than one segment. Budget conservatively for tool-heavy agents.

**Is there a contract?**
No. Plans run month to month, and you can upgrade, downgrade, or cancel at any time. There are also no refunds, which is why the 7-day trial and the free tier matter.

**How many client accounts can I run?**
The agency plan covers unlimited agents across unlimited sources, and account connections aren't capped on the free plan either. Seats, storage, and messages are the metered dimensions.

The general rule for white label chatbot pricing holds here: the platform fee is the visible number and rarely the deciding one. What decides your margin is whether usage is rebillable, what a seat costs you versus what you charge for it, and whether the CRM underneath is already in the client's budget. Get those three right and the $397 stops being an expense line. Get them wrong and you've bought yourself a nicer dashboard and a thinner month.
