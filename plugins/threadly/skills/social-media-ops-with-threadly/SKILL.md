---
name: social-media-ops-with-threadly
description: "Use when the user wants to schedule, publish, plan or analyze social media posts, build a content calendar, write captions or hashtags, find best posting times, check connected social accounts, or monitor brand mentions, using the Threadly MCP tools when connected, or planning the same workflow when not."
---

# Social media operations with Threadly

Threadly (https://threadlyhq.com) is a social-media scheduling and analytics platform. Its MCP server at `https://threadlyhq.com/api/mcp` exposes 20+ tools (full list at https://threadlyhq.com/mcp). This plugin configures that server; the user supplies an API key generated in Threadly under Settings → API. Rate limits: 60 tool calls/minute (300 on Pro). Some tools are Pro-only.

## Tool map

- **Read first:** `get_connected_accounts` (account health, token status), `get_content_queue` (upcoming and failed posts), `get_social_analytics`, `get_post_performance`, `get_audience_insights`, `get_link_analytics`, `get_best_time`.
- **Create:** `generate_caption`, `get_hashtag_suggestions`, `get_content_suggestions`, `resize_content`, `get_content_score`, `get_feed_preview`, `create_content_calendar` (Pro).
- **Write (confirm with the user before calling):** `schedule_post`, `publish_now`, `bulk_schedule` (Pro), `reschedule_post`, `cancel_post`, `engage_reply` (Pro).
- **Monitor:** `listen_mentions` (Pro), `get_competitor_insights` (Pro).

## Weekly workflow

1. **Health check** — `get_connected_accounts`; report any expired tokens first, since scheduled posts will fail silently otherwise.
2. **Review last week** — `get_social_analytics` for the period; list top 3 and bottom 3 posts with `get_post_performance`; note which formats and times won.
3. **Plan** — ask for themes/offers for the week; draft 5–7 posts per platform with `generate_caption` and `get_hashtag_suggestions`; adapt each with `resize_content` rather than cross-posting identical copy.
4. **Score and time** — run `get_content_score` on each draft; place posts using `get_best_time`.
5. **Confirm, then schedule** — show the full calendar (platform, time, caption, media) and schedule only after the user approves; use `bulk_schedule` when available, otherwise `schedule_post` per item.
6. **Verify** — `get_content_queue` to confirm everything landed; flag anything "failed".

## Rules

- Never call `publish_now`, `schedule_post`, `bulk_schedule`, `cancel_post` or `engage_reply` without explicit user confirmation of the exact content and time.
- Treat platform limits as hard: adapt length and hashtag count per platform instead of truncating.
- If the Threadly tools are not available in the session, tell the user the plugin needs an API key from Threadly Settings → API, then continue by producing the plan and copy for manual scheduling.
- Keep brand voice from the user's examples; don't invent product claims.
