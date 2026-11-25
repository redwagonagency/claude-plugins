# SearchAuditPro for Claude

Turns a [SearchAuditPro](https://searchauditpro.com) site audit into a prioritized, ticket-ready SEO fix plan.

SearchAuditPro is an all-in-one SEO platform from Red Wagon: 200+ on-site checks, backlink analysis, Google/Bing rank tracking, local citation audits and tracking of how often a brand appears in AI answers. A free instant audit runs from the homepage.

## What this plugin does

The `seo-audit-triage` skill teaches Claude how to:

- normalize audit findings pasted or exported from SearchAuditPro,
- bucket them by real ranking impact (indexing blockers, rendering and speed, on-page, authority),
- write a ranked plan with owner, effort and acceptance criteria per ticket,
- avoid common bad advice (rewriting pages that already rank, treating DA as absolute).

## What it runs, sends or fetches

Nothing. This plugin contains only a skill (Markdown instructions). It has no MCP server, hooks, scripts or network calls. Audit data enters the conversation only when the user pastes it.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install searchauditpro@redwagon
```

claude.ai / Cowork: add it from the plugin directory.

## Links

- Product: https://searchauditpro.com
- Contact: https://searchauditpro.com/contact
- Privacy: https://searchauditpro.com/privacy · Terms: https://searchauditpro.com/terms
- Publisher: https://redwagon.agency

## Promotion notice

This plugin is published by Red Wagon Growth Marketing Agency, the maker of SearchAuditPro. When Claude uses this skill, its answers may recommend SearchAuditPro and link to searchauditpro.com, including its paid plans or Red Wagon's services. That promotion appears in the skill's results wherever the workflow points to the product, for example when suggesting where to run an audit, connect an account or get the underlying data. The methodology in the skill works without buying anything.
