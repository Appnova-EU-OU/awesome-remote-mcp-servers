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
- [khglynn/spotify-bulk-actions-mcp](https://freemcp.space/featured/khglynn-spotify-bulk) — MCP server for bulk Spotify operations - batch playlist creation with confidence scoring, library exports, CSV imports, and human-in-the-loop review for uncertain matches
- [delmas41/gradusnotation](https://freemcp.space/featured/delmas41-gradusnotat) — Open music notation MCP server for AI agents. Render JSON scores to SVG, MusicXML, and MIDI. Sponsored by Gradus School of Music Composition.
- [BluesPrince/thiri-mcp](https://freemcp.space/featured/bluesprince-thiri-mc) — Deterministic music-theory MCP server & API — chord analysis, Roman-numeral analysis, voicing & reharmonization for Claude & Cursor. Computed, not hallucinated. Hosted at mcp.thiri.ai · npx @bluesprincemedia/thiri-mcp
- [AceDataCloud/MCPSeedream](https://freemcp.space/featured/acedatacloud-mcpseed) — MCP server for ByteDance Seedream image generation and editing via Ace Data Cloud.
- [AceDataCloud/MCPFlux](https://freemcp.space/featured/acedatacloud-mcpflux) — MCP server for Flux AI image generation and editing via Ace Data Cloud.
- [ertad-family/liquid](https://freemcp.space/featured/ertad-family-liquid) — AI discovers APIs. Code syncs data. No adapters to write.
- [ikoskela/wisepanel-mcp](https://freemcp.space/featured/ikoskela-wisepanel-m) — MCP server for Wisepanel multi-agent deliberation platform
- [x402-index/x402search-mcp](https://freemcp.space/featured/x402-index-x402searc) — Search 13,000+ x402-enabled APIs from your AI agent. Powered by x402search.xyz
- [RipperMercs/tensorfeed](https://freemcp.space/featured/rippermercs-tensorfe) — Real-time AI industry intelligence MCP server. 6 free tools (AI news, service status, model pricing, today summary, agent activity, MCP registry snapshot) and 13 paid premium tools (routing recommendations, news search, history series, cost projection, provider deep-dive, model comparison, agents directory, what's new brief, MCP registry series, webhook watches with daily/weekly digest tier). Pay-per-call in USDC on Base mainnet, no accounts. `npx -y @tensorfeed/mcp-server`
- [mroops0111/openapi-mcp-gateway](https://freemcp.space/featured/mroops0111-openapi-m) — Turn any OpenAPI/Swagger API into an MCP server with real OAuth2 support. Multi-spec gateway for Claude, Cursor, Codex, and other MCP clients.
- [jaspertvdm/mcp-server-openai-bridge](https://freemcp.space/featured/jaspertvdm-mcp-serve) — MCP Server - Bridge to OpenAI API. Part of HumoticaOS/SymbAIon ecosystem.
- [clanker-records/crompton-network](https://freemcp.space/featured/clanker-records-crom) — Machine-native listening platform for C.W.A.'s Straight Outta Crompton. Your agent can listen. For real.
- [forgemeshlabs/imagegen-mcp](https://freemcp.space/featured/forgemeshlabs-imageg) — MCP server for AI image generation, background removal, and upscaling with optional x402 USDC payments on Base mainnet.
- [scotia1973-bot/api-hub](https://freemcp.space/featured/scotia1973-bot-api-h) — 🧠 Memory Vault — Persistent agent memory for MCP. 46 tools: agent_memory, memory_search, 45 utilities, 300+ REST. Free + .99/mo Pro.
- [oxgeneral/agentnet](https://freemcp.space/featured/oxgeneral-agentnet) — Your agent has zero users. This fixes that.  An agent-to-agent referral network where AI agents discover each other, cross-refer users, and earn credits. Available as an MCP server and HTTP API.  Built by an AI agent that couldn't find its own customers.
- [mambalabsdev/mcp-gtm-suite](https://freemcp.space/featured/mambalabsdev-mcp-gtm) — MCP server for the full Mamba Labs GTM Suite. All six GTM actors as tools in one server via Apify. Clay-ready output.
- [jabbawocky/proposalcraft](https://freemcp.space/featured/jabbawocky-proposalc) — MCP server for freelancers — draft winning proposals in your voice from a client brief
- [gpu-bridge/mcp-server](https://freemcp.space/featured/gpu-bridge-mcp-serve) — GPU-Bridge MCP Server — 30 AI services as Model Context Protocol tools. LLMs, image gen, video, audio, embeddings, reranking, PDF parsing & more. x402 native for autonomous agents.
- [ariekogan/ateam-mcp](https://freemcp.space/featured/ariekogan-ateam-mcp) — ADAS MCP Server — build, validate, and deploy multi-agent solutions from any AI environment
- [GTCC777/pulsenetwork-mcp](https://freemcp.space/featured/gtcc777-pulsenetwork) — MCP server for PulseNetwork — discover & pay (x402, USDC on Base + Solana) for 66 real-time intelligence APIs. 68 tools, pay-per-query.
- [forgemeshlabs/coinopai-mcp](https://freemcp.space/featured/forgemeshlabs-coinop) — CoinOpAI MCP server for x402-powered crypto market intelligence, trade decision support, automation prompts, and paid agent workflows on Base.
- [mcp-server-ollama-bridge](https://freemcp.space/featured/mcp-server-ollama-br) — MCP Server - Bridge to local Ollama LLM. Part of HumoticaOS/SymbAIon ecosystem.
- [clirank-mcp-server](https://freemcp.space/featured/clirank-mcp-server-2) — MCP server for CLIRank - search, compare, and get docs for 420+ APIs ranked by AI-agent friendliness
- [aiskillstore](https://freemcp.space/featured/aiskillstore) — Agent-first skill marketplace with USK open standard — MCP server for AI agent skill discovery
- [alderpost-mcp](https://freemcp.space/featured/alderpost-mcp-4) — 8 intelligence endpoints: domain security (VirusTotal, SPF/DKIM/DMARC), threat analysis (AbuseIPDB), company intel (People Data Labs, Hunter.io), compliance, sales, sports, property, and health data. Pay-per-call via x402 USDC on Base.
- [alderpost-mcp](https://freemcp.space/featured/alderpost-mcp-3) — 8 intelligence endpoints: domain security (VirusTotal, SPF/DKIM/DMARC), threat analysis (AbuseIPDB), company intel (People Data Labs, Hunter.io), compliance, sales, sports, property, and health data. Pay-per-call via x402 USDC on Base.
- [appnova-app-store-connect-mcp](https://freemcp.space/featured/appnova-app-store-co) — App Store Connect MCP server — analytics, reviews, metadata, subscriptions, IAPs, TestFlight, bundle ID capabilities
- [alderpost-mcp](https://freemcp.space/featured/alderpost-mcp-2) — 8 intelligence endpoints: domain security (VirusTotal, SPF/DKIM/DMARC), threat analysis (AbuseIPDB), company intel (People Data Labs, Hunter.io), compliance, sales, sports, property, and health data. Pay-per-call via x402 USDC on Base.
- [Tavily MCP Server](https://freemcp.space/featured/tavily-mcp-server) — AI-powered web search with structured results, source citations, and answer synthesis.
- [intercept-mcp](https://freemcp.space/featured/intercept-mcp) — Multi-tier fallback chain for fetching web content as clean markdown. Handles tweets, YouTube, arXiv, PDFs, Wikipedia, and GitHub repos with no API keys required.
- [JotDown MCP](https://freemcp.space/featured/jotdown-mcp) — MCP server for Notion integration — create, read, update, and search notes and databases in Notion via the Notion API.
- [SharpTools MCP](https://freemcp.space/featured/sharptools-mcp) — MCP server built with .NET — provides file system, shell execution, and developer utility tools for C# and .NET workflows.
- [Spring Boot MCP Server](https://freemcp.space/featured/spring-boot-mcp-server) — Reference MCP server built with Spring AI and Spring Boot, demonstrating stdio transport integration patterns for Java applications.
- [Bundler MCP](https://freemcp.space/featured/bundler-mcp) — MCP server for Ruby Bundler — check gem dependencies, search RubyGems, resolve version conflicts, and manage Gemfile entries.
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
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
