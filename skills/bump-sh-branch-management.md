---
name: bump-sh-branch-management
description: Create a new branch for a document, list branches, and promote a branch to the default.
api: openapi/bump-sh-branches-api-openapi.yml
operations:
- postDocsByDocIdOrSlugBranches
- getDocsByDocIdOrSlugBranches
- patchDocsByDocIdOrSlugBranchesBySlugSetDefault
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bump-sh-branches-api-openapi.yml ; every operationId checked against the contract
---

# bump-sh-branch-management

Create a new branch for a document, list branches, and promote a branch to the default.

## Steps

1. 1. `postDocsByDocIdOrSlugBranches` – body fields: `name`, optional `slug`.
2. 2. `getDocsByDocIdOrSlugBranches` – query parameters: `page` (integer, default 1, minimum 1), `limit` (integer, default 10, minimum 1, maximum 100).
3. 3. `patchDocsByDocIdOrSlugBranchesBySlugSetDefault` – path parameters: `doc_id_or_slug`, `slug`.

## Rules

- Authentication: include an `Authorization` header using the `Authorization_token` scheme (Bearer token).
- Pagination: use `page` and `limit` query parameters as defined.
