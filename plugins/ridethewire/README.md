# RideTheWire for Claude

Writes wire-ready press releases and plans distribution through [RideTheWire](https://ridethewirepr.com).

RideTheWire is a press-release distribution service from Red Wagon: an editor reviews each release, it goes out to 100–650+ news sites depending on package (including guaranteed APNews.com and USAToday.com placement on the National package), and you get a shareable report listing every live placement link. A free Newsroom option publishes one release a month. Packages are per release, no subscription.

## What this plugin does

The `press-release-writing-and-distribution` skill gives Claude a qualification step (is it news?), an AP-style template, the word and link limits per RideTheWire package, image and style rules, a distribution plan by goal and budget, and a post-distribution checklist for the placement report.

## What it runs, sends or fetches

Nothing. This plugin is a single skill (Markdown). No MCP server, hooks, scripts or network calls. Submitting a release happens in your RideTheWire account.

## Install

Claude Code:

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install ridethewire@redwagon
```

claude.ai / Cowork: add it from the plugin directory.

## Links

- Product: https://ridethewirepr.com · Pricing: https://ridethewirepr.com/pricing · FAQ: https://ridethewirepr.com/faq
- Sales: sales@redwagon.agency
- Privacy: https://ridethewirepr.com/privacy · Terms: https://ridethewirepr.com/terms
