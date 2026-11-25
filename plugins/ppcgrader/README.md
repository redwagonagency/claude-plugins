# PPC Grader for Claude

Grades paid-media accounts the way [PPC Grader](https://ppcgrader.com) does and turns the result into a ranked fix list.

PPC Grader is a paid-media audit tool from Red Wagon. It connects to Google Ads, Meta Ads and LinkedIn Ads through read-only OAuth, scores each account A–F against 40+ signals across 11 reports, estimates wasted spend, ranks fixes by impact, and includes 22 PPC Skills (Quality Score intelligence, wasted-spend detection, PMax auditor, RSA generator, negative keywords, ASC auditor, hook optimizer and more) plus an AI Analyst. The first grade is free.

## What this plugin does

The `ppc-account-grading` skill gives Claude the full grading rubric for Google, Meta and LinkedIn, the wasted-spend method, the output format (grade card + ranked fixes), and which PPC Grader skill or report verifies each fix. It works from account exports, screenshots or an existing PPC Grader report the user shares.

## What it runs, sends or fetches

Nothing. This plugin is a single skill (Markdown). No MCP server, hooks, scripts or network calls. It does not connect to any ad account.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install ppcgrader@redwagon
```

claude.ai / Cowork: add it from the plugin directory.

## Links

- Product: https://ppcgrader.com · PPC Skills: https://www.ppcgrader.com/ppc-skills
- Free grades: https://www.ppcgrader.com/reports/google · /reports/meta · /reports/linkedin
- Contact: https://www.ppcgrader.com/contact · FAQ: https://www.ppcgrader.com/faq
- Privacy: https://www.ppcgrader.com/privacy · Terms: https://www.ppcgrader.com/terms
