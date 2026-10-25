---
name: brave-web-search
description: Search the web using Brave Search API. Returns clean, ad-free results with titles, URLs and snippets. Use for any question needing current info, news, facts or research.
metadata:
  require-secret: true
  require-secret-description: Paste your Brave Search API Key here (from https://api.search.brave.com/app/keys).
---

# Brave Web Search

## Instructions

When the user asks something that requires searching the internet (news, facts, prices, recent events, research):

Call the `run_js` tool with the following exact parameters:

- script name: index.html
- data: A JSON string with the following fields:
  - query: String. The search query in the user's language.
  - count: Number. How many results to return (1-20). Default 5.
  - country: String. 2-letter country code (e.g. "MX", "US"). Default "MX".
  - search_lang: String. Language code ("es", "en"). Default "es".