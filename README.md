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
- [OpenAaaS](https://freemcp.space/featured/openaaas) — OpenAaaS: science agent network — bring AI to your data, not your data to AI. AaaS, Agent as a Service, MCP protocol, local execution, Docker sandbox, zero-config Rust nodes.
- [olostep-mcp-server](https://freemcp.space/featured/olostep-mcp-server) — MCP server for Olostep — the web scraping, crawling, and search infrastructure used by top AI companies. Gives any MCP-compatible AI agent the ability to scrape, crawl, batch-extract, and search the web in real time.
- [opengenes-mcp](https://freemcp.space/featured/opengenes-mcp) — MCP for the open-genes
- [jupytercad-mcp](https://freemcp.space/featured/jupytercad-mcp) — An MCP server for JupyterCAD that allows you to control it using LLMs/natural language.
- [nakkas](https://freemcp.space/featured/nakkas) — MCP server that turns AI into an SVG artist
- [transcriptor-mcp](https://freemcp.space/featured/transcriptor-mcp-2) — An MCP server (stdio + HTTP/SSE) that fetches video transcripts/subtitles via yt-dlp, with pagination for large responses. Supports YouTube, Twitter/X, Instagram, TikTok, Twitch, Vimeo, Facebook, Bilibili, VK, Dailymotion. Whisper fallback — transcribes audio when subtitles are unavailable (local or OpenAI API). Works with Cursor and other MCP host
- [mermaid-mcp-server](https://freemcp.space/featured/mermaid-mcp-server) — MCP server for generating Mermaid diagrams from projects (local/GitHub) and rendering via Kroki.
- [unbrowser](https://freemcp.space/featured/unbrowser) — Agent-native browser and MCP server for lightweight, Chrome-free web discovery, with explicit escalation to Unchained for browser-only flows.
- [freshcontext-mcp](https://freemcp.space/featured/freshcontext-mcp) — Timestamped web intelligence for AI agents. MCP server with guaranteed freshness envelopes.
- [AgenticCrawler](https://freemcp.space/featured/agenticcrawler) — acrawl — LLM-powered web crawler. Describe what you want in plain English, get structured data back. Single Rust binary, 25 providers, MCP server built-in.
- [selenium-mcp-server](https://freemcp.space/featured/selenium-mcp-server) — A Model Context Protocol server providing web automation capabilities through Selenium WebDriver
- [iwdp-mcp](https://freemcp.space/featured/iwdp-mcp) — MCP server + CLI for iOS Safari debugging via ios-webkit-debug-proxy — full WebKit Inspector Protocol support
- [chrome-mcp-secure](https://freemcp.space/featured/chrome-mcp-secure) — Secure ChromeMCP Server - Query and Debugging sites using Google Chrome with additional security hardening layers
- [rendex-mcp](https://freemcp.space/featured/rendex-mcp) — MCP server for Rendex — capture screenshots, generate PDFs, and render HTML to images of any webpage via AI agents. Claude, Cursor, Windsurf compatible.
- [mcp-doctor](https://freemcp.space/featured/mcp-doctor) — Diagnose, secure, and benchmark your MCP servers. Zero-config CLI for Claude Code, Cursor, VS Code, and Windsurf.
- [4everland-hosting-mcp](https://freemcp.space/featured/4everland-hosting-mc) — An MCP server implementation for 4EVERLAND Hosting enabling instant deployment of AI-generated code to decentralized storage networks like Greenfield, IPFS, and Arweave.
- [snaprender-integrations](https://freemcp.space/featured/snaprender-integrati) — Official integrations for SnapRender Screenshot API — MCP server, SDKs, OpenClaw, ChatGPT Actions, Postman
- [site-shot-mcp](https://freemcp.space/featured/site-shot-mcp) — Official Site-Shot MCP server — let Claude, Cursor, and other AI agents capture website screenshots: full-page, ad & cookie-banner removal, device emulation.
- [purroxy2](https://freemcp.space/featured/purroxy2) — Record what you do on any website and securely automate it forever. Replays browser actions in headless Playwright with encrypted credentials and AI-powered selector healing.
- [prufa-mcp](https://freemcp.space/featured/prufa-mcp) — The QA agent for your vibe-coded app. Apache-2.0 MCP server.
- [devloop](https://freemcp.space/featured/devloop) — Browser control + dev-server logs on one correlated timeline — an MCP server with a headless (stdio) mode and an Electron cockpit. Built for AI agents.
- [selenium-mcp](https://freemcp.space/featured/selenium-mcp) — A Python MCP server that brings Selenium WebDriver automation to Claude and other AI assistants — with built-in code generation for Python (pytest), Java TestNG, and JUnit 5 test scripts.
- [wavexis-mcp](https://freemcp.space/featured/wavexis-mcp) — MCP server for browser automation — 220 tools for Chrome, Edge & Firefox via CDP + BiDi. 13 capability tiers, stealth mode, Lighthouse audits. No Node.js, no Chromium download. 100% Python.
- [lyrenth-mcp](https://freemcp.space/featured/lyrenth-mcp) — Read any URL as a clean AIDocument (Markdown + structure) through Lyrenth's cached index.
- [scrapeunblocker-mcp](https://freemcp.space/featured/scrapeunblocker-mcp) — Model Context Protocol (MCP) server for ScrapeUnblocker - let Claude fetch any web page's HTML through your own API key.
- [mcp-server-templates](https://freemcp.space/featured/mcp-server-templates) — A flexible platform that provides Docker & Kubernetes backends, a lightweight CLI (mcpt), and client utilities for seamless MCP integration. Spin up servers from templates, route requests through a single endpoint with load balancing, and support both deployed (HTTP) and local (stdio) transports — all with sensible defaults and YAML-based configs.
- [a2asearch-mcp](https://freemcp.space/featured/a2asearch-mcp-2) — MCP server for searching AI agents, MCP servers, CLI tools and agent skills via A2ASearch
- [deepseek-mcp-server](https://freemcp.space/featured/deepseek-mcp-server) — MCP server for DeepSeek V4 (v4-flash, v4-pro, 1M context): chat, reasoning, function calling, thinking mode, cost tracking. deepseek-chat/reasoner aliases supported.
- [context-firewall](https://freemcp.space/featured/context-firewall) — MCP proxy that collapses 50+ tools into 4 meta-tools and compresses tool outputs by 60-95% (HTML, base64, huge JSON) - cut context-token costs for any MCP client, any model
- [alphafold-sovereign-mcp](https://freemcp.space/featured/alphafold-sovereign) — BioMed MCP over AlphaFold DB + 8 public sources, with SQLite knowledge graph, offline mode, and explicit clinical-use limits.
- [mcp-server](https://freemcp.space/featured/mcp-server-6) — Ceki MCP Server — rent real residential Chrome browsers from peers (real fingerprints, residential IPs, per-minute crypto billing). Also hire specialists, post jobs.
- [ao3-mcp](https://freemcp.space/featured/ao3-mcp) — MCP server for Archive of Our Own: search fanfiction and have an AI read and rank fics for you
- [forcedream-mcp](https://freemcp.space/featured/forcedream-mcp) — MCP server for ForceDream — discover, invoke, and trustlessly verify AI agents with cryptographic proofs.
- [fda-risk-radar-mcp](https://freemcp.space/featured/fda-risk-radar-mcp) — Constat — FDA & NHTSA regulatory-risk MCP server for AI agents. 14 tools: recalls, adverse events, warning letters, 483s, 510(k) predicate chains, reimbursement, vehicle safety. com.healthai/radar on the official MCP registry. Hosted at constat.dev/api/mcp.
- [clarity-mcp](https://freemcp.space/featured/clarity-mcp) — Condition-aware ingredient & product safety MCP server — 9 tools, every answer with a verdict, evidence tier, and citations. com.healthai/clarity on the official MCP registry. Hosted at mcp.healthai.com.
- [motionlint](https://freemcp.space/featured/motionlint) — Catch bad animations before they ship. Deterministic motion audit + vision-LLM design review for your terminal and Claude Code.
- [sonovault-mcp](https://freemcp.space/featured/sonovault-mcp) — MCP server for the SonoVault music metadata API. Search 90M+ tracks, artists, and releases from AI assistants.
- [mesh-connector](https://freemcp.space/featured/mesh-connector) — Connect any MCP client to the MeshTool platform + MeshMarket exchange in 30 seconds — agents that remember, reason, and rent each other's tools.
- [mcpqueen](https://freemcp.space/featured/mcpqueen) — 👑 The evidence layer for MCP — every registry server probed live, graded with verbatim evidence, plus Trust Receipts. Itself an MCP server at mcpqueen.com/mcp (7 tools, no auth).
- [crimson-crab-mcp-template](https://freemcp.space/featured/crimson-crab-mcp-tem) — A ready-to-clone Rust MCP server that calls Claude via crimson-crab
- [gph-mcp-server](https://freemcp.space/featured/gph-mcp-server) — GPH Intelligence MCP Server — Healthcare Service Provider Finder. Access 100,000+ verified providers via MCP.
- [visionaire-engine](https://freemcp.space/featured/visionaire-engine) — Eyes for AI coding agents: deterministic MCP server that tells the LLM which CSS rule wins, in which file, on which line — and why. Cascade verdicts, blast radius, interaction timelines, pixel-perfect audits.
- [supasidebar-mcp](https://freemcp.space/featured/supasidebar-mcp) — Give your AI assistant local access to your open tabs, saved bookmarks, and recently opened links across every browser on your Mac. Open source, zero telemetry.
- [saglitzdesign-mcp](https://freemcp.space/featured/saglitzdesign-mcp) — Expert design & marketing knowledge for AI agents — an MCP server for web, iOS, Android & macOS design: UI, UX, SEO, GEO, copywriting, roadmaps & real-world patterns.
- [uniprot-mcp](https://freemcp.space/featured/uniprot-mcp) — Auditable UniProt MCP server with per-response SHA-256 provenance, release pinning, verification, and offline replay.
- [oura-mcp](https://freemcp.space/featured/oura-mcp) — Ask your Oura Ring anything, in ChatGPT or Claude, in any language. Remote MCP server for Oura data.
- [aidc-ai-mcp](https://freemcp.space/featured/aidc-ai-mcp) — AI data center automation tool — MCP connector (design · validate · layout). Remote MCP: aidc-ai.io/api/mcp · registry io.aidc-ai/design-engine. Engine private.
- [orbit-sentinel-mcp](https://freemcp.space/featured/orbit-sentinel-mcp) — MCP server for Orbit Sentinel — space regulatory filings from FCC, ITU, UNOOSA, FAA-AST
- [mcp-server](https://freemcp.space/featured/mcp-server-5) — Correctover MCP Server — LLM Reliability Engineering for AI tools. Real-time 6-dimension output validation, self-healing failover, drift detection. Zero-dep, BYOK.
- [biorobotics](https://freemcp.space/featured/biorobotics) — An open-source, stateless Model Context Protocol (MCP) framework bridging biological datasets (NCBI/UniProt) with deterministic physical coordinates for robotic automation.
- [uxloom](https://freemcp.space/featured/uxloom) — Agent-native UI/UX design validation via MCP — journey completeness, state coverage, WCAG checks before code exists
- [kavel-mcp](https://freemcp.space/featured/kavel-mcp) — Discover Kavel’s AI photo/video generators (hairstyle, figurine, pet portrait, wedding, 90s yearbook, dance video, HD restore), get model-tuned prompts, and open the right tool to generate on www.kavel.ai. `npx kavel-mcp`
- [humanforai-mcp](https://freemcp.space/featured/humanforai-mcp) — MCP server for Human For AI — let your AI agent hire a real human for real-world verification, testing, review, and errands. Free pilot, no auth.
- [skillselion-mcp](https://freemcp.space/featured/skillselion-mcp) — MCP server to search Skillselion's curated directory of Claude Code skills, MCP servers & plugin marketplaces, ranked by installs and GitHub stars.
- [releases](https://freemcp.space/featured/releases) — Download mirror for the Proofpane MCP daemon. Source stays in the private codebase; this exists so browsers (Chrome Safe Browsing, Edge SmartScreen) trust the download.
- [avots-mcp](https://freemcp.space/featured/avots-mcp) — MCP server for avots.ai: image, video, audio, face-swap, talking avatars and chat across 300+ AI models. Works with Claude Desktop, claude.ai, Cursor, Cline, openclaw, LibreChat, Continue.
- [llm-prices-cn](https://freemcp.space/featured/llm-prices-cn) — Daily-verified LLM API pricing dataset (44+ models, CN & global) with a hosted MCP server for live price queries and token cost estimation.
- [ddg-agent-payable-services](https://freemcp.space/featured/ddg-agent-payable-se) — Pay-per-call x402 gateway for AI agents — MCP server + OpenAI-compatible API for agent tools, market data, RPC, and MCP security audits. Pay in USDC on Base, no account.
- [oorlogsbronnen-mcp](https://freemcp.space/featured/oorlogsbronnen-mcp) — MCP server for accessing Dutch World War II archives through the Oorlogsbronnen API. Provides structured access to historical records, photographs, and documents from 1940-1945 Netherlands.
- [mcp-gateway](https://freemcp.space/featured/mcp-gateway-2) — MCP Gateway - A meta-server for minimal Claude Code tool bloat with progressive disclosure
- [zen-mcp](https://freemcp.space/featured/sh6drack-zen-mcp) — The first MCP server for Zen Browser. 20 tools. No Selenium, no Playwright, just WebSocket.
- [forage](https://freemcp.space/featured/isaac-levine-forage) — Self-improving tool discovery for AI agents. Agents find, install, and learn to use new MCP tools automatically.
- [agent-web-interface](https://freemcp.space/featured/lespaceman-agent-web) — Token-efficient browser automation MCP for AI agents, with semantic page snapshots and stable element IDs.
- [hashnet-mcp-js](https://freemcp.space/featured/hashgraph-online-has) — Universal MCP Server for finding + connecting to agents anywhere on the planet. https://hol.org/mcp
- [memeboat-mcp](https://freemcp.space/featured/memebo-at-memeboat-m) — MCP server for Memeboat — search 25,000+ meme templates and create memes from any AI assistant. Free, no API key. https://memebo.at
- [agentbodega](https://freemcp.space/featured/agentbodegastore-age) — AgentBodega MCP discovery package and public registry metadata
- [toolfunnel](https://freemcp.space/featured/rendeverance-toolfun) — Zero-dependency MCP gateway - attach, filter, gate, and observe MCP servers through one funnel.
- [remoteopenclaw-mcp](https://freemcp.space/featured/aidevelopers2-remote) — Search 13,870+ MCP servers, 4,384+ agent skills, and plugins from your terminal or AI agent. CLI + MCP server for remoteopenclaw.com
- [wellness-cgm-mcp](https://freemcp.space/featured/davidmosiah-wellness) — Local-first continuous glucose monitor MCP — Dexcom Developer API, FreeStyle Libre via LibreLink Up. Levels-killer, agent-first.
- [rnv-color-mcp](https://freemcp.space/featured/rnvizion-rnv-color-m) — A complete color workflow over MCP: mix (incl. Kubelka-Munk paint physics), convert formats, generate harmonies, and remember named palettes. Resolves hex, CSS, and custom brand color names, and refuses unknown colors rather than guessing. Hosted, no install: `https://rnvizion-rnv-color-mcp.hf.space/mcp`.
- [kansei-mcp-server](https://freemcp.space/featured/kansei-link-kansei-m) — Local-first MCP navigator for AI agents. 11,000+ SaaS services, 200 workflow recipes, 89-97% token savings. Works with Claude Code, Cursor, Cline, Zed, Windsurf.
- [spotify-mcp](https://freemcp.space/featured/xavierfabregat-spoti) — Control Spotify by talking to your AI — MCP server for Claude, Cursor, and any MCP client
- [joshseane/-nmlp-mcp](https://freemcp.space/featured/joshseane-nmlp-mcp) — First-edition identification — points of issue, number-line decoding, and publisher rules over a CC-BY, DOI-cited dataset of 6,717 titles — plus New Mexico book-donation logistics. Hosted remote server, no auth. Endpoint: https://newmexicoliteracyproject.org/api/mcp · Registry: `org.newmexicoliteracyproject/nmlp-mcp`
- [quokkapix-mcp](https://freemcp.space/featured/quokkapix-quokkapix) — Private browser image workflows for AI agents via MCP
- [tokenlab-mcp-server](https://freemcp.space/featured/hedging8563-tokenlab) — OpenAPI-generated MCP server for TokenLab text, image, video, music, 3D, audio, files, embeddings, rerank, translation, and async tasks.
- [awesome-mcp-tools-mcp](https://freemcp.space/featured/adw0rd-awesome-mcp-t) — CLI + MCP stdio bridge for the awesome-mcp.tools catalog of 2,000+ MCP servers. Search from terminal or wire into Claude/Cursor/Codex/Cline/Windsurf.
- [reefapi-mcp](https://freemcp.space/featured/reefapi-reefapi-mcp) — One MCP for 160+ live web-data APIs — search engines, social (Reddit, TikTok, Threads, Bluesky), e-commerce (Amazon, eBay, AliExpress, Etsy), real estate (Zillow, Redfin), jobs, travel, news, finance and company/people intel. Clean JSON from sites that block scrapers; one key, one shared credit pool, free tier. Remote streamable-http at api.reefapi.com/mcp.
- [anomaly-mcp](https://freemcp.space/featured/forgemeshlabs-anomal) — Blockchain event sequence anomaly detection MCP server. Scores event streams using NASA-derived SequenceMiner via x402 micropayments.
- [myinstants-mcp](https://freemcp.space/featured/austenstone-myinstan) — MCP server that lets your ai agent press sound buttons. it's not that deep.
- [tap](https://freemcp.space/featured/leonting1010-tap) — Capture a logged-in browser task once — replay it forever at zero LLM tokens. Local-first browser-automation MCP for Claude Code, Cursor & any MCP host; credentials never leave your machine.
- [smithsonian-mcp](https://freemcp.space/featured/molanojustin-smithso) — A Model Context Protocol (MCP) server that provides AI assistants with access to the Smithsonian Institution's Open Access collections.
- [synergy-age-mcp](https://freemcp.space/featured/longevity-genie-syne) — MCP server for the SynergyAge database of synergistic and antagonistic genetic interactions in longevity.
- [mcp-immostage](https://freemcp.space/featured/larrywalkerdev-mcp-i) — MCP Server for AI Virtual Staging — stage rooms, beautify floor plans, classify images, optimize property listings. Built by immostage.ai
- [Selenix-MCP-Server](https://freemcp.space/featured/markmircea-selenix-m) — MCP server that bridges Claude Desktop (or any other local app supporting MCP)  with Selenix for browser automation and testing. Enables creating, running, debugging, and managing browser automation tests through natural language.
- [agentdeals](https://freemcp.space/featured/robhunter-agentdeals) — MCP server aggregating free tiers, startup credits & developer tool deals. 4 tools, 54 categories, 1,525+ offers.
- [orcarouter-mcp-server](https://freemcp.space/featured/continuum-ai-corp-or) — Official MCP server for OrcaRouter — the LLM gateway with auto-routing and fallback chains. Browse models and chat from Claude Desktop, Cursor, Windsurf, or any MCP client.
- [APIFold](https://freemcp.space/featured/work90210-apifold) — Turn any REST API into an MCP server. No code required.
- [heor-agent-mcp](https://freemcp.space/featured/neptun2000-heor-agen) — HEOR (Health Economics and Outcomes Research) MCP server with 7 tools for literature search across 41 medical data sources (PubMed, NICE, CADTH, ICER, etc.), cost-effectiveness modeling (Markov/PartSA/PSA), and HTA dossier preparation for pharmaceutical and biotech teams.
- [bazi-reader-mcp](https://freemcp.space/featured/shunshi-ai-bazi-read) — Give your AI agent the ability to read Chinese Bazi (八字) charts — an open-source MCP server 🔮
- [spotify-mcp](https://freemcp.space/featured/gupta-kush-spotify-m) — Control Spotify from Claude, Cursor, or any MCP client. 100+ tools for playback, playlists, discovery, and curation.
- [MCPNanoBanana](https://freemcp.space/featured/acedatacloud-mcpnano) — MCP server for Nano Banana AI image generation and editing via Ace Data Cloud.
- [ucsc-genome-mcp](https://freemcp.space/featured/hlydecker-ucsc-genom) — An MCP server to interact with the UCSC Genome Browser API
- [ai-diagram-maker-mcp](https://freemcp.space/featured/erajasekar-ai-diagra) — MCP server for AI Diagram Maker — generate flowcharts, sequence diagrams, ERDs, system/network architecture, UML, mindmap, and workflow from natural language, code, ASCII, images, or Mermaid. Inline rendering using MCP Apps UI and editable diagram URLs. Requires API key.
- [agent-scraper-mcp](https://freemcp.space/featured/aparajithn-agent-scr) — Web scraping MCP server for AI agents — screenshots, content extraction, structured scraping
- [fulcra-context-mcp](https://freemcp.space/featured/fulcradynamics-fulcr) — MCP server for accessing personal health and biometric data including sleep stages, heart rate, HRV, glucose, workouts, calendar, and location via the Fulcra Life API with OAuth2 consent.
- [pagebolt-mcp](https://freemcp.space/featured/custodia-admin-pageb) — An MCP server to allow AI agents to interact with PageBolt to take screenshots, grab PDFs, and more.
- [agentfetch-mcp](https://freemcp.space/featured/bch1212-agentfetch-m) — MCP server for fetching web URLs with token estimation, caching, and intelligent routing. Built for AI agents.
- [snapstack-server](https://freemcp.space/featured/bgaze-snapstack-serv) — Local always-on server for SnapStack: receives browser captures and serves them to any MCP-capable LLM client over MCP (Streamable HTTP +   stdio). Listens on 127.0.0.1 only.
- [flowzap-mcp](https://freemcp.space/featured/flowzap-xyz-flowzap) — MCP server for FlowZap - Create workflow diagrams via AI assistants
- [aesthetics-wiki-mcp](https://freemcp.space/featured/leonardoca1-aestheti) — MCP server for the Aesthetics Wiki (aesthetics.fandom.com) — search, read, and discover aesthetics from your LLM.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
