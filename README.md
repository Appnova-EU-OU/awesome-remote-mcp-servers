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
- [mcgravity](https://freemcp.space/featured/mcgravity) — Fast TUI that orchestrates AI coding tools (Claude Code, Codex, Gemini) in a plan→execute→review loop. Breaks work into atomic tasks for easier verification and course-correction.
- [fhir-mcp-server](https://freemcp.space/featured/fhir-mcp-server) — FHIR MCP Server for handling medical data standard.
- [agentmail-toolkit](https://freemcp.space/featured/agentmail-toolkit) — An MCP server to create inboxes on the fly to send, receive, and take actions on email. We aren't AI agents for email, but email for AI Agents.
- [nostr-mcp](https://freemcp.space/featured/nostr-mcp) — A Nostr MCP server that allows to interact with Nostr, enabling posting notes, and more.
- [servonaut](https://freemcp.space/featured/servonaut) — Manage AWS, Hetzner, OVH, and custom servers from one TUI — with a built-in AI assistant and MCP server
- [forge](https://freemcp.space/featured/forge-2) — Terminal MCP server for AI coding agents — spawn, manage, and monitor PTY sessions via the Model Context Protocol
- [backscroll](https://freemcp.space/featured/backscroll) — Never lose a command's output again — searchable, per-command terminal scrollback recorder
- [terminal-history-mcp](https://freemcp.space/featured/terminal-history-mcp) — Search your shell history (zsh/bash/fish) from Claude/MCP. Local SQLite FTS5. Secret-redacted.
- [localhost-mcp](https://freemcp.space/featured/localhost-mcp) — MCP server: inspect, manage, kill local dev servers. Stop guessing what's on :3000.
- [when](https://freemcp.space/featured/when) — Six tools. One install. The WhenLabs developer toolkit.
- [claude-terminal-mcp](https://freemcp.space/featured/claude-terminal-mcp) — Terminal, filesystem, and background-job tools for Claude Desktop on Linux. Zero-dependency MCP extension, MIT-licensed.
- [rootpilot-mcp](https://freemcp.space/featured/rootpilot-mcp) — MCP server for safe, read-only SSH diagnostics — bring your own LLM
- [mcp-tmux](https://freemcp.space/featured/mcp-tmux) — A comprehensive, universal MCP server for driving tmux (local and over SSH).
- [ncp](https://freemcp.space/featured/ncp) — Natural Context Provider (NCP). Your MCPs, supercharged. Find any tool instantly, load on demand, run on schedule, ready for any   client. Smart loading saves tokens and energy.
- [hop](https://freemcp.space/featured/hop) — Fast, elegant SSH connection manager with a TUI dashboard and MCP server
- [codex-mcp-tool](https://freemcp.space/featured/codex-mcp-tool) — MCP server that connects your IDE or AI assistant to Codex CLI for code analysis and editing with support for multiple models (gpt-5-codex, o3, codex-1)
- [pty-mcp](https://freemcp.space/featured/pty-mcp) — MCP server for interactive terminal sessions — local shells, SSH, serial ports, and   persistent remote sessions
- [tui-mcp](https://freemcp.space/featured/tui-mcp) — What Chrome DevTools MCP is for the browser, tui-mcp is for the terminal. Launch, screenshot, and interact with any TUI app.
- [infrabroker](https://freemcp.space/featured/infrabroker) — Infrastructure access broker for AI agents — SSH & Kubernetes. Per-operation ephemeral credentials minted by a separate signer; the model never touches one. MCP stdio / HTTP+OIDC.
- [mcp-remote-ssh](https://freemcp.space/featured/mcp-remote-ssh) — MCP server for remote SSH operations -- persistent sessions, structured command output, SFTP file transfer, port forwarding, and secret-safe environment variable injection with automatic output redaction.
- [sysknife](https://freemcp.space/featured/sysknife) — Your sysadmin co-pilot — an AI that administers Linux through typed, approval-gated, Ed25519-audited actions instead of shell strings. Reference implementation of the LACS standard.
- [cygnus-ssh-mcp](https://freemcp.space/featured/cygnus-ssh-mcp) — MCP server for SSH remote server management
- [trinity-lite](https://freemcp.space/featured/trinity-lite) — Local AgentOps for cross-vendor CLI coding agents: route work, recover state, and accept only with evidence.
- [copilot-mcp-server](https://freemcp.space/featured/copilot-mcp-server) — MCP server for GitHub Copilot CLI integration
- [mcp-linux-tools](https://freemcp.space/featured/mcp-linux-tools) — A MCP server to manage linux, websites and database
- [taskbounty-mcp-server](https://freemcp.space/featured/taskbounty-mcp-serve) — MCP server for TaskBounty. Post AI-fixable bug bounties or pick them up. Funded in USD via Stripe, paid in USDC, ETH, or BTC.
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
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
