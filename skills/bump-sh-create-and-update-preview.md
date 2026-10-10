---
name: bump-sh-create-and-update-preview
description: Create a new preview and then update it.
api: openapi/bump-sh-previews-api-openapi.yml
operations:
- postPreviews
- putPreviewsByPreviewId
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bump-sh-previews-api-openapi.yml ; every operationId checked against the contract
---

# bump-sh-create-and-update-preview

Create a new preview and then update it.

## Steps

1. 1. Call `postPreviews` with the required request body fields for creating a preview and include an `Authorization` header using the `Authorization_token` or `Basic_token` scheme.
2. 2. Call `putPreviewsByPreviewId` with the `preview_id` path parameter of the created preview, the required request body fields for updating the preview, and include an `Authorization` header using the `Authorization_token` or `Basic_token` scheme.

## Rules

- Authentication: Provide an `Authorization` header using either the `Authorization_token` (Bearer) or `Basic_token` scheme.
- Idempotency: The `putPreviewsByPreviewId` operation is idempotent; repeated calls with the same payload will result in the same state.
