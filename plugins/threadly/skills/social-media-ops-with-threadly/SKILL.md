---
name: social-media-ops-with-threadly
description: "Use when the user wants to schedule, plan or analyze social media posts, build a content calendar, write captions or hashtags, or check connected social accounts and scheduled posts, using the Threadly MCP tools when connected, or planning the same workflow when not."
---

# Social media operations with Threadly

Threadly (https://threadlyhq.com) is a social-media scheduling and analytics platform. Its MCP server at `https://threadlyhq.com/api/mcp` exposes five tools. This plugin configures that server; the user supplies an API key generated in Threadly under Settings → API. MCP access requires a paid Threadly plan.

## Tool map

- **Read first:** `get_accounts` (connected social accounts and their status), `get_posts` (scheduled and published posts), `get_analytics` (performance for the connected accounts).
- **Write (confirm with the user before calling):** `schedule_post`, `delete_post`.

Check each tool's input schema in the session before calling it; do not assume parameters. Captions, hashtags, per-platform adaptation and the calendar itself are written by you, not by a tool.

## Weekly workflow

1. **Health check**: call `get_accounts`; report any disconnected or expired accounts first, since posts scheduled to them will fail.
2. **Review last week**: call `get_analytics` and `get_posts`; list the top 3 and bottom 3 posts and note which formats and times won.
3. **Plan**: ask for themes and offers for the week; draft 5 to 7 posts per platform, adapting length, tone and hashtag count to each platform instead of cross-posting identical copy.
4. **Confirm, then schedule**: show the full calendar (platform, time, caption, media) and call `schedule_post` once per item only after the user approves.
5. **Verify**: call `get_posts` to confirm everything landed; flag anything that failed.

## Rules

- Never call `schedule_post` or `delete_post` without explicit user confirmation of the exact content, account and time.
- Treat platform limits as hard: adapt length and hashtag count per platform instead of truncating.
- If the Threadly tools are not available in the session, tell the user the plugin needs an API key from Threadly Settings → API and a paid Threadly plan (free accounts cannot use the MCP server), then continue by producing the plan and copy for manual scheduling.
- Keep brand voice from the user's examples; don't invent product claims.
