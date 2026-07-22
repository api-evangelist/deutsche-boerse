---
name: Query free Eurex T7 reference data over GraphQL
description: Use the free, rate-limited Eurex T7 reference data GraphQL API with
  the published shared API key to fetch products, contracts, trading hours and
  settlement prices.
api: graphql/deutsche-boerse-eurex-t7-reference-data.graphql
operations: [ProductInfos, Contracts, TradingHours, SettlementPrices, Holidays, TickRules, Changelog]
generated: '2026-07-22'
method: generated
---

# Query free Eurex T7 reference data over GraphQL

Endpoint: `POST https://api.developer.deutsche-boerse.com/eurex-prod-graphql/`
(the trailing slash matters — without it the gateway returns 404).

Auth: header `X-DBP-APIKEY`. Eurex publishes a shared, rate-limited public key on
https://www.eurex.com/ex-en/data/free-reference-data-api; create a dedicated free
key in the Deutsche Börse developer console for better throughput. Anonymous
requests get HTTP 401.

The full schema is in `graphql/deutsche-boerse-eurex-t7-reference-data.graphql`
(70 types, live-introspected). Top-level query fields include `ProductInfos`,
`Contracts`, `Expirations`, `TradingHours`, `SettlementPrices`, `Holidays`,
`TickRules`, `VendorCodes`, `DeliverableBonds`, `FlexibleContracts`, `Enlight`,
`EnlightResponders`, `TESProfiles`, and `Changelog` (reference-data change feed).

Example:

```graphql
{
  ProductInfos(filter: {Product: {eq: "FDAX"}}) {
    date
    data { Product Name Currency }
  }
}
```

Check argument names against the SDL before querying — filters are typed per
field. Respect the shared key's rate limit; on 429 back off and retry.
