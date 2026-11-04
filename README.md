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
- [mcp-observatory](https://freemcp.space/featured/mcp-observatory-2) — Free, MIT-licensed MCP security testing from ClearFrame. Scan, audit, compare, and review locally; continue in the ClearFrame CLI or Mac app.
- [jvm-mcp-server](https://freemcp.space/featured/jvm-mcp-server) — This is an implementation project of a JVM-based MCP (Model Context Protocol) server. The project aims to provide a standardized MCP server implementation for the JVM platform, enabling AI models to better interact with the Java ecosystem.
- [xcodebuild](https://freemcp.space/featured/xcodebuild) — MCP tool for building Xcode iOS workspace/project and feeding back error to LLMs.
- [PiloTY](https://freemcp.space/featured/piloty) — PiloTY: AI pilot for PTY operations via MCP - enables AI agents to control interactive terminals like a human
- [godoc-mcp-server](https://freemcp.space/featured/godoc-mcp-server) — A mcp server provide infomation from pkg.go.dev. For all golang programmers
- [HarmonyOS-mcp-server](https://freemcp.space/featured/harmonyos-mcp-server) — MCP server for manipulating HarmonyOS next devices.
- [apifable](https://freemcp.space/featured/apifable) — MCP server that helps AI agents explore OpenAPI specs, search endpoints, and generate TypeScript types.
- [scriptflow-mcp](https://freemcp.space/featured/scriptflow-mcp) —   Script workflow management via MCP. Converts AI workflows to persistent scripts, reducing tokens & delays while minimizing hallucination risks.
- [TopicForge](https://freemcp.space/featured/topicforge) — Read-only MCP server for ROS2 and DDS robotics. Let an AI agent inspect topics, DDS participants, QoS mismatches and rosbags. No write path by architecture: it can never command your robot.
- [mcp-server-bigquery](https://freemcp.space/featured/mcp-server-bigquery) — A Model Context Protocol server that provides access to BigQuery
- [mcp-sqlite](https://freemcp.space/featured/mcp-sqlite) — 🐇 Model Context Protocol (MCP) server that provides comprehensive SQLite database interaction capabilities
- [suvadu](https://freemcp.space/featured/suvadu) — Shell history replacement with AI agent tracking and MCP server. Built in Rust, 100% local.
- [stalemap](https://freemcp.space/featured/stalemap) — Tell your coding agent which dependencies changed after its training cutoff. Diffs types and changelogs, writes a short block into AGENTS.md / CLAUDE.md.
- [wtfm](https://freemcp.space/featured/wtfm) — WTFM: Write the F***ing Manual. A plugin for your coding agent that writes your user docs, screenshots included.
- [OpenScreenShot](https://freemcp.space/featured/openscreenshot) — OpenScreenShot is a privacy-first, free, open-source screenshot extension -- zero data leaves your device, no account needed, no telemetry, no third-party services.
- [proton-mail-bridge-client](https://freemcp.space/featured/proton-mail-bridge-c) — Local-first Proton Mail MCP server and CLI via Proton Bridge. Search, draft, send and organize mail from Claude Desktop, Claude Code or any MCP client. 96 tools, read-only and send-to-self modes.
- [Devtrack_](https://freemcp.space/shashankraj28/devtrack) — Local-first developer context daemon with six read-only MCP tools for active tickets, commits, pending actions, voice profile, ticket history, and EOD summaries. Ships native MCPB bundles.
- [x64dbgMCP](https://freemcp.space/featured/x64dbgmcp) — Dynamic x64dbg/x32dbg MCP backend: launch/attach, breakpoints, memory, API/heap traces, OEP/IAT/PE dumps, key recovery, and IDA hash+RVA evidence.
- [local-ai-mcp-servers](https://freemcp.space/featured/local-ai-mcp-servers) — Two Model Context Protocol (MCP) servers for self-hosted, local AI: manage and train Ollama/vLLM models, and route questions and tasks to local LLMs through Claude, ChatGPT or local models. Use the compute of your existing hardware, and let the models tap data on your machines when you wire them in.
- [BeatBrowser](https://freemcp.space/featured/beatbrowser) — Your Chrome, now an agent browser. No browser switch. No login migration. Codex, Claude Code & more. Free & open source.
- [mq-bridge](https://freemcp.space/featured/mq-bridge) — Async Rust library to route messages between Kafka, NATS, MQTT, AMQP, databases and HTTP, with Python and Node bindings
- [pixelpact](https://freemcp.space/featured/pixelpact) — Measurement for coding agents building UI: extract a contract from the reference page, check the implementation, get numbers back
- [SolidWorks-MCP](https://freemcp.space/featured/solidworks-mcp) — MCP server that lets AI agents build, measure and verify parametric parts and assemblies in a running SolidWorks (Windows, COM).
- [pubcrawl](https://freemcp.space/featured/pubcrawl) — MCP server giving AI assistants verifiable access to PubMed, Europe PMC, US/UK drug labelling, and ClinicalTrials.gov. Built by PharmaTools.AI.
- [agentplaybooks](https://freemcp.space/featured/agentplaybooks) — Equip once. Run anywhere. Portable AI agents and toolkits—no vendor lock-in.
- [designfit](https://freemcp.space/featured/designfit) — Validate AI-built front-ends against their Figma design — deterministic token + geometry conformance, not pixels. MCP server + Claude Code skill.
- [nativekeel](https://freemcp.space/featured/nativekeel) — Health check for React Native and Expo apps: A–E ratings for security, store rules, crashes, upgrades and accessibility. Works with GitHub Actions and SonarQube. npx nativekeel
- [ennodia](https://freemcp.space/featured/ennodia) — Connects the AI agents you use: your agent hands a task to another and gets the answer back
- [mapache](https://freemcp.space/featured/mapache) — Open-source mind maps and whiteboard on your computer or your team's server: live collaboration, comments, and a built-in MCP server so your AI agent can build boards with you.
- [openhuddle](https://freemcp.space/featured/openhuddle) — Multiplayer mode for AI coding agents. Your team's Claude Code, Codex and Cursor agents huddle up: live status, one master prompt, a shared task board, and no stepping on each other's files.
- [codex-claude-council](https://freemcp.space/hamza-aziz-ai/codex-claude-council) — Two AIs. One answer. ChatGPT and Claude discuss with each other until they agree, through your own signed-in CLIs: no API keys. Both read your project (never change it) and search the web. Plugin for Claude Code, Codex, Claude Desktop and the ChatGPT app.
- [qa-orchestrator](https://freemcp.space/featured/qa-orchestrator) — Local MCP server for privacy-aware QA task routing
- [tokentoll](https://freemcp.space/featured/tokentoll) — Catch LLM cost changes in code review. Infracost for LLM spend.
- [muninn](https://freemcp.space/featured/muninn) — Code search for AI coding agents over MCP: hybrid retrieval, structural search and shared indexing across Git worktrees.
- [firefox-devtools-mcp](https://freemcp.space/featured/firefox-devtools-mcp) — Model Context Protocol server for Firefox DevTools - enables AI assistants to inspect and control Firefox browser through WebDriver BiDi
- [unitares](https://freemcp.space/featured/unitares) — Accountability infrastructure for long-running AI agents. Self-hosted MCP server: identity, claims and evidence, review, outcomes, and reconstruction across agent runtimes.
- [ifc-ruhsat](https://freemcp.space/featured/ifc-ruhsat) — Yapı ruhsatı IFC modelini Türkiye dijital proje yönetmeliğine (RG 33331) göre kontrol eder — CLI + MCP + IDS. Checks IFC models against Türkiye's building-permit BIM regulation.
- [mcp-for-maya](https://freemcp.space/featured/mcp-for-maya) — Maya MCP Server with spatial awareness, camera planning, aesthetic analysis, and scene auditing
- [ramen](https://freemcp.space/bulkguy47/ramen) — Self-hosted, multi-zone MCP server platform for GKE, EKS and AKS. A git repo of Python tools becomes canary-deployed, autoscaled Rust + Python workers with NeMo guardrails per tool, Entra ID / Google Workspace SSO, custom roles, OAuth 2.1, secrets, IP rules and audit. Clients on macOS, Windows and Linux.
- [caishi](https://freemcp.space/featured/caishi) — 采诗 · 给 AI 用的中文互联网能力包：一条命令读抖音/B站/小红书/公众号/知乎/头条等 33 站（满配 40）| Read the Chinese internet from your AI agent. Read-only, reuses your browser sessions.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
