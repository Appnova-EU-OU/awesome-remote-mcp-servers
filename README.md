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
- [unitares](https://freemcp.space/featured/unitares) — Accountability infrastructure for long-running AI agents. Self-hosted MCP server: identity, claims and evidence, review, outcomes, and reconstruction across agent runtimes.
- [ifc-ruhsat](https://freemcp.space/featured/ifc-ruhsat) — Yapı ruhsatı IFC modelini Türkiye dijital proje yönetmeliğine (RG 33331) göre kontrol eder — CLI + MCP + IDS. Checks IFC models against Türkiye's building-permit BIM regulation.
- [mcp-for-maya](https://freemcp.space/featured/mcp-for-maya) — Maya MCP Server with spatial awareness, camera planning, aesthetic analysis, and scene auditing
- [ramen](https://freemcp.space/featured/ramen) — Self-hosted, multi-zone MCP server platform for GKE, EKS and AKS. A git repo of Python tools becomes canary-deployed, autoscaled Rust + Python workers with NeMo guardrails per tool, Entra ID / Google Workspace SSO, custom roles, OAuth 2.1, secrets, IP rules and audit. Clients on macOS, Windows and Linux.
- [caishi](https://freemcp.space/featured/caishi) — 采诗 · 给 AI 用的中文互联网能力包：一条命令读抖音/B站/小红书/公众号/知乎/头条等 33 站（满配 40）| Read the Chinese internet from your AI agent. Read-only, reuses your browser sessions.
- [formfeed](https://freemcp.space/featured/formfeed) — Formfeed client libraries, CLI, development kit and integrations: PDF and image generation from templates
- [gaussdb-ro-mcp](https://freemcp.space/featured/gaussdb-ro-mcp) — Read-only MCP server for GaussDB, built for coding agents.
- [kafka-mcp](https://freemcp.space/featured/kafka-mcp-2) — MCP server that exposes Kafka debugging to an LLM: find messages, measure lag, unblock consumers. Read-only endpoints, previews before writes.
- [wraps-js](https://freemcp.space/featured/wraps-js) — TypeScript SDKs for AWS SES and SMS, plus an MCP server that lets AI agents send email from your own AWS account
- [Agent-Uplink](https://freemcp.space/featured/agent-uplink) —  Let your AI sessions talk to each other — locally. MCP server + local hub that gives Claude Code / Claude Desktop sessions role accounts, private DMs, and shared channels.
- [shipback-sftp](https://freemcp.space/featured/shipback-sftp) — Deploy to cPanel. Undo in one command.
- [agentgo-mcp](https://freemcp.space/featured/agentgo-mcp) — MCP server for AgentGo, the browser your AI agent drives: compact page outlines, diff-only replies, real input, human approval. MIT.
- [signdocs-mcp-server](https://freemcp.space/featured/signdocs-mcp-server) — Servidor MCP oficial da SignDocs Brasil: assinatura eletrônica e digital com ICP-Brasil, biometria e OTP direto de agentes de IA. Official MCP server for the SignDocs Brasil e-signature API — signing sessions, envelopes, document verification.
- [qualien-mcp](https://freemcp.space/featured/qualien-mcp) — A composite MCP gateway that aggregates multiple MCP servers behind one connection — curated for SDET/QE workflows.
- [The-top-innovation](https://freemcp.space/featured/the-top-innovation) — Lossless context guard for AI coding agents: outlines big files and digests noisy command output, nothing lost.
- [sqlite-mcp-server](https://freemcp.space/featured/sqlite-mcp-server) — A lightweight Model Context Protocol (MCP) server for inspecting and querying local SQLite databases safely.
- [mcp-creator-lead-list-all-in-one](https://freemcp.space/featured/mcp-creator-lead-lis) — Keywords or handles in, a finished influencer lead list with contact details out.
- [Selfhost-Remote-Mail-MCP](https://freemcp.space/featured/selfhost-remote-mail) — Use your own email from Claude, ChatGPT, Codex and other AI apps, on computer and phone. Self-hosted IMAP/SMTP MCP server: no middleman, OPEN SOURCE, encrypted connections and uploads, no tracking, sending only when you say so. Drop a file in the chat to email it, up to 5 mailboxes, add-ons.
- [groundmail-mcp](https://freemcp.space/featured/groundmail-mcp) — MCP server for Groundmail transactional email: send email, check delivery and set up sending domains from Claude, ChatGPT, Cursor and any MCP client. Hosted with OAuth at mcp.groundmail.dev.
- [impreza-mcp](https://freemcp.space/featured/impreza-mcp) — MCP server for Impreza Host: deploy custom apps to managed VPSes from your AI editor.
- [mcp-server](https://freemcp.space/featured/mcp-server-24) — Hostsmith MCP Server
- [TrueNAS-AIops](https://freemcp.space/featured/truenas-aiops) — Governed TrueNAS SCALE operations — pools, datasets, snapshots, disks, alerts, and services (25 tools) with unbypassable audit logging (MCP + CLI), budget/runaway guards, dry-run, and undo/rollback.
- [Proxy-AIops](https://freemcp.space/featured/proxy-aiops) — Governed AI-ops for Traefik + Caddy + HAProxy reverse proxies / load balancers: routes, services, up
- [biolit-mcp](https://freemcp.space/featured/biolit-mcp) — Citation-grounded biomedical literature review over PubMed, Europe PMC, NCBI Gene and UniProt, with a citation-accuracy benchmark.
- [luw-mcp](https://freemcp.space/featured/luw-mcp) — Official Luw.ai MCP server: AI interior, exterior & landscape design, renders, video and 3D for Claude, Cursor, VS Code and any MCP client. 
- [canvaskeep-mcp](https://freemcp.space/featured/canvaskeep-mcp) — MCP server for CanvasKeep: let Claude Code, Codex and other AI tools generate Excalidraw diagrams in your workspace
- [ai-gateway-mcp](https://freemcp.space/featured/ai-gateway-mcp) — The provider's own price, right inside your chat. Make video, images and voice with 400+ Vercel AI Gateway models (Veo, Kling, Seedance, Nano Banana, GPT Image) from Claude, ChatGPT or any MCP app. Your own copy, your own credits, no markup.
- [kitsune-mcp](https://freemcp.space/featured/kitsune-mcp) — Hot-reload for MCP servers: edit, reload(), call again in the same session. Plus mount any of 130k+ community servers mid-session, Docker-caged.
- [gateonai-mcp-server](https://freemcp.space/featured/gateonai-mcp-server) —    MCP server for GateOnAI: search the AI tools listed on GateOnAI, compare them, build AI workflows, and find tools whose providers refer to the GDPR or state EU hosting on their own pages.
- [gmail-mcp](https://freemcp.space/featured/gmail-mcp-2) — Self-hosted, owner-only Gmail MCP connector for multiple accounts over Streamable HTTP and OAuth.
- [legwork](https://freemcp.space/featured/legwork) — Your AI finds the open-source tool it needs on GitHub. Legwork installs it in a sandbox.
- [whatsapp-mcp](https://freemcp.space/featured/whatsapp-mcp-2) — Full-featured WhatsApp MCP server: Rust MCP server + Go whatsmeow bridge. 39 tools, resources, prompts, live notifications, multi-account, full-text search, raw media for your agent.
- [ascended-browser](https://freemcp.space/featured/ascended-browser) — A real, hardened browser for AI agents (MCP server): verified actions, page reading, dev tools. Works with Claude Code, Codex, opencode.
- [Octocrawl](https://freemcp.space/featured/octocrawl) — Octocrawl: readable Markdown and checked fields from public web pages, for AI agents, RAG and research. Failures come back with a reason. Self-host with REST, SDK or MCP.
- [cairn-commons](https://freemcp.space/featured/cairn-commons) — Cairn Commons participation tools: local MCP, agent skills and A2A schemas
- [mcpcost](https://freemcp.space/featured/mcpcost) — Is that MCP server alive, and what does it cost your context window? Daily health and exact token cost of every server in the MCP registry.
- [mcpolyglot](https://freemcp.space/featured/mcpolyglot) — One MCP server for the databases and REST APIs you already have (Postgres, MySQL, SQLite, MongoDB, OpenAPI), with per-table policy, read-only enforcement, redaction and audit.
- [swarmmemo](https://freemcp.space/featured/swarmmemo) — Talk with agent swarms. Public rooms, private messages, paid tasks and memory for your AI agent. Post from anywhere: MCP, HTTP, email, Nostr.
- [capes](https://freemcp.space/featured/capes) — Superpowers for any AI: a free, self-hosted MCP server (Gmail, Discord, X) with a dashboard. Deploy to your own Vercel in minutes.
- [opsgate](https://freemcp.space/featured/opsgate) — The safety gate between AI agents and your servers. An MCP server for structured, policy-checked, audited infrastructure operations.
- [terse](https://freemcp.space/featured/terse-2) — Terse — an AI-native code language: a machine-designed, token-dense format for AI coding agents. Open source, Apache-2.0.
- [nginx-proxy-manager-mcp](https://freemcp.space/featured/nginx-proxy-manager) — MCP server for Nginx Proxy Manager: automate proxy hosts, Let's Encrypt certificates, and access lists from Claude or any MCP client.
- [ritoko](https://freemcp.space/featured/ritoko) — Resumable browser, HTTP API and MCP automation for AI agents. Replay CSV/Excel batches, verify results and hold uncertain writes for review.
- [serato-dj-mcp](https://freemcp.space/featured/serato-dj-mcp) — Ask Claude or any AI assistant about your Serato DJ library: harmonic search by BPM and Camelot key, crate browsing, duplicate and missing-file audits, and new crates built with a preview before anything is written. Local, macOS. Not affiliated with Serato.
- [shotbox](https://freemcp.space/featured/shotbox) — Eyes, ears and hands for AI agents on GUI programs: a sealed X11 or Wayland session where an agent (over MCP), a script or CI reads the accessibility tree, takes screenshots, records video and sound, clicks, types and drives gamepads, then checks contrast, Tab order, visual diffs, flicker, input latency and audio dropouts. CLI, Python, Playwright.
- [AgentNexus](https://freemcp.space/featured/agentnexus) — Continuously verified registry of the APIs, MCP servers and CLIs that AI agents call — live health checks, reliability history, and an anonymous MCP endpoint agents can connect to without a consent screen.
- [agent-stack-directory](https://freemcp.space/featured/agent-stack-director) — MCP server and open dataset for Agent Stack Directory: 54 checked tools for AI agents.
- [fauxgen-mcp](https://freemcp.space/featured/fauxgen-mcp) — FauxGen MCP — fake identities, addresses & test data for Cursor, Claude and any MCP host
- [pkg-health-mcp](https://freemcp.space/featured/pkg-health-mcp) — Is this dependency still maintained? MCP server, CLI and GitHub Action that score npm packages, PyPI packages and GitHub repos 0–100 for maintenance health, with an A–F grade and plain-language risks. Works with Claude, Cursor and VS Code.
- [agentsensor](https://freemcp.space/featured/agentsensor) — Zero-config dev server & browser runtime error sensor for AI coding agents (Claude Code, Codex, Cursor, Antigravity) via MCP.
- [AgentKit](https://freemcp.space/featured/agentkit) — Governed MCP server and agent runtime: signed action approvals, typed tool effects and audit logs for Claude Desktop, Cursor and custom agents.
- [lagaam](https://freemcp.space/featured/lagaam) — MCP server that stops an AI agent's Trino or Pinot query before it stalls your shared cluster: priced from the engine's own plan, refused with a fix the agent can act on
- [scrupp-mcp-server](https://freemcp.space/featured/scrupp-mcp-server) — MCP server for Scrupp — export LinkedIn, Sales Navigator and Apollo searches, find decision makers, find and verify work emails
- [lauther-js](https://freemcp.space/featured/lauther-js) — Node client and MCP server for Lauther — push notifications and human approvals for anything that can make an HTTP request.
- [hackerearth-mcp](https://freemcp.space/featured/hackerearth-mcp) — MCP server that executes code in 24 languages on HackerEarth sandboxed cloud servers, so AI assistants run code and see real output instead of predicting it.
- [amplerun-mcp](https://freemcp.space/featured/amplerun-mcp) — MCP server for AmpleRun: AI agents find, rent and pay for GPUs (USDC on Base, x402), register their own account, and host their owner's GPU.
- [krds-a11y-mcp](https://freemcp.space/featured/krds-a11y-mcp) — KRDS 컴포넌트를 KWCAG 2.2 접근성 조건과 함께 공급하고, 위반이 남으면 AI의 작업 종료를 막는 MCP 서버
- [taskbullet-mcp-server](https://freemcp.space/featured/taskbullet-mcp-serve) — MCP server for AI agents to place real human phone calls (structured answers back) and delegate tasks to human virtual assistants via TaskBullet.
- [suprsonic-mcp](https://freemcp.space/featured/suprsonic-mcp) — Suprsonic MCP server. Gives any AI agent dozens of capabilities through one connection.
- [mcp_server_ros_2](https://freemcp.space/featured/mcp-server-ros-2) — ROS2 MCP: the MCP server that lets AI agents see, understand and operate ROS 2 robots. MPL-2.0.
- [claude-faf-mcp](https://freemcp.space/featured/claude-faf-mcp) — Persistent Project Context for Claude — IANA-registered .faf format · Core 14 MCP tools (30 with FAF_TOOLS=all) + 2 prompts · MCP Registry #2759
- [faf-mcp](https://freemcp.space/featured/faf-mcp) — Persistent Project Context for Cursor, IDEs and VS Code — IANA-registered .faf format · 29 tools
- [llm-token-tracker](https://freemcp.space/featured/llm-token-tracker) — Token usage tracker for OpenAI and Claude APIs with MCP support. Pass accurate API costs to your users.
- [omega-brain-mcp](https://freemcp.space/featured/omega-brain-mcp) — Standalone MCP server — cross-session memory, 10-gate VERITAS build pipeline, cryptographic audit ledger, Cortex approval gate. Two files, one dependency.
- [jsr-mcp](https://freemcp.space/featured/jsr-mcp) — Model Context Protocol server for the JSR (JavaScript Registry)
- [ariadne](https://freemcp.space/featured/ariadne) — Fast local MCP server for deterministic cross-service API-chain discovery across REST, GraphQL, Kafka, TypeScript, and FastAPI.
- [hocr_mcp_server](https://freemcp.space/featured/hocr-mcp-server) — Extract handwritten math formulas from uploaded images as LaTeX using a vision-language model, with a Vue frontend.
- [mcp-gateway-scan](https://freemcp.space/featured/mcp-gateway-scan) — Read-only static scanner that scores MCP and agent-gateway repos on RBAC, fail-closed behavior, supply chain, observability, cost and secrets handling.
- [clearjson](https://freemcp.space/featured/clearjson) — Large-file-safe JSON MCP server. Format, validate, search, JSONPath query, deep diff, and format conversion (CSV/TSV/YAML/TypeScript). 10 tools, zero dependencies.
- [humanizer-ru](https://freemcp.space/featured/humanizer-ru) — Правит русский текст после нейросети и сверяет цифры, даты и имена. Навык для Claude Code, Codex, Cursor и Claude.ai
- [augments-mcp-server](https://freemcp.space/featured/augments-mcp-server-2) — Comprehensive MCP server providing real-time framework documentation access for Claude Code with intelligent caching, multi-source integration, and context-aware assistance.
- [mcp-trino](https://freemcp.space/featured/mcp-trino) — A high-performance Model Context Protocol (MCP) server for Trino implemented in Go.
- [GoSQLX](https://freemcp.space/featured/gosqlx) — Pure-Go SQL parser, formatter, linter and security scanner for 8 dialects. Zero-copy, race-free, with an LSP and MCP server.
- [src-to-kb](https://freemcp.space/featured/src-to-kb) — Convert source code to LLM ready knowledge base
- [adaptive-cards-mcp](https://freemcp.space/featured/adaptive-cards-mcp-2) — AI-powered Adaptive Card MCP server — 9 tools for generating, validating, optimizing cards for Teams, Outlook, Copilot, ChatGPT. npm: adaptive-cards-mcp
- [excel-vision-mcp](https://freemcp.space/featured/excel-vision-mcp) — MCP server that lets AI agents SEE embedded images inside Excel files — full text + image extraction for .xlsx/.xlsm
- [mcp-prompt-engine](https://freemcp.space/featured/mcp-prompt-engine) — MCP Prompt Engine
- [Ollama-Omega](https://freemcp.space/featured/ollama-omega) — Sovereign Ollama Bridge — MCP server for local and cloud Ollama models. Generated by Qwen 3.5 397B.
- [verifyax-mcp](https://freemcp.space/featured/verifyax-mcp) — MCP server and typed SDK for the VerifyAX agent-evaluation platform.
- [Veris](https://freemcp.space/featured/veris) — Behavioral diff for AI-written code. Your agent changed 40 files — Veris tells it what behavior actually changed and whether any of it was verified. MCP-native, checker-resolved call graph, tamper-evident evidence. Never executes your code. Local-first, MIT.
- [sourcerer-mcp](https://freemcp.space/featured/sourcerer-mcp) — MCP for semantic code search & navigation that reduces token waste
- [ai-toolkit](https://freemcp.space/featured/ai-toolkit) — Toolkit for building AI-driven graph apps on Memgraph, with LangChain, MCP, and agent implementations. 
- [lldb-mcp](https://freemcp.space/featured/lldb-mcp) — LLDB MCP server
- [jetbrains-debugger-mcp-plugin](https://freemcp.space/featured/jetbrains-debugger-m) — JetBrains IDE plugin giving coding agents programmatic control of the debugger.
- [schemagate](https://freemcp.space/featured/schemagate) — Text-to-SQL access control: schema selection that gives the LLM only the tables the caller is allowed to read. Row-level-security-aware table pruning for LangChain, MCP and any SQL agent. Postgres, Oracle, MySQL, SQL Server. 75% fewer prompt tokens.
- [memcord](https://freemcp.space/featured/memcord) — 🧠 Self-hosted, privacy-first MCP server for long-term AI memory — save, search & summarize Claude/ChatGPT chat history locally. No cloud, no database.
- [mcp-adr-analysis-server](https://freemcp.space/featured/mcp-adr-analysis-ser) — Your ADRs are lying to you. MCP server with live drift detection, content safety, and decision memory — validates architectural decisions against your actual code.
- [DotNetMetadataMcpServer](https://freemcp.space/featured/dotnetmetadatamcpser) — A Model Context Protocol (MCP) server that provides detailed type information from .NET projects for AI coding agents.
- [TZeroAlgorithm](https://freemcp.space/featured/tzeroalgorithm) — AST Codebase Context Engine & 21-Tool MCP Server for AI Coding Agents — Up to 95% Token Reduction & Zero-Leak Security Architecture
- [pantheon-mcp](https://freemcp.space/featured/pantheon-mcp) — A collection of AI agents
- [repoguard](https://freemcp.space/featured/repoguard) — The Architecture Guardian for AI-assisted code. Generate strict .cursorrules and audit PRs.
- [signalint](https://freemcp.space/featured/signalint) — MCP server for compact, cached, loop-aware JavaScript and TypeScript diagnostics
- [cloud-finops-skills](https://freemcp.space/featured/cloud-finops-skills) — Cloud FinOps Skill & MCP by OptimNow. FinOps Foundation aligned knowledge for AI agents: cloud cost (AWS/Azure/GCP/OCI), AI inference economics, Kubernetes, data platforms, allocation, chargeback, anomaly management, waste detection, GreenOps. Installs into 12 AI tools, or connect the hosted MCP server by URL. Refreshed weekly.
- [reado](https://freemcp.space/featured/reado) — Inverted code review: a read-first IDE where you comment on the lines that matter and your coding agent (Claude Code, Codex, Cursor, Copilot) resolves them. Free and open source.
- [repopilot](https://freemcp.space/mykyta-stelmashen/repopilot) — Local, deterministic review of Git changes: weakened tests and CI gates, security boundaries, blast radius. CLI, GitHub Action, MCP server, and coding-agent plugins.
- [CodeEraser](https://freemcp.space/featured/codeeraser) — An eraser against LLM-induced code & document entropy. Support if you like it!
- [ictfax-mcp](https://freemcp.space/featured/ictfax-mcp) — MCP server for ICTFax — list and track faxes, upload documents and send faxes over ICTCore REST. By ICT Innovations.
- [bestax](https://freemcp.space/featured/bestax) — A fully-typed React component library for the Bulma CSS framework. Build modern UIs quickly with reusable, accessible, and customizable Bulma-based React components.
- [postbag](https://freemcp.space/featured/postbag) — Two local coding-agent sessions, Claude Code or Codex, write letters to each other through each agent's native input. CLI and MCP tools, stdlib core, no daemon.
- [ClefMCP](https://freemcp.space/featured/clefmcp) — Local MCP server exposing the Cloudflare Clef-Flash decision model to AI agents — structured decisions with probability outputs, fully offline via llama.cpp.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
