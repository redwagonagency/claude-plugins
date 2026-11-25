# CompetitorInbox for Claude

Analyzes competitor email programs captured with [CompetitorInbox](https://competitorinbox.com) and turns them into a scorecard, swipe file and playbook.

CompetitorInbox is a competitor email intelligence tool from Red Wagon. Each competitor gets a unique tracking address; subscribe to their lists with it and their emails are captured, searchable and analyzed — send-frequency heatmaps, subject-line patterns, CTA and preheader tactics, ESP detection, SPF/DKIM/DMARC scores, creative-change tracking and real-time alerts.

## What this plugin does

The `competitor-email-analysis` skill gives Claude a checklist for cadence, automated-flow reconstruction, subject-line and offer analysis, infrastructure checks and creative review, plus a fixed set of deliverables (scorecard, swipe file, playbook, alerts to set). It works from CompetitorInbox exports or from emails the user pastes.

## What it runs, sends or fetches

Nothing. This plugin is a single skill (Markdown). No MCP server, hooks, scripts or network calls.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install competitorinbox@redwagon
```

claude.ai / Cowork: add it from the plugin directory.

## Links

- Product: https://competitorinbox.com · Demo: https://competitorinbox.com/demo
- Knowledge base: https://competitorinbox.com/knowledge-base
- Support: support@competitorinbox.com
- Privacy: https://competitorinbox.com/privacy · Terms: https://competitorinbox.com/terms
