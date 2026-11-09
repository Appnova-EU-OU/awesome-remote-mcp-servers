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
- [jupyter-notebook-mcp](https://freemcp.space/featured/jupyter-notebook-mcp) — A Model Context Protocol (MCP) for Jupyter Notebook
- [label-studio-mcp-server](https://freemcp.space/featured/label-studio-mcp-ser) — Create, manage and automate Label Studio projects, tasks and predictions for data labeling workflows.
- [WaveGuardClient](https://freemcp.space/featured/waveguardclient) — Python SDK for WaveGuard  physics-based anomaly detection API. One call. Any data.
- [data-profiler-mcp](https://freemcp.space/featured/data-profiler-mcp) — MCP server that profiles tabular data files (CSV, Parquet, Excel, JSON) for LLM agents like Claude.
- [rigor](https://freemcp.space/featured/rigor) — Verified statistical inference for AI agents -- classical and non-parametric hypothesis testing, correlation/regression, effect sizes, power/sample-size, multiple-comparisons correction, a test-recommendation helper, and a batch pairwise-comparison tool, as a CLI and an MCP server
- [gnomon-mcp](https://freemcp.space/featured/gnomon-mcp) — Deterministic date, math and unit tools: time snapshots, calendar math with natural-language parsing, expression evaluation and Pint-based unit conversion.
- [cortexcloud-mcp](https://freemcp.space/featured/cortexcloud-mcp) — x402 pay-per-call MCP server — 22 AI/data/RPC tools, USDC on Base, no API keys
- [polymath-megablaster-mcp](https://freemcp.space/featured/polymath-megablaster) — Local MCP toolkit giving AI agents deterministic calculation instead of guessing: 15 free tools for exact math, dates, unit conversion, hashing, networking. 100% local, no network calls, no API keys, no telemetry.
- [website-downloader](https://freemcp.space/featured/website-downloader) — MCP server to download entire websites
- [chronulus-mcp](https://freemcp.space/featured/chronulus-mcp) — MCP Server for Chronulus AI Forecasting and Prediction Agents
- [growthbook-mcp](https://freemcp.space/featured/growthbook-mcp) — Official GrowthBook MCP server for creating flags, getting experiments, and more.
- [networkx-mcp-server](https://freemcp.space/featured/networkx-mcp-server) — 🕸️ First NetworkX MCP server for graph analysis in AI conversations | Community & Enterprise editions | Graph algorithms • Network analysis • MCP integration
- [math-mcp-learning-server](https://freemcp.space/featured/math-mcp-learning-se) — Educational MCP server with math operations, matrix algebra, data visualization, and persistent workspace
- [llm-advisor-mcp](https://freemcp.space/featured/llm-advisor-mcp) — Real-time LLM and VLM comparison with benchmarks, prices and personalized recommendations from multiple data sources.
- [filter-mcp-server](https://freemcp.space/featured/filter-mcp-server) — MCP server comparing approximate filters (Bloom, Counting Bloom, Cuckoo, SuRF). Listed in awesome-mcp-servers.
- [neurocode](https://freemcp.space/featured/neurocode) — In-memory Code Property Graph context slicer for local models (Ollama, Cursor, Claude Desktop): extracts sub-1,200 token reachability closures for autonomous repository bug repair on consumer edge hardware (4GB–8GB VRAM) without cloud API dependency.
- [kaggle-mcp](https://freemcp.space/featured/kaggle-mcp-2) — MCP server for Kaggle
- [fermat-mcp](https://freemcp.space/featured/fermat-mcp) — 🚀 Fermat MCP: The Ultimate Math Engine - Unifying SymPy, NumPy & Matplotlib in one powerful server! Perfect for devs & researchers. 
- [mathlas](https://freemcp.space/featured/mathlas) — Airtight math tools an AI uses over MCP — 3.7M-theorem search, PSLQ constant ID, OEIS, real Lean kernel checks, applicability checklists. No LLM inside, no API key.
- [calculator-server](https://freemcp.space/featured/calculator-server) — A comprehensive Go-based MCP server for mathematical computations with 13+ tools
- [stella-mcp](https://freemcp.space/featured/stella-mcp) — MCP server for Stella
- [dataloupe](https://freemcp.space/featured/dataloupe) — Offline data explorer + MCP server: turn CSV/Parquet/Excel into ONE self-contained interactive HTML file, or let your AI assistant query local data — nothing leaves your machine.
- [mathmethods-mcp](https://freemcp.space/featured/mathmethods-mcp) — MCP server for numerical methods and dynamic systems: root finding, integration, ODEs, Monte Carlo, 1D/2D dynamical systems, and combat models.
- [decisionmatrix-mcp](https://freemcp.space/featured/decisionmatrix-mcp) — Deterministic multi-criteria decision analysis (MCDA) for AI agents over MCP — score, rank & explain options against weighted criteria. Weighted-sum, weighted-product, TOPSIS. Exact decimals. Live remote server + self-host.
- [otakit](https://freemcp.space/featured/otakit) — Push updates directly to your Capacitor app without app store reviews.
- [mcp-architect](https://freemcp.space/featured/mcp-architect) — Give any AI assistant real architectural understanding of a codebase — local, private, zero-config MCP serve
- [Unfour](https://freemcp.space/featured/unfour) — Local-first backend troubleshooting workspace for tracing failures across API, SSH, and databases, with MCP-assisted runtime evidence.
- [qa-probe](https://freemcp.space/featured/qa-probe) — Local QA agent — maps frontend routes to backend APIs, probes every endpoint live, scores pages 0–100, and explains why data is missing. Built for LightShield SIEM. Works with any FastAPI / Express / Next.js app.
- [amendor-mcp](https://freemcp.space/featured/amendor-mcp) — Connect your coding agent to Amendor. Pulls change requests into your agent so it builds them and opens PRs.
- [codemagic-mcp](https://freemcp.space/featured/codemagic-mcp) — Build, sign, and publish iOS & Android apps through AI agents — Codemagic CI/CD + App Store Connect + Google Play
- [mcp-laya](https://freemcp.space/featured/mcp-laya) — Fast, local, non-autoregressive System-1 decision engine as MCP tools — typed decisions (classify / score / yes-no) over text, email, tickets or JSON in 100+ languages, with calibrated confidence and no text generation, so nothing to hallucinate. Offloads routing/triage/gating judgment calls from the main model; runs on-device, offline by default. `pipx install mcp-laya`
- [proxykit-mcp](https://freemcp.space/featured/proxykit-mcp) — MCP server for ProxyKit — drive a local HTTP(S) debugging proxy from Claude, Cursor, and any MCP host.
- [postman-mcp-server](https://freemcp.space/featured/postman-mcp-server) — An MCP server that provides access to Postman.
- [yandex-lavka-mcp](https://freemcp.space/featured/yandex-lavka-mcp) — Unofficial MCP server for ordering Yandex Lavka groceries from an AI assistant (search, cart, checkout with confirmation)
- [warp-agent-mcp](https://freemcp.space/featured/warp-agent-mcp) — MCP server for the Warp freight API. Quote, book, and track LTL/FTL shipments from any MCP-compatible AI agent.
- [royalmail-mcp](https://freemcp.space/featured/royalmail-mcp) — Book, label, track and cancel Royal Mail and Parcelforce shipments from any MCP-compatible AI.
- [claw-tsaver](https://freemcp.space/featured/claw-tsaver) — A token-saving MCP proxy for OpenClaw users. Cuts tool call payloads by 90%+ via lazy expansion.
- [parcel-shipping-rates-mcp](https://freemcp.space/featured/parcel-shipping-rate) — MCP server for live USPS, UPS and FedEx rates on a parcel sent from the US: domestic, Canada, UK, Germany, Australia. No scale, no account, no API key.
- [packzoo-mcp](https://freemcp.space/featured/packzoo-mcp) — PackZoo MCP server — compare parcel and letter delivery prices across 60+ carriers in 27 European countries.
- [peckish](https://freemcp.space/featured/peckish) — Order food and groceries on DoorDash via its CLI (macOS arm64): search stores, compare fee-included totals, build carts; orders need user approval.
- [DoorDash-MCP-Server](https://freemcp.space/featured/doordash-mcp-server) — Unofficial DoorDash Delivery integration.
- [DragonMCP](https://freemcp.space/featured/dragonmcp) — DragonMCP is a Model Context Protocol (MCP) server designed for AI Agents to interact with local life services in Greater China (Mainland China, HKSAR) and Asia.  DragonMCP 是一个专为 AI Agent 设计的 Model Context Protocol (MCP) 服务器，旨在提供中国内地、中国香港及亚洲地区的本地生活服务接口。
- [fagan](https://freemcp.space/featured/fagan) — Spend tokens on judgment, not typing. An MCP-native autonomous SDLC pipeline: frontier models plan and review, local models implement — engineering discipline on a $20/month budget.
- [groundwork](https://freemcp.space/featured/groundwork) — Is this document-QA system ready to ship? Deployment-readiness gate for AI document-QA and extraction systems: grounding checks, privacy redaction and cost tracking, built on OpenGATE, Redacta and PubCrawl. CLI and MCP server.
- [nostrpulse-full](https://freemcp.space/np79857/nostrpulse-full) — Autonomous Payment & Anti-Sybil Trust Layer for AI Agents via Nostr, Cashu eCash (NIP-61), and MCP.
- [mcp-yango-delivery](https://freemcp.space/featured/mcp-yango-delivery) — MCP server for the Yango Delivery B2B Express (Claims) API: quote, book and track courier deliveries from an AI app
- [mcp-yandex-dostavka](https://freemcp.space/featured/mcp-yandex-dostavka) — MCP server for the Yandex Delivery (Dostavka) B2B API: calculate cost, create and track courier, pickup point and parcel locker shipments from an AI app
- [opengist-mcp](https://freemcp.space/featured/opengist-mcp) — MCP server for Opengist, the self-hosted pastebin powered by Git
- [mcp-unifi-applications](https://freemcp.space/featured/mcp-unifi-applicatio) — UniFi MCP server that makes the official UniFi API documentation (Network, Protect, Site Manager, InnerSpace) queryable by AI agents — endpoint search, schema drill-down, code examples in 5 languages. Read-only, no controller credentials.
- [xlide_mcp](https://freemcp.space/featured/xlide-mcp) — Read, write, analyze and test the VBA inside Excel, Word, PowerPoint and Access files, and edit the document around it. No Office installation needed.
- [workspace-metabolism](https://freemcp.space/featured/workspace-metabolism) — Govern what Claude Code, Codex, Aider and OpenClaw leave in your workspace: one JSON policy file, audit, recyclable clean, rollback, hash-chained audit trail.
- [mcp-server](https://freemcp.space/featured/mcp-server-25) — Pin visual feedback on any live web page and send it to Claude Code, Cursor or your AI agent.
- [crapkit](https://freemcp.space/featured/crapkit) — Per-function CRAP scores from complexity and coverage, churn-ranked worklists, and ratchet gates for code changes. CLI, MCP, and GitHub Action.
- [anyhook-mcp](https://freemcp.space/featured/anyhook-mcp) — MCP server + signature verification for AnyHook, the webhook relay with a keyless quickstart (npx -y anyhook-mcp)
- [magzdown-agent-tools](https://freemcp.space/featured/magzdown-agent-tools) — Give any AI agent a way to hand humans a typeset document link (Claude Code skill, Cursor rule, MCP server)
- [sensorium](https://freemcp.space/featured/sensorium) — Record a program run, then let coding agents query the trace over MCP. Python, Rust, TypeScript.
- [qai-consultant](https://freemcp.space/featured/qai-consultant) — AI-powered QA Architect agent — generates ISTQB/OWASP/IEEE/ISO-grounded Test Strategies, Risk Registers, Effort Estimates & Test Plans via RAG. Cloud-hosted (Mistral API + Pinecone).
- [diffgate](https://freemcp.space/saurabh-acharya/diffgate) — Triage for AI-generated code review: grades each changed diff line green/yellow/orange by impact, so reviewers spend attention where it matters. High-signal, low-noise (0 false blocks), deterministic — in your coding agent (MCP), editor (VS Code), and CLI/CI.
- [ariadne](https://freemcp.space/featured/ariadne-2) — ariadne is an MCP (Model Context Protocol) server that provides AI agents with the ability to identify affected tests.
- [jsonfabrica-mcp-server](https://freemcp.space/featured/jsonfabrica-mcp-serv) — Generate realistic, schema-conformant JSON test data (single documents or relational batches) from reusable templates via the JsonFabrica API.
- [symfony-agent-mcp](https://freemcp.space/featured/symfony-agent-mcp) — Model Context Protocol server for Symfony applications — read-only introspection of routes, services, entities, controllers, database schema, migrations, composer packages and logs
- [wcagc-mcp](https://freemcp.space/featured/wcagc-mcp) — MCP server for wcagc — let Claude or ChatGPT run real axe-core accessibility scans (WCAG, EN 301 549, PDF/UA) through your own account.
- [quelllm-mcp](https://freemcp.space/featured/quelllm-mcp) — MCP server for quelllm.fr — 250+ open-weights LLM catalog. Tools: list/compare/estimate VRAM/estimate cost API vs self-hosted.
- [packkit-mcp](https://freemcp.space/featured/packkit-mcp) — MCP server for Packkit — scaffold, upgrade & compose fullstack projects in any supported language (JS/TS, Python, Go) as a native AI-agent tool
- [argot](https://freemcp.space/featured/argot) — A statistical code analyzer built from your repository's history.
- [rlg](https://freemcp.space/featured/rlg) — Near-lock-free structured logging for Rust: a 65,536-slot ring buffer, formatting deferred to a background thread, 14 output formats (JSON, ECS, GELF, OTLP, logfmt…) and native os_log/journald sinks. Plus an OTLP/HTTP exporter, an MCP server for AI agents, Tower middleware, PII redaction, WebAssembly bindings and a jq-style CLI.
- [synapse-code-mcp](https://freemcp.space/featured/synapse-code-mcp) — Model Context Protocol server for code intelligence. Lets AI assistants explore your codebase on demand — semantic context with dependency graphs, compressed symbol indexes for TypeScript/JavaScript, plus git diffs and ripgrep-powered search across any language.
- [inkcheck](https://freemcp.space/featured/inkcheck) — CI for ink stories — compile checks, exhaustive branch playtesting, dead-content detection. MCP server + CLI.
- [vectr](https://freemcp.space/featured/vectr) — Semantic codebase search + persistent working memory for AI code editors. Local, zero-config, MCP. No API key.
- [hooksense-mcp](https://freemcp.space/featured/hooksense-mcp) — MCP server for HookSense — the webhook & callback layer for AI agents
- [klanex-mcp](https://freemcp.space/featured/klanex-mcp) — MCP server for klanex — reliable async execution for agent tool calls
- [imagedimensions-mcp](https://freemcp.space/featured/imagedimensions-mcp) — MCP server that audits images on any web page — natural vs rendered dimensions, oversized-image detection, and format breakdown. Powered by imagedimensions.com.
- [sigrank-mcp](https://freemcp.space/featured/sigrank-mcp) — SigRank MCP — AI operator evaluation and token cascade efficiency tools. The yield cascade + live leaderboard as MCP tools any agent can call. On-device token scanner + tabbed TUI dashboard. npm i -g sigrank
- [mockd](https://freemcp.space/featured/mockd) — High-performance, multi-protocol mock server. HTTP, WebSocket, gRPC, MQTT, SSE, GraphQL, SOAP in one binary.
- [grafema](https://freemcp.space/featured/grafema) — Graph-based static analysis tool
- [OctoCounts](https://freemcp.space/featured/octocounts) — Count lines of code (SLOC) in any public GitHub repo without cloning: web app, browser extension, CLI, GitHub Action and MCP server, powered by tokei. The SLOC panel GitHub forgot.
- [graphpilot](https://freemcp.space/featured/graphpilot) — Structural memory for coding agents — index your repo once, query symbols, callers, and call-edges over MCP.
- [vs-token-safer](https://freemcp.space/featured/vs-token-safer) — Token-saving code search for AI coding agents — TypeScript, JavaScript & Python (zero setup), C#, C++, Go & 30+ more, via a language-server or tree-sitter index instead of grep. Local-only, no IDE. Claude Code plugin + MCP + CLI.
- [cpp26-adapter](https://freemcp.space/featured/cpp26-adapter) — Claude Code plugin that turns Claude into a C++26 specialist. Standard-first suggestions; compiler-honest verification.
- [opn-mcp](https://freemcp.space/featured/opn-mcp) — MCP server for opn.onl — shorten links, read analytics & manage links from AI assistants. Works with the hosted service or your self-hosted instance.
- [mcp-domain-deliverability-checker](https://freemcp.space/featured/mcp-domain-deliverab) — MCP server for the Mamba Labs Domain Deliverability Checker actor: SPF, DKIM, DMARC, MX, blacklist, catch-all, domain age. Clay-ready.
- [mcp-abacus](https://freemcp.space/featured/mcp-abacus) — High-precision calculator MCP server — goes beyond arithmetic to calculus (derivatives, integrals) and equation solving, all evaluated in fixed-point, IEEE-754, or exact rational mode with every answer labelled exact or inexact.
- [mcp-bigquery-server](https://freemcp.space/featured/mcp-bigquery-server) — A Model Context Protocol (MCP) server that provides secure, read-only access to BigQuery datasets. Enables Large Language Models (LLMs) to safely query and analyze data through a standardized interface.
- [asc-mcp](https://freemcp.space/featured/asc-mcp-2) — MCP server for App Store Connect API - 502 tools for apps, builds, TestFlight, subscriptions, Xcode Cloud, and more from Claude, Cursor, VS Code, or any MCP client
- [auto-mobile](https://freemcp.space/featured/auto-mobile) — Mobile automation suite of tools including an MCP and libraries for test authoring & execution
- [mcp-zenml](https://freemcp.space/featured/mcp-zenml) — MCP server to connect an MCP client (Cursor, Claude Desktop etc) with your ZenML MLOps and LLMOps pipelines
- [perfetto-mcp-rs](https://freemcp.space/featured/perfetto-mcp-rs) — Perfetto trace analysis via MCP — PerfettoSQL queries plus dedicated Chrome tools for scroll jank, page loads, and main-thread hotspots
- [garmin-documentation-mcp-server](https://freemcp.space/featured/garmin-documentation) — MCP server for Garmin Connect IQ API documentation - complete offline access to SDK 8.2.3
- [jaeger-mcp](https://freemcp.space/featured/jaeger-mcp) — MCP server for Jaeger — search traces, inspect spans, map service dependencies
- [dep-diff-mcp](https://freemcp.space/featured/dep-diff-mcp) — MCP server that reads dependency changelogs and tells you what's risky in an upgrade.
- [drwhome](https://freemcp.space/featured/drwhome) — drwho.me: free DNS, email, TLS and developer tools, and a free MCP server for AI agents
- [eval-view](https://freemcp.space/featured/eval-view) — Regression testing for AI agents. Snapshot behavior,diff tool calls,catch regressions in CI. Works with LangGraph, CrewAI, OpenAI, Anthropic.
- [llm-router](https://freemcp.space/featured/llm-router) — Universal LLM router for AI coding tools. Works with Claude Code, Cursor, Codex, Gemini CLI, Copilot and more. Free-first fallback chain cuts costs 35-80%.
- [multi-ai-advisor-mcp](https://freemcp.space/featured/multi-ai-advisor-mcp) — council of models for decision
- [mcp-swagger-server](https://freemcp.space/featured/mcp-swagger-server) — MCP Swagger Server 将任何符合 OpenAPI/Swagger 规范的 REST API 转换为 Model Context Protocol (MCP) 格式，让 AI 助手能够理解和调用您的 API。
- [mcp-typescribe](https://freemcp.space/featured/mcp-typescribe) — An MCP server implementation enabling LLMs to work with new APIs and frameworks
- [ros-mcp](https://freemcp.space/featured/ros-mcp) — MCP server for ROS to control robots via topics, services, and actions.
- [dotnet-template-mcp](https://freemcp.space/featured/dotnet-template-mcp) — MCP server wrapping the .NET Template Engine for AI-driven template discovery, inspection, and instantiation
- [codegraph-brain](https://freemcp.space/zaebee/codegraph-brain) — Code graph for AI agents: impact analysis and call tracing over MCP (Python, TypeScript). Local, deterministic, SQLite.
- [implicit-core](https://freemcp.space/featured/implicit-core) — Implicit is the experience layer for AI agents. For large agent training/evaluation environments, address experiences and materialize required state on demand. Python package: implicit-ai.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
