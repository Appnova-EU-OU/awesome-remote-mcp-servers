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
- [mcp-run-sql-connectorx](https://freemcp.space/featured/mcp-run-sql-connecto) — An MCP server that executes SQL via ConnectorX and streams (using Arrow RecordBatch) the result to CSV or Parquet. Supports PostgreSQL, MySQL, MariaDB, SQLite, MS SQL Server, Amazon Redshift, Google BigQuery
- [mcp-percona-pg](https://freemcp.space/featured/mcp-percona-pg) — MCP server for the Percona Operator for PostgreSQL — manage PostgreSQL + PgBouncer, pooling, backups/PITR, and DR with safe-by-default security flags.
- [ictcrm-mcp](https://freemcp.space/featured/ictcrm-mcp) — MCP server for ICTCRM (ICTContact backend) — read contact groups, manage contacts, add contacts to campaigns. By ICT Innovations.
- [textbee-mcp](https://freemcp.space/featured/textbee-mcp) — MCP server for textbee.dev: give your AI agent a phone number
- [sqemo-mcp](https://freemcp.space/featured/sqemo-mcp) — MCP server for Sqemo. AI agents query and edit ERDs, generate physical names from your team's shared glossary, import/export SQL (7 dialects) and DBML, and diff the model against a live database.
- [mysql-legacy-mcp](https://freemcp.space/featured/mysql-legacy-mcp) — MCP server for legacy MySQL 5.0–5.6: schema inspection and SELECT by default, with opt-in INSERT/UPDATE/DELETE/DDL. Live-verified against MySQL 5.0–8.0.
- [db-access-mcp](https://freemcp.space/featured/db-access-mcp) — MCP server for querying Postgres/MySQL/Redshift/SQL Server via SSH & AWS SSM tunnels, with Vault/AWS secret providers.
- [queue-inspector-mcp](https://freemcp.space/featured/queue-inspector-mcp) — MCP server for inspecting and operating Redis-backed job queues (Asynq, BullMQ): per-state counts, job detail, retries, dead letters.
- [jdbc-mcp-server](https://freemcp.space/featured/jdbc-mcp-server) — Read-only JDBC MCP server for PostgreSQL, Oracle, and SQL Server: safe SQL access for AI agents (Claude Code, Cursor, Copilot) with schema discovery, query validation, execution plans, benchmarking, and index/statistics tools
- [Postgres-AIops](https://freemcp.space/featured/postgres-aiops) — Governed AI-ops for PostgreSQL — slow-query/bloat/lock RCA, indexes, vacuum, replication, with audit/budget/undo/risk-tiers (preview)
- [echoloc-mcp](https://freemcp.space/featured/echoloc-mcp) — Remote MCP server for echoloc company technographics — search 760K+ companies by tech stack with direction of change (adopting/replacing/evaluating)
- [verify-proof](https://freemcp.space/featured/verify-proof) — Verify blockchain-anchored timestamp proofs offline. Python CLI + MCP server for SHA-256 and Merkle-path verification of ProofLedger and OpenTimestamps proofs.
- [vaemail-mcp](https://freemcp.space/featured/vaemail-mcp) — MCP server and CLI for VaEmail, email infrastructure for AI agents. Zero dependencies.
- [termgram](https://freemcp.space/featured/termgram) — Telegram in your terminal: MTProto client, MCP server with push notifications, and an SSE stream
- [sounnyforms-mcp](https://freemcp.space/featured/sounnyforms-mcp) — Official Model Context Protocol (MCP) Server for SounnyForms — Zero-API-Key Form Processing, Lead Triage & Code Generation for AI Agents
- [AgoraDM](https://freemcp.space/featured/agoradm) — DM / IM for AI agents — A2A 1.0 client SDK, daemon framework, per-friend memory + wake context, and MCP server
- [gambot-mcp](https://freemcp.space/featured/gambot-mcp) — MCP server for the Gambot WhatsApp Business API - send WhatsApp messages & templates, manage CRM, leads & campaigns from Claude, Cursor & any AI agent.
- [mcp-outlook](https://freemcp.space/featured/mcp-outlook) — Safe-by-default MCP server for Microsoft Outlook mail (Microsoft Graph) — read, search, draft, send, reply, forward and organize email, with browser sign-in.
- [reaper-daemon](https://freemcp.space/featured/reaper-daemon) — Free, open source REAPER MCP server that lets an AI agent (Claude or any MCP client) drive REAPER: read every plugin and parameter, set FX values, write automation, and measure a mix move before and after. MIT. macOS, Windows, Linux.
- [vibatchium](https://freemcp.space/featured/vibatchium) — Stealth browser automation for AI agents — unattended, headless, N parallel persistent logged-in Chromes. One MCP server + CLI, credential vault with TOTP/IMAP 2FA, vision clicking, prompt-injection scanning. Self-hosted, real Chrome. 1,250 tests.
- [hermes-action-bridge](https://freemcp.space/featured/hermes-action-bridge) — Configurable bridge for external agents to delegate actions to Hermes Agent via CLI or MCP.
- [Contradiction-MCP](https://freemcp.space/featured/contradiction-mcp) — Autonomous Model Context Protocol (MCP) engine for factual consistency, version reconciliation, and conflict resolution across engineering knowledge bases.
- [chrome-bridge](https://freemcp.space/featured/chrome-bridge) — Your real, logged-in Chrome as an MCP server for Claude Code: 59 token-efficient web-dev tools, a skill with recipes, a zero-token CLI. ChromeOS included.
- [revit-model-mcp](https://freemcp.space/featured/revit-model-mcp) — MCP server for live Autodesk Revit models: query, aggregate and inspect by default, act only behind opt-in gates
- [mcp-hub](https://freemcp.space/featured/mcp-hub) — Serve multiple stdio MCP servers from one container: path routing, hub meta-tools, OAuth 2.1 + API tokens for ChatGPT, Claude, Cursor and other MCP clients
- [hicortex](https://freemcp.space/featured/hicortex) — Self-learning memory for AI agents — experience captured automatically, distilled into lessons overnight, shared across your whole fleet. Works with Hermes, OpenClaw, Claude Code, and Pi.
- [sandbox-as-a-service-mcp](https://freemcp.space/featured/sandbox-as-a-service) — MCP server for Sandbox as a Service: give an agent a real Linux VM — run commands, move files, expose a preview URL, destroy it.
- [mcp-oci](https://freemcp.space/featured/mcp-oci) — MCP server for Oracle Cloud (OCI) — live resource discovery, dependency mapping, and Terraform generation, with security modes and access-control flags.
- [cute-web-scraper](https://freemcp.space/featured/cute-web-scraper) — A free, local MCP server that gives Claude web scraping powers. 24 tools, four escalating fetch tiers, no API key.
- [evipedia-mcp](https://freemcp.space/featured/evipedia-mcp) — MCP Server for evipedia.ai
- [mcp-server](https://freemcp.space/featured/mcp-server-17) — MCP server for Tribeunal — 39 tools and 8 Agent Skills that put humans and AI agents on the same jury
- [plopino-mcp](https://freemcp.space/featured/plopino-mcp) — MCP server for Plopino — lets an AI agent publish a page, a file, or a folder and hand back a public link.
- [shiped-mcp](https://freemcp.space/featured/shiped-mcp) — Deploy AI-generated HTML/CSS/JS to an instant public HTTPS URL from any MCP agent (Claude Code, Codex, Cursor, Kiro, Copilot). Remote HTTP MCP endpoint with OAuth 2.1 device-flow login — no API key to mint or store.
- [superglookoquery](https://freemcp.space/featured/superglookoquery) — MCP server exposing Glooko diabetes device data (any pump/CGM combination) for clinical audit, with device-agnostic capability discovery. Forked from podquery-mcp.
- [architecture_viewer](https://freemcp.space/featured/architecture-viewer) — AI coding session architecture gate — local MCP (av_guard) + CLI diffs vs git HEAD for cross-layer deps. Apache-2.0.
- [scenef-mcp](https://freemcp.space/featured/scenef-mcp) — SceneF MCP server — verified California and Hawaii movie showtimes, every operating cinema in the covered states, checked twice daily. Remote, no key: https://scenef.com/mcp
- [opticquiz-mcp](https://freemcp.space/featured/opticquiz-mcp) — Two MCP servers for color-vision accessibility: check whether a palette or image is colorblind-safe, and see it recolored as protan/deutan/tritan. Machado 2009 + CIEDE2000, published method. Local stdio.
- [ergonia](https://freemcp.space/featured/ergonia) — Ergonia Works: verifiable work for AI agents. Work isn't done because an agent says so, it's done when anyone can verify it. Every task carries an acceptance condition a stranger can execute.
- [macaroonnetwork-mcp](https://freemcp.space/featured/macaroonnetwork-mcp) — MCP client for Macaroon Network -- discover and buy from a live marketplace where AI agents pay per query via Bitcoin Lightning (L402) or Base/USDC (x402).
- [neon-mcp-gateway](https://freemcp.space/featured/neon-mcp-gateway) — Enterprise Zero-Trust security gateway, token rate-limiter, and secure SSE proxy for Model Context Protocol (MCP) servers.
- [BotHireMCPServer](https://freemcp.space/featured/bothiremcpserver) — MCP server for BotHire — the machine-to-machine labor market where AI agents hire each other and pay agent-to-agent in USDT/USDC (x402, gasless, multi-chain: Base, Arbitrum, BNB, Solana) with ownerless on-chain escrow. Read-only discovery tools: search skills/agents, market stats, hire guide.
- [moltline-mcp](https://freemcp.space/featured/moltline-mcp) — Zero-dependency stdio bridge for the Moltline Studio MCP fleet - 19 hosted streamable-HTTP servers, 132 tools, 92 of them free with no signup.
- [veilbrowser](https://freemcp.space/featured/veilbrowser) — Stealth browser for AI agents — real Chrome over raw CDP, no Playwright/Puppeteer. TypeScript + MCP-native. Passes sannysoft 57/57, bypasses Cloudflare.
- [viber-mcp](https://freemcp.space/featured/viber-mcp) — MCP server for Viber messenger (Rakuten Viber Bot API) — TypeScript
- [ictpbx-mcp](https://freemcp.space/featured/ictpbx-mcp) — Read-only MCP server for ICTPBX — extensions, DIDs, SIP trunks, tenants and PBX statistics over ICTCore REST. By ICT Innovations.
- [komnet](https://freemcp.space/featured/komnet) — Git-backed message bus for AI coding agents — Claude Code, Cursor and Codex coordinate asynchronously, with no server
- [ntfy-mcp](https://freemcp.space/featured/ntfy-mcp-2) — MCP server for ntfy: publish notifications, read cached messages, manage users and topic access
- [smtp-mcp](https://freemcp.space/featured/smtp-mcp) — MCP server that sends mail over SMTP, gated behind an allowlist and a human confirmation
- [munim](https://freemcp.space/featured/munim) — A multi-account MCP server for people who look after other people's infrastructure. Built with the Strands Agents SDK.
- [portkey-admin-mcp](https://freemcp.space/featured/portkey-admin-mcp-2) — Portkey Admin API control-plane MCP server with Prisma AIRS interoperability guidance
- [jgs-magic-sysmlv1-mcp](https://freemcp.space/featured/jgs-magic-sysmlv1-mc) — Bring Claude Code and any MCP agent to your live SysML v1 models in CATIA Magic: 130+ tools to query, audit, and edit the real model over a local, air-gapped connection. No cloud, no export. FREE / PRO / ENTERPRISE.
- [magents](https://freemcp.space/featured/magents) — Shared session bus for Claude Code, Codex, and Cursor
- [AnkusDrive](https://freemcp.space/gchen19/ankusdrive) — CLI + MCP server that turns FreeCAD into a mechanical-design workbench for LLM agents — parametric CAD, drawings, FEM/CFD simulation, and manufacturing checks
- [drop2run-cli](https://freemcp.space/featured/drop2run-cli) — Source for the drop2run CLI and MCP server — publish a static site or an agent's output to an HTTPS link, no git and no build config.
- [elicitly](https://freemcp.space/featured/elicitly) — Elicitly Free Edition — human-in-the-loop for prompts and Agent Skills over MCP elicitation. Local MCP server (npx -y elicitly) + embeddable toolkit (@elicitly/tools).
- [K8s-AIops](https://freemcp.space/featured/k8s-aiops) — Standalone governed Kubernetes ops — 15 MCP tools with built-in audit/budget/undo/risk-tier harness
- [ottersnap-mcp](https://freemcp.space/featured/ottersnap-mcp) — MCP server for the OtterSnap rendering API — screenshots, PDFs, OG images and page extraction for AI agents.
- [svipall](https://freemcp.space/featured/svipall) — Local-first MCP server and CLI in Rust: any page as LLM-ready Markdown, whole-site crawls, keyless search, and local captcha solving. No cloud, no API keys.
- [x402-scraper-engine](https://freemcp.space/featured/x402-scraper-engine) — HTTP 402 pay-per-call web scraper & Llama-3 digest engine for autonomous AI agents on Base L2. No API keys, no subscriptions.
- [vitamind-mcp](https://freemcp.space/featured/vitamind-mcp) — MCP server for solar vitamin D — when the sun where you are can actually make vitamin D, for your skin type. Bridges any stdio MCP client to the hosted Vitamin D Explorer server.
- [nightmarquee-mcp](https://freemcp.space/antdevlab/nightmarquee-mcp) — Cinematic website prompts with live previews, inside your editor. MCP server for Claude Code, Claude Desktop and Cursor.
- [mcp-server](https://freemcp.space/featured/mcp-server-16) — MCP server for cogDepot, the anonymous broker where AI agents publish capabilities, negotiate, and form direct peer-to-peer deals. Keyless discovery, or the full trading loop with a key - post, browse, negotiate, seal, rate. Local via npx or the hosted remote server.
- [browser-mcp](https://freemcp.space/featured/browser-mcp) — Drive your real, logged-in Chrome from any AI agent (Claude Code, Codex, Cursor, VS Code) — works where headless dies. Reads emailed login codes from your Gmail, 40 tools, up to 20 concurrent sessions. MIT, local-only.
- [caldav-mcp](https://freemcp.space/featured/caldav-mcp-3) — MCP server for CalDAV calendars: events, tasks and journals over the open standard
- [carddav-mcp](https://freemcp.space/featured/carddav-mcp) — Model Context Protocol (MCP) server for CardDAV address books: contacts, groups and photos
- [engagelab-email-mcp](https://freemcp.space/featured/engagelab-email-mcp) — Official EngageLab Agent Email MCP server for AI agents to send, receive, monitor, and reply to email
- [mailflat-sdks](https://freemcp.space/featured/mailflat-sdks) — Official MailFlat SDKs for Python, TypeScript/JavaScript and Java. Real email inboxes your agent or test suite can create from code and read one-time codes from.
- [outlook-mcp](https://freemcp.space/featured/outlook-mcp-2) — MCP server for tidying a large Outlook / Hotmail mailbox via Microsoft Graph. Bulk moves, folder-tree surgery, inbox rules — no send tool, no permanent delete.
- [b2-mcp](https://freemcp.space/featured/b2-mcp) — MCP server for Backblaze B2 Cloud Storage: a focused, safe 40-tool surface (17 native B2 SDK, 19 S3 data-plane, 4 analytics) for any MCP-compatible AI client, currently incubating in Backblaze-Labs
- [x402-list-mcp](https://freemcp.space/featured/x402-list-mcp) — MCP server for x402-list.com: discover x402 payment services and on-chain-verified facilitator settlement volumes. Published on npm as x402-list-mcp.
- [pbx-mcp](https://freemcp.space/featured/pbx-mcp) — MCP server for Asterisk and FreeSWITCH. Lets AI assistants inspect channels, SIP registrations, trunk status and dialplan on a live PBX.
- [meet-live-assist-extension](https://freemcp.space/featured/meet-live-assist-ext) — Your own AI agent, live in a Google Meet or Zoom call: reads the captions, answers in a side panel, runs entirely on your machine over MCP.
- [fmsg-mcp](https://freemcp.space/featured/fmsg-mcp) — MCP server for fmsg: send and receive federated messages from any AI agent via a deployed fmsg Web API
- [agent-identity-mcp](https://freemcp.space/flovoice53/agent-identity-mcp) — MCP server that gives an AI agent a disposable email address and a real UK phone number to test signup/verification flows end to end
- [giggal-mcp](https://freemcp.space/featured/giggal-mcp) — Official MCP server for Giggal.ai: catch-all, accept-all, and SEG-protected email verification for Claude, ChatGPT, Cursor, and other MCP clients.
- [sms-florin-mcp](https://freemcp.space/flovoice53/sms-florin-mcp) — MCP server for sms-florin — rent a real UK phone number and receive SMS/OTP codes from AI coding agents (Claude, Cursor, Codex...)
- [aginxbrowser](https://freemcp.space/featured/aginxbrowser) — The browser built for AI agents — fetch live pages as markdown, render JS/SPAs with built-in V8, take screenshots without Chromium, meta-search 5 engines, and drive interactive login sessions. One Rust binary, stealth TLS fingerprints, MCP native for Claude Code & Cursor. Headless browser alternative to Puppeteer/Playwright.
- [domain-mcp](https://freemcp.space/featured/domain-mcp) — Manage Dynadot domains, DNS, renewals, and transfers from Claude, Cursor, or any MCP client.
- [Agent402](https://freemcp.space/featured/agent402) — agent402.tools: 500+ pay-per-call tools, metered models and finished reports for AI agents, paid per call in USDC over x402 and MPP or by card. Open source, self-hostable, MCP-native. The applied layer of agentic finance.
- [MCPEmails](https://freemcp.space/asgeiralbretsen/mcpemails) — Give your AI agent an inbox. Hosted remote MCP server: connect Gmail or any IMAP mailbox (Fastmail, iCloud, Yahoo, Zoho) and read, search, send, organize, schedule and auto-triage email from Claude, ChatGPT, Cursor or any MCP client. OAuth sign-in, per-key permission scopes, mail fetched live and never stored. Nothing to install or deploy. Setup guides: https://mcpemails.com/docs
- [gemini-antigravity-bridge](https://freemcp.space/nandhakumar-murugan/gemini-antigravity-b) — ⚡ Bridge connecting Google Gemini Spark & Cloud AI to your local machine via MCP with autonomous file creation, terminal execution, and subagent orchestration.
- [gigamail](https://freemcp.space/featured/gigamail) — Mail for AI agents ( and humans). MCP server giving Claude (or any agent) safe, permission-controlled access to email (Microsoft Graph + IMAP), calendar and your knowledge files. Two-phase confirmation for sends, audit log, local index. No built-in LLM: your agent brings the intelligence.
- [ssh-mcp-server](https://freemcp.space/featured/ssh-mcp-server-2) — SSH MCP server for AI agents: remote commands, file transfer, log search and server audits through OpenSSH.
- [SmartCLI](https://freemcp.space/featured/smartcli) — Three Agent Skills over one pluggable PTY + pyte core: drive TUIs, design terminal effects, and render cell-accurate UIs. pip install smartcli-toolkit
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
