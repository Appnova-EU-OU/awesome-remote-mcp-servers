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
- [Rendeverance/toolfunnel](https://freemcp.space/featured/rendeverance-toolfun) — Zero-dependency MCP gateway - attach, filter, gate, and observe MCP servers through one funnel.
- [aidevelopers2/remoteopenclaw-mcp](https://freemcp.space/featured/aidevelopers2-remote) — Search 13,870+ MCP servers, 4,384+ agent skills, and plugins from your terminal or AI agent. CLI + MCP server for remoteopenclaw.com
- [davidmosiah/wellness-cgm-mcp](https://freemcp.space/featured/davidmosiah-wellness) — Local-first continuous glucose monitor MCP — Dexcom Developer API, FreeStyle Libre via LibreLink Up. Levels-killer, agent-first.
- [RNVizion/rnv-color-mcp](https://freemcp.space/featured/rnvizion-rnv-color-m) — A complete color workflow over MCP: mix (incl. Kubelka-Munk paint physics), convert formats, generate harmonies, and remember named palettes. Resolves hex, CSS, and custom brand color names, and refuses unknown colors rather than guessing. Hosted, no install: `https://rnvizion-rnv-color-mcp.hf.space/mcp`.
- [kansei-link/kansei-mcp-server](https://freemcp.space/featured/kansei-link-kansei-m) — Local-first MCP navigator for AI agents. 11,000+ SaaS services, 200 workflow recipes, 89-97% token savings. Works with Claude Code, Cursor, Cline, Zed, Windsurf.
- [XavierFabregat/spotify-mcp](https://freemcp.space/featured/xavierfabregat-spoti) — Control Spotify by talking to your AI — MCP server for Claude, Cursor, and any MCP client
- [joshseane/-nmlp-mcp](https://freemcp.space/featured/joshseane-nmlp-mcp) — First-edition identification — points of issue, number-line decoding, and publisher rules over a CC-BY, DOI-cited dataset of 6,717 titles — plus New Mexico book-donation logistics. Hosted remote server, no auth. Endpoint: https://newmexicoliteracyproject.org/api/mcp · Registry: `org.newmexicoliteracyproject/nmlp-mcp`
- [quokkapix/quokkapix-mcp](https://freemcp.space/featured/quokkapix-quokkapix) — Private browser image workflows for AI agents via MCP
- [hedging8563/tokenlab-mcp-server](https://freemcp.space/featured/hedging8563-tokenlab) — OpenAPI-generated MCP server for TokenLab text, image, video, music, 3D, audio, files, embeddings, rerank, translation, and async tasks.
- [adw0rd/awesome-mcp-tools-mcp](https://freemcp.space/featured/adw0rd-awesome-mcp-t) — CLI + MCP stdio bridge for the awesome-mcp.tools catalog of 2,000+ MCP servers. Search from terminal or wire into Claude/Cursor/Codex/Cline/Windsurf.
- [reefapi/reefapi-mcp](https://freemcp.space/featured/reefapi-reefapi-mcp) — One MCP for 160+ live web-data APIs — search engines, social (Reddit, TikTok, Threads, Bluesky), e-commerce (Amazon, eBay, AliExpress, Etsy), real estate (Zillow, Redfin), jobs, travel, news, finance and company/people intel. Clean JSON from sites that block scrapers; one key, one shared credit pool, free tier. Remote streamable-http at api.reefapi.com/mcp.
- [forgemeshlabs/anomaly-mcp](https://freemcp.space/featured/forgemeshlabs-anomal) — Blockchain event sequence anomaly detection MCP server. Scores event streams using NASA-derived SequenceMiner via x402 micropayments.
- [austenstone/myinstants-mcp](https://freemcp.space/featured/austenstone-myinstan) — MCP server that lets your ai agent press sound buttons. it's not that deep.
- [LeonTing1010/tap](https://freemcp.space/featured/leonting1010-tap) — Capture a logged-in browser task once — replay it forever at zero LLM tokens. Local-first browser-automation MCP for Claude Code, Cursor & any MCP host; credentials never leave your machine.
- [molanojustin/smithsonian-mcp](https://freemcp.space/featured/molanojustin-smithso) — A Model Context Protocol (MCP) server that provides AI assistants with access to the Smithsonian Institution's Open Access collections.
- [longevity-genie/synergy-age-mcp](https://freemcp.space/featured/longevity-genie-syne) — MCP server for the SynergyAge database of synergistic and antagonistic genetic interactions in longevity.
- [LarryWalkerDEV/mcp-immostage](https://freemcp.space/featured/larrywalkerdev-mcp-i) — MCP Server for AI Virtual Staging — stage rooms, beautify floor plans, classify images, optimize property listings. Built by immostage.ai
- [markmircea/Selenix-MCP-Server](https://freemcp.space/featured/markmircea-selenix-m) — MCP server that bridges Claude Desktop (or any other local app supporting MCP)  with Selenix for browser automation and testing. Enables creating, running, debugging, and managing browser automation tests through natural language.
- [robhunter/agentdeals](https://freemcp.space/featured/robhunter-agentdeals) — MCP server aggregating free tiers, startup credits & developer tool deals. 4 tools, 54 categories, 1,525+ offers.
- [Continuum-AI-Corp/orcarouter-mcp-server](https://freemcp.space/featured/continuum-ai-corp-or) — Official MCP server for OrcaRouter — the LLM gateway with auto-routing and fallback chains. Browse models and chat from Claude Desktop, Cursor, Windsurf, or any MCP client.
- [Work90210/APIFold](https://freemcp.space/featured/work90210-apifold) — Turn any REST API into an MCP server. No code required.
- [neptun2000/heor-agent-mcp](https://freemcp.space/featured/neptun2000-heor-agen) — HEOR (Health Economics and Outcomes Research) MCP server with 7 tools for literature search across 41 medical data sources (PubMed, NICE, CADTH, ICER, etc.), cost-effectiveness modeling (Markov/PartSA/PSA), and HTA dossier preparation for pharmaceutical and biotech teams.
- [shunshi-ai/bazi-reader-mcp](https://freemcp.space/featured/shunshi-ai-bazi-read) — Give your AI agent the ability to read Chinese Bazi (八字) charts — an open-source MCP server 🔮
- [gupta-kush/spotify-mcp](https://freemcp.space/featured/gupta-kush-spotify-m) — Control Spotify from Claude, Cursor, or any MCP client. 100+ tools for playback, playlists, discovery, and curation.
- [AceDataCloud/MCPNanoBanana](https://freemcp.space/featured/acedatacloud-mcpnano) — MCP server for Nano Banana AI image generation and editing via Ace Data Cloud.
- [hlydecker/ucsc-genome-mcp](https://freemcp.space/featured/hlydecker-ucsc-genom) — An MCP server to interact with the UCSC Genome Browser API
- [erajasekar/ai-diagram-maker-mcp](https://freemcp.space/featured/erajasekar-ai-diagra) — MCP server for AI Diagram Maker — generate flowcharts, sequence diagrams, ERDs, system/network architecture, UML, mindmap, and workflow from natural language, code, ASCII, images, or Mermaid. Inline rendering using MCP Apps UI and editable diagram URLs. Requires API key.
- [aparajithn/agent-scraper-mcp](https://freemcp.space/featured/aparajithn-agent-scr) — Web scraping MCP server for AI agents — screenshots, content extraction, structured scraping
- [fulcradynamics/fulcra-context-mcp](https://freemcp.space/featured/fulcradynamics-fulcr) — MCP server for accessing personal health and biometric data including sleep stages, heart rate, HRV, glucose, workouts, calendar, and location via the Fulcra Life API with OAuth2 consent.
- [Custodia-Admin/pagebolt-mcp](https://freemcp.space/featured/custodia-admin-pageb) — An MCP server to allow AI agents to interact with PageBolt to take screenshots, grab PDFs, and more.
- [bch1212/agentfetch-mcp](https://freemcp.space/featured/bch1212-agentfetch-m) — MCP server for fetching web URLs with token estimation, caching, and intelligent routing. Built for AI agents.
- [bgaze/snapstack-server](https://freemcp.space/featured/bgaze-snapstack-serv) — Local always-on server for SnapStack: receives browser captures and serves them to any MCP-capable LLM client over MCP (Streamable HTTP +   stdio). Listens on 127.0.0.1 only.
- [flowzap-xyz/flowzap-mcp](https://freemcp.space/featured/flowzap-xyz-flowzap) — MCP server for FlowZap - Create workflow diagrams via AI assistants
- [leonardoca1/aesthetics-wiki-mcp](https://freemcp.space/featured/leonardoca1-aestheti) — MCP server for the Aesthetics Wiki (aesthetics.fandom.com) — search, read, and discover aesthetics from your LLM.
- [drakonkat/wizzy-mcp-tmdb](https://freemcp.space/featured/drakonkat-wizzy-mcp) — The wizzy-mcp-tmdb project is an MCP (Model Context Protocol) server implemented in JavaScript that provides tools to search and retrieve information from The Movie Database (TMDB). It allows AI clients to access movie, TV show, and person data through a standardized protocol.
- [albertnahas/icogenie-mcp](https://freemcp.space/featured/albertnahas-icogenie) — MCP server for IcoGenie - Enable AI agents to generate SVG icons programmatically
- [khalidsaidi/ragmap](https://freemcp.space/featured/khalidsaidi-ragmap) — RAG MCP Registry Finder (RAGMap): subregistry API + MCP server + Firestore ingestion
- [carlosahumada89/govrider-mcp-server](https://freemcp.space/featured/carlosahumada89-govr) — GovRider MCP Server - Match your tech product or consulting service to thousands of live government tenders, RFPs, grants, and frameworks from 25+ official sources worldwide
- [SidneyBissoli/medical-terminologies-mcp](https://freemcp.space/featured/sidneybissoli-medica) — MCP Server for global medical terminologies: ICD-11, SNOMED CT, LOINC, RxNorm, MeSH
- [NyxToolsDev/dicom-hl7-mcp-server](https://freemcp.space/featured/nyxtoolsdev-dicom-hl) — DICOM/HL7 healthcare interoperability MCP server for Claude
- [aliafsahnoudeh/shahnameh-mcp-server](https://freemcp.space/featured/aliafsahnoudeh-shahn) — ام سی پی سرور برای شاهنامه
- [PantelisGeorgiadis/dicomweb-mcp-server](https://freemcp.space/featured/pantelisgeorgiadis-d) — DICOMweb Model Context Protocol (MCP) server implementation
- [pkotecha-eng/aria-mcp-server](https://freemcp.space/featured/pkotecha-eng-aria-mc) — ARIA Clinical Research MCP Server — exposes PubMed, ClinicalTrials.gov & ISRCTN as MCP tools. Any Claude agent can search 35M+ biomedical papers and 400K+ clinical trials in real time.
- [thelongevityvault/decoder-3am-mcp](https://freemcp.space/featured/thelongevityvault-de) — Sleep disruption cause classifier MCP server from The Longevity Vault
- [pubspro/pubmed-search](https://freemcp.space/featured/pubspro-pubmed-searc) — MCP server for PubMed search and literature summarization
- [tatsuju/opdstar-nhi-mcp](https://freemcp.space/featured/tatsuju-opdstar-nhi) — Taiwan National Health Insurance (NHI) data for AI agents via Model Context Protocol. Powered by OPDSTAR (https://opdstar.com).
- [musharna/plant-genomics-mcp](https://freemcp.space/featured/musharna-plant-genom) — Plant genomics MCP server — 32 tools across 11 backends (Ensembl Plants, Phytozome, UniProt, Europe PMC, QuickGO, NCBI BLAST, Gramene, KEGG, STRING-DB, ATTED-II, BAR) + cross-source synthesis. stdio + Streamable-HTTP transports.
- [MastadoonPrime/sylex-search](https://freemcp.space/featured/mastadoonprime-sylex) — Universal search engine for AI agents. Discover products, services, and businesses across every category via MCP.
- [jaspertvdm/mcp-server-gemini-bridge](https://freemcp.space/featured/jaspertvdm-mcp-serve-2) — MCP Server - Bridge to Google Gemini API. Part of HumoticaOS/SymbAIon ecosystem.
- [rdanieli/tentra-mcp](https://freemcp.space/featured/rdanieli-tentra-mcp) — Tentra MCP — memory for AI coding agents. Persistent code graph + AI architecture diagrams. 32 MCP tools. Works in Cursor, Claude Code, Codex, Windsurf.
- [karyaboyraz/mockit-mcp](https://freemcp.space/featured/karyaboyraz-mockit-m) — MCP server that turns text prompts into premium iOS mobile UI mockups (PNG + HTML). Powered by Claude (Opus 4.7) + Playwright. Two backends: local CLI or Anthropic API. MIT.
- [ejwhite7/brandkit-mcp](https://freemcp.space/featured/ejwhite7-brandkit-mc) — Open-source MCP server that gives AI tools native access to your company's design system — drop in your brand files, connect to Claude or any LLM tool
- [gavxm/ani-mcp](https://freemcp.space/featured/gavxm-ani-mcp) — MCP server for AniList with taste-aware recommendations, watch analytics, social tools, and full list management.
- [gregario/astronomy-oracle](https://freemcp.space/featured/gregario-astronomy-o) — Celestial object catalog and observing session planner MCP server
- [Swarmwage/swarmwage](https://freemcp.space/featured/swarmwage-swarmwage) — The reliability layer for agent commerce — discover, call, and verify paid x402 services (and hire AI agents) in USDC on Base, via MCP. Client-observed reliability evidence; no escrow, no token.
- [rplryan/x402-discovery-mcp](https://freemcp.space/featured/rplryan-x402-discove) — MCP server for x402 Service Discovery — continuously growing catalog of services, real-time quality signals, facilitator-compat checks. For Claude, Cursor, Windsurf.
- [sonnyflylock/voxie-ai-directory-mcp](https://freemcp.space/featured/sonnyflylock-voxie-a) — MCP server for the Voxie AI Phone Number Directory. Query AI services you can chat with via webchat.
- [sF1nX/x402station](https://freemcp.space/featured/sf1nx-x402station) — MCP adapter (x402station-mcp on npm) + AgentKit action provider + consumer-side demo agent for x402station — pre-flight oracle for x402 endpoints. Backend (signal logic, ingest pipeline, probe history) stays private.
- [rupinder2/mcp-orchestrator](https://freemcp.space/featured/rupinder2-mcp-orches) —  MCP Orchestration Gateway – aggregates tools from multiple MCP servers with BM25 search and deferred loading for Claude Desktop
- [salwks/mcp-techTrend](https://freemcp.space/featured/salwks-mcp-techtrend) — Multi-source academic + code + medical-regulatory trend monitoring (arXiv, PubMed, GitHub, Hugging Face, openFDA 510(k)/Recalls). Newspaper-style briefings, per-domain tuning, sandbox-safe Python launcher.
- [MyMedi-AI/mymedi-ai-mcp-server](https://freemcp.space/featured/mymedi-ai-mymedi-ai) — Healthcare billing MCP server — 20 AI tools for ICD-10, CPT, HCPCS lookup (81,769 codes with RVU + OPPS pricing), prior auth prediction, claims validation, denial-risk scoring, and NPI/drug enrichment. 10 free credits, then x402 USDC or Stripe.
- [rosasynthesiz/flstudio-mcp](https://freemcp.space/featured/rosasynthesiz-flstud) — AI-powered FL Studio control via the Model Context Protocol. Beyond piano-roll notes — full in-DAW mixing (Mix Doctor, gain staging, EQ/comp/reverb, reference matching), routing, and composition through Claude and other MCP clients. 67 tools. Windows.
- [mgnirck/lecka-mcp](https://freemcp.space/featured/mgnirck-lecka-mcp) — Race nutrition planning for endurance athletes. Calculates carb, sodium and fluid targets for marathons, ultras, cycling and triathlons. Returns personalised Lecka product recommendations by race type, conditions and athlete weight.
- [dnaerys/onekgpd-mcp](https://freemcp.space/featured/dnaerys-onekgpd-mcp) — 1000 Genomes Project Dataset MCP Server
- [cinderwright-ai/cinderwright-api](https://freemcp.space/featured/cinderwright-ai-cind) — MCP server + x402 Discovery Hub. Search engine for the agent economy. 1450+ services indexed.
- [AgentHotspot](https://freemcp.space/featured/agenthotspot) — 🔍 MCP server to search 6,000+ AI agent MCP connectors from AgentHotspot.com Marketplace
- [espadaw/Agent47](https://freemcp.space/featured/espadaw-agent47) — Unified job search for AI agents. MCP server integrating x402, RentAHuman, Virtuals, and more into a single interface for finding work and comparing prices across the agent economy.
- [Aganium/agenium](https://freemcp.space/featured/aganium-agenium) — AGENIUM — DNS of the Agent Web. Identity, trust & discovery for AI agents. MCP-compatible. agent:// protocol with mTLS, trust scores & capability search.
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
- [Sudo MCP](https://freemcp.space/featured/sudo-mcp) — MCP server that allows executing privileged commands via the OS native password dialog, without storing credentials.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
