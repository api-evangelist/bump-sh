# Bump.sh (bump-sh)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
