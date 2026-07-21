# Deutsche Börse (deutsche-boerse)

Deutsche Börse AG is the Frankfurt-based, publicly listed (FWB DB1) exchange organization behind the Frankfurt Stock Exchange and Xetra cash market, the Eurex derivatives exchange, EEX, 360T, Clearstream post-trade services, and the ISS STOXX index and analytics business. Its Market Data + Services arm sells real-time, historical, and reference market data, delivered through a self-serve Group API platform (developer.deutsche-boerse.com, API-key gated REST and GraphQL), the A7 Analytics Platform cloud REST API for nanosecond order-by-order Eurex/Xetra/EEX/CME history, a Cloud Stream WebSocket feed, licensed low-latency feeds, and the Datashop for commercial data purchases.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/deutsche-boerse/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/deutsche-boerse/refs/heads/main/apis.yml)

## Tags

- Financial
- Market Data
- Stocks
- Derivatives
- Trading
- Real-Time
- Order Book
- Reference Data
- Exchange
- Analytics

## Timestamps

- **Created:** 2026-07-21
- **Modified:** 2026-07-21

## APIs

### A7 Analytics Platform - Order Book API

Constructed historical order books for the T7 trading venues of Deutsche Börse Group (Eurex, Xetra) with nanosecond granularity, accessed over REST with bearer-token authentication.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-orderbook-openapi.yml)

### A7 Analytics Platform - Market Data API (EOBI)

Un-normalized, genuine historical order-by-order market data from the T7 Enhanced Order Book Interface (EOBI) feed for Eurex and Xetra.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-eobi-openapi.yml)

### A7 Analytics Platform - CME Market Data API (MDP)

Historical CME Group market data from the MDP feed served through the A7 Analytics Platform REST API.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-mdp-openapi.yml)

### A7 Analytics Platform - Reference Data API (RDI) v2

Reference data for T7 venues (markets, market segments, securities) from the Reference Data Interface, version 2 of the A7 reference data API.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [Documentation](https://deutsche-boerse.github.io/a7/usecases/02_simple_rdi.html)
- [OpenAPI](openapi/deutsche-boerse-a7-rdi-v2-openapi.yml)

### A7 Analytics Platform - CME Reference Data API (SD)

CME Group security-definition reference data served through the A7 Analytics Platform REST API.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-sd-v2-openapi.yml)

### A7 Analytics Platform - Algo Management API

Create, update, delete, and run custom algos over historical order book data and retrieve their results - a high-performance framework for custom analytics on A7.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [Documentation](https://deutsche-boerse.github.io/a7/usecases/01_simple_example.html)
- [OpenAPI](openapi/deutsche-boerse-a7-algo-openapi.yml)

### A7 Analytics Platform - Dataset API

Manage customer datasets on the A7 Analytics Platform (versions 1 and 2 of the Dataset API).

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-dataset-openapi.yml)
- [OpenAPI](openapi/deutsche-boerse-a7-dataset-v2-openapi.yml)

### A7 Analytics Platform - Market Data Insights API

Off-the-shelf market data insights and analytics derived from A7 granular historical order book data.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-insights-openapi.yml)

### A7 Analytics Platform - Option Analytics API

Option analytics computed on the A7 Analytics Platform for Eurex-traded options.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-option-analytics-openapi.yml)

### A7 Analytics Platform - Precalc API

Management of precalculated analytics runs on the A7 Analytics Platform.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-precalc-openapi.yml)

### A7 Analytics Platform - Auction Simulation API

Simulate Xetra auctions against historical order book data on the A7 Analytics Platform.

- **Human URL:** [https://a7.deutsche-boerse.com/](https://a7.deutsche-boerse.com/)
- **Base URL:** `https://a7.deutsche-boerse.com/api/v1`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/a7)
- [OpenAPI](openapi/deutsche-boerse-a7-auction-simulations-openapi.yml)

### Eurex T7 Reference Data API

Free GraphQL API for Eurex T7 reference data (products, contracts, instrument attributes) in machine- and human-readable JSON, offered with a shared rate-limited public API key or a dedicated key from the Deutsche Börse Group developer portal (X-DBP-APIKEY header).

- **Human URL:** [https://www.eurex.com/ex-en/data/free-reference-data-api](https://www.eurex.com/ex-en/data/free-reference-data-api)
- **Base URL:** `https://api.developer.deutsche-boerse.com/eurex-prod-graphql`

#### Properties

- [Documentation](https://www.eurex.com/ex-en/data/free-reference-data-api)
- [Portal](https://console.developer.deutsche-boerse.com/apis)

### Deutsche Börse Cloud Stream Market Data API

Cloud-delivered real-time market data streaming over WebSocket (host md.deutsche-boerse.com) with Protocol Buffers or JSON message encoding and API-key authentication - the published sample client subscribes to subjects such as md-tradegate (Tradegate quotes in CEF format).

- **Human URL:** [https://github.com/Deutsche-Boerse/Cloud.Stream.Client](https://github.com/Deutsche-Boerse/Cloud.Stream.Client)
- **Base URL:** `wss://md.deutsche-boerse.com`

#### Properties

- [Documentation](https://github.com/Deutsche-Boerse/Cloud.Stream.Client)

## Common Properties

- [Website](https://www.deutsche-boerse.com/dbg-en/)
- [Portal](https://console.developer.deutsche-boerse.com/)
- [Documentation](https://docs.developer.deutsche-boerse.com/)
- [GitHub Organization](https://github.com/Deutsche-Boerse)
- [LinkedIn](https://www.linkedin.com/company/deutscheboerse)
- [Blog](https://docs.developer.deutsche-boerse.com/blog/)
- [Privacy Policy](https://www.deutsche-boerse.com/dbg-en/meta/privacy-notice)
- [Terms of Service](https://www.deutsche-boerse.com/dbg-en/meta/disclaimer)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
