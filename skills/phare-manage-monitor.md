---
name: phare-manage-monitor
description: Create, view, pause, resume, and delete an uptime monitor.
api: openapi/phare-openapi.json
operations:
- createUptimeMonitor
- getUptimeMonitor
- pauseUptimeMonitor
- resumeUptimeMonitor
- deleteUptimeMonitor
generated: '2026-09-27'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/phare-openapi.json ; every operationId checked against the contract
---

# phare-manage-monitor

Create, view, pause, resume, and delete an uptime monitor.

## Steps

1. 1. Call `createUptimeMonitor` with the monitor definition in the request body and include the `Authorization: Bearer <token>` header.
2. 2. Call `getUptimeMonitor` with the returned `monitorId` path parameter and the `Authorization` header to retrieve the monitor details.
3. 3. Call `pauseUptimeMonitor` with the `monitorId` path parameter and the `Authorization` header to pause monitoring.
4. 4. Call `resumeUptimeMonitor` with the `monitorId` path parameter and the `Authorization` header to resume monitoring.
5. 5. Call `deleteUptimeMonitor` with the `monitorId` path parameter and the `Authorization` header to remove the monitor.

## Rules

- All requests require an `Authorization: Bearer <token>` header (BearerAuth).
- Operations are not idempotent except `deleteUptimeMonitor`, which can be safely retried.
- No pagination is needed for these operations.
