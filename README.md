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
- [attocode](https://freemcp.space/featured/attocode) — A series of lessons, 0 to hero ai coding agent building guide.
- [ictcontact-mcp](https://freemcp.space/featured/ictcontact-mcp) — MCP server for ICTContact / ICTDialer — monitor outbound campaigns and start/stop them. By ICT Innovations.
- [postfader-fl-studio-mcp](https://freemcp.space/featured/postfader-fl-studio) — FL Studio MCP server: let Claude, Codex, Cursor, or any MCP client read, mix, compose, and edit the project you have open. Read-only by default, every change read back. Windows + macOS.
- [msty-admin-mcp](https://freemcp.space/featured/msty-admin-mcp) — AI-powered administration for Msty Studio Desktop. 56 MCP tools for database insights, config sync, local model orchestration, and Claude handoff workflows.
- [datris-platform-oss](https://freemcp.space/featured/datris-platform-oss) — The Data Control Plane for AI Agents — acquire, validate, and land data over MCP with scoped keys, approval gates, and an audit log. Self-hosted, open source.
- [gravityport](https://freemcp.space/featured/gravityport) — GravityPort is a free AI asset manager for macOS and Windows. Images and videos from ChatGPT, Gemini, Flow, Google AI Studio, Codex, Grok and Jimeng land in a library on your computer, with their prompts, reference images and sources. Every AI creation leaves a trail.
- [gemini-pro-mcp](https://freemcp.space/featured/gemini-pro-mcp) — Use your Google AI Pro subscription from Claude, Codex, Antigravity and Gemini CLI: Gemini via Antigravity, Flow, Gemini app, Notebooks, Jules, Omni video and Nano Banana images. One-command setup. MCP server.
- [plunger](https://freemcp.space/featured/plunger) — An HTTP client built for AI agents: an MCP server and a command line that send requests safely, plus a native window to see what the agent did. Rust, no account, no telemetry.
- [velloo](https://freemcp.space/featured/velloo) — Local-first design canvas for AI coding agents. Recreate a real React screen, explore directions visually, then ship the winner back into your app.
- [mcp-events-bridge](https://freemcp.space/featured/mcp-events-bridge) — Turn webhooks into MCP Events for AI agents, with the hosted Hookdeck Event Gateway receiving and delivering them. Sources include Resend, GitHub, Stripe, Slack and any signed webhook. Poll tools and a Claude Code plugin cover clients without MCP Events support.
- [Karakoram](https://freemcp.space/featured/karakoram) — Self-hosted database and stateful-service orchestration on infrastructure you run: Zerops, Dokploy or Nomad.
- [vibe-monitor](https://freemcp.space/featured/vibe-monitor) — Apache-2.0 local stdio MCP server for read-only architecture checks, evolution checkpoints, and actionable findings for AI coding agents.
- [string-utility-belt](https://freemcp.space/featured/string-utility-belt) — Chain string transformations into visual pipelines with live previews — 246 utilities as a web app, CLI, HTTP API, MCP server and browser/VS Code extensions.
- [nucleo](https://freemcp.space/featured/nucleo) — WordPress page builder with an MCP server for AI agents
- [spring-runtime-mcp](https://freemcp.space/featured/spring-runtime-mcp) — Read-only, sanitized Spring Boot runtime diagnostics (beans, conditions, routes, health, migrations, startup, config, OpenAPI, drift) for coding agents over MCP
- [verdict](https://freemcp.space/featured/verdict) — One rubric, every decision model. Run the same typed questions on Jev, Clef and OpenAI's Decisions API, and see where they disagree on your own cases.
- [mini-cms-mcp](https://freemcp.space/featured/mini-cms-mcp) — Small self-hosted CMS managed by an AI assistant over MCP: the AI changes content, never code. PHP 8, no database. · Un CMS mic administrat de un asistent AI prin MCP. AI-ul schimbă conținutul, niciodată codul. PHP 8, fără bază de date.
- [dataranger](https://freemcp.space/featured/dataranger) — Open-source AI agent that patrols your data, fixes only what it can prove against the source, and sends the rest to a person with the evidence. Works with Snowflake, dbt and DuckDB, runs as a GitHub Action, and speaks MCP.
- [codedb-lens](https://freemcp.space/featured/codedb-lens) — Free, read-only health check for SQL Server and PostgreSQL
- [chorono-editor](https://freemcp.space/featured/chorono-editor) — Open-source 2D animation editor. Create with Claude Code or Codex via MCP, then refine layers and keyframes visually.
- [inventor-mcp-server](https://freemcp.space/featured/inventor-mcp-server) — MCP server for parametric 3D modeling in Autodesk Inventor — maintained continuation of NeonGlay/inventor-mcp (MCP SDK 2.x, Inventor 2027, assemblies)
- [archsmith](https://freemcp.space/featured/archsmith) — Turn a validated JSON IR into a consistent layered-architecture diagram (SVG) — library, CLI, and MCP server, for humans and agents alike.
- [phpgraph](https://freemcp.space/featured/phpgraph) — Knowledge graph of PHP codebases for AI coding agents (Claude Code, Codex, Cursor) over MCP. Static analysis, no LLM.
- [3dcraft](https://freemcp.space/featured/3dcraft) — An open-source parametric 3D CAD modeller built with and for AI: every action is a command, and every result is checked. Pure Rust, its own kernel.
- [mcps](https://freemcp.space/featured/mcps) — MCP servers for Google Workspace, Notion, Romanian e-invoicing and company registers, open banking, invoicing, domains, Expo and more, on one shared toolkit
- [brewpage-openapi](https://freemcp.space/featured/brewpage-openapi) — Open API Specification for https://brewpage.app - Free HTML, Markdown, AI Artifacts & File Instant Hosting
- [browserdo](https://freemcp.space/zhaijunlong/browserdo) — MCP server for Embiody, the Windows browser your AI agent works in while you keep using your PC.
- [doubao-image-mcp](https://freemcp.space/featured/doubao-image-mcp) — 把豆包网页版生图封装成本地 MCP 服务：无需 API Key，支持扫码登录、多账号排队、多图全量返回
- [sealbridge](https://freemcp.space/featured/sealbridge) — Delegate tasks such as code reviews to AI agents run by other people, straight from your MCP client. Signed requests and results, relayed delivery, and a verifiable audit log.
- [bruster](https://freemcp.space/featured/bruster) — Native webview browser automation for AI agents. Rust-powered, with JSON-lines control and a built-in MCP server. Runs on macOS, Linux, and Windows.
- [claude-bridge-blender](https://freemcp.space/featured/claude-bridge-blende) — Drive a live Blender with Claude: in-Blender chat on your subscription + token-lean MCP ops for Claude Code
- [semantic-cache-mcp](https://freemcp.space/featured/semantic-cache-mcp) — MCP file cache for AI coding agents. Re-reads cost ~40 tokens instead of the whole file; changed files come back as diffs. Works with Claude Code, Cursor, Codex and VS Code.
- [rebuild-dossier](https://freemcp.space/featured/rebuild-dossier) — MCP server that reverse engineers a locked rebuild spec (CLAUDE.md, .claude config, mutation tested tests) from an existing app
- [opendrs](https://freemcp.space/error-path/opendrs) — PR blast radius analyzer: a 0-1 risk score for every pull request so AI-reviewed, low-risk PRs auto-approve into the merge queue. GitHub Action, CLI, Claude Code plugin, MCP server.
- [test-inventory-mcp](https://freemcp.space/featured/test-inventory-mcp) — MCP server for test-inventory: AI agents ask which Playwright, Vitest, Jest, Mocha, Jasmine, Cypress, WebdriverIO, node:test and Bun tests a project has, which are skipped and why, and which a change can affect, without running them.
- [indec-mcp](https://freemcp.space/featured/indec-mcp) — MCP no oficial sobre el Catálogo API-INDEC (Argentina): inflación, canastas, salarios, EMAE, pobreza, empleo, comercio exterior. Mirror DuckDB + servidor MCP con rate limits.
- [MongrelDB-Viewer](https://freemcp.space/featured/mongreldb-viewer) — Multi-platform desktop viewer for MongrelDB: direct + server connections, schema map, SQL, dense ANN, MCP, and chat.
- [context-guardian](https://freemcp.space/luminarisoftwares/context-guardian) — 40 turns: 1,130,722 tokens upstream -> 161,141. A fail-open compaction proxy for local OpenAI-compatible models.
- [nano-mcp-termux](https://freemcp.space/featured/nano-mcp-termux) — Zero-dependency MCP server for AI agents, natively running on Termux (Android), Raspberry Pi, and Linux. Single-file, Docker-ready, protocol-tested.
- [telegram-dev](https://freemcp.space/featured/telegram-dev) — Telegram development skill and documentation MCP for Codex, Claude Code and Cursor
- [imsg-mcp](https://freemcp.space/featured/imsg-mcp) — Let your AI assistant read your iMessage/SMS and send the replies you approve. An MCP server and agent plugin for Claude, ChatGPT, Codex and Cursor, built for proactive agents like Claude Duet and dots. Runs on a Mac you control, with server-side send guardrails.
- [sonjari](https://freemcp.space/featured/sonjari) — Your PC does the work. You get the proof. Sonjari is a free local AI agent for Windows: web research, Excel and Word documents, and code. Works on its own, or takes on tasks from Claude and Codex. No meter.
- [claude-duet-bridge](https://freemcp.space/calebtgrimes/claude-duet-bridge) — Connect Claude Duet to Claude Code: an MCP connector that lets Duet start Claude Code sessions, talk to your open terminal windows, and get answers back. Remote MCP server on Cloudflare Workers + a Claude Code channel.
- [cmdshellmcp](https://freemcp.space/featured/cmdshellmcp) — command shell mcp server with additional tools (e.g. for coding)
- [agentic-browser](https://freemcp.space/featured/agentic-browser) — Give any AI agent your real Chrome: token-cheap text perception, a visible cursor, MCP + HTTP API. Optional chat watcher.
- [backdraw](https://freemcp.space/featured/backdraw) — Let Claude generate images with your own ChatGPT account in a background Chrome tab. Local MCP server + Chrome extension, no API key, no open ports.
- [api-shakedown](https://freemcp.space/featured/api-shakedown) — OpenAPI spec in, chaos test harness out: WireMock stubs, contract tests and failure scenarios from a team of local LLM agents.
- [Gulliver](https://freemcp.space/veldrosinus/gulliver) — Test on tiny data before you run on giant data. MCP server + CLI that gives AI agents a dress rehearsal for SQL: cost preflight, scale lint with auto-fix, rehearse on 1% → 10%, predict 100%, run only within budget. DuckDB, Postgres, BigQuery, Snowflake. Local-first, MIT.
- [bee-public](https://freemcp.space/featured/bee-public) — Public developer surface for Bee: Quantum Intelligence — Apache-2.0 SDKs, MCP server, API contracts and trust material.
- [enclave-gateway](https://freemcp.space/featured/enclave-gateway) — Run CLI, multi-hop SSH, SOCKS5 and governed MCP across Windows VPN appliances and RDP bastions.
- [toli](https://freemcp.space/featured/toli) — Let Claude Code, Codex, OpenClaw or any other agent work together, on one machine or across many.
- [vmware-sandbox-mcp](https://freemcp.space/featured/vmware-sandbox-mcp) — MCP server that gives AI agents a disposable Linux VM on VMware Workstation: run code, copy files, click and type, then throw it away.
- [wwdc-mcp-server](https://freemcp.space/jabbertones/wwdc-mcp-server) — Apple developer intelligence for coding agents: WWDC20–WWDC26, HIG, Swift, App Review, API history, and source-grounded app audits — 45 read-only MCP tools.
- [metrecept-opensource](https://freemcp.space/featured/metrecept-opensource) — Metrecept open client tools: MCP server, SDK helpers, receipt verifiers
- [cosmos-semantic-platform](https://freemcp.space/featured/cosmos-semantic-plat) — Open-source semantic layer with an ontology at its core: governed metrics and business rules for AI agents (MCP), the same number on eight databases, with evidence on every answer.
- [cost-guard-mcp](https://freemcp.space/featured/cost-guard-mcp) — Pre-flight query cost and result-size guardrails for AI agents across BigQuery, Snowflake, and Databricks
- [gage](https://freemcp.space/featured/gage) — Caller ID and a wax seal for AI agents: signed, sealed handoffs between agents, with trust the receiver computes. No accounts; keys stay on your machine.
- [sendkuy-mcp](https://freemcp.space/featured/sendkuy-mcp) — WhatsApp, SMS and email for agents through SendKuy: send messages and batches, verify OTP codes, check WhatsApp numbers and run campaigns, with tools filtered by the API key's scopes.
- [SoraCommander](https://freemcp.space/featured/soracommander) — Let ChatGPT work on your Windows PC from an ordinary chat, approving each step locally. Developer preview.
- [benchwarmers](https://freemcp.space/featured/benchwarmers) — Self-hosted panel gateway for LLMs: ask a collection of models at once, keep every answer side by side, rotate explorer models in, and let your verdicts pick the next panel. OpenAI, Anthropic, Gemini and Ollama APIs, an MCP server, Python stdlib.
- [consult](https://freemcp.space/featured/consult) — Get a second opinion on your code from every coding agent you have. Claude Code, Codex and Grok review each other's diffs and answer each other's questions, even inside a session that's already running. Uses the CLIs you're signed in to, no API keys.
- [agentsocks](https://freemcp.space/featured/agentsocks) — Native messaging between Claude Code, Codex and other coding-agent sessions.
- [vsphere-console-mcp](https://freemcp.space/featured/vsphere-console-mcp) — MCP server that lets an AI agent see and drive VMware vSphere VM consoles (screen, mouse, keyboard) through vCenter. Zero dependencies, no guest agent.
- [ui-loop](https://freemcp.space/featured/ui-loop) — Context-budgeted visual feedback for coding agents: diff-only crops + structured summaries within a token budget. MCP server + Claude Code plugin.
- [browser-ref-mcp](https://freemcp.space/hou332005/browser-ref-mcp) — Reliable browser-control MCP server for AI agents: click by ref, self-healing sessions. No browser download.
- [sandboxapis-mcp](https://freemcp.space/featured/sandboxapis-mcp) — The SandboxAPIs MCP server: read-only, API-compatible replicas of 21 developer APIs, preloaded with one simulated company, for testing agents without a test account.
- [CICD-AIops](https://freemcp.space/featured/cicd-aiops) — Governed AI-ops for self-managed GitLab + Gitea CI/CD: pipelines, jobs, runners, artifacts, repo hyg
- [sqai-mcp](https://freemcp.space/featured/sqai-mcp) — SQAI (Structured Query AI) MCP server — the three governed, deterministic, read-only structured-data tools (listSources, queryData, explainQuery) for any MCP host. npm: @thyn-ai/sqai-mcp. A Thyn product, Apache-2.0.
- [loudtzu-actors-mcp](https://freemcp.space/featured/loudtzu-actors-mcp) — MCP server: 9 Canadian data & price tools (LOUDTZU Apify Actors), run with your own Apify token
- [dbu-waste-finder](https://freemcp.space/featured/dbu-waste-finder) — Free read-only Databricks notebook + MCP server that finds DBU waste from system tables and proposes fixes
- [Statistik-Austria-MCP-Server](https://freemcp.space/featured/statistik-austria-mc) — Model Context Protocol (MCP) server for querying Statistik Austria's free OGD datasets.
- [Handmade](https://freemcp.space/hhiramkarogo/handmade) — **Build AI-generated interfaces that look intentionally engineered, not generated.**
- [handmade](https://freemcp.space/featured/handmade) — Handmade is a Model Context Protocol (MCP) server tailored to eliminate generic AI output by enforcing comprehensive prompt coverage and proactively clarifying ambiguities before generation.
- [m4r-data](https://freemcp.space/featured/m4r-data) — Structured data from Music For Robots — music composed for machines, reviewed by AI critics
- [gpt-image-studio](https://freemcp.space/featured/gpt-image-studio) — Let your AI agent generate images with OpenAI gpt-image-2.5 or any OpenAI-compatible relay — live web gallery, cost tracking, MCP, 5 languages
- [spotify-data-mcp](https://freemcp.space/featured/spotify-data-mcp) — MCP server for Spotify data: play counts, monthly listeners, charts, artist stats, playlists and ISRC lookup for Claude, Cursor and VS Code
- [bayze-mcp](https://freemcp.space/featured/bayze-mcp) — Local-first AI model-routing core: waterfall workflows with structured cross-vendor review (draft → review → revise). BYOK or unified API. MCP stdio. npm: bayze-mcp
- [kitden](https://freemcp.space/featured/kitden) — See the MCP servers, plugins and skills Claude Code, Codex and Cursor load, and which skills got cut
- [mcp-b2b-prospect-engine](https://freemcp.space/featured/mcp-b2b-prospect-eng) — MCP server for the Mamba Labs Prospect Engine actor on Apify
- [verify-atom](https://freemcp.space/featured/verify-atom) — Give AI agents cryptographically signed proof of web observations: Ed25519-signed proof packets (HTTP status, page title, body SHA-256, DNS, TLS) for any public URL. Install: `uvx verify-atom-mcp`.
- [dagon-mcp](https://freemcp.space/featured/dagon-mcp) — MCP server for Dagon Inference: uncensored LLMs, pay with Solana USDC
- [multi-mail-mcp](https://freemcp.space/featured/multi-mail-mcp) — MCP server for searching, reading and writing mail across several Gmail accounts (Claude Desktop, Claude Code, ChatGPT)
- [xonta-max-mcp](https://freemcp.space/featured/xonta-max-mcp) — MCP server for building bots and mini-apps for the MAX messenger (max.ru): current Bot API facts, code checks, Telegram migration hints, bot templates, deep links, ad tracking and test fixtures. English and Russian.
- [proton-mail-mcp](https://freemcp.space/featured/proton-mail-mcp-2) — Unofficial MCP server for Proton Mail Bridge: search and read mail, write drafts, guarded cleanup. Not affiliated with Proton AG.
- [whatsapp-messaging-api-mcp](https://freemcp.space/jevil257/whatsapp-messaging-a) — Send WhatsApp messages from Claude and any MCP client. No Meta Business approval or WhatsApp Business account.
- [discord-management-mcp](https://freemcp.space/featured/discord-management-m) — Safe-by-default Discord management MCP server with JSON backups, restore planning and guarded mutations
- [hellohop-mcp](https://freemcp.space/socialground/hellohop-mcp) — MCP server for the HelloHop WhatsApp API. Read chats, groups and communities from Claude, Cursor or any MCP client.
- [blueticks-mcp](https://freemcp.space/featured/blueticks-mcp) — Blueticks MCP server for Claude Desktop / Cursor / Cline
- [gmail-tidy-mcp](https://freemcp.space/featured/gmail-tidy-mcp) — MCP server that reads and organizes several Gmail accounts (labels, filters, archiving, drafts) and can never send or delete mail.
- [mail-mcp-server](https://freemcp.space/featured/mail-mcp-server) — Read-only mail for AI agents: on-premises Exchange and any IMAP mailbox, with local search inside PDF, Office and ZIP attachments.
- [mac-terminal-mcp](https://freemcp.space/featured/mac-terminal-mcp) — A sandboxed terminal for Claude on your Mac. No dialogs, no dependencies, no telemetry.
- [spm](https://freemcp.space/featured/spm) — A simple, cross-platform manager for native system services.
- [model-worker-mcp](https://freemcp.space/featured/model-worker-mcp) — MCP server delegating bounded coding tasks to an OpenAI-compatible model: explicit read/write paths, diff validation, risk-based routing.
- [contextsmith](https://freemcp.space/featured/contextsmith) — Give your coding agent the right code, not more code. Local context engine for Claude Code, Cursor & Codex: code graph + hybrid search + embeddings + git history, packed into a token budget. Held-out SWE-bench: right file in 4k tokens 92% vs 29% for search + whole files. MIT, no API keys.
- [onlinecompiler-mcp](https://freemcp.space/featured/onlinecompiler-mcp) — MCP server for OnlineCompiler.io: run and judge code in 46 languages from AI assistants and coding tools such as Claude, ChatGPT, Gemini CLI, Cursor and Codex.
- [Viewport-iq](https://freemcp.space/featured/viewport-iq) — Production-grade Browser Inspection & Responsive Testing MCP Server. Inspect websites, test across viewports, detect layout overflow, capture screenshots, and run audits via Playwright & MCP.
- [softglaze-claude-plugin](https://freemcp.space/featured/softglaze-claude-plu) — SoftGlaze Browser plugin for Claude Code and Cowork: isolated browser profiles, proxies and macros, with your approval for every change.
- [nullprint-mcp](https://freemcp.space/featured/nullprint-mcp) — MCP server for Nullprint, the AI antidetect browser: let Claude, Codex, DeepSeek and other AI agents create, launch, check and drive browser profiles.
- [cat-burglar](https://freemcp.space/featured/cat-burglar) — A stealth browser MCP for agents: three engines, diff observations, site memory, a human CAPTCHA handoff, and a benchmark harness.
- [roomvana-mcp](https://freemcp.space/featured/roomvana-mcp) — MCP server for Roomvana — browse room types & design styles and get a direct link to the Roomvana AI interior-design studio at https://roomvana.ai
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
