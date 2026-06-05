# APIToolkit (Monoscope) (apitoolkit)

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
