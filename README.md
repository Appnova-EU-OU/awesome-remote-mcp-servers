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
- [CodemagicMcp](https://freemcp.space/agimaulanadex/codemagicmcp) — A local Python MCP server that exposes the [Codemagic CI/CD REST API](https://docs.codemagic.io/rest-api/overview/) as Claude-callable tools. Trigger builds, manage apps, download artifacts, and clear caches — all from Claude Code or Claude Desktop without leaving the chat.
- [GooglePlayConsoleMcp](https://freemcp.space/agimaulanadex/googleplayconsolemcp) — A Python [Model Context Protocol](https://modelcontextprotocol.io/) server that lets AI assistants (Claude, etc.) manage the full Google Play Store release lifecycle directly — from uploading artifacts to managing testers, rollouts, and Android Vitals.
- [mcp-databricks-server](https://freemcp.space/featured/mcp-databricks-serve) — MCP Server for Databricks
- [influxdb-mcp-server](https://freemcp.space/featured/influxdb-mcp-server) — An MCP Server for querying InfluxDB
- [mnemiq](https://freemcp.space/featured/mnemiq) — Open-source text-to-SQL engine you tune and measure on your own database
- [AiDex](https://freemcp.space/featured/aidex) — MCP Server for persistent code indexing. Gives AI assistants (Claude, Gemini, Copilot, Cursor) instant access to your codebase. 50x less context than grep.
- [ontomics](https://freemcp.space/featured/ontomics) — Extract domain knowledge from codebases to reduce LLM token consumption by 20x and time in agentic search by 10x — gathers and makes concepts, naming conventions, and vocabulary queryable via MCP.
- [delimit](https://freemcp.space/featured/delimit) — Building your AI organization: shared records and handoffs, plus a merge gate for AI-written code with signed, replayable attestation. Works with Claude Code, Codex, Cursor, and Gemini CLI.
- [swift-patterns-mcp](https://freemcp.space/featured/swift-patterns-mcp) — An MCP server providing curated Swift and SwiftUI best practices from leading iOS sources.
- [deploy-mcp](https://freemcp.space/featured/deploy-mcp) — Universal deployment tracker for AI assistants - check deployment status without leaving your AI chat
- [twitterapi-docs-mcp](https://freemcp.space/featured/twitterapi-docs-mcp) — TwitterAPI.io MCP server: offline docs (endpoints, pages, blogs) for Claude and other AI assistants.
- [endiagram-mcp](https://freemcp.space/featured/endiagram-mcp) — MCP server for EN Diagram — structural analysis for any system. Install: npx @endiagram/mcp
- [mcp-server-flipt](https://freemcp.space/featured/mcp-server-flipt) — Interact with feature flags in Flipt.
- [project-context-mcp](https://freemcp.space/featured/project-context-mcp) — Give Claude Code instant access to your project's institutional knowledge. Drop docs in .context/, mention them with @, and watch Claude become an expert on your codebase.
- [time-node-mcp](https://freemcp.space/featured/time-node-mcp) — MCP server for timezone-aware date and time operations
- [swagger-testcase-mcp](https://freemcp.space/featured/swagger-testcase-mcp) — MCP server for API testing: generates test cases, validates specs, compares versions, and creates mock data from Swagger/OpenAPI specifications
- [mcp-server](https://freemcp.space/featured/mcp-server-21) — MCP server that lets AI coding agents add smart-glasses capabilities to Android and iOS apps — scaffold, validate, and simulate before touching hardware
- [pox-mcp-server](https://freemcp.space/featured/pox-mcp-server) — A Model Context Protocol (MCP) server for the POX SDN controller
- [genable](https://freemcp.space/featured/genable) — Quality-first AI UI generator for Figma. Multi-protocol: Gemini · Claude · OpenAI-compatible.
- [creative-claw-marketplace](https://freemcp.space/featured/creative-claw-market) — Creative Claw: AI video, image and voiceover generation inside ChatGPT, Claude, Codex and Cursor. Seedance 2.5, Gemini Omni, Nano Banana 2, voice cloning. Pay as you go.
- [kiprio-mcp](https://freemcp.space/featured/kiprio-mcp) — MCP server exposing kiprio.com developer APIs (email/DNS/SSL/text/dev utilities) as tools for Claude, Cursor, and any MCP client.
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
- [HuaweiAppGalleryMcp](https://freemcp.space/agimaulanadex/huaweiappgallerymcp) — Huawei AppGallery Connect publishing: upload APK/AAB, update metadata and localizations, submit for review, and manage phased rollouts.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
