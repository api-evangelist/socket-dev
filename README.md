# Socket (socket-dev)

Socket is a developer-first supply-chain security platform that protects applications from malicious dependencies, vulnerable packages, license risk, and software-supply-chain attacks across npm, PyPI, Go, Maven, Cargo, NuGet, RubyGems, and other open-source ecosystems. Socket ships a hosted API, CLI, MCP server, Firewall package-installer proxy (sfw), GitHub App, IDE extensions, SDKs, and reusable integrations for Jira, Slack, GitHub, GitLab, Bitbucket, Azure DevOps, and Microsoft Teams. The Socket API exposes 70+ alert categories — malware, typo- squats, install scripts, telemetry, native code, crypto wallets, suspicious network activity, license issues — plus full-scan reports with SBOM export (CycloneDX, SPDX, OpenVEX), diff scans for pull requests, a triage workflow, webhooks, and a real-time threat feed of newly discovered malicious packages.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/socket-dev/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/socket-dev/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Supply Chain Security
- Open Source Security
- Software Composition Analysis
- SCA
- Malware Detection
- Dependency Scanning
- SBOM
- npm
- PyPI
- Go
- Maven
- Cargo
- NuGet
- RubyGems
- Developer Security

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Socket Packages API

Look up risk scores, alerts, capabilities, license, and supply-chain metadata for any open-source package by Package URL (purl). Supports npm, PyPI, Go, Maven, Cargo, NuGet, RubyGems, and other ecosystems. The /purl endpoint accepts a list of package URLs and returns Socket's enriched package facts including capability use, telemetry, alert categories, and depscore.

- **Human URL:** [https://docs.socket.dev/reference/introduction-to-socket-api](https://docs.socket.dev/reference/introduction-to-socket-api)

#### Tags

- Packages
- Supply Chain Security
- Risk Scoring
- PURL

#### Properties

- [Documentation](https://docs.socket.dev/reference/introduction-to-socket-api)
- [OpenAPI](openapi/socket-packages-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-packages-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-packages-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/socket-package-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/socket-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Socket Full Scans API

Create, list, fetch, rescan, archive, and export full-scan reports for an organization's repos. Upload manifest files (package.json, requirements.txt, go.mod, pom.xml, Cargo.toml, etc.) and Socket returns a full dependency graph with alerts. Exports include CDX (CycloneDX), SPDX, OpenVEX, CSV, PDF, and GFM diff formats.

- **Human URL:** [https://docs.socket.dev/reference/createorgfullscan](https://docs.socket.dev/reference/createorgfullscan)

#### Tags

- Full Scans
- Supply Chain Security
- SBOM
- CycloneDX
- SPDX
- OpenVEX

#### Properties

- [Documentation](https://docs.socket.dev/reference/createorgfullscan)
- [OpenAPI](openapi/socket-full-scans-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-full-scans-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-full-scans-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/socket-full-scan-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Socket Diff Scans API

Compute and inspect diff scans between two full scans — the engine that powers Socket's pull-request comments. Identifies added, removed, and modified dependencies with their security implications. Returns added/removed alerts in JSON or GFM markdown. Diff scans can be created from full-scan IDs or from a target repo branch.

- **Human URL:** [https://docs.socket.dev/reference/createorgdiffscanfromids](https://docs.socket.dev/reference/createorgdiffscanfromids)

#### Tags

- Diff Scans
- Supply Chain Security
- Pull Request
- Change Detection

#### Properties

- [Documentation](https://docs.socket.dev/reference/createorgdiffscanfromids)
- [OpenAPI](openapi/socket-diff-scans-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-diff-scans-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-diff-scans-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Alerts API

Query current and historical security alerts for an organization across all scans, repos, and packages. Supports trend analysis, filtering by alert type and severity, and full-scan attribution. Backed by Socket's catalog of 70+ alert categories covering malware, typosquats, install scripts, telemetry, native code, crypto wallets, and other supply-chain risks.

- **Human URL:** [https://docs.socket.dev/reference/getorgalerts](https://docs.socket.dev/reference/getorgalerts)

#### Tags

- Alerts
- Supply Chain Security
- Historical Analytics

#### Properties

- [Documentation](https://docs.socket.dev/reference/getorgalerts)
- [OpenAPI](openapi/socket-alerts-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-alerts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-alerts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/socket-alert-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Socket Triage API

Triage workflow for alerts — list and update the disposition (ignore, acknowledge, escalate, allow) of any alert in an organization. Comments and decision history are recorded for audit. Triage is the human-in-the-loop counterpart to Socket's automated security gates.

- **Human URL:** [https://docs.socket.dev/reference/listorgtriagealerts](https://docs.socket.dev/reference/listorgtriagealerts)

#### Tags

- Triage
- Alerts
- Workflow
- Governance

#### Properties

- [Documentation](https://docs.socket.dev/reference/listorgtriagealerts)
- [OpenAPI](openapi/socket-triage-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-triage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-triage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Repos API

Manage the repositories Socket is monitoring inside an organization, plus repo labels for policy targeting. CRUD repos, attach/detach labels, and configure per-label settings that override organization-level security and license policies.

- **Human URL:** [https://docs.socket.dev/reference/getorgrepolist](https://docs.socket.dev/reference/getorgrepolist)

#### Tags

- Repositories
- Labels
- Organization

#### Properties

- [Documentation](https://docs.socket.dev/reference/getorgrepolist)
- [OpenAPI](openapi/socket-repos-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-repos-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-repos-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Organization Settings API

Configure Socket at the organization level — security policy (which alerts block/warn/ignore), license policy (allowed/denied SPDX identifiers), telemetry collection toggles, Socket Basics SAST/Secrets/Container scanning configuration, and integration event hooks for GitHub/GitLab/Bitbucket apps.

- **Human URL:** [https://docs.socket.dev/reference/getorgsecuritypolicy](https://docs.socket.dev/reference/getorgsecuritypolicy)

#### Tags

- Organization Settings
- Security Policy
- License Policy
- Telemetry

#### Properties

- [Documentation](https://docs.socket.dev/reference/getorgsecuritypolicy)
- [OpenAPI](openapi/socket-org-settings-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-org-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-org-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Webhooks API

Register, list, update, and delete webhooks that fire when scans complete, alerts trigger, triage decisions are made, or threat-feed entries match an organization's packages. Useful for connecting Socket to Slack, Jira, PagerDuty, or custom internal automation.

- **Human URL:** [https://docs.socket.dev/reference/listorgwebhooks](https://docs.socket.dev/reference/listorgwebhooks)

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://docs.socket.dev/reference/listorgwebhooks)
- [OpenAPI](openapi/socket-webhooks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-webhooks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-webhooks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Threat Feed API

Real-time feed of newly discovered malicious or suspicious packages across npm, PyPI, Go, RubyGems, and other ecosystems. Filter by ecosystem, alert type, and time window. Powers Socket's malware research dashboards and the public-disclosure firehose.

- **Human URL:** [https://docs.socket.dev/reference/getorgthreatfeed](https://docs.socket.dev/reference/getorgthreatfeed)

#### Tags

- Threat Feed
- Malware
- Real-Time Intelligence

#### Properties

- [Documentation](https://docs.socket.dev/reference/getorgthreatfeed)
- [OpenAPI](openapi/socket-threat-feed-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-threat-feed-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-threat-feed-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Fixes API

List available fixes — version bumps, patches, and overrides — for vulnerable or risky dependencies in an organization's scanned projects. Powers Socket's auto-fix pull-request generation.

- **Human URL:** [https://docs.socket.dev/reference/getorgfixes](https://docs.socket.dev/reference/getorgfixes)

#### Tags

- Fixes
- Remediation
- Patches

#### Properties

- [Documentation](https://docs.socket.dev/reference/getorgfixes)
- [OpenAPI](openapi/socket-fixes-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-fixes-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-fixes-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Dependencies API

Search and reverse-look-up dependencies across all of an organization's scanned repos. Find every project consuming a specific package and version, plus historical dependency-count trends used by Socket's analytics dashboards.

- **Human URL:** [https://docs.socket.dev/reference/searchdependencies](https://docs.socket.dev/reference/searchdependencies)

#### Tags

- Dependencies
- Search
- Reverse Lookup

#### Properties

- [Documentation](https://docs.socket.dev/reference/searchdependencies)
- [OpenAPI](openapi/socket-dependencies-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-dependencies-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-dependencies-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket API Tokens API

Provision, rotate, and revoke API tokens for an organization, inspect the caller's quota, and list the organizations the calling token has access to. Token-scoped permission grants are configured at creation and on update.

- **Human URL:** [https://docs.socket.dev/reference/getorgtokens](https://docs.socket.dev/reference/getorgtokens)

#### Tags

- API Tokens
- Authentication
- Administration
- Quota

#### Properties

- [Documentation](https://docs.socket.dev/reference/getorgtokens)
- [OpenAPI](openapi/socket-api-tokens-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-api-tokens-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-api-tokens-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Audit Log API

Append-only audit log of every administrative event in a Socket organization — policy changes, member changes, token actions, triage decisions, and integration changes. Use for compliance evidence and incident review.

- **Human URL:** [https://docs.socket.dev/reference/getauditlog](https://docs.socket.dev/reference/getauditlog)

#### Tags

- Audit Log
- Compliance
- Governance

#### Properties

- [Documentation](https://docs.socket.dev/reference/getauditlog)
- [OpenAPI](openapi/socket-audit-log-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-audit-log-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-audit-log-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Organization Snapshots API

Retrieve historical organization-level snapshots — point-in-time aggregations of dependencies, alerts, and risk metrics across all monitored repos. Used to populate trend dashboards and compliance posture reports.

- **Human URL:** [https://docs.socket.dev/reference/getorghistoricalsnapshots](https://docs.socket.dev/reference/getorghistoricalsnapshots)

#### Tags

- Snapshots
- Historical Analytics
- Reporting

#### Properties

- [Documentation](https://docs.socket.dev/reference/getorghistoricalsnapshots)
- [OpenAPI](openapi/socket-org-snapshots-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-org-snapshots-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-org-snapshots-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Socket Metadata API

Reference metadata for the Socket platform — the live machine-readable OpenAPI spec, the catalog of alert types and their severities, the catalog of license metadata used by license-policy, and the list of file types Socket can detect and scan.

- **Human URL:** [https://docs.socket.dev/reference/getalerttypes](https://docs.socket.dev/reference/getalerttypes)

#### Tags

- Metadata
- Reference Data
- OpenAPI

#### Properties

- [Documentation](https://docs.socket.dev/reference/getalerttypes)
- [OpenAPI](openapi/socket-metadata-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/socket-metadata-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/socket-metadata-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://socket.dev/)
- [Documentation](https://docs.socket.dev/)
- [Documentation](https://docs.socket.dev/reference/introduction-to-socket-api)
- [Getting Started](https://docs.socket.dev/docs/getting-started)
- [Authentication](https://docs.socket.dev/reference/authentication-types)
- [Sign Up](https://socket.dev/login)
- [Blog](https://socket.dev/blog)
- [Changelog](https://socket.dev/blog/categories/product-updates)
- [Status Page](https://status.socket.dev/)
- [Pricing](https://socket.dev/pricing)
- [Terms of Service](https://socket.dev/legal/terms)
- [Privacy Policy](https://socket.dev/legal/privacy)
- [Trust Center](https://socket.dev/legal/trust)
- [GitHub Organization](https://github.com/SocketDev)
- [LinkedIn](https://www.linkedin.com/company/socket-security)
- [Twitter](https://twitter.com/SocketSecurity)
- [SDK](https://github.com/SocketDev/socket-sdk-js)
- [SDK](https://github.com/SocketDev/socket-sdk-python)
- [Tool](https://github.com/SocketDev/socket-cli)
- [Tool](https://github.com/SocketDev/socket-python-cli)
- [Tool](https://github.com/SocketDev/socket-mcp)
- [Tool](https://github.com/SocketDev/sfw-free)
- [Tool](https://github.com/SocketDev/socket-vscode)
- [Tool](https://github.com/SocketDev/action)
- [Tool](https://github.com/SocketDev/socket-basics)
- [Tool](https://github.com/SocketDev/socket-patch)
- [Tool](https://github.com/SocketDev/socket-siem-connector)
- [Tool](https://github.com/SocketDev/bun-security-scanner)
- [Tool](https://github.com/SocketDev/socket-registry)
- [Tool](https://github.com/SocketDev/socket-config-js)
- [Integrations](https://github.com/apps/socket-security)
- [Integrations](https://docs.socket.dev/docs/gitlab-integration)
- [Integrations](https://docs.socket.dev/docs/bitbucket-integration)
- [Integrations](https://docs.socket.dev/docs/azure-devops-integration)
- [Integrations](https://docs.socket.dev/docs/jira-integration)
- [Integrations](https://docs.socket.dev/docs/slack-integration)
- [Integrations](https://docs.socket.dev/docs/microsoft-teams-integration)
- [OpenAPI](https://api.socket.dev/v0/openapi) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](plans/socket-dev-plans-pricing.yml)
- [Rate Limits](rate-limits/socket-dev-rate-limits.yml)
- [Fin Ops](finops/socket-dev-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** API Evangelist
**Email:** info@apievangelist.com
