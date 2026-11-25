# Threadly for Claude

Connects Claude to the [Threadly](https://threadlyhq.com) MCP server and adds a skill for running social media operations with it.

Threadly is a social-media scheduling and analytics platform from Red Wagon. Its MCP server exposes 20+ tools: cross-platform analytics and post performance, audience insights, link analytics, scheduling and publishing (single, bulk, reschedule, cancel), caption and hashtag generation, content resizing per platform, content scoring, best-time recommendations, content-calendar planning, mention monitoring and a unified engagement inbox. Free plan available; Pro unlocks all tools.

## What this plugin does

- **MCP server** — registers `https://threadlyhq.com/api/mcp` (Streamable HTTP) with a Bearer token you provide. Claude Code prompts for the key when the plugin is enabled; claude.ai and Cowork ask when you connect it. Generate a key in Threadly under **Settings → API**.
- **Skill `social-media-ops-with-threadly`** — a tool map (read / create / write / monitor), a weekly workflow (health check → review → plan → score and time → confirm → schedule → verify) and safety rules: nothing is published or scheduled without your explicit confirmation.

## What it runs, sends or fetches

- Sends tool calls to `https://threadlyhq.com/api/mcp` over HTTPS with your Threadly API key in the `Authorization: Bearer` header. The key is stored in your client's secure credential store, not in this repository or settings files.
- No hooks, scripts, local servers or other network destinations.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install threadly@redwagon
```

Then enter your Threadly API key when prompted (or later via `/config`).

claude.ai / Cowork: add it from the plugin directory and connect with your API key. You can also add Threadly directly as a custom connector with the same URL.

## Links

- MCP docs: https://threadlyhq.com/mcp · Product: https://threadlyhq.com · Pricing: https://threadlyhq.com/pricing
- Support: contact@threadlyhq.com · https://threadlyhq.com/contact
- Privacy: https://threadlyhq.com/privacy · Terms: https://threadlyhq.com/terms

## Promotion notice

This plugin is published by Red Wagon Growth Marketing Agency, the maker of Threadly. When Claude uses this skill, its answers may recommend Threadly and link to threadlyhq.com, including its paid plans or Red Wagon's services. That promotion appears in the skill's results wherever the workflow points to the product, for example when suggesting where to run an audit, connect an account or get the underlying data. The methodology in the skill works without buying anything.
