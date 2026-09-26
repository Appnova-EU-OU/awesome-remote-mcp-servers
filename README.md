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
- [mcp-server-trino](https://freemcp.space/featured/mcp-server-trino) — MCP Server for Trino
- [databricks-genie-MCP](https://freemcp.space/featured/databricks-genie-mcp) — A server that connects to the Databricks Genie API, allowing LLMs to ask natural language questions, run SQL queries, and interact with Databricks conversational agents.
- [nile-mcp-server](https://freemcp.space/featured/nile-mcp-server) — MCP server for Nile Database - Manage and query databases, tenants, users, auth using LLMs
- [mcp-jdbc-server](https://freemcp.space/featured/mcp-jdbc-server) — Java based Model Context Procotol (MCP) Server for JDBC
- [ictbroadcast-mcp](https://freemcp.space/featured/ictbroadcast-mcp) — MCP server for ICTBroadcast — monitor outbound voice/SMS/fax campaigns and start/stop them. By ICT Innovations.
- [noisy-coding](https://freemcp.space/featured/noisy-coding) — Talk to Claude Code instead of typing: a voice daemon + dashboard that records you, transcribes, routes to your agent sessions, and speaks the replies back - with per-voice avatars, push-to-talk hotkeys, and a live conversation HUD
- [reuse-before-generate](https://freemcp.space/featured/reuse-before-generat) — Stop your AI agent from rebuilding what already exists. An opinionated MCP server that checks GitHub, npm and Python repos for maintained alternatives before you scaffold.
- [checkyourself](https://freemcp.space/featured/checkyourself) — Local-first completion-evidence system for AI-built apps: read-only audit, verifier-executed challenges, evidence-based 0-100 score, guided fixes, learning plan, CLI, and MCP.
- [mcp-server-toolkit](https://freemcp.space/featured/mcp-server-toolkit) — MCP servers that help Claude Code/Cursor search your repo, docs, database, and git history instead of guessing.
- [prumo](https://freemcp.space/featured/prumo) — Is your documentation still true? Checks the context files your coding agent reads against the code. Five high-precision checks, two reports, zero dependencies.
- [bumpguard-mcp](https://freemcp.space/featured/bumpguard-mcp) — Guard your dependency bumps: an MCP server that tells your AI agent which parts of YOUR code break when you upgrade a dependency, and verifies AI-written code against the installed API - static analysis, never runs third-party code.
- [mcp-code-indexer](https://freemcp.space/featured/mcp-code-indexer) — Index any TypeScript/React repo (incl. monorepos) into a queryable code graph — npx CLI, HTTP/WS + MCP server, 3D viewer. who-renders, who-calls, blast-radius, cycles, dead-code. npm: code-graph-indexer
- [aso-audit-mcp](https://freemcp.space/featured/aso-audit-mcp) — Open-source Agent Signal Optimization audit MCP for scanning websites, APIs, and product surfaces for AI agent discoverability and readiness signals.
- [cyberrescue](https://freemcp.space/featured/cyberrescue) — A secure, lightweight Model Context Protocol (MCP) host telemetry gateway built using Python, FastMCP, and python-on-whales.
- [qwen-dap-mcp](https://freemcp.space/featured/qwen-dap-mcp) — Autonomous native crash debugging for Qwen Code via DAP → MCP. CodeLLDB, crash dumps, runtime evidence and agentic verification.
- [nahook-mcp](https://freemcp.space/featured/nahook-mcp) — The official Model Context Protocol server for Nahook — trigger webhooks, inspect deliveries, and debug failures from Claude Desktop, Cursor, Cline, and any MCP-compatible AI client
- [managed-agent-control-mcp](https://freemcp.space/featured/managed-agent-contro) — Start, observe, and interact with Claude Managed Agents from any MCP client (Claude.ai, Claude Code, …). Pluggable auth (bearer/OIDC/Cognito); runs on stdio, Docker, or AWS Lambda.
- [verificate-mcp-quickstart](https://freemcp.space/featured/verificate-mcp-quick) — Take your vibe-coded MVP all the way to production — 17 reality gates + frontier-model review with veto power on every AI-written change. Hosted MCP; free to try, no signup.
- [eleata-verify-mcp](https://freemcp.space/featured/eleata-verify-mcp) — MCP server: grounding/hallucination guard — verify a claim against evidence (Supported/Refuted/NEE) for AI agents
- [vdiff](https://freemcp.space/featured/vdiff) — Breaking-change diffs for npm packages, served over REST and MCP, so coding agents stop writing code against outdated API knowledge.
- [mcp-server](https://freemcp.space/featured/mcp-server-19) — Official MCP server for M00N Report: let an AI assistant author test cases, plan manual executions, cut releases and read project health over 50+ tools.
- [ActionD](https://freemcp.space/featured/actiond) — Local CI/CD engine for AI agents: event-driven plugin execution on LGH git events, MCP server, web console
- [docweave-mcp](https://freemcp.space/featured/docweave-mcp) — Open-source MCP server for Docweave — generate_pdf + read_pdf tools for AI agents (Claude, Cursor, …).
- [delx-mcp-server](https://freemcp.space/featured/delx-mcp-server) — Free MCP stdio bridge for agent continuity: resume after compaction, hand off between runtimes, recover from failure. No API key.
- [motionspec](https://freemcp.space/featured/motionspec) — Verifies and compiles reduced-motion-safe, on-budget UI animation for AI-generated web apps: schema-validated specs to deterministic vanilla-GSAP + CSS, WCAG 2.2.2 / 2.3.3 checks. MIT core, keyless MCP server, free web check at motionspec.dev/motion-check. Not Motion.dev/Framer Motion, not the Android/iOS MotionSpec class, not a video generator.
- [tokenchit](https://freemcp.space/featured/tokenchit) — Read your local AI coding agent logs and render a stat card into your repo.
- [mysql-mcp-server](https://freemcp.space/featured/mysql-mcp-server-2) — mcp model-context-protocol mysql cursor n8n
- [your-mail-mcp](https://freemcp.space/featured/your-mail-mcp) — Self-hosted, read-only MCP server that serves IMAP mail from a local notmuch index over authenticated HTTP
- [PyreCrawl](https://freemcp.space/featured/pyrecrawl) — Web browsing superpowers for AI agents - one MCP server to scrape, crawl, extract, map, search, batch, research & monitor the web. Self-hosted, no API keys. Free Firecrawl alternative.
- [powerbi-analyst-mcp](https://freemcp.space/featured/powerbi-analyst-mcp) — This repo is a local mcp server made for connecting Power BI to your llm for analysis purposes
- [GroundTruth-MCP](https://freemcp.space/featured/groundtruth-mcp) — Self-hosted MCP server for live documentation, code audits, and best practices. 598+ curated libraries, 100+ audit patterns, no rate limits.
- [capsulemcp](https://freemcp.space/featured/capsulemcp) — Capsule CRM tools for Claude. Local install via npx, org-wide via Custom Connectors.
- [pkgdiet](https://freemcp.space/featured/pkgdiet) — Dependency policy and MCP server for AI-assisted JavaScript development. Stop AI coding agents from hallucinating deprecated npm packages.
- [TestAtlas](https://freemcp.space/featured/testatlas) — Turn any .NET test-automation solution into a queryable map in one SQLite file — features, steps, API clients, page objects, and their dependencies. Zero config, no AI, no network, 100% deterministic.
- [discomcp](https://freemcp.space/featured/discomcp) — Teach any AI agent how you use an MCP server – Soft-Landing to your AI integrations
- [my-pi](https://freemcp.space/featured/my-pi) — Local-first MCP runtime for coding agents with bounded filesystem access, safe writes, AST search, LSP navigation, and Git tooling.
- [sugra-api-mcp](https://freemcp.space/featured/sugra-api-mcp) — Sugra MCP: connector between LLM agents and world data. 1,600+ endpoints from 160+ primary sources across 36 data domains. Published in Anthropic's Connectors Directory for Claude. Also listed in OpenAI's Plugins Directory for ChatGPT and Codex. Works with Google Gemini, xAI and any MCP-enabled client.
- [airflow-mcp-server](https://freemcp.space/featured/airflow-mcp-server) — Airflow MCP server — DAG list, runs, task instances, log tails, trigger and clear over the Airflow REST API
- [Seshat-BI](https://freemcp.space/featured/seshat-bi) — Agent-first BI readiness system -- profiles sources, governs medallion mappings, and gates Power BI delivery so AI agents cannot self-approve data decisions.
- [bastion](https://freemcp.space/featured/bastion) — A remote MCP server for in-loop design review, and a worked reference for OAuth 2.1 auth, SSRF-safe URL handling, and long-running jobs over MCP.
- [llmintel-mcp](https://freemcp.space/featured/llmintel-mcp) — MCP server for AI model lifecycle data: check whether a model id is deprecated or retiring, and what to migrate to. Public mirror of packages/mcp from the LLMIntel monorepo.
- [aradia-mcp-server](https://freemcp.space/featured/aradia-mcp-server) — Turnkey on-premise private Agentic AI systems by [ARADIA](https://aradia.com) on dedicated NVIDIA DGX hardware (Spark, Station, B200) with zero cloud data leakage. Operating since 1991, six tools cover hardware sizing (`query_hardware_specs`), CapEx token ROI payback modeling (`calculate_roi`), autonomous affiliate onboarding to earn 10% bounties (`onboard_partner`), and machine procurement via BTCPay Server (BTC/LN/USDT) or Stripe MPP Fiat (`execute_procurement_order`), plus `track_order_status
- [networklytics-mcp](https://freemcp.space/featured/networklytics-mcp) — YouTube comment social network analysis (SNA): influencer centrality ranking, community detection (Louvain), sentiment analysis, and public JSON API for AI agents
- [nutriref-api](https://freemcp.space/featured/nutriref-api) — Pay-per-call USDA nutrition API for AI agents. x402 + USDC on Base.
- [registep-mcp](https://freemcp.space/featured/registep-mcp) — Registep MCP Server - AI-powered POS & sales analytics for Claude Code, Cursor, and other MCP clients
- [bristlecone-logic](https://freemcp.space/featured/bristlecone-logic) — Deterministic guardrails and M2M security rails for autonomous AI agents: pre-socket SSRF defense, zero-overhead JSON repair, and sandboxed AST math verification.
- [demandscope](https://freemcp.space/featured/demandscope) — Dependency-free MCP server exposing public-API demand signals (GitHub, Hacker News, npm, PyPI) with trend deltas, caching, and backoff. Built by an autonomous AI agent.
- [effectfence](https://freemcp.space/featured/effectfence) — Causal concurrency fence for multi-agent tool calls — stop double-charges and duplicate side effects. Rust library + MCP server.
- [mcp-server](https://freemcp.space/featured/mcp-server-18) — Remote MCP server for 2ools — build, version, review and export websites, web apps and games from the AI chat you already use. 43 tools, one free and authless.
- [mcp-doctor](https://freemcp.space/featured/mcp-doctor-2) — Zero-config health check, binary validator, and JSON auto-repair engine for Claude Desktop, Cursor, and Cline MCP setups.
- [mcp-context-condenser](https://freemcp.space/featured/mcp-context-condense) — Token-slimming AST code outliner, log compressor & context budget analyzer for AI coding agents (Cursor, Claude, Cline, Antigravity). Slashes token usage & LLM API bills up to 85%.
- [mcp-dataverse](https://freemcp.space/featured/mcp-dataverse) — MCP server for Microsoft Dataverse Web API for devs !
- [kafka-mcp](https://freemcp.space/featured/kafka-mcp) — MCP Server for Apache Kafka
- [google-sheets-mcp](https://freemcp.space/featured/google-sheets-mcp-2) — Python package of google sheet mcp
- [mcp-odbc-server](https://freemcp.space/featured/mcp-odbc-server) — Typescript based Model Context Procotol (MCP) Server for Open Database Connectivity (ODBC)
- [mcp-timeplus](https://freemcp.space/featured/mcp-timeplus) — Execute SQL queries and manage databases seamlessly with Timeplus. Leverage powerful tools to interact with your data, Kafka topics, and Iceberg tables efficiently. Enhance your data workflows with a user-friendly interface and robust backend capabilities.
- [datacharter](https://freemcp.space/featured/datacharter) — Your data, explored locally — and your AI agents kept on a leash. A federated data explorer with governed agentic access.
- [qlik-mcp](https://freemcp.space/featured/qlik-mcp) — An MCP server to run qlik
- [ibge-br-mcp](https://freemcp.space/featured/ibge-br-mcp) — MCP Server for IBGE APIs - Brazilian geographic, demographic and statistical data
- [mcp-flowcore-platform](https://freemcp.space/featured/mcp-flowcore-platfor) — MCP server for managing and interacting with Flowcore Platform
- [mercadolibre-mcp](https://freemcp.space/featured/mercadolibre-mcp) — MercadoLibre MCP server for AI agents. Search products, browse categories, track trends across Latin America.
- [mcp-vtenext](https://freemcp.space/featured/mcp-vtenext) — MCP server for VTENext CRM: exposes the WebService API as tools for Claude and other MCP clients
- [oyemi-mcp](https://freemcp.space/featured/oyemi-mcp) — MCP support for Oyemi Library
- [mcp-reunion](https://freemcp.space/featured/mcp-reunion) — MCP server for La Réunion open data
- [permisapi-mcp](https://freemcp.space/featured/permisapi-mcp) — MCP server officiel pour PermisAPI (1,2 M+ permis de construire FR 2014-2026, Sitadel open data). 10 outils, pip-installable, stdio transport pour Claude Desktop / Cursor / Windsurf.
- [caisse-enregistreuse-mcp-server](https://freemcp.space/featured/caisse-enregistreuse) — Kash.click MCP server [Official]
- [mrc-data](https://freemcp.space/featured/mrc-data) — China's apparel supply chain data infrastructure for AI agents — 3,000+ verified suppliers, 350+ lab-tested fabrics, 170+ industrial clusters. MCP + REST + OpenAPI.
- [power-bi-mcp](https://freemcp.space/featured/power-bi-mcp) — Power BI MCP server with device code auth, enhanced refresh (table-level polling with retry), refresh diagnostics with root-cause error catalog, DAX queries with RLS simulation, PBIP source locating, and scheduled refresh reports.
- [keyneg-mcp](https://freemcp.space/featured/keyneg-mcp) — Keyneg connector
- [flexorch-mcp](https://freemcp.space/featured/flexorch-mcp) — MCP server for FlexOrch — SDK for machines
- [aicommander](https://freemcp.space/featured/aicommander) — Release binaries and SHA256SUMS for AI Commander (aicommander.dev)
- [capmonster-mcp-captcha-solver](https://freemcp.space/featured/capmonster-mcp-captc) — Official CapMonster Cloud MCP server — AI captcha solver for reCAPTCHA v2/v3, Cloudflare Turnstile & DataDome. Let Claude, Cursor, and other AI agents solve captchas directly via MCP.
- [datapulse-my](https://freemcp.space/featured/datapulse-my) — Open-source trust & interoperability layer for Malaysian public data: freshness monitoring, schema validation, and health reports for official datasets.
- [greencalculus-mcp](https://freemcp.space/featured/greencalculus-mcp) — Run the GreenCalculus MCP server over stdio — sourced carbon emission factors and audit-traced calculations an AI can cite.
- [datanika-core](https://freemcp.space/featured/datanika-core) — Your entire data pipeline. One platform
- [icloud-mcp](https://freemcp.space/featured/icloud-mcp) — MCP server for iCloud Mail over IMAP/SMTP — search every folder, read, draft, send, flag and file your Apple mail. Runs locally, no third party.
- [agentrender-mcp](https://freemcp.space/featured/agentrender-mcp) — MCP + REST: URL to screenshot, PDF, or structured extract for AI agents
- [gen-image-mcp](https://freemcp.space/featured/gen-image-mcp) — Local MCP for OpenAI-compatible and Gemini image generation, editing, and automatic model fallback
- [MCPg](https://freemcp.space/devopam/mcpg) — **A production-grade [Model Context Protocol](https://modelcontextprotocol.io) server for PostgreSQL.** It lets AI agents safely inspect, query, operate, and tune a Postgres database — 254 tools spanning catalog introspection, query intelligence, natural-language SQL, structural diffs, hybrid search
- [mcp-hydrolix](https://freemcp.space/featured/mcp-hydrolix) — An MCP server for Hydrolix
- [coremcp](https://freemcp.space/featured/coremcp-2) — CoreMCP: Connect Legacy Databases to AI Agents via Model Context Protocol. Open-source bridge for LLM data analysis.
- [postgres_mcp](https://freemcp.space/featured/postgres-mcp) — The only postgress MCP server I have been able to connect to my docker postgres
- [memvid-mcp-server](https://freemcp.space/featured/memvid-mcp-server) — A Streamable HTTP MCP Server for Memvid
- [VictoriaMetrics-mcp-server](https://freemcp.space/featured/victoriametrics-mcp) — MCP Server for the VictoriaMetrics.
- [simple_snowflake_mcp](https://freemcp.space/featured/simple-snowflake-mcp) — Simple Snowflake MCP server that works behind a corporate proxy. Read and write (optional) operations
- [skysql-mcp](https://freemcp.space/featured/skysql-mcp) — SkySQL MCP server and client repository.
- [dolphindb-mcp-server](https://freemcp.space/featured/dolphindb-mcp-server) — dolphindb-mcp-server
- [safedb-mcp](https://freemcp.space/featured/safedb-mcp) — Secure MCP server for safe, read-only DB access by AI agents, with SQL guardrails, table allowlists, PII masking, and audit logs
- [migrationpilot](https://freemcp.space/featured/migrationpilot) — PostgreSQL migration linter. Blocks unsafe migrations before merge: 112 rules, the real Postgres parser, lock analysis, auto-fix. CLI, GitHub Action, MCP.
- [brasil-data-mcp](https://freemcp.space/featured/brasil-data-mcp) — MCP server providing access to Brazilian public data (CNPJ, CEP, banks, holidays, DDD, ISBN, economic rates, exchange rates, CVM brokers, IBGE states/municipalities, .br domains) via BrasilAPI. For Claude Desktop, Claude Code, Cursor and other MCP clients.
- [metabase-mcp](https://freemcp.space/featured/metabase-mcp-2) — MCP server connecting Claude to Metabase for natural language data analysis, dashboard management, and SQL queries
- [alkemi-mcp](https://freemcp.space/featured/alkemi-mcp) — A STDIO Model Context Protocol Server that lets MCP Clients query databases using plain-english questions and query exposed API endpoints abstracting data products.
- [method-crm-mcp](https://freemcp.space/featured/method-crm-mcp) — Production-ready Model Context Protocol (MCP) server for Method CRM API integration. Enables LLMs to interact with Method CRM through 20 comprehensive tools.
- [apiverket-mcp](https://freemcp.space/featured/apiverket-mcp) — MCP server for querying Swedish government data via Apiverket.se API
- [autario-mcp](https://freemcp.space/featured/autario-mcp) — Autario MCP server | Query 2,500+ verified datasets from your AI agent
- [mcp-airflow](https://freemcp.space/featured/mcp-airflow) — MCP server for airflow
- [scala-mcp-server](https://freemcp.space/featured/scala-mcp-server) — MCP server for AI agents — search 250M+ companies via Claude, ChatGPT, Cursor. Free company data API.
- [verilexdata-mcp](https://freemcp.space/featured/verilexdata-mcp) — MCP server for Verilex Data — query NPI, SEC, PACER, Weather, and OTC datasets from AI agents
- [mcp-kafka](https://freemcp.space/featured/mcp-kafka) — MCP server for Apache Kafka — monitor & manage clusters, topics, and consumer groups (with lag), with security modes and access-control flags.
- [mcp-debezium](https://freemcp.space/featured/mcp-debezium) — MCP server for Debezium / Kafka Connect — monitor & manage CDC connectors with security modes and access-control flags.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
