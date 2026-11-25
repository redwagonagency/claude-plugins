# UnboundKeyword for Claude

A keyword-research workflow for data from [UnboundKeyword](https://unboundkeyword.com): clean, label intent, cluster, map to content and prioritize.

UnboundKeyword is a cross-platform keyword research tool from Red Wagon. It surfaces keyword ideas from Google, YouTube, Amazon and TikTok, with question discovery, an A–Z explorer, autocomplete and People-Also-Ask insights, competitor gap, Google Search Console integration, LLM-visibility checks and CSV-exportable keyword lists. Starting is free.

## What this plugin does

The `keyword-research-workflow` skill gives Claude a six-step process — collect, clean, label intent, cluster, build a content map, prioritize — with explicit rules for platform-specific keywords, zero-volume questions and striking-distance GSC terms. It works from UnboundKeyword CSV exports or any pasted keyword list.

## What it runs, sends or fetches

Nothing. This plugin is a single skill (Markdown). No MCP server, hooks, scripts or network calls.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install unboundkeyword@redwagon
```

claude.ai / Cowork: add it from the plugin directory.

## Links

- Product: https://unboundkeyword.com
- Contact: https://unboundkeyword.com/contact
- Privacy: https://unboundkeyword.com/privacy · Terms: https://unboundkeyword.com/terms
