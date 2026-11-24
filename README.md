# arXiv Scraper – Paper Search, Abstracts & Authors

arXiv scraper and paper search: find research papers by keyword, author, category (cs.AI, cs.CL, stat.ML...) or ID and export titles, abstracts, authors, PDF links and DOIs from the official arXiv API.

**[Run it on Apify →](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)** (pay per result, free Apify account to start)


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

1. Create a free account at [apify.com](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper) and copy your API token.
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

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/arxiv-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper) for current pay-per-result pricing.

## More data actors

- [Bluesky Scraper – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [UK Companies House Scraper – Companies & Directors](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [Hacker News Scraper – Stories, Comments & Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [npm Package Scraper – Downloads & Dependencies](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [SEC EDGAR Scraper – 10-K, 8-K & Form D Funding Filings](https://apify.com/devteamdrew/sec-edgar-scraper?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [UK Government Tenders Scraper – Contracts Finder, Find a Tender](https://apify.com/devteamdrew/uk-public-tenders?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [UK CQC Care Homes & Providers Scraper – Ratings & Care Leads](https://apify.com/devteamdrew/uk-cqc-care-providers?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [SAM.gov Scraper – Federal Contract Opportunities, No API Key](https://apify.com/devteamdrew/sam-gov-opportunities?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [UK Operator Licence Scraper – HGV & Bus Operators (DVSA VOL)](https://apify.com/devteamdrew/uk-operator-licences?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [USAspending Federal Awards Scraper – Contracts & Grants](https://apify.com/devteamdrew/usaspending-awards?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)
- [EU Tenders Scraper – TED Public Procurement Notices](https://apify.com/devteamdrew/eu-ted-tenders?utm_source=github&utm_medium=readme&utm_campaign=arxiv-scraper)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
