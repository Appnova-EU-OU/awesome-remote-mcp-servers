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
- [reaper-mcp](https://freemcp.space/featured/reaper-mcp) — MCP server to control REAPER DAW with AI. 176 tools for mixing, mastering, MIDI composition, and full music production.
- [build123d-mcp](https://freemcp.space/featured/build123d-mcp) — MCP server for build123d to improve AI cognition when creating 3D CAD models
- [mcp-apple-music](https://freemcp.space/featured/mcp-apple-music) — Full Apple Music integration for Claude via MCP — search catalog, manage library & playlists
- [auth-fetch-mcp](https://freemcp.space/featured/auth-fetch-mcp) — MCP server that lets AI assistants fetch content from authenticated web pages.
- [cloakbrowser-mcp](https://freemcp.space/featured/cloakbrowser-mcp) — ⚡ CloakBrowser MCP server for AI agents: Playwright-powered browsing, clean tool forwarding, Docker support, and multi-session HTTP transport.
- [cert-manager-mcp-server](https://freemcp.space/featured/cert-manager-mcp-ser) — MCP Server for cert-manager
- [python-openstackmcp-server](https://freemcp.space/featured/python-openstackmcp) — openstack mcp server
- [pythonanywhere-mcp-server](https://freemcp.space/featured/pythonanywhere-mcp-s) — MCP server implementation for PythonAnywhere cloud platform.
- [rancher-mcp-server](https://freemcp.space/featured/rancher-mcp-server) — Model Context Protocol (MCP) server for the Rancher ecosystem: multi-cluster Kubernetes, Harvester HCI (VMs, storage, networks), and Fleet GitOps.
- [infomaniak-mcp-agent](https://freemcp.space/featured/infomaniak-mcp-agent) — Full unofficial agentic Infomaniak MCP server — guided automation of web hosting, mail, kDrive, domains and DNS.
- [tilt-mcp](https://freemcp.space/featured/tilt-mcp) — MCP server for Tilt - enables LLMs to interact with your Tilt dev environment for building, deploying, and debugging Kubernetes workloads
- [portkey-admin-mcp](https://freemcp.space/featured/portkey-admin-mcp) — Full Portkey Admin API MCP server
- [mcp-server-s3](https://freemcp.space/featured/mcp-server-s3) — MCP server for AWS S3 — list buckets, browse objects, upload/download, presigned URLs
- [mcp-server-cloudflare](https://freemcp.space/featured/mcp-server-cloudflar) — MCP server to manage Cloudflare Workers, KV, R2, DNS, and cache from your IDE
- [aidc-ai-mcp](https://freemcp.space/featured/aidc-ai-mcp) — AI data center automation tool — MCP connector (design · validate · layout). Remote MCP: aidc-ai.io/api/mcp · registry io.aidc-ai/design-engine. Engine private.
- [TokenBurnRate](https://freemcp.space/featured/tokenburnrate) — Track LLM token costs across Claude, GPT and Gemini. MCP server + CLI with optimization hints and $ savings estimates. 📇🏠
- [nebulablock-mcp-server](https://freemcp.space/featured/nebulablock-mcp-serv) — integrates with the fastmcp library to expose the full range of NebulaBlock API functionalities as accessible tools
- [mctl-mcp](https://freemcp.space/featured/mctl-mcp) — AI-native platform for Kubernetes management and automated GitOps (30+ tools).
- [dynadot-mcp](https://freemcp.space/featured/dynadot-mcp) — MCP server for Dynadot domain registrar API3 — 60 tools for domains, DNS, contacts, transfers & more
- [rnv-color-mcp](https://freemcp.space/featured/rnv-color-mcp) — Color-computation server on the Model Context Protocol. Nine deterministic tools for conversion, harmony, mixing, WCAG contrast, and CIEDE2000. Published to the official MCP registry and listed in awesome-mcp-servers. Also an OAuth 2.1 resource server with RFC 9728 metadata and enforced per-tool scopes.
- [mcp-server-terraform](https://freemcp.space/featured/mcp-server-terraform) — Safety-first MCP server for Terraform — plan risk & cost analysis, drift detection, confirmation flows, and provider auth pre-flight for Claude and other AI assistants
- [openpouch](https://freemcp.space/featured/openpouch) — Agent-native hosting: coding agents deploy apps to a live URL in one command - no account, no CAPTCHA. CLI + MCP server, Apache-2.0.
- [mcp-aoai-web-browsing](https://freemcp.space/featured/mcp-aoai-web-browsin) — A minimal Model Context Protocol 🖥️ server/client🧑‍💻with OpenAI and 🌐 web browser control via Playwright.
- [mcpmcp-server](https://freemcp.space/featured/mcpmcp-server) — Discover, setup, and integrate MCP servers with your favorite clients. Unlock the full potential of AI in your daily workflow.
- [mcp-server-python](https://freemcp.space/featured/mcp-server-python) — Python MCP Server for Kestra — you can use it as a tool in Kestra's AI Agents
- [localstack-mcp-server](https://freemcp.space/featured/localstack-mcp-serve) — MCP Server for LocalStack
- [proximo](https://freemcp.space/featured/proximo) — The Proxmox MCP you can hand the keys: VE/PBS/PMG/PDM. Plan, prove, undo, diagnose. MCP/A2A/API.
- [azure-resource-graph-mcp-server](https://freemcp.space/featured/azure-resource-graph-2) — Model Context Protocol (MCP) server that provides access to Azure Resource Graph queries. It allows you to retrieve information about Azure resources across your subscriptions using Resource Graph queries.
- [liveblocks-mcp-server](https://freemcp.space/featured/liveblocks-mcp-serve) — MCP server for Liveblocks.
- [netskope-mcp](https://freemcp.space/featured/netskope-mcp) — An MCP to give access to all Netskope Private Access components within a Netskope Private Access environments including detailed setup information and LLM examples on usage.
- [ionoscloud-mcp](https://freemcp.space/featured/ionoscloud-mcp) — This project implements an MCP server to interact with ionos cloud resources.
- [docker-mcp](https://freemcp.space/featured/docker-mcp) — Docker-MCP-Server - An MCP server covering the full management surface of Docker.  Manage, maintain and audit multiple docker environments with ease.
- [oci-pricing-mcp](https://freemcp.space/featured/oci-pricing-mcp) — OCI Pricing MCP Server - Model Context Protocol server for Oracle Cloud Infrastructure pricing information
- [cloud-cost-mcp](https://freemcp.space/featured/cloud-cost-mcp-2) — Model Context Protocol server for Cloud Infrastructure pricing information
- [spinnaker-mcp](https://freemcp.space/featured/spinnaker-mcp) — MCP Server for Spinnaker — manage applications, pipelines, and deployments via the Model Context Protocol
- [NetLicensing-MCP](https://freemcp.space/featured/netlicensing-mcp) — The official NetLicensing MCP Server is a natural language interface that enables agentic applications to manage the full software licensing lifecycle in Labs64 NetLicensing 👉🏼 without writing a single API call.
- [easypanel-mcp-server](https://freemcp.space/featured/easypanel-mcp-server) — MCP Server for Easypanel — control deployments, services, logs and databases from Claude Code, Cursor and Claude Desktop
- [cloudflare-mcp-pro](https://freemcp.space/featured/cloudflare-mcp-pro) — Cloudflare MCP: 69 tools over the REST API v4 — DNS, Workers, KV, R2, D1, Pages, WAF, SSL, Email, AI — with a human-approval gate
- [kops](https://freemcp.space/featured/kops) — Read-only kubectl as an MCP server for Claude Code — structured JSON, hardcoded safe verbs, one-shot triage & inventory.
- [mcp-server](https://freemcp.space/featured/mcp-server-7) — Infrawise MCP server for Claude Code — Azure FinOps cost optimization
- [tempmd-mcp](https://freemcp.space/featured/tempmd-mcp) — MCP server for temp.md — one stable public link for agent-made artifacts, updated in place
- [hostodo-mcp](https://freemcp.space/featured/hostodo-mcp) — Registry metadata for the hosted Hostodo MCP server
- [biothings-mcp](https://freemcp.space/featured/biothings-mcp) — MCP (Model Context Protocol) server for biothings
- [metmuseum-mcp](https://freemcp.space/featured/metmuseum-mcp) — Met Museum MCP integration to discover the art collection at The Metropolitan Museum of Art in New York
- [mcp-cyclops](https://freemcp.space/featured/mcp-cyclops) — Model Context Protocol server for Cyclops
- [gget-mcp](https://freemcp.space/featured/gget-mcp) — Bioinformatic MCP server that wraps the most useful functions of the gget library
- [encode-toolkit](https://freemcp.space/featured/encode-toolkit) — MCP server and Claude Plugin for a full ENCODE Project genomic data and analysis toolkit — search, download, track, and analyze functional genomics experiments
- [tdmcp](https://freemcp.space/featured/tdmcp) — TouchDesigner MCP server, describe a visual to Claude, Cursor or Codex and it builds a real, playable node network (audio-reactive, generative, particle, 3D, feedback) with live knobs + MIDI/OSC/DMX, then checks for errors and previews its own work.
- [agoragentic-integrations](https://freemcp.space/featured/agoragentic-integrat-2) — Public adapters and discovery catalog for Triptych OS (Agent OS): agent frameworks, MCP/A2A/x402 protocols, workflows, wallets, SDKs, and examples for execute-first routing, governed handoffs, and receipt-aware agent commerce.
- [photopea-mcp-server](https://freemcp.space/featured/photopea-mcp-server) — MCP server for AI-driven image editing with Photopea
- [mcp-ipfs](https://freemcp.space/featured/mcp-ipfs) — 🪐 MCP IPFS Server 
- [esp-rainmaker-mcp](https://freemcp.space/featured/esp-rainmaker-mcp) — ESP RainMaker MCP server
- [finopsmcp](https://freemcp.space/featured/finopsmcp) — The headless FinOps intelligence layer: API-first, agent-first cost control for cloud + AI. Connect your cloud stack in Claude, Cursor, or the terminal, and gate what agents do to your infra before they act. Propose-only. Open source, local-first.
- [mcp-server-aws-sso](https://freemcp.space/featured/mcp-server-aws-sso) — Node.js/TypeScript MCP server for AWS Single Sign-On (SSO). Enables AI systems (LLMs) with tools to initiate SSO login (device auth flow), list accounts/roles, and securely execute AWS CLI commands using temporary credentials. Streamlines AI interaction with AWS resources.
- [mcp-proxmox](https://freemcp.space/featured/mcp-proxmox) — MCP server for managing Proxmox VE clusters through AI assistants
- [adls-mcp-server](https://freemcp.space/featured/adls-mcp-server) — Microsoft Azure Data Lake Storage MCP Server
- [docker-mcp-server](https://freemcp.space/featured/docker-mcp-server) — Docker MCP server designed for agents that need their containers to stay running. Health checks, auto-restart, Compose lifecycle, log streaming.
- [mcp-pfsense](https://freemcp.space/featured/mcp-pfsense) — MCP server for managing pfSense firewalls through AI assistants
- [devops-mcp-webui](https://freemcp.space/featured/devops-mcp-webui) — Bridge connecting OpenWebUI to Kubernetes clusters via MCP protocol
- [agent-deploy-dashboard-mcp](https://freemcp.space/featured/agent-deploy-dashboa-2) — Unified deployment management MCP server for Vercel, Render, Railway, and Fly.io
- [ovh-api-mcp](https://freemcp.space/featured/ovh-api-mcp) — MCP server for the OVH API — explore and execute any OVH endpoint from Claude, Cursor, or any MCP-compatible LLM client. Built in Rust.
- [cloudprice-mcp](https://freemcp.space/featured/cloudprice-mcp) — MCP server that compares on-demand VM pricing across AWS, Azure, and GCP in real time
- [cloudscope-mcp](https://freemcp.space/featured/cloudscope-mcp-2) — Multi-cloud cost management MCP server (Azure + GCP). Read-only access to spending, anomalies, forecasts, budgets, and guided FinOps workflows. Ask your AI about your cloud bill.
- [mcp-server-spotinst](https://freemcp.space/featured/mcp-server-spotinst) — MCP server for Spot.io (Spotinst) API - Ocean clusters, VNGs, Elastigroups, costs, right-sizing across AWS and Azure
- [eds-mcp-server](https://freemcp.space/featured/eds-mcp-server) — MCP server for Adobe Edge Delivery Services — 20 tools for AI agents to preview, publish, read content, query metrics, and manage EDS sites
- [Nutanix-AIops](https://freemcp.space/featured/nutanix-aiops) — Governed Nutanix Prism Central v4 ops: clusters/VMs/storage/DR/LCM, ETag-safe, 47 MCP tools (preview)
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
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
