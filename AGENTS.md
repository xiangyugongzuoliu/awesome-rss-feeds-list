# AGENTS.md

## Overview

awesome-rss-feeds-list is a curated collection of 1987 RSS feeds across 30 categories.

## Build & Test

No build step. Content is Markdown and OPML files.

Validation: Ensure all RSS feed URLs are valid and accessible.

## Code Style

- One feed per line in LIST.md
- Category files in `feeds/` match README categories
- OPML file kept in sync with LIST.md

## Boundaries

- Feeds must be publicly accessible
- Each feed entry includes: name, URL, and category
- Do not add feeds that require authentication
