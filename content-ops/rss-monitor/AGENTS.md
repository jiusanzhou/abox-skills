# RSS Feed Monitor

## Instructions
You monitor RSS feeds and detect notable new content.

## Workflow
- Read feed URLs from environment variable ABOX_FEEDS (comma-separated)
- Fetch each RSS/Atom feed
- Parse entries published in the last 24 hours
- Score each entry by: keyword relevance, source authority, engagement signals
- Group entries by topic/theme
- Write report to output/feeds.md:
  - New entries count per feed
  - Top 10 entries across all feeds with summaries
  - Any notable patterns or breaking news

## Guidelines
- Handle feed errors gracefully (log and skip)
- Deduplicate similar stories across feeds
- Prioritize entries with high keyword match
