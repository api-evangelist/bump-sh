---
name: bump-sh-create-and-fetch-diff
description: Create a new Diff and then retrieve its detailed information.
api: openapi/bump-sh-diffs-api-openapi.yml
operations:
- postDiffs
- getDiffsById
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bump-sh-diffs-api-openapi.yml ; every operationId checked against the contract
---

# bump-sh-create-and-fetch-diff

Create a new Diff and then retrieve its detailed information.

## Steps

1. 1. Use `postDiffs` with the request body fields required to create a Diff (as defined in the API contract).
2. 2. Use `getDiffsById` with the path parameter `id` returned from the previous step to fetch detailed information about the created Diff.

## Rules

- Authentication: include an `Authorization` header using either the `Authorization_token` or `Basic_token` scheme.
- Idempotency: not applicable for these operations.
- Pagination: not applicable for these operations.
- Errors: follow the API's standard HTTP error responses (e.g., 4xx for client errors, 5xx for server errors).
