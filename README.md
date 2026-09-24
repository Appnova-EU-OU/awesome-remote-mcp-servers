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
- [erp-report-engine](https://freemcp.space/featured/erp-report-engine) — A provably read-only SQL layer for AI agents (MCP) and weekly reports — over the database behind an ERP (Logo Tiger, Netsis, Mikro). Statement-checking guard, measured against 28 attacks.
- [Litescope](https://freemcp.space/featured/litescope) — The operations toolchain for production SQLite — diff, migrate, monitor, and run staged migrations across an entire fleet of Turso & Cloudflare D1 databases.
- [civicdataforge-mcp](https://freemcp.space/featured/civicdataforge-mcp) — Official public-records MCP tools for STR permits, LEIE screening, childcare licensing, and film permits.
- [astrofabric-mcp](https://freemcp.space/featured/astrofabric-mcp) — Agentic AI for business intelligence over MCP: company and contact discovery, verification, enrichment, business signals and governed delivery.
- [schema-bridge-mcp](https://freemcp.space/featured/schema-bridge-mcp) — Universal schema compiler (SQL/Prisma to Zod, TypeScript, Pydantic) and realistic synthetic mock API data generator for MCP.
- [SqlAugur](https://freemcp.space/featured/sqlaugur) — MCP server providing AI assistants with safe, read-only access to SQL Server databases. AST-based query validation, rate limiting, and DBA      diagnostic tooling.
- [fluxmail](https://freemcp.space/featured/fluxmail) — Self-hosted email CLI / API / MCP server for AI agents and apps
- [vikingdb-mcp-server](https://freemcp.space/featured/vikingdb-mcp-server) — a mcp server for vikingdb store and search
- [tabpilot-mcp](https://freemcp.space/featured/tabpilot-mcp) — Drive the real, logged-in Chrome you already have open — cross-platform, token-optimized, and Ubuntu headless 24/7.
- [vibe-testing](https://freemcp.space/featured/vibe-testing) — Code-aware browser testing agent — 13 MCP tools for AI editors (Claude Code, Cursor, Windsurf). Reads your codebase, opens Playwright, tests everything, reports with screenshots.
- [mcp-datalink](https://freemcp.space/featured/mcp-datalink) — MCP server for secure database access (PostgreSQL, MySQL, SQLite)
- [ms-graph-mcp](https://freemcp.space/featured/ms-graph-mcp) — Microsoft Graph MCP server for AI agents — 85 tools across Outlook mail & calendar, Teams, OneDrive, SharePoint, OneNote, Planner and Entra ID. Delegated OAuth, stdio or Streamable HTTP.
- [urdb-mcp](https://freemcp.space/featured/urdb-mcp) — Search URDB's product integrity database for integrity scores, enshittification events, and change tracking across consumer products
- [dbridge-mcp](https://freemcp.space/featured/dbridge-mcp) — MCP server that lets AI agents query SQL databases in natural language - read-only, with column masking, row caps, and query limits. SQLite / PostgreSQL / MySQL.
- [ratatosk-mcp](https://freemcp.space/featured/ratatosk-mcp) — MCP server for Ratatosk — CNCF release intelligence facts for AI agents. check_stack compares your running versions locally; only project slugs leave your cluster.
- [mcp-kubernetes](https://freemcp.space/featured/mcp-kubernetes) — MCP server for Kubernetes — multi-cluster ops with security modes (read-only/read-write/admin) and access-control flags.
- [mcpdbwizard-open](https://freemcp.space/featured/mcpdbwizard-open) — Open source MCP server for Oracle PLSQL, SQL statements and Tables
- [tgatlas-mcp](https://freemcp.space/featured/tgatlas-mcp) — MCP server for public Telegram channels — profiles, posting cadence, and the channels Telegram itself considers similar.
- [tirith](https://freemcp.space/featured/tirith) — The tower of guard for parallel coding agents. Keeps parallel coding agents from stepping on each other. Claims, contracts and change notices over MCP.
- [seedfast-mcp](https://freemcp.space/featured/seedfast-mcp) — Public integration surface for the Seedfast MCP server: client configuration, tool reference and a smoke test
- [infino-mcp](https://freemcp.space/featured/infino-mcp) — MCP Server for Infino
- [limzo-mcp](https://freemcp.space/featured/limzo-mcp) — MCP server for Limzo — read-only public Telegram group statistics (leaderboards, levels, activity) from limzo.com. npx limzo-mcp
- [mailmcp-dist](https://freemcp.space/featured/mailmcp-dist) — All your mailboxes in ChatGPT and Claude: self-hosted email MCP server (Gmail, Outlook, iCloud, any IMAP/SMTP). Passwords stay yours.
- [aamio-python](https://freemcp.space/featured/aamio-python) — Ephemeral rendezvous for agents: threads with a secret read key and a public write address that expire on time, receipts that outlive them, and an open board where agents that have never met find each other. Hosted at aamio.at/mcp with no account, or as a local runtime that keeps the key.
- [Pandaone-AI-Agent](https://freemcp.space/featured/pandaone-ai-agent) — Pandaone Guard — Free open-source MCP server for AI code audit. L1-L6 defense (file lock + audit log + pre-commit hooks) for Claude/Cursor/Trae. Local stdio, no API key, MIT.
- [wg-easy-mcp](https://freemcp.space/featured/wg-easy-mcp) — MCP server for administering wg-easy (WireGuard Easy) instances
- [basicdeploy-mcp](https://freemcp.space/featured/basicdeploy-mcp) — The runtime your AI agent deploys to one MCP call gives a live container with Postgres, S3 storage, and a public URL. Create, deploy, exec, and manage apps.
- [mcp-openshift](https://freemcp.space/featured/mcp-openshift) — Safe-by-default MCP server for OpenShift / Kubernetes — projects, pods, logs, deployments, routes and more, with username/password (local IdP) or token auth.
- [snapmcp](https://freemcp.space/featured/snapmcp) — All-in-one MCP server for visual captures: terminal, code, browser, markdown, diffs, HTML, and PDF — via Playwright
- [alterlab-mcp-server](https://freemcp.space/featured/alterlab-mcp-server) — Web scraping MCP server for Claude, Cursor, Windsurf & AI agents — scrape any site, extract structured data, take screenshots. Anti-bot bypass, proxy rotation, authenticated scraping.
- [ghostfox](https://freemcp.space/ajat/ghostfox) — The agent-native stealth browser you can own — fingerprint-coherent Firefox engine + Rust MCP runtime. Self-hosted, open source, engine-level anti-detect.
- [mcp-server-decisions](https://freemcp.space/featured/mcp-server-decisions) — Servidor MCP para rastreamento de decisões arquiteturais com validação de predições e outcome gates.
- [musajala-mcp](https://freemcp.space/featured/musajala-mcp) — Anthropic Model Context Protocol (MCP) Server for Musajala (مُسَاجَلَة) — Living Collaborative Arabic Poetry Arena
- [mundane-mcp](https://freemcp.space/featured/mundane-mcp) — MCP server for Mundane: let your AI agent hire verified humans for real-world tasks — errands, photos, queues, in-person bookings. 22 tools, connect to the hosted endpoint over Streamable HTTP or self-run over stdio. Escrow-backed, ID-verified, policy-screened.
- [AIsa-mcp-server](https://freemcp.space/featured/aisa-mcp-server) — One MCP server in front of 950+ data APIs — SEO and AI visibility, finance, social, web search, sales and agent mail. `tools/list` returns five meta tools rather than hundreds: `search` finds an operation from a plain-language task, `get_details` gives its contract and price, `use` runs it, and `max_price_usd` refuses anything above a cap before any spend. OAuth, nothing to paste. Install: `npx -y @aisa-one/mcp`, or point a remote client straight at `https://mcp.aisa.one/mcp`.
- [amnesic](https://freemcp.space/featured/amnesic) — Persistent semantic memory for SQL databases (Postgres, MySQL, MSSQL, SQLite) — the MCP server with the most ironic name. One-line install for Claude Code, Cursor, and any MCP-compatible client.
- [mcp-server-sqlite](https://freemcp.space/featured/mcp-server-sqlite) — MCP server for SQLite — query databases, inspect schemas, explain queries
- [nlqueries](https://freemcp.space/featured/nlqueries) — Open source natural language to SQL (NL2SQL) engine with schema validation and an MCP server for Claude and Cursor
- [mongodb-atlas-mcp-server](https://freemcp.space/featured/mongodb-atlas-mcp-se) — MCP server for mongodb atlas api. Internally uses mongodb-atlas-api-client
- [pg-mnemosyne-mcp](https://freemcp.space/featured/pg-mnemosyne-mcp) — 🧠 A high-performance PostgreSQL-backed MCP server acting as a super memory, task tracker, and dynamic database manager for AI agents. Features built-in connection pooling, a professional tasks schema, and a unique shared multi-agent coordination hub to prevent coding conflicts in real-time.
- [postgres-mcp-hardened](https://freemcp.space/featured/postgres-mcp-hardene) — Secure read-only PostgreSQL MCP server in Rust — a hardened alternative to the deprecated @modelcontextprotocol/server-postgres.
- [mcp-server-questdb](https://freemcp.space/featured/mcp-server-questdb) — QuestDB MCP server connects coding agents to a running QuestDB Web Console. The agent gets tools to create notebook cells, run queries, and build charts.
- [querywise-mcp](https://freemcp.space/featured/querywise-mcp) — An MCP server (and a CLI) that lets an LLM query your databases in natural language through a business semantic layer — glossary, metric definitions, data dictionary, knowledge base, and example queries — grounded against your real schema.
- [izTolkMcp](https://freemcp.space/featured/iztolkmcp) — MCP server for Tolk smart contract compiler — compile, check, and deploy TON blockchain smart contracts from any MCP-compatible AI assistant
- [flamerobin-mcp-server](https://freemcp.space/featured/flamerobin-mcp-serve) — Firebird database MCP server that reads connection details from [FlameRobin's](http://www.flamerobin.org/) config — no credential setup required. Access all locally registered databases in one session with full schema introspection, DDL/DML execution, execution plans, and missing index analysis.
- [mcp-sqlserver](https://freemcp.space/featured/mcp-sqlserver) — One MCP server for every SQL Server you administer — grouped connections, execution plans, index audits, stored-procedure analysis
- [mcp-clickhouse](https://freemcp.space/featured/mcp-clickhouse-2) — MCP server for ClickHouse — explore, query, and manage with SQL-classification-based security modes and access-control flags.
- [mxprobe](https://freemcp.space/featured/mxprobe) — Email verification for AI agents: send, hold or kill with the reason. CLI, MCP server and hosted API.
- [thinair-data](https://freemcp.space/featured/thinair-data) — Secure read-only MCP server for PostgreSQL, MySQL, and SQL Server — built for ThinAir Data, operational analytics, reporting, and AI-assisted database workflows.
- [redash-mcp](https://freemcp.space/featured/redash-mcp) — MCP server for querying and managing Redash with Claude AI
- [mcp-multi-db](https://freemcp.space/featured/mcp-multi-db) — Read-only MCP server for querying PostgreSQL, MySQL, and SQLite from AI agents — multi-database, safe by default.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
