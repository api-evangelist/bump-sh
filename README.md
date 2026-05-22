# Bump.sh (bump-sh)

Bump.sh is "the modern API doc platform" — automatic, diff-aware documentation for OpenAPI and AsyncAPI specifications, plus a managed Model Context Protocol (MCP) platform that compiles Flower or Arazzo workflow documents into deterministic, observable MCP servers for AI agents. Customers include Aviobook, MongoDB, Elastic, Lightspeed, and BigID.

**APIs.json:** [bump-sh/apis.yml](https://raw.githubusercontent.com/api-evangelist/bump-sh/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **x-type:** company
- **Access:** 3rd-Party
- **Specification version:** 0.19

## Tags

API Changelog · API Documentation · API Hub · API Governance · Arazzo · AsyncAPI · CI/CD · Flower · MCP · OpenAPI · Workflows

## APIs

### Bump.sh API

The official Bump.sh REST API (v1). 15 operations across 9 tags, with one outbound webhook (`DocStructureChange`).

- **HumanURL:** https://bump.sh
- **BaseURL:** https://bump.sh/api/v1
- **OpenAPI:** [openapi/bump-sh-openapi.yaml](./openapi/bump-sh-openapi.yaml)
- **API Reference:** https://developers.bump.sh
- **Auth:** `Authorization: Token {documentation_or_hub_or_org_token}`

| Method | Path | Summary |
|---|---|---|
| POST | `/diffs` | Create a Diff |
| GET | `/diffs/{id}` | Fetch Detailed Information from an Existing Diff |
| GET | `/hubs` | List All Hubs |
| GET | `/hubs/{hub_id_or_slug}` | Fetch Information of an Existing Hub |
| POST | `/versions` | Create a New Version |
| GET | `/versions/{version_id}` | Fetch a Full Documentation Version Including Diff Summary |
| GET | `/docs/{doc_id_or_slug}/branches` | List Available Branches |
| POST | `/docs/{doc_id_or_slug}/branches` | Create a New Branch |
| DELETE | `/docs/{doc_id_or_slug}/branches/{slug}` | Delete a Branch |
| PATCH | `/docs/{doc_id_or_slug}/branches/{slug}/set_default` | Promote Branch as the Default One |
| POST | `/validations` | Validate a Documentation Definition |
| POST | `/previews` | Create a Preview |
| PUT | `/previews/{preview_id}` | Update an Existing Preview |
| GET | `/ping` | Check the API Status |
| POST | `/mcp_servers/{mcp_server_id_or_slug}/deploy` | Deploy a New MCP Server Document |

## Specifications Supported

OpenAPI 2.x / 3.0.x / 3.1.x · AsyncAPI 2.x / 3.x · JSON Schema · Arazzo 1.0.0 (OAI workflow spec) · Flower (Bump.sh-native workflow spec).

## Features

- Automated documentation generation from OpenAPI/AsyncAPI specs
- Diff-based API changelog with visual diffs
- Multi-API hubs with custom domains, branding, and login
- Branches that mirror source-control workflow
- Previews for pull-request review without publishing
- Validations endpoint for spec linting
- CI integration (GitHub Actions, GitLab CI, CircleCI, Travis, Azure DevOps)
- Open-source CLI (TypeScript) and GitHub Action
- Webhook notifications on spec changes (`DocStructureChange`)
- **Managed MCP platform** — compile Flower or Arazzo workflows into hosted MCP servers
- Deterministic, observable agent execution with built-in authentication
- Ask AI and Markdown rendering inside published docs
- Embed mode, SSO, reverse proxy, and 99.99% SLA on the Custom tier

## Use Cases

- Publish API documentation automatically on every commit
- Generate API changelogs for downstream consumers
- Run multi-API portals for internal and external developer audiences
- Notify stakeholders of breaking changes via webhook
- Preview spec changes on pull requests
- Validate OpenAPI/AsyncAPI definitions before deploy
- Compile Arazzo workflows into MCP servers for ChatGPT, Claude, and Cursor agents

## Repository Layout

| Folder | Contents |
|---|---|
| [`openapi/`](./openapi/) | OpenAPI 3.2.0 specification (`bump-sh-openapi.yaml`) |
| [`examples/`](./examples/) | 16 request/response example payloads — one per operation plus the webhook |
| [`rules/`](./rules/) | Spectral ruleset enforcing Bump.sh conventions (`bump-sh-api-rules.yml`) |
| [`capabilities/`](./capabilities/) | Naftiko capability compositions (continuous docs, breaking-change governance, branch-based docs, MCP publishing, preview-on-PR, hub index) + shared per-API definition |
| [`json-schema/`](./json-schema/) | JSON Schemas for Diff, Version, Hub, Branch, Preview, Validation, MCP deployment, doc-change event |
| [`json-structure/`](./json-structure/) | JSON Structure mirrors of the same entities |
| [`json-ld/`](./json-ld/) | JSON-LD context (`bump-sh-context.jsonld`) |
| [`vocabulary/`](./vocabulary/) | Domain vocabulary (`bump-sh-vocabulary.yml`) |
| [`plans/`](./plans/) | API Commons Plans 0.1 — Basic $50/mo, Pro $250/mo, Custom, Open Source program |
| [`rate-limits/`](./rate-limits/) | API Commons Rate Limits 0.1 |
| [`finops/`](./finops/) | FOCUS 1.3 / FinOps Framework alignment |
| [`blogs/`](./blogs/) | Cached blog index |

## Pricing (from https://bump.sh/pricing)

| Tier | Price | API Docs | Internal Users | External Guests | Notable |
|---|---|---|---|---|---|
| Basic | $50/mo | 10 | 3 | 20 | OpenAPI/AsyncAPI, CLI, GitHub integration, custom domain/logo, hubs |
| Pro | $250/mo | 30 | 5 | 40 | Adds branches, API Explorer, CI integration, rollback, automatic changelog |
| Custom | Contact | unlimited | unlimited | unlimited | SSO, reverse proxy, embed mode, custom analytics, 99.99% SLA |
| Open Source | Free (on application) | per Pro | per Pro | per Pro | Pro-equivalent for qualifying OSS projects |

## GitHub Org Highlights — github.com/bump-sh

- **`cli`** (TypeScript, MIT, 68★) — "Bump.sh CLI - Deploy your OpenAPI & AsyncAPI documentations from your CI"
- **`github-action`** (TypeScript, MIT, 47★) — "GitHub action to deploy your API documentation on Bump"
- **`flower-spec`** (Ruby, MIT) — "The flower specification to define API workflows"
- **`bump-ci-example`** (Shell) — multi-CI integration examples
- **`examples`** — curated public OpenAPI/AsyncAPI definitions
- **`docs`** — content hub for Bump.sh

## Links

- Website: https://bump.sh
- Documentation: https://docs.bump.sh
- API reference: https://developers.bump.sh
- GitHub: https://github.com/bump-sh
- Blog: https://bump.sh/blog
- Pricing: https://bump.sh/pricing
- Changelog: https://bump.sh/changelog
- Status: https://bumpsh.statuspage.io/

## Timestamps

- **Created:** 2026-03-16
- **Modified:** 2026-05-22

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
