# Socket (socket-dev)
Socket is a developer-first supply-chain security platform that protects applications from malicious dependencies, vulnerable packages, license risk, and software-supply-chain attacks across npm, PyPI, Go, Maven, Cargo, NuGet, RubyGems, and other open-source ecosystems. Socket ships a hosted API, CLI, MCP server, Firewall package-installer proxy (sfw), GitHub App, IDE extensions, SDKs, and integrations for Jira, Slack, GitHub, GitLab, Bitbucket, Azure DevOps, and Microsoft Teams. The Socket API exposes 70+ alert categories — malware, typo-squats, install scripts, telemetry, native code, crypto wallets, suspicious network activity, license issues — plus full-scan reports with SBOM export (CycloneDX, SPDX, OpenVEX), diff scans for pull requests, a triage workflow, webhooks, and a real-time threat feed.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/socket-dev/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Supply Chain Security, Open Source Security, Software Composition Analysis, SCA, Malware Detection, Dependency Scanning, SBOM, npm, PyPI, Go, Maven, Cargo, NuGet, RubyGems, Developer Security

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Socket Packages API
Look up risk scores, alerts, capabilities, license, and supply-chain metadata for any open-source package by Package URL (purl). Supports npm, PyPI, Go, Maven, Cargo, NuGet, RubyGems, and other ecosystems.

**Human URL:** [https://docs.socket.dev/reference/introduction-to-socket-api](https://docs.socket.dev/reference/introduction-to-socket-api)

- [Documentation](https://docs.socket.dev/reference/introduction-to-socket-api)
- [OpenAPI](openapi/socket-packages-api-openapi.yml)
- [JSON Schema — Package](json-schema/socket-package-schema.json)
- [JSON-LD](json-ld/socket-context.jsonld)
- [Naftiko Capability — Packages (purl)](capabilities/packages-purl.yaml)

### Socket Full Scans API
Create, list, fetch, rescan, archive, and export full-scan reports for an organization's repos. Exports include CycloneDX, SPDX, OpenVEX, CSV, PDF, and GFM diff formats.

**Human URL:** [https://docs.socket.dev/reference/createorgfullscan](https://docs.socket.dev/reference/createorgfullscan)

- [OpenAPI](openapi/socket-full-scans-api-openapi.yml)
- [JSON Schema — Full Scan Artifact](json-schema/socket-full-scan-schema.json)
- [Naftiko Capability — Full Scans](capabilities/full-scans-full-scans.yaml)

### Socket Diff Scans API
Compute and inspect diff scans between two full scans — the engine that powers Socket's pull-request comments. Output JSON or GFM markdown.

**Human URL:** [https://docs.socket.dev/reference/createorgdiffscanfromids](https://docs.socket.dev/reference/createorgdiffscanfromids)

- [OpenAPI](openapi/socket-diff-scans-api-openapi.yml)
- [Naftiko Capability — Diff Scans](capabilities/diff-scans-diff-scans.yaml)

### Socket Alerts API
Query current and historical security alerts for an organization across all scans, repos, and packages. 70+ alert categories.

**Human URL:** [https://docs.socket.dev/reference/getorgalerts](https://docs.socket.dev/reference/getorgalerts)

- [OpenAPI](openapi/socket-alerts-api-openapi.yml)
- [JSON Schema — Alert](json-schema/socket-alert-schema.json)
- [Naftiko Capability — Alerts](capabilities/alerts-alerts.yaml)

### Socket Triage API
Triage workflow for alerts — list and update the disposition (ignore, acknowledge, escalate, allow) of any alert in an organization.

**Human URL:** [https://docs.socket.dev/reference/listorgtriagealerts](https://docs.socket.dev/reference/listorgtriagealerts)

- [OpenAPI](openapi/socket-triage-api-openapi.yml)
- [Naftiko Capability — Triage Alerts](capabilities/triage-alerts.yaml)

### Socket Repos API
Manage the repositories Socket is monitoring inside an organization plus repo labels for policy targeting.

**Human URL:** [https://docs.socket.dev/reference/getorgrepolist](https://docs.socket.dev/reference/getorgrepolist)

- [OpenAPI](openapi/socket-repos-api-openapi.yml)
- [Naftiko Capability — Repos](capabilities/repos-repos.yaml)
- [Naftiko Capability — Repo Labels](capabilities/repos-repo-labels.yaml)

### Socket Organization Settings API
Configure security policy, license policy, telemetry, Socket Basics, and integration event hooks at the organization level.

**Human URL:** [https://docs.socket.dev/reference/getorgsecuritypolicy](https://docs.socket.dev/reference/getorgsecuritypolicy)

- [OpenAPI](openapi/socket-org-settings-api-openapi.yml)
- [Naftiko Capability — Security Policy](capabilities/org-settings-security-policy.yaml)
- [Naftiko Capability — License Policy](capabilities/org-settings-license-policy.yaml)
- [Naftiko Capability — Telemetry](capabilities/org-settings-telemetry.yaml)
- [Naftiko Capability — Socket Basics](capabilities/org-settings-socket-basics.yaml)
- [Naftiko Capability — Integration Events](capabilities/org-settings-integration-events.yaml)

### Socket Webhooks API
Register webhooks for scan completion, alert generation, triage decisions, and threat-feed matches.

**Human URL:** [https://docs.socket.dev/reference/listorgwebhooks](https://docs.socket.dev/reference/listorgwebhooks)

- [OpenAPI](openapi/socket-webhooks-api-openapi.yml)
- [Naftiko Capability — Webhooks](capabilities/webhooks-webhooks.yaml)

### Socket Threat Feed API
Real-time feed of newly discovered malicious or suspicious packages across npm, PyPI, Go, RubyGems, and other ecosystems.

**Human URL:** [https://docs.socket.dev/reference/getorgthreatfeed](https://docs.socket.dev/reference/getorgthreatfeed)

- [OpenAPI](openapi/socket-threat-feed-api-openapi.yml)
- [Naftiko Capability — Threat Feed](capabilities/threat-feed-threat-feed.yaml)

### Socket Fixes API
List available fixes — version bumps, patches, and overrides — for vulnerable or risky dependencies. Powers Socket's auto-fix pull-request generation.

**Human URL:** [https://docs.socket.dev/reference/getorgfixes](https://docs.socket.dev/reference/getorgfixes)

- [OpenAPI](openapi/socket-fixes-api-openapi.yml)
- [Naftiko Capability — Fixes](capabilities/fixes-fixes.yaml)

### Socket Dependencies API
Search and reverse-look-up dependencies across all of an organization's scanned repos, plus historical dependency-count trends.

**Human URL:** [https://docs.socket.dev/reference/searchdependencies](https://docs.socket.dev/reference/searchdependencies)

- [OpenAPI](openapi/socket-dependencies-api-openapi.yml)
- [Naftiko Capability — Dependencies Search](capabilities/dependencies-search.yaml)

### Socket API Tokens API
Provision, rotate, and revoke API tokens for an organization; inspect quota; list accessible organizations.

**Human URL:** [https://docs.socket.dev/reference/getorgtokens](https://docs.socket.dev/reference/getorgtokens)

- [OpenAPI](openapi/socket-api-tokens-api-openapi.yml)
- [Naftiko Capability — API Tokens](capabilities/api-tokens-api-tokens.yaml)
- [Naftiko Capability — Organizations](capabilities/api-tokens-organizations.yaml)

### Socket Audit Log API
Append-only audit log of every administrative event in a Socket organization — policy changes, member changes, token actions, triage decisions, and integration changes.

**Human URL:** [https://docs.socket.dev/reference/getauditlog](https://docs.socket.dev/reference/getauditlog)

- [OpenAPI](openapi/socket-audit-log-api-openapi.yml)
- [Naftiko Capability — Audit Log](capabilities/audit-log-audit-log.yaml)

### Socket Organization Snapshots API
Retrieve historical organization-level snapshots — point-in-time aggregations of dependencies, alerts, and risk metrics across all monitored repos.

**Human URL:** [https://docs.socket.dev/reference/getorghistoricalsnapshots](https://docs.socket.dev/reference/getorghistoricalsnapshots)

- [OpenAPI](openapi/socket-org-snapshots-api-openapi.yml)
- [Naftiko Capability — Snapshots](capabilities/org-snapshots-snapshots.yaml)

### Socket Metadata API
Reference metadata for the Socket platform — the live OpenAPI spec, alert-type catalog, license-metadata catalog, and supported-files list.

**Human URL:** [https://docs.socket.dev/reference/getalerttypes](https://docs.socket.dev/reference/getalerttypes)

- [OpenAPI](openapi/socket-metadata-api-openapi.yml)
- [Naftiko Capability — Metadata](capabilities/metadata-alert-types.yaml)

## Common Properties

- [Portal](https://socket.dev/)
- [Documentation](https://docs.socket.dev/)
- [Documentation — Introduction to Socket API](https://docs.socket.dev/reference/introduction-to-socket-api)
- [Getting Started](https://docs.socket.dev/docs/getting-started)
- [Authentication](https://docs.socket.dev/reference/authentication-types)
- [Sign Up](https://socket.dev/login)
- [Blog](https://socket.dev/blog)
- [Changelog](https://socket.dev/blog/categories/product-updates)
- [Status](https://status.socket.dev/)
- [Pricing](https://socket.dev/pricing)
- [Terms of Service](https://socket.dev/legal/terms)
- [Privacy Policy](https://socket.dev/legal/privacy)
- [Trust Center](https://socket.dev/legal/trust)
- [GitHub Organization](https://github.com/SocketDev)
- [LinkedIn](https://www.linkedin.com/company/socket-security)
- [Twitter](https://twitter.com/SocketSecurity)
- [Live OpenAPI](https://api.socket.dev/v0/openapi)

### SDKs and Tooling

- [JavaScript / TypeScript SDK (`@socketsecurity/sdk`)](https://github.com/SocketDev/socket-sdk-js)
- [Python SDK](https://github.com/SocketDev/socket-sdk-python)
- [Socket CLI](https://github.com/SocketDev/socket-cli)
- [Socket Python CLI](https://github.com/SocketDev/socket-python-cli)
- [Socket MCP Server](https://github.com/SocketDev/socket-mcp)
- [Socket Firewall (sfw-free)](https://github.com/SocketDev/sfw-free)
- [Socket VSCode Extension](https://github.com/SocketDev/socket-vscode)
- [Socket GitHub Action](https://github.com/SocketDev/action)
- [Socket Basics (SAST + Secrets + Container)](https://github.com/SocketDev/socket-basics)
- [Socket Patch CLI](https://github.com/SocketDev/socket-patch)
- [Socket SIEM Connector](https://github.com/SocketDev/socket-siem-connector)
- [Bun Security Scanner](https://github.com/SocketDev/bun-security-scanner)
- [Socket Optimize (registry overrides)](https://github.com/SocketDev/socket-registry)
- [Socket Config (socket.yml)](https://github.com/SocketDev/socket-config-js)

### Integrations

- [GitHub App](https://github.com/apps/socket-security)
- [GitLab Integration](https://docs.socket.dev/docs/gitlab-integration)
- [Bitbucket Integration](https://docs.socket.dev/docs/bitbucket-integration)
- [Azure DevOps Integration](https://docs.socket.dev/docs/azure-devops-integration)
- [Jira Integration](https://docs.socket.dev/docs/jira-integration)
- [Slack Integration](https://docs.socket.dev/docs/slack-integration)
- [Microsoft Teams Integration](https://docs.socket.dev/docs/microsoft-teams-integration)

## Commercial Surface

- [Plans](plans/socket-dev-plans-pricing.yml)
- [Rate Limits](rate-limits/socket-dev-rate-limits.yml)
- [FinOps](finops/socket-dev-finops.yml)

## Features

- Socket API — supply-chain risk data via Package URL (purl) across npm, PyPI, Go, Maven, Cargo, NuGet, RubyGems, and others
- Full Scans — repository-wide dependency graph and alert reports with SBOM export (CycloneDX, SPDX, OpenVEX, CSV, PDF)
- Diff Scans — pull-request-aware comparison between two full scans, output as JSON or GFM markdown comment
- Triage workflow — list and update disposition (ignore, acknowledge, escalate, allow) for alerts at scale
- Historical alerts, dependencies, and snapshots — long-window trend analytics for posture reporting
- Threat Feed — real-time discovery of malicious and suspicious packages across ecosystems
- Fixes — version bumps, patches, and overrides for vulnerable dependencies, including auto-PR generation
- 70+ alert categories — malware, typosquats, install scripts, telemetry, native code, crypto wallets, supply-chain risks
- Security and license policies per organization with per-repo label overrides
- Webhooks for scan completion, alert generation, triage events, and threat-feed matches
- Socket Firewall — registry proxy and `sfw` runtime that prevents installation of malicious packages
- Socket CLI (JavaScript + Python) for scanning, fixing, and config validation
- Socket MCP Server — Model Context Protocol server exposing Socket data to AI agents
- Socket Optimize — drop-in package overrides for npm/pnpm/yarn
- Socket Basics — bundled SAST + Secrets + Container scanning
- Socket VS Code extension and Socket GitHub Action for in-editor and in-CI security gates
- GitHub, GitLab, Bitbucket, Azure DevOps, Jira, Slack, and Microsoft Teams integrations
- SDKs for JavaScript / TypeScript and Python
- Append-only audit log of every administrative action
- Live OpenAPI spec served from `https://api.socket.dev/v0/openapi`

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
