---
name: phare-manage-alert-rules
description: Create, retrieve, update, and delete an alert rule.
api: openapi/phare-openapi.json
operations:
- createUptimeAlertRule
- getAlertRule
- updateUptimeAlertRule
- deleteUptimeAlertRule
generated: '2026-09-27'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/phare-openapi.json ; every operationId checked against the contract
---

# phare-manage-alert-rules

Create, retrieve, update, and delete an alert rule.

## Steps

1. 1. Use `createUptimeAlertRule` with the request body fields required to define a new alert rule and the `Authorization: Bearer <token>` header.
2. 2. Use `getAlertRule` with the path parameter `alertRuleId` returned from step 1 and the `Authorization` header to retrieve the created rule.
3. 3. Use `updateUptimeAlertRule` with the same `alertRuleId`, the request body fields for the updates, and the `Authorization` header.
4. 4. Use `deleteUptimeAlertRule` with the `alertRuleId` and the `Authorization` header to remove the rule.

## Rules

- Auth: All requests require the `Authorization: Bearer <token>` header (BearerAuth).
- Idempotency: `createUptimeAlertRule` is not idempotent; repeat calls may create duplicate rules.
- Errors: The API returns standard HTTP error codes (e.g., 400 for bad request, 401 for unauthorized, 404 for not found, 500 for server error).
