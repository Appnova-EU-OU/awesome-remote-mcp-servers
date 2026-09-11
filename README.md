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
- [aginxbrowser](https://freemcp.space/featured/aginxbrowser) — The browser built for AI agents — fetch live pages as markdown, render JS/SPAs with built-in V8, take screenshots without Chromium, meta-search 5 engines, and drive interactive login sessions. One Rust binary, stealth TLS fingerprints, MCP native for Claude Code & Cursor. Headless browser alternative to Puppeteer/Playwright.
- [domain-mcp](https://freemcp.space/featured/domain-mcp) — Manage Dynadot domains, DNS, renewals, and transfers from Claude, Cursor, or any MCP client.
- [Agent402](https://freemcp.space/featured/agent402) — agent402.tools: 500+ pay-per-call tools, metered models and finished reports for AI agents, paid per call in USDC over x402 and MPP or by card. Open source, self-hostable, MCP-native. The applied layer of agentic finance.
- [MCPEmails](https://freemcp.space/asgeiralbretsen/mcpemails) — Give your AI agent an inbox. Hosted remote MCP server: connect Gmail or any IMAP mailbox (Fastmail, iCloud, Yahoo, Zoho) and read, search, send, organize, schedule and auto-triage email from Claude, ChatGPT, Cursor or any MCP client. OAuth sign-in, per-key permission scopes, mail fetched live and never stored. Nothing to install or deploy. Setup guides: https://mcpemails.com/docs
- [gemini-antigravity-bridge](https://freemcp.space/nandhakumar-murugan/gemini-antigravity-b) — ⚡ Bridge connecting Google Gemini Spark & Cloud AI to your local machine via MCP with autonomous file creation, terminal execution, and subagent orchestration.
- [gigamail](https://freemcp.space/featured/gigamail) — Mail for AI agents ( and humans). MCP server giving Claude (or any agent) safe, permission-controlled access to email (Microsoft Graph + IMAP), calendar and your knowledge files. Two-phase confirmation for sends, audit log, local index. No built-in LLM: your agent brings the intelligence.
- [ssh-mcp-server](https://freemcp.space/featured/ssh-mcp-server-2) — SSH MCP server for AI agents: remote commands, file transfer, log search and server audits through OpenSSH.
- [SmartCLI](https://freemcp.space/featured/smartcli) — Three Agent Skills over one pluggable PTY + pyte core: drive TUIs, design terminal effects, and render cell-accurate UIs. pip install smartcli-toolkit
- [markdown-to-whatsapp](https://freemcp.space/featured/markdown-to-whatsapp) — Convert Markdown into WhatsApp formatting: tables drawn to fit the phone's monospace width. Web page, library, CLI and MCP server.
- [clawdcall-mcp](https://freemcp.space/featured/clawdcall-mcp) — Let AI agents place consent-based outbound phone calls and retrieve transcripts, summaries, and outcomes. Use the hosted Streamable HTTP server or install with `npx -y clawdcall-mcp`.
- [sendgrid-mcp-secure](https://freemcp.space/featured/sendgrid-mcp-secure) — Security-first MCP server for SendGrid — recipient allowlists, send caps, review-mode, audit log, no silent BCC. Hardened against the postmark-mcp incident class.
- [heliograph](https://freemcp.space/featured/heliograph) — Remote, captured, auditable execution on a machine you cannot log into. Control CLI, relay and transports around the heliograph method.
- [public-browser](https://freemcp.space/featured/public-browser) — Lets Claude Code and Cursor drive Chrome. Browse your real profile: -30% tokens, -25% cost, -41% tool calls, -34% tool defs, +40% faster. Direct CDP, a11y-tree refs, server-side plan executor. MIT, no paid tier.
- [claude-codex-bridge](https://freemcp.space/featured/claude-codex-bridge) — Use Codex agents from Claude Code with live progress, steering, and session continuation.
- [Nimbus](https://freemcp.space/featured/nimbus) — On-call intelligence for DevOps and platform teams. Local-first AI agent over your tools — HITL-gated, MCP-native, AGPL-3.0.
- [cursor-delegate-mcp](https://freemcp.space/featured/cursor-delegate-mcp) —  Stop burning your Claude or Codex limits on boilerplate. Delegate multi-file implementation to Cursor's Composer 2.5 over MCP — your frontier model writes the brief and reviews the diff; Composer does the typing, fast, on a separate quota.
- [unclick](https://freemcp.space/featured/unclick) — The universal remote for AI: one MCP install gives agents 450+ callable endpoints across 60+ integrations, plus persistent cross-session memory. Works with Claude, ChatGPT, Cursor, and any MCP client.
- [allmcps-server](https://freemcp.space/featured/allmcps-server) — Official MCP server for AllMCPs.com — submit MCP servers to the directory directly from your AI agent.
- [relayer-mcp](https://freemcp.space/featured/relayer-mcp) — MCP server for XNS S3-compatible storage — agent-driven Relayer install & management. Mirrored from GitLab.
- [mcp-server-vibes-coded](https://freemcp.space/featured/mcp-server-vibes-cod) — 26-tool MCP server for agent security, scanner consensus, x402 reliability, and Vibes-Coded's 344-resource commerce catalog.
- [LiuHe](https://freemcp.space/featured/liuhe) — LLM-native code toolkit: Rust multi-language parser (tree-sitter) + 44 MCP tools for atomic editing, impact analysis, reference tracing and deterministic zero-LLM code quality gates. Built for the handless, eyeless, memoryless LLM.
- [synapse-mcp](https://freemcp.space/featured/synapse-mcp) — Free, 100% local MCP server. Turns your codebase into an AST knowledge graph so AI coding agents (Claude, Cursor, Copilot) get exact caller trees, semantic search, and safe writes — 60% fewer tokens, zero data egress.
- [dochost-mcp](https://freemcp.space/featured/dochost-mcp) — Official MCP server for dochost (https://dochost.io) — publish Markdown or HTML to a shareable link from Claude, ChatGPT or Cursor. OAuth, no API keys.
- [mcp-azure](https://freemcp.space/featured/mcp-azure) — MCP server for Azure (Resource Manager) — inventory, tags, VM power, lifecycle — with governance controls (scoping, protected groups, location allowlist, delete gating, confirmation).
- [snapshot-site-mcp](https://freemcp.space/featured/snapshot-site-mcp) — Let Claude, ChatGPT, and other MCP clients capture, compare, and analyze any web page — hosted with OAuth, or local over stdio.
- [awarse-mcp](https://freemcp.space/featured/awarse-mcp) — Model Context Protocol (MCP) server for automated test heal, Playwright orchestration, and AI-assisted QA workflows.
- [traecnclaw-mcp-skill](https://freemcp.space/featured/traecnclaw-mcp-skill) — Public TRAECNclaw MCP Agent Skill and installable server package bundle.
- [opticparse-public](https://freemcp.space/featured/opticparse-public) — Stealth Multimodal Web Scraper & 0-Day Phishing Shield for AI Agents. Alternative to Firecrawl & Crawl4AI with zero-CSS vision extraction, 200 free trial credits, and native LangChain / ElizaOS / MCP support.
- [repo-cartographer](https://freemcp.space/featured/repo-cartographer) — Understand any codebase in 60 seconds - an MCP server, CLI and GitHub Action that turns any repo into an architecture diagram (Mermaid/Graphviz) and enforces architecture rules in CI. Works with Claude, Cursor, ChatGPT and any MCP client.
- [picoberry-mcp](https://freemcp.space/featured/picoberry-mcp) — PicoBerry MCP server — an AI 3D workspace for games, VR, and beyond. Generate, remesh, texture, and animate 3D assets from any MCP client. Multi-engine, one API.
- [lambdacad-mcp](https://freemcp.space/featured/lambdacad-mcp) — λ MCP server for any AutoLISP-capable CAD — AI drafting with 105 tools, 2D + 3D solids, STL export. BricsCAD® on Linux is the reference adapter. No COM, no SDK.
- [bridgenode-mcp](https://freemcp.space/featured/bridgenode-mcp) — BridgeNode — x402 pay-per-request AI inference. MCP server for AI agents.
- [minia2a-mcp](https://freemcp.space/featured/minia2a-mcp) — Remote MCP server for minia2a.uk — 1,680+ x402 pay-per-call agent tools. USDC on Base, 5 free trial calls per wallet.
- [k8s-mcp-server](https://freemcp.space/featured/k8s-mcp-server) — Model Context Protocol (MCP) server for debugging, analyzing, and diagnosing Kubernetes clusters directly from AI agents.
- [stacktree-mcp](https://freemcp.space/featured/stacktree-mcp) — MCP server for stacktr.ee — publish HTML privately from any AI agent (Claude Code, Codex, Cursor, Claude.ai). Seven tool calls for unguessable, replace-in-place URLs.
- [eqvps-mcp](https://freemcp.space/eqvps/eqvps-mcp) — Crypto-native VPS that AI agents rent and pay for autonomously via MCP — no KYC
- [krova-node](https://freemcp.space/featured/krova-node) — Monorepo for the Krova Cloud JS/TS packages — SDK, CLI, MCP, webhook verifier, n8n node.
- [noodle-mcp](https://freemcp.space/featured/noodle-mcp) — Noodle Biomedical Literature Discovery MCP — search papers and traverse citation or semantic literature graphs.
- [identityforge-mcp](https://freemcp.space/featured/identityforge-mcp) — Design systems, brand naming, and domain research for coding agents through MCP and CLI.
- [mcp-imslp](https://freemcp.space/featured/mcp-imslp) — MCP server for IMSLP, the Petrucci Music Library. Read works, scores and recordings. No API key required.
- [mcp-lrclib](https://freemcp.space/featured/mcp-lrclib) — MCP server for LRCLIB: search tracks and fetch plain or time-synced (LRC) lyrics. No API key.
- [runcomfy-mcp](https://freemcp.space/featured/runcomfy-mcp) — Remote MCP for RunComfy: ComfyUI deployments, hosted models, LoRA training. 31 tools.
- [fatenava-mcp](https://freemcp.space/featured/fatenava-mcp) — FateNava MCP — BaZi, Zi Wei Dou Shu & Western Astrology chart casting for AI agents
- [glyphdna-mcp](https://freemcp.space/featured/glyphdna-mcp) — GlyphDNA MCP adapter: machine-native identity, verifiable meeting rooms, script provenance. Join with one MCP call.
- [frantic-mcp](https://freemcp.space/featured/frantic-mcp) — A public bounty board where AI agents do paid work. Claim funded bounties, get paid in USDC on Base on accepted delivery.
- [taghvim](https://freemcp.space/qazvinyjavad/taghvim) — Deterministic temporal reasoning engine for AI agents. 12 tools for date/time arithmetic, timezone conversion with DST, business days across 100+ countries, public holidays, RFC 5545 recurrence, Gregorian/Persian calendar conversion, and temporal claim verification. `npx taghvim-mcp`
- [codecalc](https://freemcp.space/featured/codecalc) — Universal code & logic calculator for AI models: 52 MCP tools across 31 languages. Rust-sandboxed execution with verdicts, sessions, artifacts, exact arithmetic, and verified translation/optimization. No LLM, no gateway, no telemetry: the caller is the model. Apache-2.0.
- [lizard-mcp](https://freemcp.space/featured/lizard-mcp) — MCP server for deploying and managing apps on Lizard — connect ChatGPT, Claude or any MCP client to ship services, read logs, set secrets, scale and attach domains. 33 tools, OAuth 2.1, destructive actions require explicit confirmation.
- [tarot-mcp-server](https://freemcp.space/featured/tarot-mcp-server) — MCP server exposing 78-card tarot deck meanings and spreads to Claude, Cursor, Windsurf. Powered by deckaura.com
- [openhire](https://freemcp.space/featured/openhire) — Agent-native job protocol over public ATS APIs — remote AI/Infra jobs for your MCP client. Your résumé never transits the server.
- [claimidx](https://freemcp.space/featured/claimidx) — Prior art for AI agents. Public signed claim index of failures other agents have already paid to solve.
- [flowproof-mcp](https://freemcp.space/featured/flowproof-mcp) — Run reproducible bioinformatics pipelines from an AI assistant over MCP, with verifiable provenance
- [mirastack-redfish-mcp](https://freemcp.space/featured/mirastack-redfish-mc) — Governed MCP server for DMTF Redfish-compliant BMCs. Read-only by default; power, firmware and account operations require explicit opt-in
- [snapsurf](https://freemcp.space/featured/snapsurf) — Web navigation and verification for AI agents: a compact semantic page digest, a typed diff after each action, and assertions over that diff. MCP server and CLI on Playwright and SnapDOM.
- [nutrients-mcp](https://freemcp.space/featured/nutrients-mcp) — MCP server giving AI assistants food image & text nutrition analysis — calories, macros, vitamins, minerals, allergens. Powered by TastyAPI.
- [den_archi_mcp](https://freemcp.space/featured/den-archi-mcp) — AI Agent 를 위한 한국 AEC 전문 지식 큐레이션 MCP — 기준·법령과 실무, 그 사이의 이유까지. 답에는 근거가 붙고, 근거가 없으면 답하지 않습니다. Curated Korean AEC expertise for AI agents.
- [mcp-bideetmusique](https://freemcp.space/featured/mcp-bideetmusique) — MCP server for Bide & Musique: search the hand-built catalogue of forgotten French songs by performer, title, writer or lyrics. No API key.
- [image-mcp](https://freemcp.space/featured/image-mcp) — 本地 Pillow 图片处理 MCP：12 工具（信息/缩放/裁剪/转换/压缩/旋转/翻转/缩略图/水印/特效/占位/叠加），离线零成本，经 dsh-mcp-client 接入 DSH。Local Pillow image MCP with 12 tools for DeepSeek Harness, offline & free. | Platforms: macOS/Windows/Linux (Python+Pillow)
- [shakespeare-monologues-mcp](https://freemcp.space/featured/shakespeare-monologu) — Read-only MCP server for shakespeare-monologues.org - search and fetch Shakespeare monologue metadata over the Model Context Protocol
- [vineverse-mcp](https://freemcp.space/featured/vineverse-mcp) — stdio bridge to the hosted VineVerse MCP server - the Bible as a knowledge graph
- [infyicon-mcp](https://freemcp.space/featured/infyicon-mcp) — MCP server for Infyicon — search 161,000+ free hand-drawn icons and fetch ready-to-embed SVG/PNG from Claude, ChatGPT, Cursor, VS Code and any MCP client. Hosted endpoint: https://infyicon.com/mcp (no auth)
- [sansfiction-mcp](https://freemcp.space/featured/sansfiction-mcp) — Search a books catalog (titles, authors, series, ISBNs, collections) and manage a personal reading library — status, reading progress, ratings, reviews, collections, stats. Public catalog needs no auth; personal library uses a bearer token. Hosted MCP: https://sansfiction.com/api/mcp
- [microtap-mcp](https://freemcp.space/featured/microtap-mcp) — Repo for the microtap-mcp 
- [utility-grid-mcp](https://freemcp.space/featured/utility-grid-mcp) — MCP server for discovering and calling 400+ practical APIs through six compact tools, with free catalog search and pay-per-call x402 execution on Base.
- [findagent-mcp](https://freemcp.space/featured/findagent-mcp) — The MCP server for FindAgent — the vetted, cross-LLM marketplace of doer agents. Hosted remote endpoint: mcp.findagent.cloud/mcp
- [alibabacloud-tablestore-mcp-server](https://freemcp.space/featured/alibabacloud-tablest) — MCP service for Tablestore, features include adding documents, semantic search for documents based on vectors and scalars, RAG-friendly, and serverless.
- [dicom-mcp](https://freemcp.space/featured/dicom-mcp) — Model Context Protocol (MCP) for interacting with dicom servers (PACS etc.)
- [mcp-server-tidb](https://freemcp.space/featured/mcp-server-tidb) — mcp server for tidb
- [node-code-sandbox-mcp](https://freemcp.space/featured/node-code-sandbox-mc) — A Node.js–based Model Context Protocol server that spins up disposable Docker containers to execute arbitrary JavaScript.
- [schemabrain](https://freemcp.space/featured/schemabrain) — The trust and intelligence layer between AI agents and your database. Read-only by architecture, semantic knowledge graph + audit log, MCP-native.
- [local-ydb-toolkit](https://freemcp.space/featured/local-ydb-toolkit) — Codex skill and MCP server for operating Docker-based local YDB deployments, locally or over SSH.
- [OpenDataMCP](https://freemcp.space/featured/opendatamcp) — Connect any Open Data to any LLM with Model Context Protocol.
- [mcp-k8s](https://freemcp.space/featured/mcp-k8s) — A Kubernetes MCP (Model Control Protocol) server that enables interaction with Kubernetes clusters through MCP tools.
- [mcp-cockroachdb](https://freemcp.space/featured/mcp-cockroachdb) — The CockroachDB MCP Server is a natural language interface designed for agentic applications to manage, monitor and query data in CockroachDB.
- [sql-query-mcp](https://freemcp.space/featured/sql-query-mcp) — A general-purpose MCP server that lets AI work with multiple databases within clear boundaries.
- [mcp-aiven](https://freemcp.space/featured/mcp-aiven) — Model Context Protocol server for Aiven
- [inoyu-mcp-unomi-server](https://freemcp.space/featured/inoyu-mcp-unomi-serv) — An implementation of Anthropic's Model Context Protocol for the Apache Unomi CDP
- [google-searchconsole-mcp](https://freemcp.space/featured/google-searchconsole) — MCP server for Google Search Console — query search analytics, inspect URLs, find keyword opportunities, track SEO performance. Works with Claude Desktop, Cursor, Windsurf.
- [yanifend-mcp](https://freemcp.space/featured/yanifend-mcp) — YaniFend MCP server — manage your YaniFend feedback questionary (works on any website) and read answers from Claude
- [kom](https://freemcp.space/featured/kom) — kom 是一个用于 Kubernetes 操作的工具，SDK级的kubectl、client-go的使用封装。并且支持作为管理k8s 的 MCP server。 它提供了一系列功能来管理 Kubernetes 资源，包括创建、更新、删除和获取资源，甚至使用SQL查询k8s资源。这个项目支持多种 Kubernetes 资源类型的操作，并能够处理自定义资源定义（CRD）。 通过使用 kom，你可以轻松地进行资源的增删改查和日志获取以及操作POD内文件等动作。
- [mcp-server-iaptic](https://freemcp.space/featured/mcp-server-iaptic) —  Model Context Protocol server for interacting with iaptic
- [mcp-analytics](https://freemcp.space/featured/mcp-analytics) — The statistical analyst in your AI chat — bring data and a question, own a citable, re-runnable analysis. Four depth tiers, from instant Snapshot to full Deck study. Works in Claude, Cursor, and any MCP client.
- [mcp-icp-fit-scorer](https://freemcp.space/featured/mcp-icp-fit-scorer) — MCP server for ICP Fit Scorer. Scores a company against your ideal customer profile with weighted signals via Apify. Returns a 0 to 100 score, a tier, and a per-signal breakdown. Clay-ready output.
- [excalidraw-architect-mcp](https://freemcp.space/featured/excalidraw-architect) — Turn your architecture into a living, queryable knowledge graph - and render it as beautiful auto-laid-out Excalidraw diagrams. An MCP server for Cursor, Claude Code & Windsurf. Offline, no API keys.
- [WebReaper](https://freemcp.space/featured/webreaper) — AI-native web scraper. Single binary with a bundled Claude Code skill. MIT-licensed alternative to Firecrawl.
- [pipedrive-mcp-server](https://freemcp.space/featured/pipedrive-mcp-server) — MCP server for Pipedrive CRM. 155 contract-tested tools, v2-first API, gated destructive ops. Works with Claude Desktop, Claude Code, and any MCP client.
- [horizon-shield](https://freemcp.space/featured/horizon-shield) — NENRIN: tree rings for AI facing services. Bitcoin-anchored public ledger, open witnessing, and an MCP server for verifiable Japanese construction estimates. The operator cannot delete a valid record.
- [outlook-local-mcp](https://freemcp.space/featured/outlook-local-mcp) — Local MCP server for Microsoft Outlook — calendars, events, and email via Microsoft Graph API
- [openagentemail](https://freemcp.space/featured/openagentemail) — Self-hosted email for AI agents — the open-source alternative to AgentMail. One compose file → unlimited inboxes, OTP extraction, MCP server.
- [wellness-nourish](https://freemcp.space/featured/wellness-nourish) — Local-first nutrition MCP for Claude/Cursor: USDA food search, barcode + photo, meal logging
- [standard-vocal-mcp](https://freemcp.space/featured/standard-vocal-mcp) — Voice Agent Factory MCP — deploy, eval, and audit phone agents built on Vapi. Vertical templates, self-testing agents, audio forensics, prompt versioning, CI regression gates.
- [cloudflare-workers-ai-mcp](https://freemcp.space/featured/cloudflare-workers-a) — MCP server for Cloudflare Workers AI — LLM inference, embeddings, and image generation for AI agents
- [coolify-mcp](https://freemcp.space/featured/coolify-mcp) — MCP server for Coolify — 64 tools to deploy, diagnose, and manage apps, databases, and services on your self-hosted PaaS. OpenAPI-generated schemas, docs search, secrets masked by default.
- [nodriver-mcp-server](https://freemcp.space/featured/nodriver-mcp-server) — Undetected browser automation MCP server - a stealth, anti-bot-resistant alternative to chrome-devtools-mcp for Claude, Cursor and AI agents. Powered by nodriver (bypasses Cloudflare/WebDriver detection). 65 tools, plus several isolated browsers at once so parallel agents never share a session.
- [BlazingCDN-MCP](https://freemcp.space/featured/blazingcdn-mcp) — Official MCP server for BlazingCDN - AI agents (Claude, Cursor, Windsurf) manage CDN resources, purge cache, query metrics, domains, Cloud Storage and Video CDN
- [ghostlight](https://freemcp.space/featured/ghostlight) — Give compatible AI agents a visible workspace in the Chromium browser you already use. Local-first, with optional policy and audit.
- [discord-mcp](https://freemcp.space/featured/discord-mcp-2) — MCP server over the Discord REST API: 5 read tools always on, 7 write tools gated off by default behind an env flag. Typed errors for every failure mode.
- [redditapis-mcp](https://freemcp.space/featured/redditapis-mcp) — Official MCP server for redditapis.com — 11 read-only Reddit tools for Claude, Cursor, and any MCP client.
- [hetzner-dns-mcp](https://freemcp.space/featured/hetzner-dns-mcp) — MCP server for managing DNS zones and records via the Hetzner Cloud API
- [screenshotscout-mcp](https://freemcp.space/featured/screenshotscout-mcp) — Official MCP server for the Screenshot Scout screenshot API.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
