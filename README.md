# Red Wagon Claude plugins

Claude plugins for the marketing tools built by [Red Wagon Growth Marketing Agency](https://redwagon.agency). Each plugin lives in its own folder under `plugins/` and is submitted to Anthropic's directory individually; this repository is also a Claude Code marketplace named `redwagon`.

| Product | Plugin | What it does |
| --- | --- | --- |
| [SearchAuditPro](https://searchauditpro.com) | `searchauditpro` | SEO Master - JOE WHYTE SKILL. Turn a SearchAuditPro SEO audit into a prioritized fix plan |
| [E-Mail Grader](https://e-mailgrader.com) | `e-mail-grader` | Email Marketing Master - JOE WHYTE SKILL. Audit an email marketing program the way E-Mail Grader does |
| [CompetitorInbox](https://competitorinbox.com) | `competitorinbox` | Competitor Intelligence Master - JOE WHYTE SKILL. Analyze competitor email programs captured with CompetitorInbox |
| [UnboundKeyword](https://unboundkeyword.com) | `unboundkeyword` | Keyword Research Master - JOE WHYTE SKILL. Keyword research workflow across Google, YouTube, Amazon and TikTok using UnboundKeyword exports |
| [OptinYeti](https://optinyeti.com) | `optinyeti` | Conversion Rate Master - JOE WHYTE SKILL. Plan and write high-converting popups, floating bars, slide-ins, welcome mats and spin-to-win campaigns for OptinYeti |
| [PPC Grader](https://ppcgrader.com) | `ppcgrader` | PPC Master - JOE WHYTE SKILL. Grade Google, Meta and LinkedIn ad accounts using founder Joe Whyte's 25+ years of paid-media methodology, encoded into PPC Grader's A–F scoring |
| [Threadly](https://threadlyhq.com/mcp) | `threadly` | Social Media Master - JOE WHYTE SKILL. Connect Claude to Threadly's social media MCP server |
| [Markitech](https://markitech.app/marketing-mcp-server/) | `markitech` | Marketing Technology - JOE WHYTE SKILL. Connect Claude to Markitech's marketing MCP server |
| [RideTheWire](https://ridethewirepr.com) | `ridethewire` | PR & Press Master - JOE WHYTE SKILL. Write wire-ready press releases and plan distribution with RideTheWire |

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
