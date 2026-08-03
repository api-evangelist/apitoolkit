# APIToolkit (Monoscope) (apitoolkit)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

APIToolkit (now Monoscope) is an open-source-friendly API observability and monitoring platform that helps teams find and fix production issues before customers notice. It unifies logs, traces, metrics, errors, monitors, and session replay across 17+ framework SDKs and 780+ OpenTelemetry integrations. The platform exposes a REST API (api.monoscope.tech/api/v1) for programmatic access to metrics, telemetry schema, and monitors, plus a hosted MCP server with ~50 auto-derived tools and workflow tools (analyze_issue, find_error_patterns, search_events_nl) and four Claude Code skills (investigate, triage, kql-reference, instrument) so agents can drive observability from the terminal or any LLM client. The apitoolkit.io domain now redirects to monoscope.tech.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/apitoolkit/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/apitoolkit/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI Observability
- API Analytics
- API Catalog
- API Management
- API Monitoring
- API Testing
- Breaking Change Detection
- CLI
- Debugging
- Error Tracking
- LLM Observability
- Logs and Traces
- MCP Server
- Metrics
- Monitors
- Observability
- OpenTelemetry
- Platform
- Session Replay

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-05-22

## APIs

### Monoscope Platform API

The Monoscope Platform REST API lets teams programmatically query metrics, retrieve telemetry schemas, and manage monitors per project. Authentication is via project-scoped Bearer API keys. Companion surfaces include native OpenTelemetry SDKs for 17+ frameworks, a CLI, a hosted MCP server, and Claude Code skills.

- **Human URL:** [https://monoscope.tech/](https://monoscope.tech/)
- **Base URL:** `https://api.monoscope.tech/api/v1`

#### Tags

- API Analytics
- API Catalog
- API Monitoring
- Breaking Change Detection
- Error Tracking
- Logs and Traces
- Metrics
- Monitors
- Observability
- OpenTelemetry
- Session Replay

#### Properties

- [Documentation](https://monoscope.tech/docs/)
- [Getting Started](https://monoscope.tech/docs/onboarding/)
- [SDK](https://monoscope.tech/docs/sdks/)
- [API Reference](https://monoscope.tech/docs/api-reference/)
- [Authentication](https://monoscope.tech/docs/api-reference/getting-started/authentication/)
- [Rate Limits](https://monoscope.tech/docs/api-reference/getting-started/rate-limits/)
- [Glossary](https://monoscope.tech/docs/glossary/)
- [F A Q](https://monoscope.tech/docs/faqs/)
- [OpenAPI](openapi/monoscope-platform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monoscope-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monoscope-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Spectral Rules](rules/monoscope-platform-rules.yml)
- [Capabilities](capabilities/monoscope-platform.yaml)
- [Vocabulary](vocabulary/apitoolkit-vocabulary.yml)
- [JSON-LD](json-ld/apitoolkit-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Monoscope MCP Server

Hosted Model Context Protocol endpoint exposing approximately 50 auto-derived REST tools plus workflow tools (analyze_issue, find_error_patterns, search_events_nl) under the same Bearer API key as the REST API. Lets any MCP-compatible LLM client drive observability workflows.

- **Human URL:** [https://monoscope.tech/docs/api-reference/mcp-server/](https://monoscope.tech/docs/api-reference/mcp-server/)

#### Tags

- AI Observability
- LLM Observability
- MCP Server
- Observability

#### Properties

- [Documentation](https://monoscope.tech/docs/api-reference/mcp-server/)
- [Source Code](https://github.com/monoscope-tech/skills)
- [Postman Collection](collections/monoscope-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monoscope-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monoscope CLI

Terminal-based client for Monoscope. Same auth, same primitives, same JSON as the REST API and MCP server. Drives investigate, triage, KQL, and instrumentation workflows from the shell.

- **Human URL:** [https://monoscope.tech/docs/onboarding/cli/](https://monoscope.tech/docs/onboarding/cli/)

#### Tags

- CLI
- Observability

#### Properties

- [Documentation](https://monoscope.tech/docs/onboarding/cli/)
- [Postman Collection](collections/monoscope-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monoscope-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Testkit (YAML API Testing DSL)

MIT-licensed Rust testing tool by the APItoolkit/Monoscope team that uses a simplified YAML DSL for defining API test scenarios and browser automation. Scripts persist in version control and can serve as both individual tests and load tests.

- **Human URL:** [https://github.com/monoscope-tech/testkit](https://github.com/monoscope-tech/testkit)

#### Tags

- API Testing
- Browser Automation
- CLI

#### Properties

- [Source Code](https://github.com/monoscope-tech/testkit)
- [Postman Collection](collections/monoscope-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monoscope-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TimeFusion (Timeseries Engine)

Rust-based timeseries database for events, logs, traces, and metrics using a PostgreSQL dialect over S3 / Delta Lake storage. Underpins Monoscope's affordable long-term retention and self-hosted offering.

- **Human URL:** [https://github.com/monoscope-tech/timefusion](https://github.com/monoscope-tech/timefusion)

#### Tags

- Database
- Open Source
- Storage

#### Properties

- [Source Code](https://github.com/monoscope-tech/timefusion)
- [Postman Collection](collections/monoscope-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monoscope-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Documentation](https://monoscope.tech/docs/)
- [Getting Started](https://monoscope.tech/docs/onboarding/)
- [API Reference](https://monoscope.tech/docs/api-reference/)
- [Authentication](https://monoscope.tech/docs/api-reference/getting-started/authentication/)
- [Rate Limits](https://monoscope.tech/docs/api-reference/getting-started/rate-limits/)
- [SDK](https://monoscope.tech/docs/sdks/)
- [Pricing](https://monoscope.tech/pricing/)
- [Status Page](https://status.monoscope.tech/)
- [Blog](https://monoscope.tech/blog/)
- [Integrations](https://monoscope.tech/integrations/)
- [GitHub Organization](https://github.com/monoscope-tech)
- [X (Twitter)](https://twitter.com/monoscope_tech)
- [LinkedIn](https://linkedin.com/company/monoscope)
- [YouTube](https://www.youtube.com/@Monoscope)
- [F A Q](https://monoscope.tech/docs/faqs/)
- [Glossary](https://monoscope.tech/docs/glossary/)
- [Source Code](https://github.com/monoscope-tech/monoscope)
- [License](undefined)
- [Plans](plans/apitoolkit-plans-pricing.yml)
- [Rate Limits](rate-limits/apitoolkit-rate-limits.yml)
- [Fin Ops](finops/apitoolkit-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [SDK](undefined)
- [Tools](undefined)
- [Blog](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
