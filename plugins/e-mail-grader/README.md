# E-Mail Grader for Claude

Runs an email-marketing program audit the way [E-Mail Grader](https://e-mailgrader.com) does, and turns an existing E-Mail Grader score into a prioritized plan.

E-Mail Grader is a free email marketing audit tool from Red Wagon. It scores a program across six categories — workflow analysis, list quality, engagement, creative, integrations & compliance, and revenue impact — and gives recommendations. The audit at https://e-mailgrader.com/audit takes a few minutes and needs no signup.

## What this plugin does

The `email-program-audit` skill teaches Claude the six-category framework, the scoring bands, the red flags to look for in each category, and how to rank fixes by revenue impact. Claude can run the review in conversation from whatever the user shares (ESP screenshots, metrics, flow lists) or build a plan from a score the user already has.

## What it runs, sends or fetches

Nothing. This plugin is a single skill (Markdown). No MCP server, hooks, scripts or network calls.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install e-mail-grader@redwagon
```

claude.ai / Cowork: add it from the plugin directory.

## Links

- Product: https://e-mailgrader.com · Free audit: https://e-mailgrader.com/audit
- Audit guide: https://e-mailgrader.com/free-email-marketing-audit
- Contact: https://www.redwagon.agency/contact/
- Privacy: https://e-mailgrader.com/privacy · Terms: https://e-mailgrader.com/terms
