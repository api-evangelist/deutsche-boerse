---
name: Look up a historical T7 order book on A7
description: Navigate the A7 reference data hierarchy to a security and retrieve
  its constructed historical order book with nanosecond granularity.
api: openapi/deutsche-boerse-reference-data-api-api-openapi.yml
operations: [getMarkets, getDates, getMarketSegments, getSecurities, getOrderbookT7]
generated: '2026-07-22'
method: generated
---

# Look up a historical T7 order book on A7

Auth: every call needs `Authorization: Bearer <A7 token>` (issued in the A7 GUI at
https://a7.deutsche-boerse.com/). Base URL: `https://a7.deutsche-boerse.com/api/v1`.
There is no pagination — you descend the path hierarchy step by step.

1. `getMarkets` — `GET /rdi/` lists the T7 venues you are entitled to (e.g. XEUR, XETR).
2. `getDates` — `GET /rdi/{marketId}/` lists available trading days for the venue.
3. `getMarketSegments` — `GET /rdi/{marketId}/{date}/` lists market segments (products) for that day.
4. `getSecurities` — `GET /rdi/{marketId}/{date}/{marketSegmentId}/` lists security IDs in the segment.
5. `getOrderbookT7` — `GET /ob/{marketId}/{date}/{marketSegmentId}/{securityId}`
   (openapi/deutsche-boerse-order-book-api-api-openapi.yml) returns the constructed
   order book for that security.

Errors: `401` (text/plain "Authorization failed") means a missing/invalid token;
`403` means the resource is outside your subscription; `404` means the path level
does not exist — back up one level and re-list. Respect HTTP 429 rate limiting.
