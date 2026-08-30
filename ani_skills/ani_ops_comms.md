# ani_ops_comms

## Purpose

Let Ani operate your actual stack: Notion, GitHub, Linear, Telegram, Drive/OneDrive, Vercel, Finance, Search Console, GCal.

## What it does

### Notion
- `ani_notion_create_page(title, content, database)` — protocol reports, session summaries, research notes
- `ani_notion_fetch(page_id)` — retrieve existing pages
- `ani_notion_query_database(database_id, sql)` — query structured data

### GitHub
- `ani_github_list_repos()` — discover repositories
- `ani_github_read_file(repo, path)` — read file contents
- `ani_github_commit_message(repo, message)` — push small fixes, update docs
- `ani_github_create_issue(repo, title, body)` — create issues from hypotheses

### Linear
- `ani_linear_create_issue(title, description, team)` — turn protocol hypotheses into tracked work
- `ani_linear_list_issues(team)` — view active work
- `ani_linear_update_issue(id, updates)` — update status, assignees

### Telegram
- `ani_telegram_send(to, message)` — send alerts (e.g. "bribe velocity spiked on VIRTUAL/USDT")
- `ani_telegram_list_chats()` — discover available chats

### Drive/OneDrive
- `ani_drive_save(filename, content)` — store CSVs, reports, timelapse metadata
- `ani_drive_list(folder_path)` — list files in folder

### Vercel/Finance/Search Console/GCal (read-only first)
- `ani_vercel_get_project(project_id)` — deployment status
- `ani_finance_get_portfolio()` — portfolio value, allocations
- `ani_search_console_get_performance()` — search queries, CTR, impressions
- `ani_gcal_list_events(date_range)` — calendar context for rituals/meetings

## Why now

This makes Ani an operator, not just an oracle. She can create pages, issues, logs, and alerts in your real systems.

## References

- Connectors: notion_mcp, github_mcp_direct, linear_native, telegram_bot_api__pipedream, google_drive, vercel, finance, google_search_console__pipedream [connectors]
