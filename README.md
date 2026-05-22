# APIToolkit / Monoscope (apitoolkit)

APIToolkit (now Monoscope) is an open-source-friendly API observability and monitoring platform that helps teams find and fix production issues before customers notice. It unifies logs, traces, metrics, errors, monitors, and session replay across 17+ framework SDKs and 780+ OpenTelemetry integrations. The platform exposes a REST API at `api.monoscope.tech/api/v1` for programmatic access to metrics, telemetry schema, and monitors, plus a hosted MCP server (~50 auto-derived tools + workflow tools `analyze_issue`, `find_error_patterns`, `search_events_nl`) and four Claude Code skills (`investigate`, `triage`, `kql-reference`, `instrument`) so agents can drive observability from the terminal or any LLM client.

**URL:** [https://monoscope.tech/](https://monoscope.tech/) (apitoolkit.io now redirects here)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- AI Observability, API Analytics, API Catalog, API Management, API Monitoring, API Testing, Breaking Change Detection, CLI, Debugging, Error Tracking, LLM Observability, Logs and Traces, MCP Server, Metrics, Monitors, Observability, OpenTelemetry, Platform, Session Replay

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-05-22

## APIs

### Monoscope Platform API

Public REST API at `https://api.monoscope.tech/api/v1` for querying metrics, retrieving telemetry schema, and listing monitors per project. Authentication is via project-scoped Bearer API key.

- [Documentation](https://monoscope.tech/docs/)
- [API Reference](https://monoscope.tech/docs/api-reference/)
- [Authentication](https://monoscope.tech/docs/api-reference/getting-started/authentication/)
- [Rate Limits](https://monoscope.tech/docs/api-reference/getting-started/rate-limits/)
- [SDKs](https://monoscope.tech/docs/sdks/)
- [OpenAPI](openapi/monoscope-platform-openapi.yml)
- [Spectral Rules](rules/monoscope-platform-rules.yml)
- [Capabilities](capabilities/monoscope-platform.yaml)

### Monoscope MCP Server

Hosted Model Context Protocol endpoint with ~50 auto-derived REST tools plus workflow tools (`analyze_issue`, `find_error_patterns`, `search_events_nl`).

### Monoscope CLI

Terminal client sharing auth and primitives with the REST API and MCP server.

### Testkit

YAML-based DSL (Rust, MIT) for API testing and browser automation by the APIToolkit / Monoscope team. [github.com/monoscope-tech/testkit](https://github.com/monoscope-tech/testkit)

### TimeFusion

Rust timeseries database (PostgreSQL dialect + S3 / Delta Lake) underpinning long-term retention. [github.com/monoscope-tech/timefusion](https://github.com/monoscope-tech/timefusion)

## Common Properties

- [Documentation](https://monoscope.tech/docs/)
- [Getting Started](https://monoscope.tech/docs/onboarding/)
- [API Reference](https://monoscope.tech/docs/api-reference/)
- [SDKs](https://monoscope.tech/docs/sdks/)
- [Pricing](https://monoscope.tech/pricing/)
- [Status Page](https://status.monoscope.tech/) (updown.io)
- [Blog](https://monoscope.tech/blog/)
- [Integrations](https://monoscope.tech/integrations/)
- [GitHub Organization](https://github.com/monoscope-tech)
- [Source Code (AGPL-3.0)](https://github.com/monoscope-tech/monoscope)
- [Glossary](https://monoscope.tech/docs/glossary/)
- [FAQ](https://monoscope.tech/docs/faqs/)

## Plans

| Tier | Price | Included | Retention | Support |
|------|-------|----------|-----------|---------|
| Monoscope Cloud | $29/mo | 20M events/mo (+$1 per 1M) | 30 days | Community + Email |
| Monoscope Cloud + Your Own S3 | $199/mo | 100M events/mo (+$1 per 1M) | Unlimited (BYO S3) | Priority |
| Self-Hosted Community | Free (AGPL-3.0) | Unlimited | Custom | Community |
| Self-Hosted Enterprise | From $500/mo | Unlimited | Custom | Enterprise / SLA |

See [plans/apitoolkit-plans-pricing.yml](plans/apitoolkit-plans-pricing.yml).

## Rate Limits

| Tier | Limit | Burst |
|------|-------|-------|
| Free | 60 req/min | 10 |
| Pro | 300 req/min | 50 |
| Enterprise | Custom | Custom |

Signaled via `X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset`; 429 on exceed. See [rate-limits/apitoolkit-rate-limits.yml](rate-limits/apitoolkit-rate-limits.yml).

## FinOps

Usage-based ($1 per 1M events overage) with FOCUS-aligned columns. See [finops/apitoolkit-finops.yml](finops/apitoolkit-finops.yml).

## Features

| Name | Description |
|------|-------------|
| Error Tracking | Catch breaking changes and critical errors in real time before customers notice. |
| Logs and Traces | Unified view correlating logs with trace breakdowns and request timelines. |
| API Analytics | Identify trends and monitor API performance metrics that matter to your business. |
| API Catalog and Docs | Dynamic catalog with up-to-date documentation and developer onboarding. |
| Metrics and Dashboards | Custom metrics tracking with real-time data visualization, pre-built templates per stack. |
| Performance Monitoring | Monitor APIs, databases, and services with uptime tracking. |
| Monitors and Healthchecks | Automated uptime tracking and early failure detection with threshold and interval-based monitors. |
| Alerts and Notifications | Real-time alerts routed to Slack, PagerDuty, email, and webhooks. |
| Anomaly Detection | Real-time API change detection and automated monitoring of unusual traffic. |
| Breaking Change Detection | Identify API schema and contract changes in real time. |
| Session Replay | Watch user sessions that triggered errors for root-cause analysis. |
| AI-Powered Natural Language Query | Ask questions in plain English via `search_events_nl` and get instant answers. |
| AI Agents | AI agents analyze logs, metrics, events, and API traffic in real time. |
| Weekly Reports | AI-generated summaries of new errors, regressions, and anomalies. |
| MCP Server | Hosted Model Context Protocol endpoint with ~50 auto-derived REST tools and workflow tools. |
| Claude Code Skills | Drop-in skills (investigate, triage, kql-reference, instrument) wrapping the CLI. |
| CLI | Terminal-based queries, log tailing, request tracing, and resource management. |
| KQL Query Language | Kusto-style query language for searching events, logs, and traces. |

## Use Cases

| Name | Description |
|------|-------------|
| Real-Time Error Detection | Detect and debug API errors in production before they impact end users. |
| API Performance Optimization | Monitor and optimize API performance with analytics and trend identification. |
| Third-Party Integration Monitoring | Monitor third-party API dependencies and detect breaking changes automatically. |
| Incident Response | Correlate logs, traces, and errors for faster root-cause analysis and incident resolution. |
| API Contract Monitoring | Continuously monitor API contracts for compliance and detect schema drift. |
| Agent-Driven Observability | Let LLM agents query, triage, and remediate via the MCP server and Claude Code skills. |
| API Testing in CI | Run Testkit YAML scenarios against APIs as part of CI pipelines and load testing. |

## SDKs

| Name | Repo | Notes |
|------|------|-------|
| monoscope-go | [monoscope-tech/monoscope-go](https://github.com/monoscope-tech/monoscope-go) | Gin, Echo, Fiber, Chi, Gorilla Mux, native net/http. MIT. |
| monoscope-python | [monoscope-tech/monoscope-python](https://github.com/monoscope-tech/monoscope-python) | Django, FastAPI, Flask, Pyramid. MIT. |
| monoscope-js | [monoscope-tech/monoscope-js](https://github.com/monoscope-tech/monoscope-js) | Shared TypeScript for Node/Browser SDKs. |
| monoscope-laravel | [monoscope-tech/monoscope-laravel](https://github.com/monoscope-tech/monoscope-laravel) | Laravel / PHP. |
| monoscope-web | [monoscope-tech/monoscope-web](https://github.com/monoscope-tech/monoscope-web) | Browser SDK + session replay. |
| apitoolkit-dotnet | [monoscope-tech/apitoolkit-dotnet](https://github.com/monoscope-tech/apitoolkit-dotnet) | ASP.NET Core. |

## Tools

| Name | Repo | Notes |
|------|------|-------|
| monoscope (platform) | [monoscope-tech/monoscope](https://github.com/monoscope-tech/monoscope) | Open-source Haskell observability platform. AGPL-3.0. |
| TimeFusion | [monoscope-tech/timefusion](https://github.com/monoscope-tech/timefusion) | Rust timeseries DB (PostgreSQL + S3 / Delta Lake). |
| Testkit | [monoscope-tech/testkit](https://github.com/monoscope-tech/testkit) | YAML DSL for API testing and browser automation. MIT. |
| Claude Code Skills | [monoscope-tech/skills](https://github.com/monoscope-tech/skills) | investigate, triage, kql-reference, instrument. |
| OpenTelemetry Demo | [monoscope-tech/opentelemetry-demo](https://github.com/monoscope-tech/opentelemetry-demo) | Demo integration patterns. |

## Integrations

Node.js, Python, Go, Java, .NET, PHP, Elixir, Browser/Web, Flutter, PostgreSQL, MongoDB, MySQL, Redis, Elasticsearch, Kafka, RabbitMQ, Kubernetes, Docker, NGINX, HAProxy, AWS, Google Cloud, Azure, Prometheus, Jaeger, Zipkin, Datadog, New Relic, Splunk, OpenTelemetry (780+), Slack, PagerDuty, MCP / Model Context Protocol, Claude Code.

## Artifacts

- `openapi/monoscope-platform-openapi.yml`
- `rules/monoscope-platform-rules.yml`
- `capabilities/monoscope-platform.yaml`, `capabilities/incident-triage.yaml`, `capabilities/api-performance-review.yaml`, `capabilities/shared/monoscope-platform-shared.yaml`
- `json-schema/monoscope-platform-monitor-schema.json`, `monoscope-platform-metric-point-schema.json`, `monoscope-platform-schema-field-schema.json`
- `json-structure/monoscope-platform-monitor-structure.json`, `monoscope-platform-metric-point-structure.json`
- `json-ld/apitoolkit-context.jsonld`
- `vocabulary/apitoolkit-vocabulary.yml`
- `examples/monoscope-platform-queryMetrics-example.json`, `monoscope-platform-getTelemetrySchema-example.json`, `monoscope-platform-listMonitors-example.json`, `monoscope-platform-monitor-example.json`
- `plans/apitoolkit-plans-pricing.yml`, `rate-limits/apitoolkit-rate-limits.yml`, `finops/apitoolkit-finops.yml`

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
