# Website Contact Scraper: Emails, Phones & Social Links — MCP Server

Get contact details for any company website from your AI agent or MCP client — one row per site: emails (role or person, MX-checked), validated phones (E.164), LinkedIn, Facebook, Instagram, X and YouTube links, address, contact-form URL and company name. Plain HTTP, robots.txt respected, and you are only charged when contacts are found.

This repo is the MCP listing for the [Website Contact Scraper: Emails, Phones & Social Links](https://apify.com/magnova/website-contact-info-scraper) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--website-contact-info-scraper** — Scrape a company website for emails, validated phones, social links, address and contact-form URL. Returns one structured record per site, charged only when contacts are found.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/website-contact-info-scraper
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "website-contact-info-scraper": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/website-contact-info-scraper"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "website-contact-info-scraper": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/website-contact-info-scraper"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/website-contact-info-scraper-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.003 per site — $3 per 1,000 sites**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/website-contact-info-scraper
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/website-contact-info-scraper

*Contact records come from the site's own public pages; robots.txt respected.*
