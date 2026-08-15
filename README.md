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
- [mcp-shell](https://freemcp.space/featured/mcp-shell) — Give hands to AI. MCP server to run shell commands securely, auditably, and on demand.
- [MayaMCP](https://freemcp.space/featured/mayamcp) — Model Context Protocol (MCP) server implementation for Autodesk Maya
- [code-to-tree](https://freemcp.space/featured/code-to-tree) — A runtime-free MCP server that converts source code into AST🌲, regardless of language.
- [mcp-open-library](https://freemcp.space/featured/mcp-open-library) — A Model Context Protocol (MCP) server for the Internet Archive's Open Library API that enables AI assistants to search for book and author information.
- [svgmaker-mcp](https://freemcp.space/featured/svgmaker-mcp) — Model Context Protocol server for SVGMaker - AI-powered SVG generation and editing. Seamlessly integrate SVG creation into AI workflows.
- [anilist-mcp](https://freemcp.space/featured/anilist-mcp) — AniList MCP server for accessing anime and manga data
- [opentakeoff](https://freemcp.space/featured/opentakeoff) — Open-source (Apache-2.0) PDF takeoff for construction & flooring — the first engine an AI agent drives natively over MCP, not bolted on. One-click room detection, materials + quantities, built for preconstruction. Runs entirely in your browser.
- [touchpoint](https://freemcp.space/featured/touchpoint) — Give your AI agent eyes and hands on any desktop — cross-platform accessibility API with MCP server
- [cicada](https://freemcp.space/featured/cicada) — AI Coders search blindly. Be their guide.
- [skill-cortex-server](https://freemcp.space/featured/skill-cortex-server) — A third-party MCP server that enable all IDEs to access Claude Code Skills capabilities
- [Blind-Auditor](https://freemcp.space/featured/blind-auditor) — MCP tool for improving model coding quality by mandatory self-audition
- [mcp_creator_growth](https://freemcp.space/featured/mcp-creator-growth) — Intelligent learning sidecar for AI coding assistants. Helps developers learn from AI-generated code changes through interactive blocking quizzes and provides agents with persistent project-specific debugging memory using silent RAG tools. Features 56% token optimization and multi-language support.
- [vibekit-mcp](https://freemcp.space/featured/vibekit-mcp) — MCP server for VibeKit — build, deploy, and manage hosted apps and chat with their AI agents from Claude Desktop, Cursor, and other MCP clients.
- [pyATS_MCP](https://freemcp.space/featured/pyats-mcp) — An MCP Server for pyATS (experimental)
- [quran-mcp-server](https://freemcp.space/featured/quran-mcp-server) — Quran.com API integration for verse search, translation and tafsir
- [rijksmuseum-mcp](https://freemcp.space/featured/rijksmuseum-mcp) — Rijksmuseum MCP integration for artwork exploration and analysis
- [Network-AI](https://freemcp.space/featured/network-ai) — Traffic light for AI Agents and TypeScript/Node multi-agent orchestrator with shared state, guardrails, and adapters for 32 AI frameworks
- [arch-mcp](https://freemcp.space/featured/arch-mcp) — Arch Linux MCP (Model Context Protocol) Server
- [mcp-console-automation](https://freemcp.space/featured/mcp-console-automati) — MCP server for AI-driven console application automation and monitoring
- [multi_mcp](https://freemcp.space/featured/multi-mcp-2) — Multi-Model chat, code review and analysis MCP Server for Claude Code
- [deepseek-as-subagent](https://freemcp.space/featured/deepseek-as-subagent) — Run DeepSeek as a real sub-agent inside Claude Code / Codex CLI — DeepSeek gets its own 7-tool agent loop in a sandboxed workspace, not just a single LLM call.
- [term_mcp_deepseek](https://freemcp.space/featured/term-mcp-deepseek) — A MCP‑like server using the DeepSeek API for Terminal
- [preflight](https://freemcp.space/featured/preflight) — ✈️ 24-tool MCP server for Claude Code: preflight checks for your prompts, cross-service context, session history search with LanceDB vectors, correction pattern learning, cost estimation
- [OzBridge](https://freemcp.space/featured/ozbridge) — Bring Warp™ Oz™ to any IDE or agent via MCP — plus native @oz in VS Code Copilot Chat. OzBridge is an independent project and is not affiliated with, endorsed by, or sponsored by Warp.
- [glm-mcp](https://freemcp.space/featured/glm-mcp) — GLM (Zhipu/Z.ai) as a cheap, full-capability subagent for the Claude Code app — works on a subscription Claude (no API key for the main agent), auto-routes between Opus and GLM, file-editing agent with diff/dry-run/git-revert, one-command npx install.
- [plori](https://freemcp.space/featured/plori) — plori (plori.ai): a cloud AI agent with its own computer - persistent disk, real CLI tools, and memory that carry over between sessions. Connect any MCP client.
- [VMware-AIops](https://freemcp.space/featured/vmware-aiops) — VMware vCenter/ESXi AI-powered monitoring and operations. Two skills: vmware-monitor (read-only, safe) and vmware-aiops (full operations) | Claude Code Skill
- [imagen3-mcp](https://freemcp.space/featured/imagen3-mcp) — A powerful image generation tool using Google's Imagen 3.0 API through MCP. Generate high-quality images from text prompts with advanced photography, artistic, and photorealistic controls.
- [esxi-mcp-server](https://freemcp.space/featured/esxi-mcp-server) — A VMware ESXi/vCenter management server based on MCP (Model Control Protocol), providing simple REST API interfaces for virtual machine management.
- [mkp](https://freemcp.space/featured/mkp) — MKP is a Model Context Protocol (MCP) server for Kubernetes
- [mcp_safe_local_python_executor](https://freemcp.space/featured/mcp-safe-local-pytho) — Stdio MCP Server wrapping custom Python runtime (LocalPythonExecutor) from Hugging Faces' `smolagents` framework. The runtime combines the ease of setup (compared to docker, VM, cloud runtimes) while providing safeguards and limiting operations/imports that are allowed inside the runtime.
- [forge](https://freemcp.space/featured/forge) — Turn Claude Code into a plan-execute-validate loop with parallel work, intelligent retry, and memory
- [winx-code-agent](https://freemcp.space/featured/winx-code-agent) — 🦀 A high-performance code agent written in Rust, combining the best features of WCGW for maximum efficiency and semantic capabilities. 
- [kill-process-mcp](https://freemcp.space/featured/kill-process-mcp) — AI-powered cross-platform MCP server exposing LLM-accessible tools to list and terminate OS processes via natural language queries
- [persistproc](https://freemcp.space/featured/persistproc) — MCP server to allow LLMs to manage and inspect long-running processes
- [kagan](https://freemcp.space/featured/kagan) — OpenCode Plugin for supervised agentic software development on a Kanban board
- [claude-mcp-bridge](https://freemcp.space/featured/claude-mcp-bridge) — MCP server bridging Claude CLI to Codex, Cursor - queries, and search with hardened subprocess management
- [veto](https://freemcp.space/featured/veto) — Veto MCP — gives every major AI CLI (Claude Code, Codex, Gemini, Cursor, Windsurf) a council of 49 specialist agents + 93 tools. Deterministic-first, self-learning, no API keys.
- [mcp-injector](https://freemcp.space/featured/mcp-injector) — Local MCP daemon that compresses your codebase before sending it to Claude  41-89% token reduction
- [depwire](https://freemcp.space/featured/depwire) — The missing context layer for AI-assisted refactoring
- [PersonalizationMCP](https://freemcp.space/featured/personalizationmcp) — 🎯 A unified personal data hub built on MCP that allows AI assistants to access your digital life from Steam, YouTube, Bilibili and more platforms for truly personalized interactions.
- [mcp-browser-kit](https://freemcp.space/featured/mcp-browser-kit) — An MCP Server that enables AI assistants to interact with your local browsers.
- [1mcpserver](https://freemcp.space/featured/1mcpserver-2) — MCP of MCPs. Automatic discovery and configure MCP servers on your local machine.
- [mcp-server-leetcode](https://freemcp.space/featured/mcp-server-leetcode) — A Model Context Protocol (MCP) server for LeetCode that provides access to problems, user data, and contest information through GraphQL
- [any-cli-mcp-server](https://freemcp.space/featured/any-cli-mcp-server) — Convert any (whatever) CLI to proper MCP server with tools mapped based on CLI help
- [ssh-mcp](https://freemcp.space/featured/ssh-mcp) — SSH MCP server that runs locally making it easy to manage hosts and perform commands across a group of hosts
- [mcp-server-terminal](https://freemcp.space/featured/mcp-server-terminal) — Terminal MCP Server - Model Context Protocol server for TUI/CLI automation with structured Terminal State Tree (TST)
- [ejentum-mcp](https://freemcp.space/featured/ejentum-mcp) — MCP server for the Ejentum API. 8 cognitive operations across 4 harnesses (reasoning, code, anti-deception, memory) in dynamic and adaptive modes.
- [claude-concilium](https://freemcp.space/featured/claude-concilium) — Multi-agent AI consultation framework for Claude Code via MCP — get second opinions from OpenAI, Gemini, Qwen, DeepSeek
- [mcp-proxmox](https://freemcp.space/featured/mcp-proxmox) — MCP server for managing Proxmox VE clusters through AI assistants
- [llm-council](https://freemcp.space/featured/llm-council) — LLM Council fork with persistence, decision traces, stability fixes, repeatable checks, and MCP integration.
- [llm-bus](https://freemcp.space/featured/llm-bus) — Open-source coordination engine for AI agents, over MCP. Atomic claims, shared ledger, leases, presence, handoffs, tasks. Self-host it or use the hosted service at llm-bus.com.
- [telleroutlook/agentkit-js/mcp-server](https://freemcp.space/featured/telleroutlook-agentk) — Embedded agent runtime compliance layer — WASM sandbox, MCP firewall, capability manifests, verifiable rollouts, and trace-to-training export
- [mcp-pfsense](https://freemcp.space/featured/mcp-pfsense) — MCP server for managing pfSense firewalls through AI assistants
- [Citio](https://freemcp.space/featured/citio) — Self-hosted AI coding agents that live in Slack — run Claude Code or Codex in your own infra, ship PRs, and keep every credential behind a controlled MCP tool layer.
- [tailtest-cline](https://freemcp.space/featured/tailtest-cline) — tailtest for Cline: MCP server + .clinerules pack + Memory Bank integration. Reaches 8+ editors via Cline. Adversarial test mode shipped from day one.
- [brandkit-mcp](https://freemcp.space/featured/brandkit-mcp) — Open-source MCP server that gives AI tools native access to your companys design system — drop in your brand files, connect to Claude or any LLM tool
- [telleroutlook/agentkit-js/mcp-server](https://freemcp.space/featured/telleroutlook-agentk-2) — Embedded agent runtime compliance layer — WASM sandbox, MCP firewall, capability manifests, verifiable rollouts, and trace-to-training export
- [Brave Search MCP](https://freemcp.space/featured/brave-search-mcp) — Brave's official MCP server — web, image, video, and news search via the Brave Search API, directly from an MCP client.
- [GitHub MCP](https://freemcp.space/featured/github-mcp) — GitHub's official MCP server — access repositories, issues, pull requests, actions, code search, and more directly from an MCP client.
- [Fetch MCP](https://freemcp.space/featured/fetch-mcp) — Fetches a URL and returns its content as clean Markdown, plain text, HTML, JSON, or readable article text — ideal for feeding web content to an LLM.
- [fal-mcp-server](https://freemcp.space/featured/fal-mcp-server) — MCP server for Fal.ai - Generate images, videos, music and audio with Claude
- [mcp-js](https://freemcp.space/featured/mcp-js) — MCP server that exposes a V8 JavaScript runtime as a tool for AI agents like Claude and Cursor. Supports persistent heap snapshots via S3 or local filesystem, and is ready for integration with modern AI development environments.
- [mermaid-mcp](https://freemcp.space/featured/mermaid-mcp) — AI-powered Mermaid diagram generation with 22+ diagram types including flowcharts, sequence diagrams, class diagrams, ER diagrams, architecture diagrams, state machines, and more. Features 50+ pre-built templates, advanced layout engines, SVG/PNG/PDF exports, and seamless integration with GitHub Copilot, Claude, and any MCP-compatible client. Install via NPM: `npm install -g @narasimhaponnada/mermaid-mcp-server`
- [Grok-MCP](https://freemcp.space/featured/grok-mcp) —     MCP server for xAI’s Grok API with Web/X search, vision, image/video generation and file support
- [mcp-server-js](https://freemcp.space/featured/mcp-server-js) — MCP server that exposes YepCode processes as callable tools for AI platforms. Securely connect AI assistants to your YepCode workflows, APIs, and automations.
- [agy-bridge](https://freemcp.space/featured/agy-bridge) — MCP bridge that lets Claude Code delegate heavy tasks to the Antigravity CLI (agy) — purpose-built tools, model routing with fallback, session continuity, and output truncation to save Claude's context and tokens.
- [openapi-to-mcp](https://freemcp.space/featured/openapi-to-mcp) — An MCP server for your API
- [colab-mcp](https://freemcp.space/featured/colab-mcp) — Fixed & enhanced fork of Google's Colab MCP — tools visible at startup, GPU control, Windows support, no more 'Disconnected'
- [netops-mcp](https://freemcp.space/featured/netops-mcp) — A comprehensive  MCP server that provides access to essential DevOps and networking tools through a standardized interface.
- [prolog-reasoner](https://freemcp.space/featured/prolog-reasoner) — SWI-Prolog as a logic calculator for LLMs — MCP server and Python library
- [Edict](https://freemcp.space/featured/edict) — A programming language designed for AI agents. No parser, no syntax — agents produce AST directly as JSON. Statically typed, effect-tracked, contract-verified, compiled to WASM via MCP.
- [agent-nexus](https://freemcp.space/featured/agent-nexus) — A service-boundary-aware document exchange center for coordinating heterogeneous LLM code agents via MCP. Implements versioned Markdown store, pub-sub notifications, and diff-aware update protocol.
- [matlab-mcp-server-python](https://freemcp.space/featured/matlab-mcp-server-py) — MCP server that connects any AI agent to MATLAB — execute code, async jobs, interactive Plotly plots, custom tools, and monitoring dashboard
- [mcp-server](https://freemcp.space/featured/mcp-server-9) — MCP server for Agent Blueprint — connect AI agents to your blueprints, business cases, and implementation plans
- [jobd](https://freemcp.space/featured/jobd) — Self-hostable GPU-aware job broker for your own machines, with native MCP/agent integration
- [5dive-mcp](https://freemcp.space/featured/5dive-mcp) — MCP (Model Context Protocol) server for 5dive. Exposes the agent-fleet CLI (tasks, agents, digest) as stdio MCP tools. MIT.
- [alderpost-mcp](https://freemcp.space/featured/alderpost-mcp-5) — 8 intelligence endpoints: domain security (VirusTotal, SPF/DKIM/DMARC), threat analysis (AbuseIPDB), company intel (People Data Labs, Hunter.io), compliance, sales, sports, property, and health data. Pay-per-call via x402 USDC on Base.
- [OpenNews MCP](https://freemcp.space/featured/opennews-mcp) — 85+ real-time news and market-data sources (Bloomberg, Reuters, CoinDesk, exchange listings, on-chain whale trades) behind one MCP API. Every article carries an AI-generated impact score and a long/short trading signal.
- [real-browser-mcp](https://freemcp.space/featured/real-browser-mcp) — MCP server + Chrome extension that gives AI agents control of your real browser with existing sessions and logins
- [mcp-gateway](https://freemcp.space/featured/mcp-gateway-3) — One endpoint in front of unlimited MCP servers and REST APIs. The agent sees a fixed ~15-tool surface however many you connect, so tool-list token cost stays flat (about 89% less on a 100-tool stack) and the savings climb as you add more. Single Rust binary.
- [odoo-claude-mcp](https://freemcp.space/featured/odoo-claude-mcp) — Self-hosted MCP server connecting Claude to Odoo 15→19 — 197+ tools, multi-tenant, Bulgaria l10n
- [MikroMCP](https://freemcp.space/featured/mikromcp) — Production-grade MCP server for MikroTik RouterOS with secure AI-native network automation.
- [outsource-mcp](https://freemcp.space/featured/outsource-mcp) — Give your AI assistant its own AI assistants.
- [PRIMS](https://freemcp.space/featured/prims) — PRIMS is a lightweight, open-source Model Context Protocol (MCP) server that lets LLM agents safely execute arbitrary Python code in a secure, throw-away sandbox.
- [srunx](https://freemcp.space/featured/srunx) — A modern Python library for SLURM workload manager integration with workflow orchestration capabilities.
- [VMware-Monitor](https://freemcp.space/featured/vmware-monitor-2) — Read-only VMware vCenter/ESXi monitoring — code-level enforced safety, zero destructive operations
- [piston-mcp](https://freemcp.space/featured/piston-mcp-2) — MCP server that allows LLMs to connect to and execute code using Piston
- [VMware-VKS](https://freemcp.space/featured/vmware-vks) — MCP Skill + CLI for vSphere with Tanzu (VKS) — Supervisor, Namespace, and TanzuKubernetesCluster lifecycle management. Requires vSphere 8.x+.
- [VMware-NSX](https://freemcp.space/featured/vmware-nsx) — VMware NSX networking management: segments, gateways, NAT, routing, IPAM — 32 MCP tools
- [VMware-NSX-Security](https://freemcp.space/featured/vmware-nsx-security) — VMware NSX DFW microsegmentation and security: distributed firewall, security groups, tags, traceflow, IDPS — MCP tools for AI agents
- [cloudcostsmcp](https://freemcp.space/featured/cloudcostsmcp) — Anchor AI FinOps to real, live cloud pricing — open source MCP server for AWS, GCP, and Azure
- [e2b-sandbox-mcp](https://freemcp.space/featured/e2b-sandbox-mcp-2) — MCP server connecting Claude Code with E2B cloud sandboxes for working on any GitHub repo
- [VMware-Storage](https://freemcp.space/featured/vmware-storage) — VMware vSphere storage management: datastores, iSCSI, vSAN. Domain-focused MCP skill with 11 tools.
- [VMware-AVI](https://freemcp.space/featured/vmware-avi) — AVI (NSX Advanced Load Balancer) management and AKO Kubernetes operations tool
- [hatchable-mcp](https://freemcp.space/featured/hatchable-mcp) — Hosted full-stack app platform. Creates a Postgres database, deploys API functions, and serves static sites from any MCP client. OAuth 2.1 + PKCE with DCR; bearer fallback. Free tier.
- [mcp-server](https://freemcp.space/featured/mcp-server-8) — A generic, modular server for implementing the Model Context Protocol (MCP). 
- [ChatSpatial](https://freemcp.space/featured/chatspatial) — MCP server for spatial transcriptomics analysis through natural language interfaces.
- [browser-use-rs](https://freemcp.space/featured/browser-use-rs) — A Rust library for browser automation via Chrome DevTools Protocol with built-in AI integration through Model Context Protocol (MCP)
- [mcp-browser-agent](https://freemcp.space/featured/mcp-browser-agent) — A Model Context Protocol (MCP) integration that provides Claude Desktop with autonomous browser automation capabilities. This agent enables Claude to interact with web content, manipulate DOM elements, execute JavaScript, and perform API requests.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
