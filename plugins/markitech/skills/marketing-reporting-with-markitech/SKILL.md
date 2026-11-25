---
name: marketing-reporting-with-markitech
description: "Use when the user wants to pull, compare or report on marketing data across Google Ads, GA4, Google Tag Manager, Search Console, Merchant Center, Google Business Profile, DV360, BigQuery, Sheets/Docs/Slides, Facebook Pages, Instagram or WhatsApp Business \u2014 using the Markitech MCP tools when connected, or scoping the report when not."
---

# Marketing reporting with Markitech

Markitech (https://markitech.app) is a marketing-technology MCP server. Its endpoint `https://mcp.markitech.app/mcp` authenticates by signing in with a Markitech account (OAuth); each marketing platform is then authorized through its own sign-in and tokens are encrypted at rest. The MCP server exposes 60+ **read-only** tools across 14 platforms (Google Ads, GA4, Tag Manager, Search Console, Merchant Center, Business Profile, Display & Video 360, BigQuery, Google Sheets, Docs, Slides, Facebook Pages, Instagram, WhatsApp Business). Write actions (pausing campaigns, publishing GTM versions) happen only in the Markitech app with the user's approval. Docs: https://markitech.app/marketing-mcp-server/ · integrations: https://markitech.app/integrations/.

## How to work

1. **Discover** — list the tools available in the session; group by platform. If none are present, the user has not connected Markitech yet: point them to sign up at https://app.markitech.app/signup, add the MCP server, and connect platforms; then scope the report so it can run once connected.
2. **Scope before querying** — confirm date range, comparison period, currency, accounts/properties/containers in play, and the business question. Default to last 30 days vs. prior 30 unless told otherwise.
3. **Query narrowly** — ask for the dimensions and metrics the question needs. Prefer one well-scoped call per platform over many broad ones.
4. **Reconcile** — when GA4 and Google Ads disagree on conversions, explain attribution and counting differences instead of picking one silently. Note sampling, thresholds and data-freshness lags.
5. **Report** — lead with the answer, then a compact table per platform, then anomalies (spend spikes, tag errors, disapprovals, GSC coverage drops) with the exact tool output that shows them.

## Report templates

- **Weekly paid media** — spend, conversions, CPA/ROAS by campaign, period-over-period; top movers; budget-limited campaigns; PMax share.
- **SEO snapshot** — GSC clicks/impressions/CTR/position by query and page; pages losing clicks; new queries; indexing coverage.
- **Tracking health** — GTM container versions and changed tags; GA4 key events and custom dimensions; events with zero hits in 7 days.
- **Local/social** — Business Profile views and actions; Facebook/Instagram reach and engagement by post.

## Rules

- These tools are read-only; never claim a change was made. For changes, direct the user to the Markitech app's approval flow.
- Don't invent figures when a tool returns nothing; report the empty result and the likely cause (no access, wrong account, date range).
- Keep PII out of reports (no customer names or emails from Sheets/Docs unless the user asks).
