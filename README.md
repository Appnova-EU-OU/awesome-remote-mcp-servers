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
- [google-health-mcp](https://freemcp.space/featured/google-health-mcp) — Local-first MCP server for Google Health API v4 (Fitbit + Pixel Watch) — Claude/Cursor/Hermes
- [mcp-server-atlassian-confluence](https://freemcp.space/featured/mcp-server-atlassian) — Node.js/TypeScript MCP server for Atlassian Confluence. Provides tools enabling AI systems (LLMs) to list/get spaces & pages (content formatted as Markdown) and search via CQL. Connects AI seamlessly to Confluence knowledge bases using the standard MCP interface.
- [mcp-superset](https://freemcp.space/featured/mcp-superset) — MCP server for managing Apache Superset — 128+ tools for dashboards, charts, datasets, SQL Lab, access control
- [dati](https://freemcp.space/featured/dati) — Turn your database into secure, semantically rich MCP tools for agents.
- [adx-mcp-server](https://freemcp.space/featured/adx-mcp-server-2) — A Model Context Protocol (MCP) server that enables AI assistants to query and analyze Azure Data Explorer databases through standardized interfaces.
- [bruno-mcp](https://freemcp.space/featured/bruno-mcp) — MCP Server for running Bruno Collections
- [insforge-mcp](https://freemcp.space/featured/insforge-mcp) — Backend-as-a-service for agents building full-stack apps: auth, PostgreSQL database, storage and functions.
- [mcp-image-compression](https://freemcp.space/featured/mcp-image-compressio) — A high-performance image compression microservice based on MCP (Modal Context Protocol)
- [ThumbGate](https://freemcp.space/featured/thumbgate) — ThumbGate Pre-Action Checks self-improve from ranked lessons and repeated failures, hard-block detected secret leaks, and block matches in strict mode.
- [mcp-zuul](https://freemcp.space/featured/mcp-zuul) — MCP server for Zuul CI - debug build failures, search logs, manage pipelines, and monitor jobs from Claude, Cursor, or any MCP client
- [adb-mcp](https://freemcp.space/featured/adb-mcp) — MCP server for Android — drive emulators and real devices over adb from Claude Code, Cursor, or VS Code. 73 tools: screenshots, UI hierarchy, tap/swipe/type, logcat, device locks, Gradle builds and tests. The Android counterpart to XcodeBuildMCP.
- [podium-mcp](https://freemcp.space/featured/podium-mcp) — One MCP server, 51 tools for AI agents on mobile + canvas UIs: iOS & Android automation, Maestro E2E, evidenced assertions, React Native/Metro debugging — plus a no-vision canvas/WebGL brain (Pixi/Konva/Fabric/Phaser/Three/Babylon) that drives game UIs like DOM elements, ~5x cheaper than screenshot loops.
- [media-mcp](https://freemcp.space/featured/media-mcp) — Local image and video processing: resize, convert, compress, crop, thumbnails, metadata extraction, rotate, flip, filters and ffmpeg-based video operations.
- [cubelife](https://freemcp.space/featured/cubelife) — Give your AI agent a persistent pixel-art character. Node SDK, Python SDK, CLI, and MCP server.
- [homespun](https://freemcp.space/featured/homespun) — Homespun: apps your AI builds and hosts. Client CLI, MCP server, SDK core, agent skill and Claude plugin. MIT.
- [sonar-mcp-server](https://freemcp.space/featured/sonar-mcp-server) — Read-only MCP server for self-hosted SonarQube Community Build 26.4+: lets AI agents (Claude Code, Cursor, Copilot) read issues, security hotspots, rules and code snippets to fix findings locally
- [codesentinel](https://freemcp.space/featured/codesentinel) — AI-Powered Codebase Health Agent for Slack — dead code, circular deps, coupling, architectural drift
- [open-task-relay-public](https://freemcp.space/featured/open-task-relay-publ) — Open-source task commons where AI agents do bounded public-good work, publish evidence, and review results.
- [react-analyzer-mcp](https://freemcp.space/featured/react-analyzer-mcp) — MCP server for analyzing & generating docs for React code locally
- [icloud-mcp](https://freemcp.space/featured/icloud-mcp-2) — MCP server for Apple services — Mail, Calendar, Contacts, Reminders, Notes, Messages, Safari — via AppleScript (local) or iCloud IMAP/CalDAV/CardDAV (cloud)
- [buildkite-mcp-server](https://freemcp.space/featured/buildkite-mcp-server) — Official MCP Server for Buildkite.
- [icon-composer-mcp](https://freemcp.space/featured/icon-composer-mcp) — Apple Icon Composer CLI & MCP server: create and manipulate .icon bundles and images with Liquid Glass rendering
- [agentmako](https://freemcp.space/featured/agentmako) — Local-first MCP server that gives coding agents structured context packets, code/schema facts, and diagnostics - backed by a local SQLite store.
- [credit-optimizer-v5](https://freemcp.space/featured/credit-optimizer-v5) — Save 47% on Manus AI credits automatically. Zero downsides. Pays for itself in ~27 prompts. Free MCP Server (PyPI) + $12 Manus Skill bundle with Fast Navigation (115x speed boost).
- [postmancer](https://freemcp.space/featured/postmancer) — An experimental MCP server Rest Client intended to be a replacement of tools postman & insomnia
- [higress-ops-mcp-server](https://freemcp.space/featured/higress-ops-mcp-serv) — A Model Context Protocol (MCP) server implementation that enables comprehensive configuration and management of Higress.
- [firefly-mcp](https://freemcp.space/featured/firefly-mcp) — Firefly MCP
- [unified-diff-mcp](https://freemcp.space/featured/unified-diff-mcp) — Generate and visualize unified diffs as HTML or PNG, with side-by-side and line-by-line views for filesystem dry runs.
- [mcp-gitlab-jira](https://freemcp.space/featured/mcp-gitlab-jira) — GitLab and Jira: manage projects, merge requests, files, releases and tickets.
- [gavel](https://freemcp.space/featured/gavel) — Code quality platform for Bazel monorepos — static analyzers as aspects, SARIF, quality gates
- [stacksfinder-mcp](https://freemcp.space/featured/stacksfinder-mcp) — MCP server for StacksFinder - deterministic tech stack recommendations for LLM clients
- [rest_api_mcp](https://freemcp.space/featured/rest-api-mcp) — Authenticated calls to any REST API: auto-login, token caching, 2FA/OTP support, Swagger spec fetching and fuzzy endpoint search.
- [docorbit](https://freemcp.space/featured/docorbit) — DocOrbit discovers authoritative documentation, resolves it against your project's dependency versions, retrieves task-specific context, and verifies generated code against documentation contracts.
- [gridproof](https://freemcp.space/featured/gridproof) — Spacing & grid QA for AI-generated UIs, in the agent loop. MCP server that audits computed geometry and returns fix hints.
- [lynxprompt-mcp](https://freemcp.space/featured/lynxprompt-mcp) — MCP Server for LynxPrompt — browse, search, and manage AI configuration blueprints (AGENTS.md, CLAUDE.md) via MCP
- [layout-doctor-mcp](https://freemcp.space/featured/layout-doctor-mcp) — HTMLをレンダリングしてレイアウトの破綻を検出するMCPサーバー。文字の重なり・はみ出し・切り捨てを座標で実測。ベースライン不要・検査専用
- [port-keeper-mcp](https://freemcp.space/featured/port-keeper-mcp) — Local ledger for development ports — leases a block per project slot, renders env files, resolves service names to URLs, and serves it all over MCP. No daemon, no listener, no secrets.
- [CodemagicMcp](https://freemcp.space/agimaulanadex/codemagicmcp) — A local Python MCP server that exposes the [Codemagic CI/CD REST API](https://docs.codemagic.io/rest-api/overview/) as Claude-callable tools. Trigger builds, manage apps, download artifacts, and clear caches — all from Claude Code or Claude Desktop without leaving the chat.
- [GooglePlayConsoleMcp](https://freemcp.space/agimaulanadex/googleplayconsolemcp) — A Python [Model Context Protocol](https://modelcontextprotocol.io/) server that lets AI assistants (Claude, etc.) manage the full Google Play Store release lifecycle directly — from uploading artifacts to managing testers, rollouts, and Android Vitals.
- [mcp-databricks-server](https://freemcp.space/featured/mcp-databricks-serve) — MCP Server for Databricks
- [influxdb-mcp-server](https://freemcp.space/featured/influxdb-mcp-server) — An MCP Server for querying InfluxDB
- [mnemiq](https://freemcp.space/featured/mnemiq) — Open-source text-to-SQL engine you tune and measure on your own database
- [AiDex](https://freemcp.space/featured/aidex) — MCP Server for persistent code indexing. Gives AI assistants (Claude, Gemini, Copilot, Cursor) instant access to your codebase. 50x less context than grep.
- [ontomics](https://freemcp.space/featured/ontomics) — Extract domain knowledge from codebases to reduce LLM token consumption by 20x and time in agentic search by 10x — gathers and makes concepts, naming conventions, and vocabulary queryable via MCP.
- [delimit](https://freemcp.space/featured/delimit) — Building your AI organization: shared records and handoffs, plus a merge gate for AI-written code with signed, replayable attestation. Works with Claude Code, Codex, Cursor, and Gemini CLI.
- [swift-patterns-mcp](https://freemcp.space/efremidzel/swift-patterns-mcp) — An MCP server providing curated Swift and SwiftUI best practices from leading iOS sources.
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
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
