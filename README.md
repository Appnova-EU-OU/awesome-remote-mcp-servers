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
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
