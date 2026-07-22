---
name: Upload and run a custom algo on A7
description: Manage a customer-owned algorithm over A7 historical order book data -
  upload the algo, run it, and retrieve its metadata and code.
api: openapi/deutsche-boerse-algo-management-api-api-openapi.yml
operations: [getOwners, getAlgos, addAlgo, runAlgo, getAlgoMetadata, getAlgoCode, deleteAlgo]
generated: '2026-07-22'
method: generated
---

# Upload and run a custom algo on A7

Auth: `Authorization: Bearer <A7 token>`; base `https://a7.deutsche-boerse.com/api/v1`.

1. `getOwners` — `GET /algo` lists algo owners visible to your subscription.
2. `getAlgos` — `GET /algo/{owner}` lists that owner's algos.
3. `addAlgo` — `PUT /algo/{owner}/{algoName}` uploads or replaces the algo. PUT is
   an upsert: re-sending the same body is safe (there is no Idempotency-Key
   contract on this API; write retry-safety comes from the PUT semantics).
4. `runAlgo` — `GET /algo/{owner}/{algoName}/run` executes the algo over the
   requested historical data range (parameters per the spec).
5. `getAlgoMetadata` / `getAlgoCode` — `GET /algo/{owner}/{algoName}` and
   `GET /algo/{owner}/{algoName}/download` retrieve the definition and source.
6. `deleteAlgo` — `DELETE /algo/{owner}/{algoName}` removes it when finished.

For scheduled/precalculated runs use the Precalc API
(openapi/deutsche-boerse-precalc-api-api-openapi.yml): `addPrecalcData`,
`activatePrecalc`, `getTasks`, `getResultSets`, `getData`.

Errors: 401 invalid token, 403 forbidden resource (JSON body), 404 not found.
