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
- [nexus-browser-mcp](https://freemcp.space/featured/nexus-browser-mcp) — Browser automation MCP server with event-driven deterministic snapshots (Playwright + a11y tree) / 事件驱动确定性快照的浏览器操控 MCP 服务器
- [groundhog](https://freemcp.space/featured/groundhog) — Safe, self-hosted web grounding for AI agents and crawlers — stealth Chrome over MCP
- [pymol-mcp](https://freemcp.space/featured/pymol-mcp) — Headless PyMOL MCP server for molecular visualization, GROMACS/LAMMPS MD workflows, and clathrate-hydrate cage analysis
- [diagrams-mcp-app-core](https://freemcp.space/featured/diagrams-mcp-app-cor) — MCP server for Diagrams.so. 23 tools that let an AI agent generate, edit and review cloud architecture diagrams as native draw.io files.
- [mcp-books](https://freemcp.space/smeet666/mcp-books) — MCP server that searches inside several archives at once, browses their catalogues and reads records. No API key.
- [mcp-server](https://freemcp.space/featured/mcp-server-15) — External anchoring layer: records AI agent accountability boundaries on both sides. Content-blind.
- [gliana-mcp](https://freemcp.space/featured/gliana-mcp) — Pay-per-call access to 90+ AI models (LLM chat, image, video, music, speech) plus utility and data tools — web scraping, screenshots, OCR, face matching, crypto and FX rates. No signup and no API key: HTTP 402 settles each call from your own wallet in USDC on Base, Solana, BNB Chain or Algorand. The tool list is read live from the gateway, so it is never stale. `npx -y gliana-ai-mcp` or remote `https://mcp.glianalabs.com`.
- [maket](https://freemcp.space/featured/maket) — Visual design workspace for AI assistants: create posters, flyers, labels and social posts as multi-page HTML/CSS documents with live preview, annotations, brand guides, asset libraries and data-driven collections; validate layouts, export print-ready PDFs and prepare Gmail drafts. Works with Codex, Claude, Gemini and any MCP client.
- [reachpad-mcp](https://freemcp.space/featured/reachpad-mcp) — MCP server for reachpad: lets Claude, Codex and other coding agents build full-stack apps in persistent workspaces and share them by link, without a separate deployment.
- [agent-cold-email](https://freemcp.space/featured/agent-cold-email) — Coldrig — cold email infrastructure run entirely by your coding agent (Claude Code / Codex / Cursor / Cline). One token, 28 intent-level MCP + HTTP tools and an npm CLI: domain purchase, mailboxes, warmup, sequences, replies, deliverability guardrails. Free fault-injecting sandbox.
- [solvegate-mcp](https://freemcp.space/featured/solvegate-mcp) — MCP server for Cloudflare Turnstile — inspect a page for Turnstile without an API key, and clear Turnstile and WAF challenges.
- [dibs](https://freemcp.space/featured/dibs) — Call dibs on files. Coordination for parallel coding agents — file claims with expiry, enforcement hooks, and git-native lessons. One binary, no server, no database.
- [chinese-almanac-mcp](https://freemcp.space/yonlandwu/chinese-almanac-mcp) — MCP server for the Chinese almanac — auspicious date picking (择日) for weddings, moves, openings & major purchases, lucky hours (吉时), hour pillars, solar terms, horoscopes. JPL precision. 中国黄历择日 MCP 服务 — 嫁娶开业搬家择吉日.
- [calibreweb-mcp](https://freemcp.space/featured/calibreweb-mcp) — MCP server for Calibre-Web — read-only library access via the OPDS feed
- [a11y-toolkit](https://freemcp.space/featured/a11y-toolkit) — MCP server + CLI for WCAG 2.2 accessibility: contrast (pairs & text-over-image), EU accessibility declarations (RD 1112/2018 · Ley 11/2023 · EAA), aria-live monitor. Multilanguage es/en · zero dependencies
- [magg](https://freemcp.space/featured/magg) — Magg: The MCP Aggregator
- [enigma-python-mcp](https://freemcp.space/featured/enigma-python-mcp) — An MCP (Model Context Protocol) server that brings the capabilities of the enigmapython library to LLMs, allowing them to encrypt and decrypt messages using historically accurate Enigma machine emulators
- [b2b-enrichment-mcp](https://freemcp.space/featured/b2b-enrichment-mcp) — Unified MCP server combining Hunter.io and Apollo for B2B lead enrichment
- [dchub-mcp-server](https://freemcp.space/featured/dchub-mcp-server) — Live data-center, power-grid, energy, interconnection-queue, fiber, natural-gas & M&A intelligence for AI agents — 82 tools, 18,000+ facilities, 300+ markets scored daily (DC Hub Power Index), 1,900+ tracked M&A deals, live grid telemetry across 49 regions. Remote MCP at dchub.cloud/mcp. DCPI & grid analysis CC-BY-4.0.
- [mcp-bytesmith](https://freemcp.space/featured/mcp-bytesmith) — Pure-Python MCP server for encoding, hashing, and crypto-primitives — computed for real, locally.
- [apple-mail-mcp](https://freemcp.space/featured/apple-mail-mcp-2) — MCP server for Apple Mail: sub-ms search over 300k+ messages via Mail's own SQLite index, verified sends, Exchange body backfill, triage plan/review/apply. 849 tests, MIT.
- [Claude-MCP-Read-Email-Attachments](https://freemcp.space/featured/claude-mcp-read-emai-2) — Local MCP server for Claude Desktop to read Outlook emails/bodies/attachments and send local files as attachments.
- [browserless-mcp](https://freemcp.space/featured/browserless-mcp) — Official MCP server for the Browserless.io 
- [cognigy-ai-mcp-management-server](https://freemcp.space/featured/cognigy-ai-mcp-manag) — MCP server for Cognigy.AI - 132 tools that let Claude, Cursor & other AI assistants build, configure, test & operate conversational AI agents via the Model Context Protocol.
- [waxseal-sdk](https://freemcp.space/featured/waxseal-sdk) — Ed25519 cryptographic identity for apps and AI agents — MCP server for Claude/Cursor/Windsurf + JS/TS verify SDK
- [lobbyvoices-mcp](https://freemcp.space/featured/lobbyvoices-mcp) — Official MCP server for Lobby (lobbyvoices.com) — 8 free, no-auth receptionist tools for AI agents: phone scripts & IVR menus (EN+ES), ElevenLabs agent prompts, missed-call math, call simulation, and more.
- [zerodrop-mcp](https://freemcp.space/featured/zerodrop-mcp) — MCP server for ZeroDrop — gives AI agents disposable inboxes with auto-extracted OTPs and magic links. Claude, Cursor, Claude Code.
- [leetcode-mcp-server](https://freemcp.space/featured/leetcode-mcp-server) — An MCP server enabling automated access to LeetCode's problems, solutions, and public data with optional authentication for user-specific features, supporting leetcode.com & leetcode.cn sites.
- [open-feishu-mcp-server](https://freemcp.space/featured/open-feishu-mcp-serv) — A Model Context Protocol (MCP) server with built-in Feishu OAuth authentication, supporting remote connections and providing comprehensive Feishu document management tools including block creation, content updates, and advanced features.
- [nworks](https://freemcp.space/featured/nworks) — Full-featured MCP server and CLI for LINE WORKS (NAVER WORKS) — 26 tools covering messages, calendar, drive, mail, tasks, and boards. Automate with AI agents or scripts.
- [whatsapp-mcp-stream](https://freemcp.space/featured/whatsapp-mcp-stream) — A WhatsApp MCP server built around Streamable HTTP transport, using Baileys for WhatsApp connectivity, with a web admin UI and bidirectional media flow (upload + download).
- [mcp-server](https://freemcp.space/featured/mcp-server-14) — WAzion MCP Server - Connect AI agents to WhatsApp via WAzion API. Smart copilot, 24/7 automation, mass marketing.
- [websitetoolbox-mcp](https://freemcp.space/featured/websitetoolbox-mcp) — MCP server for Website Toolbox forum — exposes Categories, Topics, Posts, Users, and more via the Forum REST API
- [zulipmcp](https://freemcp.space/featured/zulipmcp) — Run AI agents in Zulip as @mentionable bots — or wire into any MCP client.
- [owlex](https://freemcp.space/featured/owlex) — AI council server: query CLI agents (Claude Code, Codex, Gemini, and OpenCode) in parallel with deliberation rounds
- [pluggedin-mcp-proxy](https://freemcp.space/featured/pluggedin-mcp-proxy) — Plugged.in MCP Server manages all your other MCPs in one MCP.
- [ntfy-mcp](https://freemcp.space/featured/ntfy-mcp) — The MCP server that keeps you informed by sending the notification on phone using ntfy
- [imessage-mcp](https://freemcp.space/wyattjoh/imessage-mcp-2) — A Model Context Protocol server for reading iMessage data from macOS.
- [neurodock](https://freemcp.space/featured/neurodock) — A local-first cognitive substrate for neurodivergent professionals. Gives Claude memory, a sense of time, a translator for corporate ambiguity, and a guardrail that refuses to amplify rumination, hyperfocus, or sycophancy. MCP-native. No telemetry. AGPL-3.0-or-later. Self-ID sufficient — no diagnosis gating.
- [didlogic_mcp](https://freemcp.space/featured/didlogic-mcp) — An MCP server for [DIDLogic](https://didlogic.com). Adds functionality to manage SIP endpoints, numbers and destinations.
- [spix-mcp](https://freemcp.space/featured/spix-mcp) — Spix MCP Server — give AI agents phone calls, SMS, and email as tool calls
- [fhir-mcp-server](https://freemcp.space/featured/fhir-mcp-server-2) — FHIR MCP Server – helping you expose any FHIR Server or API as a MCP Server.
- [sendmux-sdk](https://freemcp.space/featured/sendmux-sdk) — Official monorepo of SDKs, CLI, and MCP servers for Sendmux email APIs across TypeScript, Python, Go, PHP, Rust, and Ruby.
- [vrchat-mcp](https://freemcp.space/featured/vrchat-mcp) — This project is a Model Context Protocol (MCP) server for interacting with the VRChat API.
- [fast-mcp-telegram](https://freemcp.space/featured/fast-mcp-telegram) — Telegram MCP gateway for AI agents: 8 tools, multi-tenant HTTP/stdio, MTProto
- [mcp-hey](https://freemcp.space/featured/mcp-hey) — MCP server for Hey.com: read, send, search, and organise email from Claude or any MCP client. Runs locally, stores no credentials, respects rate limits.
- [zoho-mail-mcp](https://freemcp.space/featured/zoho-mail-mcp) — MCP server for Zoho Mail — read, search, and send email via Claude
- [botbell-mcp](https://freemcp.space/featured/botbell-mcp-2) — BotBell MCP Server — Give Your AI a Voice
- [mcp-telegram](https://freemcp.space/featured/mcp-telegram) — Telegram MCP Server — connect Telegram to Claude AI & ChatGPT. 181 tools: messages, media, reactions, polls, stories & more. MTProto userbot. Self-host (npx) or hosted at mcp-telegram.com.
- [discord-mcp](https://freemcp.space/featured/discord-mcp) — MCP server to control Discord — messages, channels, roles, permissions, members, and moderation
- [cv-mcp-server](https://freemcp.space/featured/cv-mcp-server) — Carbon Voice MCP Server
- [chatterboxio-mcp-server](https://freemcp.space/featured/chatterboxio-mcp-ser-2) — A Model Context Protocol server implementation for ChatterBox, enabling AI agents to interact with online meetings and generate meeting summaries
- [Omnicord](https://freemcp.space/featured/omnicord) — Discord server management MCP for AI agents. Chat, moderation, administration, and full server building from one brief. 150+ tools, with destructive actions gated behind a preview.
- [mcp-server](https://freemcp.space/featured/mcp-server-13) — MCP server for Postcard.bot — let AI agents send real printed postcards. Works with Claude, Cursor, Windsurf, and any MCP client.
- [aiogram-mcp](https://freemcp.space/featured/aiogram-mcp-2) — MCP server middleware for aiogram Telegram bots — expose your bot to AI agents via the Model Context Protocol
- [outlook-assistant](https://freemcp.space/featured/outlook-assistant) — MCP server for Outlook email, calendar, and contacts — let your AI assistant manage your inbox directly from the conversation.
- [better-email-mcp](https://freemcp.space/featured/better-email-mcp) — IMAP/SMTP email for AI agents -- read, send, organize folders, and manage attachments across multiple accounts, with auto-discovery.
- [ringback](https://freemcp.space/featured/ringback) — Let your AI agent call your phone and talk to you — MCP servers for live, interruptible voice calls + tiered alerts, using free self-hosted pieces (pjsua2 + whisper.cpp + Linphone). No paid telephony, no extra API key.
- [email-mcp](https://freemcp.space/featured/email-mcp-2) — Unified MCP server for email access across Gmail, Outlook, iCloud, and IMAP
- [caldav-mcp](https://freemcp.space/featured/caldav-mcp-2) — Universal MCP server for CalDAV protocol integration. Works with any CalDAV-compatible calendar server including Yandex Calendar, Google Calendar (via CalDAV), Nextcloud, ownCloud, Apple iCloud, and others. Supports creating events with recurrence, categories, priority, attendees, reminders, searching events, and retrieving events by UID.
- [mingle-mcp](https://freemcp.space/featured/mingle-mcp) — Your AI meets other people's AIs. You meet the people. Agent-native networking via MCP.
- [Xadeus-QQ-MCP](https://freemcp.space/xadeus/xadeus-qq-mcp) — QQ MCP Server - connect AI agents to QQ via NapCatQQ. Auto-wake, messaging, group management, file sharing, cross-platform.
- [mcp-server](https://freemcp.space/featured/mcp-server-12) — MCP server for MultiMail — Verifiable identity email for AI agents
- [leximo-ai-call-assistant-mcp-server](https://freemcp.space/featured/leximo-ai-call-assis) — An MCP (Model Context Protocol) server that lets you schedule AI phone calls and manage Leximo assignments directly from Claude Desktop or Claude Code — no app switching needed.
- [qorami-sdk](https://freemcp.space/featured/qorami-sdk) — Official Qorami SDK — JS/Python clients, tool schemas and an MCP server so AI agents check email before sending. https://qorami.fr
- [alibaba-cloud-ops-mcp-server](https://freemcp.space/featured/alibaba-cloud-ops-mc-2) — AlibabaCloud CloudOps MCP Server
- [roundtable](https://freemcp.space/featured/roundtable) — Zero-configuration MCP server that unifies multiple AI coding assistants (Codex, Claude Code, Cursor, Gemini) through intelligent auto-discovery and standardized interface
- [codex-control-plane-mcp](https://freemcp.space/featured/codex-control-plane) — Durable MCP control plane for long-running Codex Desktop tasks
- [neurolink](https://freemcp.space/featured/neurolink) — One TypeScript interface for 24+ LLM providers — swap providers without rewriting. MCP-native (connect any MCP server), voice (TTS/STT/realtime), RAG, memory, file processors. Production-origin: powers Tara, Yama, and Clairvoyance at Juspay.
- [join.cloud](https://freemcp.space/featured/join-cloud) — Join.cloud lets AI agents work together in real-time rooms. Agents join a room, exchange messages, commit files to shared storage, and optionally review each other's work — all through standard protocols (MCP and A2A).
- [local-mcp-releases](https://freemcp.space/lmcp/local-mcp-releases) — 215+ local tools for Claude, ChatGPT, Cursor & Grok — Mail, iMessage, Teams, Slack, WhatsApp, OneDrive, Google Drive, Zoom, Outlook, Office. Native macOS, 100% local, no API keys.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
