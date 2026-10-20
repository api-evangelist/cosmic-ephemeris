---
name: cosmic-ephemeris-calculate-full-birth-chart
description: Generate a complete natal chart and derive its aspects and house positions.
api: openapi/cosmic-ephemeris-openapi.json
operations:
- calculateBirthChart
- calculateAspects
- calculateHouses
generated: '2026-10-20'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/cosmic-ephemeris-openapi.json ; every operationId checked against the contract
---

# cosmic-ephemeris-calculate-full-birth-chart

Generate a complete natal chart and derive its aspects and house positions.

## Steps

1. 1. Call `calculateBirthChart` with the required birth data fields and include an authentication header (Bearer token or `x-api-key`).
2. 2. Call `calculateAspects` using the chart output from step 1; provide the chart identifier and include the authentication header.
3. 3. Call `calculateHouses` with the same birth data and desired house system; include the authentication header.

## Rules

- Include an authentication header: either `Authorization: Bearer <token>` (BearerApiKey) or `x-api-key: <key>` (HeaderApiKey).
- Send the `Idempotency-Key` header on each POST request to ensure safe retries.
