# Allabolag Scraper - Sweden Company Register & Financials

Allabolag scraper for Swedish companies without login: search by keyword, org.nr, county or municipality, or enrich org numbers with revenue, profit, employees, NACE codes, financials, board roles, shareholders and watch mode.

**[Run it on Apify Store](https://apify.com/kamerozkan/allabolag-scraper)**: no servers, no proxies to manage, results as JSON, CSV or Excel, or straight into your app through the API.

## Why use it

- Runs in the cloud on [Apify](https://apify.com/kamerozkan/allabolag-scraper); start it from the browser, the API, a schedule, or tools like Make, n8n and Zapier.
- Pay only for results. The current price and plan discounts are always on the [Store page](https://apify.com/kamerozkan/allabolag-scraper).
- Cap the cost of any run with the maximum cost per run setting.

## Quick start

1. Open the [Actor page](https://apify.com/kamerozkan/allabolag-scraper) and click **Try for free**.
2. Paste an input like the one below and click **Start**.
3. Download the dataset or read it over the API.

```json
{
  "queries": [
    "software"
  ],
  "includeDetails": true,
  "maxResults": 10
}
```

## Use it from code

Python ([examples/python_example.py](examples/python_example.py)), Node.js ([examples/node_example.js](examples/node_example.js)) and cURL ([examples/curl.sh](examples/curl.sh)) examples are in the `examples` folder. All of them need an [Apify API token](https://console.apify.com/settings/integrations).

## Use in n8n & Make

- **n8n:** Import [integrations/n8n-workflow.json](integrations/n8n-workflow.json) directly into your n8n workspace, set your `APIFY_TOKEN` environment variable (or Bearer token header), and click **Execute Workflow**.
- **Make / Zapier:** Call the Apify **Run an Actor** module with Actor ID `kamerozkan/allabolag-scraper` and the JSON input above, or POST to `https://api.apify.com/v2/acts/kamerozkan~allabolag-scraper/run-sync-get-dataset-items`.

## Use with AI Agents (Apify MCP)

This Actor works with Claude Desktop, Cursor, Windsurf and any MCP-compatible AI agent through the official [Apify MCP Server](https://mcp.apify.com). Copy [integrations/mcp-config.json](integrations/mcp-config.json) into your MCP client configuration and replace `YOUR_APIFY_TOKEN` with your token.

## Sample output

Real rows from a recent run, with any contact details masked. Full sample: [sample-output.json](sample-output.json).

```json
[
  {
    "orgnr": "5565873147",
    "orgnrFormatted": "556587-3147",
    "companyId": "2K1RZ7FI5YFOF",
    "name": "Aurevia AB",
    "legalName": "Aurevia AB",
    "companyType": "Aktiebolag",
    "companyTypeCode": "AB",
    "status": "ACTIVE",
    "registrationDate": "2000-03-13",
    "foundationDate": "13.03.2000",
    "currency": "SEK",
    "revenueThousandsSek": 46881,
    "revenueSek": 46881000,
    "profitThousandsSek": -727,
    "profitSek": -727000,
    "shareCapitalThousands": 100,
    "employees": 28,
    "primaryIndustry": "Läkemedel",
    "industries": [
      "Läkemedel",
      "Medicinteknisk utrustning",
      "Forskning",
      "Facklig, vetenskaplig och teknisk verksamhet"
    ],
    "naceCodes": [
      "72109 Annan naturvetenskaplig och teknisk forskning och utveckling"
    ],
    "county": "Uppsala Län",
    "municipality": "Uppsala",
    "visitorAddress": {
      "street": "Skolgatan 8",
      "zipCode": "75015",
      "city": "Uppsala"
    },
    "postalAddress": {
      "street": "Box 15027",
      "zipCode": "75015",
      "city": "Uppsala"
    },
    "latitude": 59.86098,
    "longitude": 17.628925,
    "phone": "+1 555 0100",
    "email": "contact@example.com",
    "website": "https://www.aurevia.com/",
    "socialLinks": {
      "linkedInUrl": "https://www.linkedin.com/company/aurevia-cro",
      "facebookUrl": "https://www.facebook.com/aureviacro",
      "instagramUrl": "https://www.instagram.com/aurevia_clinical_research_cro/"
    },
    "registeredForVat": true,
    "registeredForPayrollTax": true,
    "purpose": "Aktiebolaget ska bedriva konsulttjänster inom läkemedelsbranschen samt utföra tjänster relaterade till forskning inom läkemedel och medicintekniska produkter, med avseende på kvalitets- och regleringsfrågor samt idka därmed förenlig verksamhet.",
    "latestAccountsYear": "2025",
    "financialAccounts": [
      {
        "year": "2025",
        "period": "2025-12",
        "currency": "SEK",
        "revenueThousands": 46881,
        "operatingProfitThousands": -727,
        "netProfitThousands": -727,
        "totalAssetsThousands": 11635,
        "equityThousands": -26,
        "equityRatioPercent": 31.9,
        "profitMarginPercent": 145.7,
        "ebitdaThousands": -4378,
        "employees": 28
      },
      {
        "year": "2024",
        "period": "2024-12",
        "currency": "SEK",
        "revenueThousands": 45549,
        "operatingProfitThousands": 2504,
        "netProfitThousands": 1960,
        "totalAssetsThousands": 17273,
        "equityThousands": -37,
        "equityRatioPercent": 42,
        "profitMarginPercent": 184.7,
        "ebitdaThousands": 3335,
        "employees": 29
      },
      {
        "year": "2023",
        "period": "2023-12",
        "currency": "SEK",
        "revenueThousands": 47809,
        "operatingProfitThousands": 4362,
        "netProfitThousands": 3430,
        "totalAssetsThousands": 14844,
        "equityThousands": -59,
        "equityRatioPerce
```

## Support

Found a problem or need a field? Open an issue on the [Actor's Issues tab](https://apify.com/kamerozkan/allabolag-scraper/issues) and include your run link.

---
This repository holds usage examples and sample data. The Actor itself runs on Apify.
