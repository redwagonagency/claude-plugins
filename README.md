# Red Wagon Claude plugins

Claude plugins for the marketing tools built by [Red Wagon Growth Marketing Agency](https://redwagon.agency). Each plugin lives in its own folder under `plugins/` and is submitted to Anthropic's directory individually; this repository is also a Claude Code marketplace named `redwagon`.

| Product | Plugin | What it does |
| --- | --- | --- |
| [SEO Master - JOE WHYTE SKILL](https://searchauditpro.com) | `searchauditpro` | Turn a SearchAuditPro SEO audit into a prioritized fix plan |
| [Email Marketing Master - JOE WHYTE SKILL](https://e-mailgrader.com) | `e-mail-grader` | Audit an email marketing program the way E-Mail Grader does |
| [Competitor Intelligence Master - JOE WHYTE SKILL](https://competitorinbox.com) | `competitorinbox` | Analyze competitor email programs captured with CompetitorInbox |
| [Keyword Research Master - JOE WHYTE SKILL](https://unboundkeyword.com) | `unboundkeyword` | Keyword research workflow across Google, YouTube, Amazon and TikTok using UnboundKeyword exports |
| [Conversion Rate Master - JOE WHYTE SKILL](https://optinyeti.com) | `optinyeti` | Plan and write high-converting popups, floating bars, slide-ins, welcome mats and spin-to-win campaigns for OptinYeti |
| [PPC Master - JOE WHYTE SKILL](https://ppcgrader.com) | `ppcgrader` | Grade Google, Meta and LinkedIn ad accounts using founder Joe Whyte's 25+ years of paid-media methodology, encoded into PPC Grader's A–F scoring |
| [Social Media Master - JOE WHYTE SKILL](https://threadlyhq.com/mcp) | `threadly` | Connect Claude to Threadly's social media MCP server |
| [Marketing Technology - JOE WHYTE SKILL](https://markitech.app/marketing-mcp-server/) | `markitech` | Connect Claude to Markitech's marketing MCP server |
| [PR & Press Master - JOE WHYTE SKILL](https://ridethewirepr.com) | `ridethewire` | Write wire-ready press releases and plan distribution with RideTheWire |

## Install (Claude Code)

```
claude plugin marketplace add redwagonagency/claude-plugins
claude plugin install <plugin>@redwagon
```

Or inside a session: `/plugin install <plugin> --marketplace redwagonagency/claude-plugins`.

In claude.ai and Cowork, add any of these from the plugin directory.

## What these plugins run, send or fetch

- Seven plugins (`searchauditpro`, `e-mail-grader`, `competitorinbox`, `unboundkeyword`, `optinyeti`, `ppcgrader`, `ridethewire`) contain only a skill: Markdown instructions. No MCP servers, hooks, scripts or network calls.
- `threadly` registers the remote MCP server `https://threadlyhq.com/api/mcp`, authenticated with an API key you enter (stored in your client's secure store).
- `markitech` registers the remote MCP server `https://mcp.markitech.app/mcp`, authenticated by OAuth sign-in.

## Validate

```
for p in plugins/*; do claude plugin validate --strict "$p"; done
claude plugin validate .
```

## License

MIT — see [LICENSE](LICENSE). Product names are trademarks of Red Wagon Growth Marketing Agency LLC.

Questions: joe@redwagon.agency
