# Indian Stock Market API

A Node.js API project for retrieving and exposing Indian stock-market information from NSE and BSE data sources.

## Overview

This project was built as an API layer around Indian market-data sources, providing programmatic access to information such as indices, stock quotes, gainers and losers, market statistics, historical/intraday data, and chart-oriented data.

It demonstrates backend API development, external data integration, request handling, and transformation of market data into application-friendly responses.

## API Capabilities

### NSE

The original implementation includes endpoints for:

- Market status
- NSE indices
- Index constituents
- Stock quote information
- Stock search
- Top gainers and losers
- Advances / declines
- 52-week highs and lows
- Top-value and top-volume stocks
- Intraday data
- Futures data
- Chart data

### BSE

The original implementation includes endpoints for:

- BSE indices
- Index information
- Index constituents
- Company information
- Historical/chart data
- Top gainers and losers
- Top turnover information

## Example Requests

The API was originally designed to run locally on port `3000`.

```text
GET /get_market_status
GET /nse/get_indices
GET /nse/get_quote_info?companyName=TCS
GET /nse/get_gainers
GET /nse/get_losers
GET /nse/get_index_stocks?symbol=nifty
GET /bse/get_indices
GET /bse/get_gainers
```

## Architecture

At a high level, the project follows an API-integration pattern:

```text
Client Application
       |
       v
Node.js / Express API
       |
       v
Market Data Sources
       |
       v
Normalised API Responses
```

This approach separates client applications from the underlying external market-data sources and provides a consistent HTTP interface.

## Technology

- **Node.js**
- **Express**
- **JavaScript**
- **REST-style HTTP APIs**
- **NSE / BSE data integration**

## Running Locally

The project is an older Node.js application. If you are evaluating or restoring it, first inspect `package.json` and the source code for the dependency versions and original startup command.

A typical legacy workflow is:

```bash
npm install
node app.js 3000
```

Then access the API through `http://localhost:3000`.

## Important: Historical Project

This repository is a **legacy project**. The original external NSE/BSE endpoints and data-access mechanisms may no longer be available, may have changed, or may require different access patterns today.

The project should therefore be viewed primarily as a demonstration of **Node.js backend development and external financial-data integration**, not as a guaranteed current market-data service.

Before production use, the data providers, authentication requirements, request headers, rate limits, error handling, data schemas, and legal/licensing requirements should all be reviewed and updated.

## Engineering Takeaways

- Designing API wrappers around external services
- Working with heterogeneous data formats
- Building backend endpoints for frontend consumption
- Handling third-party data dependencies
- Structuring market data into application-oriented APIs

## License

See the repository's `LICENSE` file for the applicable license.
