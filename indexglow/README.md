# IndexGlow

Understand your site's organic search traffic and visibility on Google and Bing from a conversation with Claude. IndexGlow connects Claude to your Google Search Console and Bing Webmaster Tools data: clicks, impressions, CTR, rankings, top pages and queries, trends, keyword opportunities, cannibalization, and indexing or crawl issues. Google and Bing figures stay separate, and search clicks are not total website visits.

## What the plugin adds

- The IndexGlow connector, a remote MCP server at https://indexglow.com/api/mcp, with tools to read performance, compare periods, find opportunities, inspect URLs, review sitemaps and Bing crawl health, and open an interactive dashboard.
- Skills that tell Claude how to use it well:
  - Review organic search performance (`seo-review`)
  - Investigate an organic traffic change (`traffic-change`)
  - Review URL indexing and crawl evidence (`indexing-review`)
  - Find search keyword opportunities (`keyword-opportunities`)
  - Review and manage search sitemaps (`sitemap-management`)
  - Submit specific URLs to Bing (`bing-url-submission`)

## Set it up

1. Create an account at https://indexglow.com, then connect Google Search Console, Bing Webmaster Tools, or both.
2. Add the plugin: from Customize > Plugins in claude.ai and Cowork, or in Claude Code with `claude plugin marketplace add maxkenfr/indexglow-claude-plugin` then `claude plugin install indexglow@indexglow`.
3. Connect its IndexGlow connector: from the plugin's Connectors tab in claude.ai and Cowork, or with `/mcp` in Claude Code. Sign in with your IndexGlow account when asked.
4. Ask a question, for example:
   - "Show my Google and Bing search performance for the last 28 days."
   - "Why did my organic search clicks fall last month?"
   - "Check whether a page on my site is indexed by Google and has been crawled by Bing."

Reading is the default. Sitemap changes and Bing URL submissions happen only when you ask for them, and only if you allowed management for that search engine in IndexGlow.

## Data

The plugin contains instructions and the connector address; it runs no code on your computer. Each tool request Claude makes (the tool name and its arguments, such as a site URL, dates or filters) goes to IndexGlow at https://indexglow.com/api/mcp. IndexGlow reads the requested data from Google Search Console or Bing Webmaster Tools, for the accounts you connected, and returns the results to Claude, where Anthropic's terms and your Claude settings apply. Google and Bing tokens are never sent to Claude.

IndexGlow does not store the search data it returns to Claude. It keeps a history of tool calls, arguments included, for 90 days and daily usage counts for 90 days. Details are in the privacy policy: https://indexglow.com/privacy.

## Support

Help: https://indexglow.com/support. Terms of use: https://indexglow.com/terms.
