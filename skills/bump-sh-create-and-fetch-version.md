---
name: bump-sh-create-and-fetch-version
description: Create a new documentation version and then retrieve it with its diff summary.
api: openapi/bump-sh-versions-api-openapi.yml
operations:
- postVersions
- getVersionsByVersionId
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bump-sh-versions-api-openapi.yml ; every operationId checked against the contract
---

# bump-sh-create-and-fetch-version

Create a new documentation version and then retrieve it with its diff summary.

## Steps

1. 1. Use `postVersions` with the required request body fields for creating a version and include the `Authorization` header as defined by the `Authorization_token` scheme.
2. 2. Use `getVersionsByVersionId` with the `version_id` path parameter returned from the previous step and include the `Authorization` header as defined by the `Authorization_token` scheme.

## Rules

- Authentication: Include an `Authorization` header using the `Authorization_token` scheme (Bearer token).
- Pagination: Not applicable for these operations.
- Idempotency: Not specified for these endpoints.
- Error handling: Follow standard HTTP error responses; no specific error codes are documented.
