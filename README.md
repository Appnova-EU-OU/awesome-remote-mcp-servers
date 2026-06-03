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
- [alderpost-mcp](https://freemcp.space/featured/alderpost-mcp-4) — 8 intelligence endpoints: domain security (VirusTotal, SPF/DKIM/DMARC), threat analysis (AbuseIPDB), company intel (People Data Labs, Hunter.io), compliance, sales, sports, property, and health data. Pay-per-call via x402 USDC on Base.
- [alderpost-mcp](https://freemcp.space/featured/alderpost-mcp-3) — 8 intelligence endpoints: domain security (VirusTotal, SPF/DKIM/DMARC), threat analysis (AbuseIPDB), company intel (People Data Labs, Hunter.io), compliance, sales, sports, property, and health data. Pay-per-call via x402 USDC on Base.
- [appnova-app-store-connect-mcp](https://freemcp.space/featured/appnova-app-store-co) — App Store Connect MCP server — analytics, reviews, metadata, subscriptions, IAPs, TestFlight, bundle ID capabilities
- [alderpost-mcp](https://freemcp.space/featured/alderpost-mcp-2) — 8 intelligence endpoints: domain security (VirusTotal, SPF/DKIM/DMARC), threat analysis (AbuseIPDB), company intel (People Data Labs, Hunter.io), compliance, sales, sports, property, and health data. Pay-per-call via x402 USDC on Base.
- [Tavily MCP Server](https://freemcp.space/featured/tavily-mcp-server) — AI-powered web search with structured results, source citations, and answer synthesis.
- [intercept-mcp](https://freemcp.space/featured/intercept-mcp) — Multi-tier fallback chain for fetching web content as clean markdown. Handles tweets, YouTube, arXiv, PDFs, Wikipedia, and GitHub repos with no API keys required.
- [SharpTools MCP](https://freemcp.space/featured/sharptools-mcp) — MCP server built with .NET — provides file system, shell execution, and developer utility tools for C# and .NET workflows.
- [Spring Boot MCP Server](https://freemcp.space/featured/spring-boot-mcp-server) — Reference MCP server built with Spring AI and Spring Boot, demonstrating stdio transport integration patterns for Java applications.
- [Gje Unofficial Forti](https://freemcp.space/templates/gje-unofficial-forti) — MCP server: unofficial-fortimonitor-mcp-server
- [Hovsteder/powersun-tron-mcp](https://freemcp.space/templates/hov-powersun-tron-mc) — PowerSun Tron MCP server
- [Kzino/vorim-mcp-server](https://freemcp.space/templates/kzi-vorim-mcp-server) — Vorim MCP server for security
- [HubLensOfficial/mcp-server](https://freemcp.space/templates/hub-mcp-server) — HubLens MCP server
- [ClaudeCodeNavi/claudecodenavi-mcp](https://freemcp.space/templates/claudecodenavi-mcp) — Claude Code knowledge platform & marketplace MCP server. Search and share snippets, prompts, Q&A solutions, error fixes, and MCP server configurations from the ClaudeCodeNavi community.
- [shibley/apistatuscheck-mcp-server](https://freemcp.space/templates/apistatuscheck-mcp-s) — Check real-time operational status of 114+ cloud services and APIs (AWS, GitHub, Stripe, OpenAI, Vercel, etc.) directly from AI assistants. Published on npm.
- [liveblocks-mcp](https://freemcp.space/templates/liveblocks-mcp) — Liveblocks rooms and storage management via MCP
- [s2-stream-mcp](https://freemcp.space/templates/s2-stream-mcp) — Official MCP server for S2.dev serverless stream platform
- [chatterboxio-mcp](https://freemcp.space/templates/chatterboxio-mcp) — MCP server for ChatterBox.io — AI agents in online meetings
- [getsentry/sentry-mcp](https://freemcp.space/templates/sentry-mcp) — Sentry.io integration for error tracking and performance monitoring
- [Xuanwo/mcp-server-opendal](https://freemcp.space/templates/mcp-server-opendal) — Access any storage with Apache OpenDAL™
- [pab1it0/adx-mcp-server](https://freemcp.space/featured/adx-mcp-server) — Query and analyze Azure Data Explorer databases
- [SureScaleAI/openai-gpt-image-mcp](https://freemcp.space/templates/openai-gpt-image-mcp) — OpenAI GPT image generation/editing MCP server.
- [particlefuture/MCPDiscovery](https://freemcp.space/featured/1mcpserver) — MCP of MCPs. Automatic discovery and configure MCP servers on your local machine.
- [AgentHotspot](https://freemcp.space/featured/agenthotspot-mcp) — Search, integrate and monetize MCP connectors on the AgentHotspot MCP marketplace
- [espadaw/Agent47](https://freemcp.space/featured/agent47) — Unified job aggregator for AI agents across 9+ platforms (x402, RentAHuman, Virtuals, etc).
- [kaiyuanxiaobing/atomgit-mcp-server](https://freemcp.space/featured/atomgit-mcp-server) — Official AtomGit server for integration with repository management, PRs, issues, branches, labels, and more.
- [JaviMaligno/mcp-server-bitbucket](https://freemcp.space/templates/mcp-server-bitbucket) — Bitbucket MCP server with 58 tools for repository management, PRs, pipelines, branches, commits, deployments, webhooks, tags, branch restrictions, and source browsing.
- [loglux/authmcp-gateway](https://freemcp.space/featured/authmcp-gateway) — Auth proxy for MCP servers: OAuth2 + DCR, JWT, RBAC, rate limiting, multi-server aggregation, and monitoring dashboard.
- [slouchd/cyberchef-api-mcp-server](https://freemcp.space/featured/cyberchef-api-mcp-se) — MCP server for interacting with the CyberChef server API which will allow an MCP client to utilise the CyberChef operations.
- [samvas-codes/dawshund_mcp](https://freemcp.space/templates/dawshund-mcp) — An MCP server based on dAWShund to enumerate AWS IAM data, analyze effective permissions, and visualize access relationships across users, roles, and resources. Built for cloud security engineers who want fast, easy and effective insights into AWS identity risk.
- [mariocandela/beelzebub](https://freemcp.space/templates/beelzebub) — Beelzebub is a honeypot framework that lets you build honeypot tools using MCP. Its purpose is to detect prompt injection or malicious agent behavior. The underlying idea is to provide the agent with tools it would never use in its normal work.
- [ndl-systems/kevros-mcp](https://freemcp.space/templates/kevros-mcp) — Governance primitives for autonomous agents — verify actions against policy, record signed provenance, and bind intents cryptographically. Free tier: 100 calls/month.
- [jaspertvdm/mcp-server-inject-bender](https://freemcp.space/templates/mcp-server-inject-be) — Security through absurdity: transforms SQL injection and XSS attempts into harmless comedy responses using AI-powered humor defense.
- [fr0gger/MCP_Security](https://freemcp.space/templates/mcp-security) — MCP server for querying the ORKL API. This server provides tools for fetching threat reports, analyzing threat actors, and retrieving intelligence sources.
- [creatorrmode-lead/avp-sdk](https://freemcp.space/featured/avp-sdk) — Trust, identity (W3C DID), and EigenTrust reputation for AI agents. Attestations, disputes, sybil detection, IPFS audit anchoring.
- [vinaybhosle/agentstamp](https://freemcp.space/featured/agentstamp) — Trust intelligence for AI agents — identity stamps, reputation scoring (0-100), registry, forensic audit trails, and A2A passports via x402 micropayments.
- [agentgraph-co/agentgraph](https://freemcp.space/featured/agentgraph) — Trust verification and security scanning for AI agents. Checks security posture of third-party MCP servers and tools with signed attestations (Ed25519/JWS) before interaction.
- [BrowseAI-HQ/BrowserAI-Dev](https://freemcp.space/featured/browserai-dev) — Evidence-backed web research for AI agents. Real-time search with cited claims, confidence scores, and compare mode (raw LLM vs evidence-backed). MCP server, REST API, and Python SDK.
- [shibley/apistatuscheck-mcp-server](https://freemcp.space/featured/apistatuscheck-mcp-s) — Check real-time operational status of 114+ cloud services and APIs (AWS, GitHub, Stripe, OpenAI, Vercel, etc.) directly from AI assistants. Published on npm.
- [gsmethells/preflight-mcp](https://freemcp.space/templates/preflight-mcp) — TrustPilot for APIs — independent reliability ratings for APIs and MCP servers, powered by synthetic probes and crowdsourced agent telemetry.
- [ejcho623/agent-breadcrumbs](https://freemcp.space/featured/agent-breadcrumbs) — Unified agent work logging and observability across ChatGPT, Claude, Cursor, Codex, and OpenClaw with config-first schemas and pluggable sinks.
- [alimuratkuslu/byok-observability-mcp](https://freemcp.space/featured/byok-observability-m) — Comprehensive MCP server for Grafana, Prometheus, Kafka UI, and Datadog with a secure "Bring Your Own Key" or BYOK model.
- [var-gg/mcp](https://freemcp.space/templates/mcp-14) — Enforces team naming consistency for AI-generated code via Cursor MCP integration. [Guide ↗](https://var.gg)
- [softvoyagers/qrmint-api](https://freemcp.space/templates/qrmint-api) — Free styled QR code generator API with custom colors, logos, frames, and batch generation. No API key required.
- [softvoyagers/ogforge-api](https://freemcp.space/templates/ogforge-api) — Free Open Graph image generator API with themes, Lucide icons, and custom layouts. No API key required.
- [sapientpants/sonarqube-mcp-server](https://freemcp.space/templates/sonarqube-mcp-server) — A Model Context Protocol (MCP) server that integrates with SonarQube to provide AI assistants with access to code quality metrics, issues, and quality gate statuses
- [Pharaoh-so/pharaoh](https://freemcp.space/templates/pharaoh-mcp) — Hosted MCP server that parses TypeScript and Python codebases into Neo4j knowledge graphs for blast radius analysis, dead code detection, dependency tracing, and architectural context.
- [optimaquantum/claude-critical-rules-mcp](https://freemcp.space/featured/claude-critical-rule) — Automatic enforcement of critical rules for Claude AI preventing 96 documented failure patterns. Provides compliance verification checklist and rules summary via MCP tools.
- [Neo1228/spring-boot-starter-swagger-mcp](https://freemcp.space/templates/spring-boot-starter) — Turn your Spring Boot application into an MCP server instantly by reusing existing Swagger/OpenAPI documentation.
- [MerabyLabs/promptarchitect-mcp](https://freemcp.space/templates/promptarchitect-mcp) — Workspace-aware prompt engineering. Refines, analyzes and generates prompts based on your project's tech stack, dependencies and context. Free to use.
- [LumabyteCo/clarifyprompt-mcp](https://freemcp.space/featured/clarifyprompt-mcp) — MCP server for AI prompt optimization — transforms vague prompts into platform-optimized prompts for 58+ AI platforms across 7 categories (image, video, voice, music, code, chat, document).
- [kindly-software/kdb](https://freemcp.space/templates/kdb) — AI-powered time-travel debugger with bidirectional execution replay, audit-compliant hash-chain logging, and SIMD-accelerated stack unwinding. Free Hobby tier available.
- [jaspertvdm/mcp-server-tibet](https://freemcp.space/templates/mcp-server-tibet) — TIBET provenance tracking for AI decisions. Cryptographic audit trails with ERIN/ERAAN/EROMHEEN/ERACHTER intent logging for compliance.
- [izzzzzi/codewiki-mcp](https://freemcp.space/featured/codewiki-mcp) — MCP server for codewiki.google. Search repos, fetch AI-generated wiki docs, and ask questions about any open-source repository.
- [Inspizzz/jetbrains-datalore-mcp](https://freemcp.space/templates/jetbrains-datalore-m) — MCP server for interacting with cloud deployments of Jetbrains Datalore platform. Fully incorporated Datalore API ( run, run interactively, get run data, fetch files )
- [endorhq/cli](https://freemcp.space/templates/cli) — Endor lets your AI agents run services like MariaDB, Postgres, Redis, Memcached, Alpine, or Valkey in isolated sandboxes. Get pre-configured applications that boot in less than 5 seconds.
- [ClaudeCodeNavi/claudecodenavi-mcp](https://freemcp.space/featured/claudecodenavi-mcp) — Claude Code knowledge platform & marketplace MCP server. Search and share snippets, prompts, Q&A solutions, error fixes, and MCP server configurations from the ClaudeCodeNavi community.
- [agent-hanju/char-index-mcp](https://freemcp.space/featured/char-index-mcp) — Precise character-level string indexing for LLMs. Provides tools for finding, extracting, and manipulating text by exact character position to solve position-based operations.
- [prisma/mcp](https://freemcp.space/templates/mcp-13) — Gives LLMs the ability to manage Prisma Postgres databases (e.g. spin up new databases and run migrations or queries).
- [corebasehq/coremcp](https://freemcp.space/templates/coremcp) — A secure, tunnel-native database bridge for AI agents. Connects localhost & on-premise databases (MSSQL, etc.) to LLMs with AST-based query safety and PII masking.
- [aliyun/alibabacloud-tablestore-mcp-server](https://freemcp.space/templates/alibabacloud-tablest) — MCP service for Tablestore, features include adding documents, semantic search for documents based on vectors and scalars, RAG-friendly, and serverless.
- [timkulbaev/mcp-gmail](https://freemcp.space/templates/mcp-gmail) — Full Gmail operations via Unipile API: send, reply, list, read, delete, search, manage labels, attachments, and drafts. Dry-run by default on destructive actions.
- [OverQuotaAI/chatterboxio-mcp-server](https://freemcp.space/featured/chatterboxio-mcp-ser) — MCP server implementation for ChatterBox.io, enabling AI agents to send bots to online meetings (Zoom, Google Meet) and obtain transcripts and recordings.
- [jaspertvdm/mcp-server-rabel](https://freemcp.space/templates/mcp-server-rabel) — AI-to-AI messaging via I-Poll protocol and AInternet. Enables agents to communicate using .aint domains, semantic messaging, and trust-based routing.
- [bababoi-bibilabu/agent-mq](https://freemcp.space/featured/agent-mq) — Message queue for AI coding assistants. Let AI agents (Claude Code, Cursor, Codex) send messages to each other across sessions and machines. UUID-based auth, self-hostable.
- [VmLia/books-mcp-server](https://freemcp.space/featured/books-mcp-server) — This is an MCP server used for querying books, and it can be applied in common MCP clients, such as Cherry Studio.
- [trilogy-group/aws-pricing-mcp](https://freemcp.space/featured/aws-pricing-mcp) — Get up-to-date EC2 pricing information with one call. Fast. Powered by a pre-parsed AWS pricing catalogue.
- [newageflyfish-max/volthq](https://freemcp.space/templates/volthq) — Compute price oracle for AI agents. Compare inference pricing across 8 providers in real time with routing recommendations and spend tracking. One-command install: `npx volthq-mcp-server --setup`.
- [jasonwilbur/cloud-cost-mcp](https://freemcp.space/featured/cloud-cost-mcp) — Multi-cloud pricing comparison across AWS, Azure, GCP, and OCI with 2,700+ instance types. Real-time pricing from public APIs, workload calculators, and migration savings estimator.
- [hardik-id/azure-resource-graph-mcp-server](https://freemcp.space/featured/azure-resource-graph) — A Model Context Protocol server for querying and analyzing Azure resources at scale using Azure Resource Graph, enabling AI assistants to explore and monitor Azure infrastructure.
- [elevy99927/devops-mcp-webui](https://freemcp.space/templates/devops-mcp-webui) — MCP Server for Kubernetes integrated with Open-WebUI, bridging the gap between DevOps and non-technical teams. Supports `kubectl` and `helm` operations through natural-language commands.
- [softvoyagers/pageshot-api](https://freemcp.space/templates/pageshot-api) — Free webpage screenshot capture API with format, viewport, and dark mode options. No API key required.
- [khalidsaidi/ragmap](https://freemcp.space/templates/ragmap) — MapRag: RAG-focused subregistry + MCP server to discover and route to retrieval-capable MCP servers using structured constraints and explainable ranking.
- [K-Dense-AI/claude-skills-mcp](https://freemcp.space/templates/claude-skills-mcp) — Intelligent search capabilities to let every model and client use [Claude Agent Skills](https://www.anthropic.com/news/skills) like native.
- [glenngillen/mcpmcp-server](https://freemcp.space/templates/mcpmcp-server) — A list of MCP servers so you can ask your client which servers you can use to improve your daily workflow.
- [edgarriba/prolink](https://freemcp.space/templates/prolink) — Agent-to-agent marketplace middleware — MCP-native discovery, negotiation, and transaction between AI agents
- [blockrunai/blockrun-mcp](https://freemcp.space/featured/blockrun-mcp) — Access 30+ AI models (GPT-5, Claude, Gemini, Grok, DeepSeek) without API keys. Pay-per-use via x402 micropayments with USDC on Base.
- [ariekogan/ateam-mcp](https://freemcp.space/featured/ateam-mcp) — Build, validate, and deploy multi-agent AI solutions on the ADAS platform. Design skills with tools, manage solution lifecycle, and connect from any AI environment via stdio or HTTP.
- [rhein1/agoragentic-integrations](https://freemcp.space/featured/agoragentic-integrat) — Agent-to-agent marketplace where AI agents discover, invoke, and pay for services from other agents using USDC on Base L2.
- [Work90210/APIFold](https://freemcp.space/featured/apifold) — Turn any REST API into a hosted MCP server. 18 free public servers (GitHub, Stripe, Slack, OpenAI, Notion, and more) — no setup required, bring your own API key.
- [doggychip/agentforge](https://freemcp.space/featured/agentforge) — Unified API gateway and marketplace for 300+ AI agents. One API key, REST + streaming, 90% creator revenue share, health monitoring. Self-hostable (MIT).
- [tadas-github/a2asearch-mcp](https://freemcp.space/featured/a2asearch-mcp) — MCP server to search 4,800+ MCP servers, AI agents, CLI tools and agent skills. Install: `npx -y a2asearch-mcp`. Ask Claude: "Find MCP servers for database access". Free, no auth required.
- [8randonpickart5/alderpost-mcp](https://freemcp.space/featured/alderpost-mcp) — 8 bundled intelligence endpoints (security, company, threat, compliance, sales, sports, property, health) via x402 micropayments on Base.
- [cuttalo/depscope](https://freemcp.space/templates/depscope) — Package Intelligence for AI agents. 22 tools across 17 ecosystems (npm/pypi/cargo/go/maven/nuget/rubygems/composer/pub/hex/swift/cocoapods/cpan/hackage/cran/conda/homebrew) — check health, vulnerabilities (OSV + CISA KEV + EPSS), typosquats, malicious flags, alternatives, known bugs, breaking changes, stack compatibility and error-to-fix. 31k+ packages, 2.2k+ CVEs enriched. Zero auth, MIT. Remote URL https://mcp.depscope.dev/mcp or stdio `npx depscope-mcp`.
- [tponscr-debug/oracle-h-mcp](https://freemcp.space/templates/oracle-h-mcp) — Mandatory human approval gate for autonomous AI agents. Intercepts critical, irreversible, or financially significant actions and routes them to a human via Telegram for real-time approve/reject. Raises workflow success probability from 81.5% to 99.6%.
- [Thezenmonster/agentscore-mcp-server](https://freemcp.space/featured/agentscore-mcp-serve) — MCP security trust layer. Continuously monitors 800+ MCP packages on npm for install scripts, command injection, hardcoded secrets, capability drift, and publisher posture. Ships a GitHub Action policy gate for PR-level allow/warn/block decisions with OIDC auto-provisioning. 5 MCP tools, no API key required.
- [ark-forge/arkforge-mcp](https://freemcp.space/featured/arkforge-mcp) — Third-party certifying proxy — sign any HTTP call (AI agents, webhooks, microservices) with an independent Ed25519 signature, RFC 3161 timestamp, and Sigstore Rekor anchor. Works with Claude, GPT-4, Mistral, LangChain, AutoGen, or any HTTP client.
- [KOVY/agentforge-trust-mcp](https://freemcp.space/featured/agentforge-trust-mcp) — Query the AgentForge Trust Score (0-100 across five dimensions: security, code health, behavioral audit, community trust, EU compliance) for any MCP server before connecting. Exposes `check_trust`, `evaluate_policy`, `list_trusted`, and `recommend` tools. 3,600+ servers audited, free public API.
- [alexfleetcommander/agent-trust-stack-mcp](https://freemcp.space/featured/agent-trust-stack-mc) — Cryptographic provenance, bilateral blind reputation scoring, and tamper-evident logging for AI agent interactions. 7 interlocking trust protocols (CoC, ARP, ASA, AJP, ALP, AMP, CWEP) available in Python (pip) and TypeScript (npm). 663 tests. Bitcoin-anchored provenance chains, anti-Goodhart reputation scoring, machine-readable contracts, dispute resolution, lifecycle management, trust-weighted matchmaking, and context-window cost allocation. Also on [Smithery](https://smithery.ai/server/@alexfl
- [connerlambden/bgpt-mcp](https://freemcp.space/featured/bgpt-mcp) — Search scientific papers with structured experimental data extracted from full-text studies. Returns 25+ fields per paper including methods, results, sample sizes, and quality scores. 50 free searches, then $0.01/result.
- [TANTIOPE/datadog-mcp-server](https://freemcp.space/featured/datadog-mcp-server) — MCP server providing comprehensive Datadog observability access for AI assistants. Features grep-like log search, APM trace filtering with duration/status/error queries, smart sampling modes for token efficiency, and cross-correlation between logs, traces, and metrics.
- [babyblueviper1/invinoveritas](https://freemcp.space/templates/invinoveritas) — Lightning-native AI reasoning, decisions, persistent memory, and agent marketplace for autonomous agents. Pay-per-use via Bitcoin Lightning. Register free — 250 starter sats. Agents earn sats selling services (seller keeps 95%), DM each other, and run autonomously. `npm install invinoveritas-mcp`
- [gpartin/CryptoGuardClient](https://freemcp.space/featured/cryptoguardclient) — Per-transaction deterministic crypto validator for AI trading agents. Validate trades (PROCEED/CAUTION/BLOCK), scan tokens, detect rug pulls — powered by WaveGuard physics engine. 5 free calls/day, x402 USDC payments. `pip install CryptoGuardClient`
- [hifriendbot/agentwallet-mcp](https://freemcp.space/featured/agentwallet-mcp) — Permissionless wallet infrastructure for AI agents. 29 tools for wallet creation, transaction signing, token transfers, and x402 payments across all EVM chains and Solana. No KYC, no API keys — agents pay with USDC.
- [Handshake58/DRAIN-marketplace](https://freemcp.space/templates/drain-marketplace) — Open marketplace for AI services — LLMs, image/video generation, web scraping, model hosting, data extraction, and more. Agents pay per use with USDC micropayments on Polygon. No API keys, no subscriptions.
- [conviction-fm/conviction-mcp](https://freemcp.space/featured/conviction-fm) — The arena where AI agents compete for real returns. Prompt a strategy in plain English, get a funded agent that runs autonomously. Agents enter daily parimutuel pools and the conviction multiplier rewards being early and right over being late with size.
- [grahammccain/chart-library-mcp](https://freemcp.space/featured/chart-library-mcp) — Historical stock chart pattern intelligence for AI agents. 24M pre-computed embeddings across 15K stocks and 10 years of data. Search by ticker+date or screenshot to find the most similar historical patterns and see what happened next. 19 tools including pattern search, forward returns, regime analysis, and trade simulation. Install: `pip install chartlibrary-mcp`. Free tier: 200 calls/day.
- [@czagents/cnb](https://freemcp.space/featured/cz-agents-mcp) — Czech National Bank (ČNB) daily FX rates: fetch official CZK exchange rates, convert between currencies, fetch historical rates. Cached 10 min to ease upstream load. npm `@czagents/cnb` or HTTP at cnb.cz-agents.dev/mcp.
- [@arbitova/mcp-server](https://freemcp.space/featured/arbitova) — Non-custodial on-chain escrow + AI dispute arbitration for agent-to-agent USDC payments on Base. Seven tools covering the full `EscrowV1` contract surface: create escrow, mark delivered with on-chain content hash, confirm or dispute, arbiter resolves with signed verdict, cancel/escalate on timeout. `npx @arbitova/mcp-server`
- [ONE8943/ai-furniture-hub](https://freemcp.space/featured/ai-furniture-hub) — Japan-focused furniture & home product hub for AI agents. 15 tools for mm-precision search across 300+ products and 31 categories, curated sets (bundles, room presets, influencer picks), dimension-compatible replacement finder with fit_score, AI visibility diagnosis, Rakuten live API, and OpenAPI 3.1 schema. Install via `npx ai-furniture-hub`.
- [OFODevelopment/cerebrochain-mcp-server](https://freemcp.space/featured/cerebrochain-mcp-ser) — Supply chain & logistics intelligence — rate shopping across 85+ carriers, inventory management, order tracking, fleet logistics, and AI-powered demand forecasting. 20 tools and 3 resources for warehouse and supply chain operations.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
