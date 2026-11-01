# arXiv Scraper – Paper Search, Abstracts & Authors

arXiv scraper and paper search: find research papers by keyword, author, category (cs.AI, cs.CL, stat.ML...) or ID and export titles, abstracts, authors, PDF links and DOIs from the official arXiv API.

**[Run it on Apify →](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=hero)** (pay per result, free Apify account to start)


**arXiv Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- Daily alerts of new papers in your field (incremental mode)
- Literature reviews and research dashboards
- Feeding abstracts into RAG / AI research agents
- Tracking competitors' and labs' publications

## Data source

The official arXiv API (`export.arxiv.org`), used within its terms (one request every 3 seconds). Metadata only.

## Features

- **Pay only for results** (pay-per-event pricing, no monthly rental)
- **Incremental mode**: scheduled runs return only items you haven't received before
- **LLM-ready output**: optional compact Markdown per item for RAG / AI agents
- **Polite rate limiting** with automatic retries and backoff
- Clean, flat JSON you can export as CSV, Excel, JSON or via API


## Quick start

1. Create a free account at [apify.com](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=quickstart) and copy your API token.
2. `export APIFY_TOKEN=...`
3. Run one of the examples:

```bash
bash examples/run.sh          # curl
node examples/run.js          # JavaScript (apify-client)
python examples/run.py        # Python (apify-client)
```

Example input ([examples/input.json](examples/input.json)):

```json
{
  "queries": [
    "retrieval augmented generation"
  ],
  "maxItems": 20
}
```

## FAQ

**Why is it slower than other actors?**
arXiv asks API users to wait 3 seconds between requests; each request returns up to 100 papers.

**Does it download PDFs?**
It returns PDF links; metadata only.

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/arxiv-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=pricing) for current pay-per-result pricing.

## Sample data

Browse real sample rows, download a free CSV sample and see ready-made feeds at [rowsift.co.uk](https://rowsift.co.uk/feeds/arxiv-scraper/?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=sample-data).

## More data actors

- [Bluesky Scraper – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [UK Companies House Scraper – Companies & Directors](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [Hacker News Scraper – Stories, Comments & Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [npm Package Scraper – Downloads & Dependencies](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)
- [SEC EDGAR Scraper – 10-K, 10-Q & 8-K Filings](https://apify.com/devteamdrew/sec-edgar-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper&utm_content=more)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
