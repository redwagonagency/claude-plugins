# Markitech for Claude

Connects Claude to the [Markitech](https://markitech.app) marketing MCP server and adds a skill for cross-platform marketing reporting.

Markitech is "one AI, every marketing platform": an MCP server with 60+ read-only tools across Google Ads, GA4, Google Tag Manager, Search Console, Merchant Center, Google Business Profile, Display & Video 360, BigQuery, Google Sheets/Docs/Slides, Facebook Pages, Instagram and WhatsApp Business. You sign in with a Markitech account, authorize each platform through its own OAuth, and ask questions in plain language. Write actions require approval inside the Markitech app.

## What this plugin does

- **MCP server** — registers `https://mcp.markitech.app/mcp` (Streamable HTTP). Authentication is OAuth sign-in with your Markitech account; no key is stored in the plugin.
- **Skill `marketing-reporting-with-markitech`** — a discover → scope → query → reconcile → report workflow, four report templates (weekly paid media, SEO snapshot, tracking health, local/social) and rules for read-only tools, empty results and PII.

## What it runs, sends or fetches

- Sends tool calls to `https://mcp.markitech.app/mcp` over HTTPS after you sign in through Markitech's OAuth flow.
- No hooks, scripts, local servers or other network destinations.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install markitech@redwagon
```

Sign in when Claude Code prompts for the server's authentication.

claude.ai / Cowork: add it from the plugin directory, or add `https://mcp.markitech.app/mcp` as a custom connector.

## Links

- MCP docs: https://markitech.app/marketing-mcp-server/ · Integrations: https://markitech.app/integrations/
- Sign up: https://app.markitech.app/signup · Pricing: https://markitech.app/#pricing
- Support: contact@markitech.app · Security: https://markitech.app/security/
- Privacy: https://markitech.app/privacy/ · Terms: https://markitech.app/terms/
