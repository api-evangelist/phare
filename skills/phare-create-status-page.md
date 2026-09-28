---
name: phare-create-status-page
description: Create a new status page and retrieve it.
api: openapi/phare-openapi.json
operations:
- createUptimeStatusPage
- getUptimeStatusPage
generated: '2026-09-27'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/phare-openapi.json ; every operationId checked against the contract
---

# phare-create-status-page

Create a new status page and retrieve it.

## Steps

1. 1. `createUptimeStatusPage` – send a request body with the fields defined in the contract for creating a status page.
2. 2. `getUptimeStatusPage` – provide the path parameter `statusPageId` returned from the create call to retrieve the newly created page.

## Rules

- Include a Bearer token in the `Authorization` header (BearerAuth).
- All requests are made to the base URL `https://api.phare.io`.
