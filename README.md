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
- [cloud-finops-skills](https://freemcp.space/featured/cloud-finops-skills) — Cloud FinOps Skill & MCP by OptimNow. FinOps Foundation aligned knowledge for AI agents: cloud cost (AWS/Azure/GCP/OCI), AI inference economics, Kubernetes, data platforms, allocation, chargeback, anomaly management, waste detection, GreenOps. Installs into 12 AI tools, or connect the hosted MCP server by URL. Refreshed weekly.
- [reado](https://freemcp.space/featured/reado) — Inverted code review: a read-first IDE where you comment on the lines that matter and your coding agent (Claude Code, Codex, Cursor, Copilot) resolves them. Free and open source.
- [repopilot](https://freemcp.space/mykyta-stelmashen/repopilot) — Local, deterministic review of Git changes: weakened tests and CI gates, security boundaries, blast radius. CLI, GitHub Action, MCP server, and coding-agent plugins.
- [CodeEraser](https://freemcp.space/featured/codeeraser) — An eraser against LLM-induced code & document entropy. Support if you like it!
- [ictfax-mcp](https://freemcp.space/featured/ictfax-mcp) — MCP server for ICTFax — list and track faxes, upload documents and send faxes over ICTCore REST. By ICT Innovations.
- [bestax](https://freemcp.space/featured/bestax) — A fully-typed React component library for the Bulma CSS framework. Build modern UIs quickly with reusable, accessible, and customizable Bulma-based React components.
- [postbag](https://freemcp.space/featured/postbag) — Two local coding-agent sessions, Claude Code or Codex, write letters to each other through each agent's native input. CLI and MCP tools, stdlib core, no daemon.
- [ClefMCP](https://freemcp.space/featured/clefmcp) — Local MCP server exposing the Cloudflare Clef-Flash decision model to AI agents — structured decisions with probability outputs, fully offline via llama.cpp.
- [layermap](https://freemcp.space/featured/layermap) — LayerMap MCP: a layered map of your codebase for coding agents: callers, callees and the impact of a change, for TypeScript, JavaScript, Go, Python and Java. MCP server, CLI, and plugins for Claude Code and Codex.
- [infrastructure-mcp](https://freemcp.space/featured/infrastructure-mcp) — Give Claude Code, Cursor, and other AI agents safe access to your real infrastructure — without giving them raw SSH access.
- [slop-chop](https://freemcp.space/featured/slop-chop) — Strip AI tells from text: em-dashes, slop words, and stock phrases, in one deterministic local pass. CLI, GitHub Action, Obsidian plugin, and MCP server.
- [codetopo](https://freemcp.space/featured/codetopo) — See your codebase the way an agent sees it. Rust code-graph engine: index any repo, query descendants, blast radius, paths. CLI, HTTP API, and MCP server.
- [ableton-mcp-server](https://freemcp.space/featured/ableton-mcp-server) — Local MCP server for Ableton Live: session inspection, MIDI editing, device control, audio analysis and groove tools via a Python Remote Script.
- [permark](https://freemcp.space/edelmar/permark) — 🔖 Read what your AI writes. Write what it reads. A free, open-source Markdown app for Windows, macOS and Linux: open any .md as a clean page, keep notes that save themselves, and follow, review and steer what your AI agents write.
- [pylos-mcp](https://freemcp.space/featured/pylos-mcp) — Email MCP server for Gmail, Outlook and any IMAP mailbox, hardened against prompt injection
- [dbprint](https://freemcp.space/featured/dbprint) — Portable, git-committed snapshot of a database's structure and column-level data distributions, consumable offline by humans, AI coding agents, and CI.
- [Tower](https://freemcp.space/featured/tower) — Multiplayer for AI coding agents: collision detection before the edit, messaging, delegation. MCP server for Claude Code, Cursor, Codex.
- [CDPM](https://freemcp.space/featured/cdpm) — MCP server that lets many Claude Code sessions and subagents share numbered, logged-in Chrome instances over CDP
- [chrome-dev-mcp](https://freemcp.space/featured/chrome-dev-mcp) — An MCP server for Chrome runtime debugging
- [huddo-mcp](https://freemcp.space/featured/huddo-mcp) — MCP server for Huddo: a group chat where people and AI agents talk in the same room
- [sendraven-mcp-server](https://freemcp.space/featured/sendraven-mcp-server) — SendRaven is email infrastructure for AI agents. Send, read replies as threads, run campaigns and automations, with limits on the API key.
- [remcp](https://freemcp.space/featured/remcp) — Remote MCP access to computers you explicitly pair — files, terminal, desktop UI, browser automation, diagnostics, and documents.
- [backwork-mcp](https://freemcp.space/featured/backwork-mcp) — Official MCP server for the Backwork healthcare API
- [illugen-mcp](https://freemcp.space/featured/illugen-mcp) — MCP server for JangaFX IlluGen: let AI agents (Claude, Cursor...) build, edit and render IlluGen node graphs, invisibly.
- [inam-protocol](https://freemcp.space/featured/inam-protocol) — Verify before your agent pays: x402 payments only reach agents whose wallet and countersigned work history check out. Open receipts + reputation for AI agents.
- [terse](https://freemcp.space/featured/terse) — Shrinks your AI agent's tool output so it burns fewer tokens, without changing what the agent reads. Lossless by default, no decode step.
- [MySQL-AIops](https://freemcp.space/featured/mysql-aiops) — Governed AI-ops for MySQL/MariaDB DBA operations: slow-query RCA, InnoDB lock-wait & deadlock analys
- [mcp-people-finder](https://freemcp.space/featured/mcp-people-finder) — MCP server for the Mamba Labs People Finder & Email Verifier actor on Apify
- [amocrm-kommo-mcp](https://freemcp.space/featured/amocrm-kommo-mcp) — MCP server for amoCRM / Kommo CRM: leads, contacts, tasks, notes and sales analytics (pipeline report, stale deals, overdue tasks)
- [honest-gmail-mcp](https://freemcp.space/featured/honest-gmail-mcp) — Local MCP server for Gmail — send/search/label with your data staying between your machine and Google
- [Network-AIops](https://freemcp.space/featured/network-aiops) — Standalone governed multi-vendor network ops (NAPALM) — 13 MCP tools with audit/budget/undo/risk-tier harness
- [MinIO-AIops](https://freemcp.space/featured/minio-aiops) — Governed AI-ops for MinIO object storage: capacity & usage RCA, bucket exposure audit, lifecycle/ILM
- [snapdeploy-mcp](https://freemcp.space/featured/snapdeploy-mcp) — SnapDeploy MCP connector: deploy from Claude Code, Cursor, Codex and Gemini CLI
- [Container-Host-AIops](https://freemcp.space/featured/container-host-aiops) — Governed AI-ops for Docker + Portainer container hosts — restart-loop/resource/bloat RCA, guarded writes, with audit/budget/undo (preview)
- [Ceph-AIops](https://freemcp.space/featured/ceph-aiops) — Governed Ceph mgr Dashboard ops: HEALTH_WARN RCA, OSD/PG/pool/RBD/CephFS/RGW, 35 MCP tools (preview)
- [agenteyes-mcp](https://freemcp.space/featured/agenteyes-mcp) — A Node.js MCP server (stdio transport) exposing agent tools backed by headless Chromium. One tool call returns screenshot PNG + accessibility tree + page text — the "eyes for agents" pitch.
- [morfiade-mcp](https://freemcp.space/featured/morfiade-mcp) — MCP server for local Google Chrome profiles on Windows — 18 tools over Morfiade's local API
- [zamery-browser](https://freemcp.space/featured/zamery-browser) — Typed browser control for AI agents through provider-neutral contracts and live Firefox integration.
- [label-image-mcp](https://freemcp.space/featured/label-image-mcp) — MCP server and LangGraph agent for the Image Label annotation app (labels.sachin-kale.com)
- [aesthete-agent](https://freemcp.space/featured/aesthete-agent) — Mechanically validated frontend aesthetics for AI agents: 89-palette evidence library, OKLCH generation, WCAG/APCA contrast, color-blind-safe data colors, AI-slop detection, theme packs, W3C design tokens. Skill + MCP server.
- [janction-render](https://freemcp.space/featured/janction-render) — Cloud GPU rendering for Blender scenes and 3D models (GLB/FBX/USD/STL) for AI agents: MCP server, HTTP API, CLI. Product shots, turntables, animations from Claude, ChatGPT, Codex, Cursor. Free to start (100 JPY with no card, 400 JPY more after saving a card), then 0.1 JPY per GPU-second.
- [forbiz-mcp](https://freemcp.space/featured/forbiz-mcp) — MCP server for Forbiz, the CRM for AI agents: commitments, expected signals, evidence and outcomes your agent can resume later.
- [CodeMCP](https://freemcp.space/featured/codemcp) — Code intelligence for AI assistants - MCP server, CLI, and HTTP API with symbol navigation, impact analysis, and architecture mapping
- [chap](https://freemcp.space/featured/chap) — CHAP, the Collaborative Human Agent Protocol, is a MCP/A2A-compatible runtime for auditable human-agent work: approvals, overrides, handoffs, escalation and verifiable evidence logs.
- [awesome-ionic-mcp](https://freemcp.space/featured/awesome-ionic-mcp) — An Awesome MCP Server to help building mobile apps in React/Vue/Angular/VanillaJS using Capacitor and Ionic
- [flowbite-mcp](https://freemcp.space/featured/flowbite-mcp) — Convert Figma design to code with the official Flowbite MCP server
- [bugsnag-mcp](https://freemcp.space/featured/bugsnag-mcp) — A Model Context Protocol (MCP) server for interacting with Bugsnag. This server allows LLM tools like Cursor and Claude to investigate and resolve issues in Bugsnag.
- [replicant-mcp](https://freemcp.space/featured/replicant-mcp) — Android MCP server - production-grade, token-optimized, accessibility-first
- [vex](https://freemcp.space/featured/vex) — Fast hybrid code search built for AI agents
- [tip-md-x402-mcp-server](https://freemcp.space/featured/tip-md-x402-mcp-serv) — 🏆 Hackathon: Transform any AI agent into a payment-enabled agent using x402 + CDP. MCP server for instant crypto tipping with automatic disbursement.
- [wsc](https://freemcp.space/featured/wsc) — Prose linter + AI-slop detector: weasel words, passive voice, hedging, and 190+ research-cited AI tells. Web editor, API, MCP server, CLI, GitHub Action.
- [testdino-mcp](https://freemcp.space/featured/testdino-mcp) — A MCP server that bridges TestDino with AI agents such as Cursor and Claude. Navigate test results, analyze failures, and manage test cases through conversational commands.
- [Tokenectomy](https://freemcp.space/featured/tokenectomy) — Autonomous M2M MCP server that scrubs framework noise & redacts secrets from AI agent error logs before they hit your context window
- [ReftrixMCP](https://freemcp.space/featured/reftrixmcp) — MCP server with 40 tools for web design analysis — layout extraction, motion detection, quality scoring, accessibility audit, Core Web Vitals, design comparison, and semantic search via Playwright, pgvector, ONNX Runtime, and Ollama.
- [x402-mcp](https://freemcp.space/featured/x402-mcp) — MCP server bringing 100+ x402-paid APIs to AI agents. Auto-syncs from CDP Bazaar. Stablecoin micropayments via x402 protocol across multi-chain (Base, Solana, Polygon, BNB, EVM). Built for agentic commerce: developer utilities, validators, encoders, generators, M2M payments, autonomous workflows. Works with Claude, Cursor, and any MCP-aware client.
- [sqlite-explorer-fastmcp-mcp-server](https://freemcp.space/featured/sqlite-explorer-fast) — An MCP server that provides safe, read-only access to SQLite databases through Model Context Protocol (MCP). This server is built with the FastMCP framework, which enables LLMs to explore and query SQLite databases with built-in safety features and query validation.
- [mcp-gopls](https://freemcp.space/hloiseau/mcp-gopls) — Model Context Protocol (MCP) server for Go using gopls – LSP-powered analysis, tests, coverage, and tooling.
- [mcp-gsheets](https://freemcp.space/featured/mcp-gsheets) — MCP server for Google Sheets - Read, write and manipulate spreadsheets through Claude Desktop
- [srclight](https://freemcp.space/featured/srclight) — Deep code indexing MCP server for AI agents. 25 tools: hybrid FTS5 + embedding search, call graphs, git blame/hotspots, build system analysis. Multi-repo workspaces, GPU-accelerated semantic search, 10 languages via tree-sitter. Fully local, zero cloud dependencies.
- [xray](https://freemcp.space/featured/xray) — XRAY MCP provides progressive code intelligence and navigation capabilities for AI assistants   through structural code analysis using ast-grep
- [vibealive](https://freemcp.space/featured/vibealive) — Full-featured utility to test Next.js projects for unused files and APIs + MCP server 
- [testcollab-mcp-server](https://freemcp.space/featured/testcollab-mcp-serve) — MCP server for TestCollab test management. Lets AI coding assistants (Claude Code, Cursor, Windsurf, Codex) create, update, and query test cases, create test plans, and suite hierarchy. Connect your AI workflow to your QA process.
- [jira-github-mcp](https://freemcp.space/featured/jira-github-mcp) — A Model Context Protocol (MCP) server exposing Jira and GitHub actions as AI tools to streamline developer workflows end-to-end.
- [moth](https://freemcp.space/featured/moth) — A debugging workflow plugin for AI coding agents. Turns terminal failures into source-backed fixes via MCP and structured skills.
- [devpulse-mcp](https://freemcp.space/featured/devpulse-mcp) — Zero-config MCP server that gives AI coding assistants a real-time diagnostic snapshot of your dev environment
- [tactual](https://freemcp.space/featured/tactual) — Screen-reader navigation cost analyzer — models the real effort to discover, reach, and operate interactive web content
- [dvera-plugin](https://freemcp.space/featured/dvera-plugin) — DVERA agent skills for CT C/C++ verification workflows: project setup, analysis, test generation, coverage, reporting, and regression.
- [specshield-mcp-server](https://freemcp.space/featured/specshield-mcp-serve) — The API-change deploy gate for AI coding agents (MCP server): is it safe to ship this API change to my consumers? Read-only, over OpenAPI/Pact.
- [mcp-victorialogs](https://freemcp.space/featured/mcp-victorialogs) — The implementation of Model Context Protocol (MCP) server for VictoriaLogs.
- [sequa-mcp](https://freemcp.space/featured/sequa-mcp) — Gives AI coding tools context from your entire codebase and docs via Sequa.
- [shipstores](https://freemcp.space/featured/shipstores) — Ship iOS and Android apps from your AI agent. MCP server for App Store Connect, Google Play Console and Expo EAS.
- [heap-seance](https://freemcp.space/featured/heap-seance) — MCP server that channels JVM forensics into structured leak verdicts — for Claude Code.
- [wsapi-mcp](https://freemcp.space/featured/wsapi-mcp) — WSAPI MCP Server
- [Proxmox-AIops](https://freemcp.space/featured/proxmox-aiops) — Standalone governed Proxmox VE ops — 23 MCP tools with built-in audit/budget/undo/risk-tier harness
- [askone](https://freemcp.space/phuryn/askone) — MCP server for AskOne live audience Q&A and polls with free AI moderation: let your agent start rooms, launch polls, moderate and answer questions, and draft a FAQ. Hosted or npx askone-mcp. Also AskOne's issue tracker.
- [elekto-mcp-sql](https://freemcp.space/featured/elekto-mcp-sql) — MCP Server (read-only) for SQL Server schema introspection and data sampling
- [Queue-AIops](https://freemcp.space/featured/queue-aiops) — Governed AI-ops for redis + rabbitmq: memory-pressure/latency/queue-backlog/connection-churn RCAs, s
- [zihin-mcp](https://freemcp.space/featured/zihin-mcp) — MCP Server proxy stdio-to-HTTP para a plataforma Zihin.ai
- [mcp-google-chat](https://freemcp.space/featured/mcp-google-chat) — MCP server for the Google Chat API — list and search spaces, read and send messages, work with threads, reactions, attachments and memberships. For Claude, Cursor, Codex and other AI clients.
- [agent-bridge](https://freemcp.space/featured/agent-bridge) — MCP server that lets Claude and Codex steer each other's chats. Read chats, send steers, control Codex goals for agent orchestration natively.
- [appcrane-mcp](https://freemcp.space/featured/appcrane-mcp) — Standalone MCP connector for AppCrane: exposes its 62 deploy and ops tools to any MCP client, proxied to your own self-hosted AppCrane.
- [quickcast-mcp](https://freemcp.space/featured/quickcast-mcp) — QuickCast Screen-to-Action Protocol MCP Server: Automated Bug Reports, Playwright E2E Tests, and SOP Generator from Screen Recordings.
- [mail-mcp](https://freemcp.space/featured/mail-mcp) — Secure IMAP/SMTP/EWS/Graph API MCP server in Rust — Microsoft 365, Hotmail, Gmail, Zoho, OAuth2, multi-account
- [legion-mcp](https://freemcp.space/featured/legion-mcp) — A server that helps people access and query data in databases using the Legion Query Runner with Model Context Protocol (MCP) in Python.
- [a11ymcp](https://freemcp.space/featured/a11ymcp) — MCP Server for Web Accessibility Testing (10k+ Downloads, #20 on ProductHunt)
- [mcp-openapi](https://freemcp.space/featured/mcp-openapi) — OpenAPI specification MCP server.
- [memi](https://freemcp.space/featured/memi) — The design layer for agentic AI — design context, interface checks, and verification for coding agents.
- [Rootly-MCP-server](https://freemcp.space/featured/rootly-mcp-server) — Rootly MCP server
- [selvage](https://freemcp.space/featured/selvage) — LLM-based code review with AST-based context extraction, supporting Claude, GPT, Gemini and other models via OpenRouter.
- [github-repo-mcp](https://freemcp.space/featured/github-repo-mcp) — Model Context Protocol server for Github Repo // Reading Github Repo
- [janee](https://freemcp.space/featured/janee) — Secrets management for AI agents via MCP • @janeesecure
- [mcp-broker](https://freemcp.space/featured/mcp-broker) — Local MCP broker that exposes one compact MCP entry for MCP clients while routing to many configured upstream servers.
- [reelier](https://freemcp.space/featured/reelier) — Agents make claims. Reelier writes receipts — record an agent's tool-call workflow once, replay it deterministically at 0 tokens, and diff runs to catch drift.
- [mcp-server-boilerplate](https://freemcp.space/featured/mcp-server-boilerpla) — Production-ready MCP server templates in TypeScript and Python. Quickstart boilerplate for building Model Context Protocol servers.
- [mcp-code-sanitizer](https://freemcp.space/featured/mcp-code-sanitizer) — Strict AI code reviewer MCP server powered by Groq
- [retrieval-lens](https://freemcp.space/featured/retrieval-lens) — MCP server that audits RAG retrieval - logs what chunks the model saw before any answer was generated
- [repo-test-architect](https://freemcp.space/featured/repo-test-architect) — Evidence-first test strategy tooling for real codebases.
- [mcp-server-circleci](https://freemcp.space/featured/mcp-server-circleci) — [DEPRECATED] This package is no longer maintained. Migrate to CircleCI's hosted MCP server or the CircleCI CLI MCP. See https://circleci.com/docs/guides/toolkit/circleci-mcp-overview/
- [PhpCodeArcheology](https://freemcp.space/featured/phpcodearcheology) — PHP static analysis for architecture & maintainability — 60+ metrics, complexity analysis, dependency graphs, git churn hotspots, and AI-ready MCP server. Alternative to PHPMetrics.
- [mindpilot-mcp](https://freemcp.space/featured/mindpilot-mcp) — See through your agent's eyes. Visualize legacy code, architect new systems, understand everything.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
