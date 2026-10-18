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
- [mcp-gopls](https://freemcp.space/featured/mcp-gopls) — Model Context Protocol (MCP) server for Go using gopls – LSP-powered analysis, tests, coverage, and tooling.
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
- [jmeter-mcp-server](https://freemcp.space/qainsights/jmeter-mcp-server) — ✨ JMeter Meets AI Workflows: Introducing the JMeter MCP Server! 🤯 
- [spreadsheet-mcp](https://freemcp.space/featured/spreadsheet-mcp) — MCP server for spreadsheet analysis and editing. Slim, token-efficient tool surface designed for LLM agents.
- [javalens-mcp](https://freemcp.space/featured/javalens-mcp) — MCP server providing semantic Java code analysis for AI agents. Built on Eclipse JDT with tools for navigation, refactoring, search, and metrics.
- [sharplens-mcp](https://freemcp.space/featured/sharplens-mcp) — Roslyn-powered MCP server for AI-driven C# semantic analysis, refactoring, and code generation
- [k6-mcp-server](https://freemcp.space/qainsights/k6-mcp-server) — k6 MCP server
- [ARBuilder](https://freemcp.space/featured/arbuilder-2) — AI-powered code generator for Arbitrum Stylus, SDK bridging, dApps & Orbit chains — 19 MCP tools with RAG
- [locust-mcp-server](https://freemcp.space/featured/locust-mcp-server) — A Model Context Protocol (MCP) server implementation for running Locust load tests. This server enables seamless integration of Locust load testing capabilities with AI-powered development environments.
- [godotlens-mcp](https://freemcp.space/featured/godotlens-mcp) — MCP server for GDScript semantic analysis via Godot's built-in language server
- [pt-edge](https://freemcp.space/featured/pt-edge) — Precomputed reasoning cache for AI infrastructure decisions — 220K+ pages tracking the open-source AI ecosystem
- [qr-agent-core](https://freemcp.space/featured/qr-agent-core) — QR-as-a-Service API for AI agents — 34 MCP tools, 11 QR types, dynamic links, scan analytics, webhooks, custom domains. REST API + MCP server.
- [appstore-release-mcp](https://freemcp.space/featured/appstore-release-mcp) — App Store release pilot MCP server — version bump, archive + TestFlight upload, metadata, review submission. The MCP server that actually ships your binary.
- [pubship](https://freemcp.space/featured/pubship) — Open-source MCP server for Google Play developer workflows. Runs locally with your own credentials.
- [unitree-go2-mcp-server](https://freemcp.space/featured/unitree-go2-mcp-serv) — The Unitree Go2 MCP Server is a server built on the MCP that enables users to control the Unitree Go2 robot using natural language commands interpreted by a LLM.
- [airtable-mcp](https://freemcp.space/featured/airtable-mcp-2) — Airtable integration for AI-powered applications via Anthropic's Model Context Protocol (MCP)
- [just-mcp](https://freemcp.space/featured/just-mcp) — mcp server for just
- [pagecast](https://freemcp.space/featured/pagecast) — Record any browser page as GIF or video via MCP — powered by Playwright + ffmpeg
- [mac-monitor-mcp](https://freemcp.space/featured/mac-monitor-mcp) — Identifies resource-intensive processes on macOS and suggests performance improvements.
- [docket](https://freemcp.space/featured/docket) — Local-first, self-hostable coordination workspace for AI coding agents. Shared tasks, claims, sync and MCP integration.
- [pipepie](https://freemcp.space/featured/pipepie) — Self-hosted encrypted tunnel for webhooks, AI pipelines, and local development. End-to-end Noise encryption, pipeline tracing, web dashboard, MCP server for AI tools.
- [claude-critical-rules-mcp](https://freemcp.space/featured/claude-critical-rule-2) — MCP server for Claude AI providing automatic enforcement of critical rules - Prevents 96 documented failure patterns
- [pmpt-cli](https://freemcp.space/featured/pmpt-cli) — Record and share your AI-driven product development journey
- [devutils-mcp-server](https://freemcp.space/featured/devutils-mcp-server) — An open-source DevUtils MCP Server — a comprehensive developer utilities toolkit for the Docker MCP Catalog. It provides 36 tools across 8 categories that AI assistants can invoke directly.
- [P-Link-MCP](https://freemcp.space/featured/p-link-mcp) — x402 client implementation (x402-fetch), HTTP 402 server implementation and Model Context Protocol (MCP) for P-Link.io : pay, send and receive money with agents
- [pylon-mcp](https://freemcp.space/featured/pylon-mcp) — MCP server for Pylon AI — 10 pay-per-request APIs as AI agent tools. Powered by x402 on Base.
- [pincushion-plugin](https://freemcp.space/featured/pincushion-plugin) — Cursor marketplace plugin for Pincushion — MCP server + slash commands
- [promethic-mcp](https://freemcp.space/featured/promethic-mcp) — Hosted MCP docs and packaging for Promethic prompt library (Streamable HTTP at mcp.getpromethic.com/v1)
- [asc-mcp](https://freemcp.space/featured/asc-mcp) — MCP server for App Store Connect — check review status, read reviews, download sales reports from Claude Code, Cursor, or any AI agent. Free tier included.
- [gin-mcp](https://freemcp.space/featured/gin-mcp) — Enable MCP features for any Gin API with a line of code
- [agent-droid-bridge](https://freemcp.space/featured/agent-droid-bridge) — Agent Droid Bridge gives AI agents programmatic control over Android devices and emulators via ADB, exposed as an MCP server.
- [mcp-server-markdown](https://freemcp.space/featured/mcp-server-markdown) — MCP server for markdown — search, extract sections, list headings, find code blocks
- [jitapi](https://freemcp.space/featured/jitapi) — Just-in-Time API Orchestration for LLMs - An MCP server for dynamic API discovery and execution
- [mcp-server-scraper](https://freemcp.space/featured/mcp-server-scraper) — MCP server for web scraping — extract clean markdown, links, metadata from any URL
- [mcp-server-github-actions](https://freemcp.space/featured/mcp-server-github-ac) — MCP server for GitHub Actions — view runs, read logs, re-run jobs, trigger workflows
- [mcp-server-devutils](https://freemcp.space/featured/mcp-server-devutils) — Zero-auth MCP server with everyday developer utilities: base64, UUID, hash, JWT decode, cron, timestamps, JSON, regex
- [spring-boot-starter-swagger-mcp](https://freemcp.space/featured/spring-boot-starter) — Turn SpringDoc OpenAPI into production-ready MCP tools for Spring Boot: discovery, validation, workflows, and guardrails.
- [mcp-server-docker](https://freemcp.space/featured/mcp-server-docker) — MCP server for Docker — manage containers, images, volumes from your IDE
- [mcp-server-dns](https://freemcp.space/featured/mcp-server-dns) — MCP server for DNS — lookups, reverse DNS, WHOIS, zero auth
- [hird](https://freemcp.space/featured/hird) — A typed language for LLM agent systems on BEAM: effect-row tracking, auditable tool effects, typed actors, and OTP supervision, queryable by agents over MCP.
- [mcp-toolkit](https://freemcp.space/featured/mcp-toolkit) — 59 MCP servers for React + TypeScript automation — component scaffolding, CRUD feature factory, WCAG checks, test gen, TS enforcement, render/perf analysis, CRA→Vite migration, legacy analysis. npx-installable.
- [mcp-server-github-gist](https://freemcp.space/featured/mcp-server-github-gi) — MCP server to create, read, update, list, and search GitHub Gists from your IDE
- [mcp-server-npm-plus](https://freemcp.space/featured/mcp-server-npm-plus) — MCP server for npm - search, bundle sizes, vulnerabilities, download trends, dependency trees
- [rhizome-mcp](https://freemcp.space/featured/rhizome-mcp) — Crash-safe task tracking for AI coding agents over MCP: expiring leases, resumable attempts, version-pinned reviews. One Go binary, one SQLite file per project.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
