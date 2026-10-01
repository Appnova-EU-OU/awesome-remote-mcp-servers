# Awesome Remote MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Connect your AI assistant to the world — no installs, no Docker, no config files.

Remote MCP servers are accessible via a URL. Paste the endpoint into your AI client and start using it immediately.

**→ Want to host your own?** [freemcp.space](https://freemcp.space) deploys any MCP server from a Dockerfile or GitHub repo in seconds.

---

## Registry Structure

This repository now maintains a **machine-readable registry** of MCP servers under `servers/<category>/`. Each server is a JSON file validated against `schemas/server.schema.json`. The registry is automatically synced to [freemcp.space](https://freemcp.space) so every listed server can be deployed in one click.

### Categories

| Category | Description |
|----------|-------------|
| `ai-agents` | AI agents, browser automation, reasoning tools |
| `cloud-infra` | Cloud platforms, CDN, serverless, infrastructure |
| `communication` | Email, messaging, notifications |
| `databases` | Databases, ORMs, query engines |
| `data-processing` | ETL, analytics, data transformation |
| `developer-tools` | Git, APIs, SDKs, developer utilities |
| `media` | Image, video, audio processing |
| `productivity` | Task management, calendars, workspace tools |
| `search` | Web search, semantic search, knowledge retrieval |
| `security` | Auth, secrets, scanning, compliance |

### Submit a Server

1. Create a JSON file under `servers/<category>/<server-name>.json`
2. Validate against the schema:  
   `check-jsonschema --schemafile schemas/server.schema.json your-file.json`
3. Open a Pull Request — CI will verify the JSON and check that the `git_url` is reachable.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for full details.

### One-Click Deploy

Every server in this registry can be deployed instantly on freemcp.space:

```
https://freemcp.space/featured/<slug>
```

---

## How to Connect

Most AI clients support remote MCP via SSE or HTTP. Add the server URL in your client settings:

| Client | Where to add |
|--------|-------------|
| Claude Desktop | `claude_desktop_config.json` → `url` field |
| Cursor | Settings → MCP → Add Server URL |
| Windsurf | MCP Config → Remote |
| Continue.dev | `config.json` → mcpServers |

---

## Contents

- [Platforms & Hosting](#platforms--hosting)
- [Code & Development](#code--development)
- [Data & Search](#data--search)
- [Productivity & Workspace](#productivity--workspace)
- [Cloud Infrastructure](#cloud-infrastructure)
- [Finance & Payments](#finance--payments)
- [Communication](#communication)
- [AI & Models](#ai--models)

---

## Badge Guide

| Badge | Meaning |
|-------|---------|
| 🆓 | Free tier available |
| 💰 | Paid only |
| 🔑 | API key required |
| 🌐 | Open source |
| ✅ | Verified working (April 2026) |

---

## Platforms & Hosting

---

## Hosted on freemcp.space

<!-- freemcp:start -->
- [bitrise-mcp](https://freemcp.space/featured/bitrise-mcp-2) — MCP Server for the Bitrise API, enabling app management, build operations, artifact management and more.
- [open-code-review](https://freemcp.space/featured/open-code-review) — 🤖 AI code quality gate for AI-generated code. Detects hallucinated packages, phantom dependencies, stale APIs, and more. MCP Server + CLI + CI/CD Action.
- [package-registry-mcp](https://freemcp.space/featured/package-registry-mcp) — MCP server for searching and getting up-to-date information about NPM, Cargo, PyPi, and NuGet packages.
- [codelogic-mcp-server](https://freemcp.space/featured/codelogic-mcp-server) — An MCP Server to utilize Lineai's rich software dependency data in your AI programming assistant.
- [apisix-mcp](https://freemcp.space/featured/apisix-mcp) — APISIX Model Context Protocol (MCP) server is used to bridge large language models (LLMs) with the APISIX Admin API.
- [influxdb3_mcp_server](https://freemcp.space/featured/influxdb3-mcp-server) — MCP Server for InfluxDB 3
- [teamcity-mcp](https://freemcp.space/featured/teamcity-mcp) — Model Context Protocol (MCP) server for JetBrains TeamCity: control builds, tests, agents and configs from AI coding assistants.
- [aibolit-mcp-server](https://freemcp.space/featured/aibolit-mcp-server-2) — MCP Server for Aibolit Java Static Analyzer: Helping Your AI Agent Identify Hotspots for Refactoring
- [currents-mcp](https://freemcp.space/featured/currents-mcp) — Currents MCP Server
- [patchloom](https://freemcp.space/featured/patchloom) — Structured file edits for AI agents (JSON/YAML/TOML, markdown, AST, dry-run, MCP). Not a generic filesystem MCP.
- [mcp-server](https://freemcp.space/featured/mcp-server-20) — Official ConfigCat Model Context Protocol (MCP) Server 
- [context-rot-detection](https://freemcp.space/featured/context-rot-detectio) — Context Rot Detection & Healing MCP Service — gives AI agents self-awareness about their cognitive state
- [bldbl-mcp](https://freemcp.space/featured/bldbl-mcp-2) — Buildable development platform: manage tasks, track progress, get project context and collaborate with humans on software projects.
- [conan-mcp](https://freemcp.space/featured/conan-mcp) — Model Context Protocol server for Conan
- [api-testing-mcp](https://freemcp.space/featured/api-testing-mcp) — The most complete MCP server for API testing. 27 tools: requests, assertions, flows, OpenAPI, mock data, load testing, collections, environments, cURL export, response diffing. Zero config, zero dependencies.
- [cursor-usage](https://freemcp.space/featured/cursor-usage) — Ask your AI agent about your team's Cursor spending. MCP server + Cursor plugin + Claude Code plugin wrapping the full Cursor Enterprise API.
- [tuning-engines-cli](https://freemcp.space/featured/tuning-engines-cli) — CLI & MCP server for Tuning Engines — fine-tune LLMs on code repositories
- [claudecodenavi-mcp](https://freemcp.space/featured/claudecodenavi-mcp-2) — ClaudeCodeNavi MCP Server - Claude Code knowledge platform & marketplace
- [chatpipe-mcp](https://freemcp.space/featured/chatpipe-mcp) — Publish live web pages from your AI coding agent — instant shareable URLs from your terminal.
- [codesign](https://freemcp.space/featured/codesign) — CoDesign gives AI agents like Claude Code, Codex and PI a real design engine for genuine, editable designs, not flat images. Bring in what you have: InDesign, Photoshop, PowerPoint and PDF files stay editable. Exports print-ready PDFs with CMYK and bleed. Every design opens in a built-in editor for manual fixes. Runs on your machine, no account.
- [mcp-server-couchbase](https://freemcp.space/featured/mcp-server-couchbase) — Model Context Protocol server for Couchbase - connect AI agents and LLMs like Claude, Cursor, and Copilot to Couchbase/Capella
- [app-publish-mcp](https://freemcp.space/featured/app-publish-mcp) — Unified MCP server for App Store Connect & Google Play Console — 91 tools for listings, screenshots, releases, reviews & submissions
- [roku-dev-studio](https://freemcp.space/featured/roku-dev-studio) — Cross-platform Electron desktop studio for Roku developers: remote control, device queries, sideload, telnet console, RALE/App Connector, BrightScript Fiddle, JSON Action Scripts, an `rds` CLI, an MCP server for AI agents, and an internet relay.
- [dynatrace-managed-mcp](https://freemcp.space/featured/dynatrace-managed-mc) — An MCP server for self-hosted Dynatrace Managed platform
- [kafka-schema-reg-mcp](https://freemcp.space/featured/kafka-schema-reg-mcp) — A comprehensive Message Control Protocol (MCP) server for Kafka Schema Registry.
- [code-context](https://freemcp.space/featured/code-context) — Retrieval + inference offload for AI coding agents.
- [docguard](https://freemcp.space/featured/docguard) — Audit and enforce canonical project documentation for AI-assisted development. Detect drift, validate specs, and brief agents. Part of the Guard family with TestGuard and WebSec Validator.
- [mcp-database-server](https://freemcp.space/featured/mcp-database-server) — Store and load JSON documents from LLM tool use
- [ydb-mcp](https://freemcp.space/featured/ydb-mcp) — Interact with YDB databases.
- [mcp-code-runner](https://freemcp.space/featured/mcp-code-runner) — Run code in multiple programming languages locally via Docker.
- [agent-skill-loader](https://freemcp.space/featured/agent-skill-loader) — MCP server to expose Claude Code Skills to AI agents
- [fastmcp-sonarqube-metrics](https://freemcp.space/featured/fastmcp-sonarqube-me) — Chat with your SonarQube data: explore metrics, compare trends, and track issues—effortlessly.
- [memorydetective](https://freemcp.space/featured/memorydetective) — MCP server for iOS leak hunting and performance investigation. 28 MCP tools, 34-pattern retain-cycle classifier with Swift fixTemplate snippets, compareTracesByPattern for CI gating, SourceKit-LSP source bridging. Reads .memgraph and .trace files; macOS only.
- [echo-mcp](https://freemcp.space/featured/echo-mcp) — Enable AI assistants to interact with your Echo API 
- [python-docs-mcp-server](https://freemcp.space/featured/python-docs-mcp-serv) — Read-only MCP server for official Python docs: local index, no API keys, exact symbol lookup, version-aware retrieval.
- [openapi-to-mcp](https://freemcp.space/featured/openapi-to-mcp-2) — OpenApiMCPServer is an MCP server that automatically converts any OpenAPI/Swagger specification into a set of usable MCP tools
- [squiggles](https://freemcp.space/featured/squiggles) — MCP server that lets your coding agent see the squiggles — LSP diagnostics, navigation, refactoring, and each server's custom superpowers
- [jenkins-mcp-server](https://freemcp.space/featured/jenkins-mcp-server) — An MCP server for interacting with a Jenkins server. Allows you to trigger jobs, check build statuses, and manage your Jenkins instance through MCP.
- [codex-pets](https://freemcp.space/astandrik/codex-pets) — Community gallery, CLI, and MCP service for Codex-compatible animated pets, backed by YDB.
- [resharper-cli-mcp](https://freemcp.space/featured/resharper-cli-mcp) — MCP server wrapping JetBrains' ReSharper CLI for headless C# inspection and code cleanup for coding agents. Unofficial, not affiliated with JetBrains.
- [featureflip-mcp](https://freemcp.space/featured/featureflip-mcp) — MCP server for Featureflip — manage feature flags from AI agents and editors (read-only mirror)
- [SchemaCrawler-MCP-Server-Usage](https://freemcp.space/featured/schemacrawler-mcp-se) — Find out how to use SchemaCrawler AI MCP Server
- [pgtuner_mcp](https://freemcp.space/featured/pgtuner-mcp) — provides AI-powered PostgreSQL performance tuning capabilities.
- [greptimedb-mcp-server](https://freemcp.space/featured/greptimedb-mcp-serve) — A Model Context Protocol (MCP) server for GreptimeDB
- [agrobr-mcp](https://freemcp.space/featured/agrobr-mcp) — MCP server for Brazilian agricultural data — connect LLMs to 10 public data sources via agrobr
- [hono-telescope](https://freemcp.space/featured/hono-telescope) — Laravel Telescope-style debugging for Hono — plus an MCP server so your AI agent can read the app's live requests, exceptions and queries
- [simctl-mcp](https://freemcp.space/featured/simctl-mcp) — Control the iOS Simulator.
- [skill-ninja-mcp-server](https://freemcp.space/featured/skill-ninja-mcp-serv) — MCP Server for Agent Skill Ninja - Search, Install, and Manage Agent Skills
- [MCP_AI_SOC_Sher](https://freemcp.space/featured/mcp-ai-soc-sher) — AI SOC  Security Threat analysis using  MCP Server 
- [webhook-tester-mcp](https://freemcp.space/featured/webhook-tester-mcp) — FastMCP server for managing and testing webhooks via webhook-test.com API
- [mobile-easy-use](https://freemcp.space/featured/mobile-easy-use) — Runtime access for AI coding agents to observe and control Android and iOS apps. 
- [wopee-mcp](https://freemcp.space/featured/wopee-mcp) — Autonomous web app testing: run test cases in real browsers with pass/fail results and screenshots, and generate user stories, test cases and Playwright code.
- [cws-mcp](https://freemcp.space/featured/cws-mcp) — MCP server for Chrome Web Store — upload, publish, status, metadata & Playwright-based UI automation
- [desktopinsights-mcp](https://freemcp.space/featured/desktopinsights-mcp) — MCP server for desktopinsights.com
- [ellmos-codecommander-mcp](https://freemcp.space/featured/ellmos-codecommander) — Developer-focused MCP server with 23 tools for Python code analysis, structural editing, JSON repair, imports, encoding, Markdown/PDF export, diffs, and regex testing
- [server](https://freemcp.space/featured/server) — MCP server that teaches any AI agent the AIDE spec methodology — progressive   disclosure specs alongside code
- [bigindexer](https://freemcp.space/featured/bigindexer) — BGI tries to group code based on what the code actually does (its behavior), not just which file imports what.
- [adr-mcp-setup](https://freemcp.space/featured/adr-mcp-setup) — Generates Architecture Decision Records from Claude Code conversations, with quality review, duplicate detection, a dependency graph and stale ADR alerts.
- [atlassian-browser-mcp](https://freemcp.space/featured/atlassian-browser-mc-2) — Browser-backed MCP server wrapping mcp-atlassian with Playwright SSO auth for Atlassian Server/Data Center
- [imagcon-mcp](https://freemcp.space/featured/imagcon-mcp) — MCP server for Imagcon — generate deployment-ready PWA, iOS, and Android app icon sets from a text description
- [telos](https://freemcp.space/featured/telos) — Build shared AI workspaces for creation, simulation, verification, MCP tools, and replayable receipts.
- [codelattice](https://freemcp.space/featured/codelattice) — 面向 AI 编程的本地代码图谱分析工具
- [defluff](https://freemcp.space/featured/defluff) — Deterministic slop detector for AI-generated prose. No model, no API key.
- [npm-mcp](https://freemcp.space/featured/npm-mcp) — MCP server for npm package management — 32 tools for publish, install, audit, search, security & more
- [omni-dev](https://freemcp.space/featured/omni-dev) — AI-powered git commit rewriter, PR generator, and MCP server for Jira, Confluence, and Datadog. Single Rust binary.
- [kilo-kit-mcp](https://freemcp.space/featured/kilo-kit-mcp) — An MCP server for safer coding agents: skill routing, C4 workflow gates, memory checks, and verification before completion.
- [DevProjex](https://freemcp.space/featured/devprojex) — Build safe, token-efficient codebase context for LLMs, AI chats, and coding agents — local-first GUI, TUI, CLI, and a read-only MCP server with Smart Ignore, secret/PII redaction, Git scopes, and code compression.
- [dbconvert-streams-public](https://freemcp.space/dbconvert/dbconvert-streams-pu) — DBConvert Streams: Database IDE, Federated SQL, Real-time CDC & AI assistants via MCP — explore, query, and replicate data across databases and files
- [mcp-sqlalchemy-server](https://freemcp.space/featured/mcp-sqlalchemy-serve) — A simple MCP ODBC server using FastAPI, ODBC and SQLAlchemy.
- [fable-mode](https://freemcp.space/featured/fable-mode) — Open-source MCP control plane for AI coding agents: mechanical time-locks, evidence-gated proof receipts, red-team remediation, and persistent engineering memory.
- [primitiv](https://freemcp.space/featured/primitiv) — The design system infrastructure keeping teams and agents in sync.
- [aspnetcore-debugger-mcp](https://freemcp.space/featured/aspnetcore-debugger) — MCP server that lets AI agents (Claude, Cursor) debug your .NET / ASP.NET Core app
- [ios-mcp-code-quality-server](https://freemcp.space/featured/ios-mcp-code-quality) — This server enables AI assistants to run Xcode tests, perform linter analysis, and provide detailed feedback on iOS projects through structured, actionable reports.
- [codebeamer-mcp](https://freemcp.space/featured/codebeamer-mcp-2) — Codebeamer ALM: read and write work items, trackers, projects, associations, references, comments and risk management data via the REST API.
- [ai-dev-analytics](https://freemcp.space/featured/ai-dev-analytics-2) — An open-source AI coding observability layer. Silently tracks vibe coding sessions via MCP and codifies AI deviations into project rules. 100% local.
- [studiomcphub](https://freemcp.space/featured/studiomcphub) — Creative AI MCP server — 32 tools (18 free): image generation, upscaling, bg removal, mockups, CMYK, print-ready PDF, vectorization, watermarking, enrichment, provenance. Pay per call via x402/Stripe/GCX.
- [agent-utils-mcp](https://freemcp.space/featured/agent-utils-mcp-2) — Utility tools with x402 micropayments: JSON validation, base64, hashing, UUIDs, regex testing, Markdown and datetime conversion, cron parsing and JWT decoding.
- [wp-cli-mcp](https://freemcp.space/featured/wp-cli-mcp) — MCP server that gives AI tools full WordPress management via WP-CLI — 30+ tools for themes, plugins, posts, menus, users, database, and scaffolding
- [HuaweiAppGalleryMcp](https://freemcp.space/featured/huaweiappgallerymcp) — Huawei AppGallery Connect publishing: upload APK/AAB, update metadata and localizations, submit for review, and manage phased rollouts.
- [agent-gate](https://freemcp.space/featured/agent-gate) — MCP server that adds a fail-closed quality gate and hash-chained receipt ledger to any AI agent workflow.
- [elementor-mcp-agent](https://freemcp.space/featured/elementor-mcp-agent) — Agency-grade MCP server for WordPress Elementor — multi-site management, safe Elementor data editing, template export/import, version tracking. MIT.
- [mcp-devtools](https://freemcp.space/featured/mcp-devtools) — AI-native developer tools via MCP — filesystem, databases, processes and OpenAPI for any MCP-compatible agent
- [4DA](https://freemcp.space/featured/4da) — Privacy-first developer intelligence — surfaces what matters from the noise
- [codebase-agent-mcp](https://freemcp.space/featured/codebase-agent-mcp) — A sub-harness (both an MCP server and an MCP client). Delegates documentation and source code analysis, as well as interactions with related context-providing MCP servers, to a local or inexpensive OpenAI-compatible LLM. Drastically reduces token usage and context size for coding agents on the top-tier LLM.
- [briefkit-mcp-server](https://freemcp.space/featured/briefkit-mcp-server) — BriefKit — Engineer-grade specs for AI-built SaaS. 14 files. $9. briefkit.online
- [mcp-agent-health](https://freemcp.space/featured/mcp-agent-health) — MCP server for AOS-compliant agent health reporting (P2 · advisory)
- [mcp-blast-radius](https://freemcp.space/featured/mcp-blast-radius) — MCP Blast-Radius Auditor — static blast radius extraction and CI divergence gate for MCP servers.
- [mobius-mcp](https://freemcp.space/featured/mobius-mcp) — MCP server + skill file for Sweipe/FlatMobile WordPress sites (agent REST surface)
- [wordpress-mcp-agent-bridge](https://freemcp.space/featured/wordpress-mcp-agent) — WordPress MCP + REST bridge for AI agents — verified Rank Math SEO and schema writes, hashed snapshots, verified restore, additive-only gates. Claude Code, Cursor, any MCP client. Pairs with EMCP.
- [selvedge](https://freemcp.space/featured/selvedge) — Decision provenance for AI-coded codebases: the why, and what was already tried and rejected.
- [dbt-docs-mcp](https://freemcp.space/featured/dbt-docs-mcp) — MCP (model context protocol) server for interacting with dbt Docs
- [mcp-postgres-server](https://freemcp.space/featured/mcp-postgres-server) — MCP server for PostgreSQL. Works with VS Code, Cursor, Claude Code, Codex, and Windsurf.
- [davinci-resolve-ai-bridge-mcp](https://freemcp.space/featured/davinci-resolve-ai-b) — DaVinci Resolve (Free Version and Studio) MCP server for Claude, Cursor, Codex, and Antigravity. Full timeline editing, cuts, camera zoom, and color grading.
- [mcp-swiss](https://freemcp.space/featured/mcp-swiss) — Swiss open data MCP server — transport, weather, geodata, companies, etc,. Zero API keys.
- [mcp-libsql](https://freemcp.space/featured/mcp-libsql) — Secure MCP server for libSQL databases with comprehensive tools, connection pooling, and transaction support. Built with TypeScript for Claude Desktop, Claude Code, Cursor, and other MCP clients.
- [rag-rat](https://freemcp.space/featured/rag-rat) — Local repo-intelligence index + MCP server: semantic search, symbol/graph navigation, impact-surface preflight, git + GitHub papertrail, and a source-anchored memory graph.
- [druid-mcp-server](https://freemcp.space/featured/druid-mcp-server) — A comprehensive Model Context Protocol (MCP) server for Apache Druid that provides extensive tools, resources, and AI-assisted prompts for managing and analyzing Druid clusters. Built with Spring Boot and Spring AI, this server enables seamless integration between AI assistants and Apache Druid through standardized MCP protocol.
- [axint](https://freemcp.space/featured/axint) — Proof and repair for Apple coding agents. Validate Swift, run Xcode evidence, repair failures, and generate inspectable Apple-native capabilities.
- [etincel](https://freemcp.space/featured/etincel) — Find the AI tells in your prose. Deterministic, local, runs in CI. MCP server + CLI + Action.
- [mason](https://freemcp.space/featured/mason) — A context engineer MCP for your AI agents. Stops agents from writing code with outdated instructions.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
