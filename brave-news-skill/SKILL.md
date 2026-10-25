---
name: brave-news-search
description: Search recent news using Brave News API. Returns headlines, sources, dates and snippets. Use for current events, breaking news, sports results, or anything time-sensitive.
metadata:
  require-secret: true
  require-secret-description: Paste your Brave Search API Key here (same key as web search).
---

# Brave News Search

## Instructions

When the user asks about news, recent events, sports results, or anything that happened recently:

Call the `run_js` tool with the following exact parameters:

- script name: index.html
- data: A JSON string with the following fields:
  - query: String. The news topic to search.
  - count: Number. How many articles (1-20). Default 5.
  - freshness: String. Time window: "pd" (past day), "pw" (past week), "pm" (past month). Default "pw".
  - country: String. 2-letter code ("MX", "US"). Default "MX".
  - search_lang: String. "es" or "en". Default "es".