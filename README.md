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
- [reaper-daemon](https://freemcp.space/featured/reaper-daemon) — Free, open source REAPER MCP server that lets an AI agent (Claude or any MCP client) drive REAPER: read every plugin and parameter, set FX values, write automation, and measure a mix move before and after. MIT. macOS, Windows, Linux.
- [vibatchium](https://freemcp.space/featured/vibatchium) — Stealth browser automation for AI agents — unattended, headless, N parallel persistent logged-in Chromes. One MCP server + CLI, credential vault with TOTP/IMAP 2FA, vision clicking, prompt-injection scanning. Self-hosted, real Chrome. 1,250 tests.
- [hermes-action-bridge](https://freemcp.space/featured/hermes-action-bridge) — Configurable bridge for external agents to delegate actions to Hermes Agent via CLI or MCP.
- [Contradiction-MCP](https://freemcp.space/featured/contradiction-mcp) — Autonomous Model Context Protocol (MCP) engine for factual consistency, version reconciliation, and conflict resolution across engineering knowledge bases.
- [chrome-bridge](https://freemcp.space/featured/chrome-bridge) — Your real, logged-in Chrome as an MCP server for Claude Code: 59 token-efficient web-dev tools, a skill with recipes, a zero-token CLI. ChromeOS included.
- [revit-model-mcp](https://freemcp.space/featured/revit-model-mcp) — MCP server for live Autodesk Revit models: query, aggregate and inspect by default, act only behind opt-in gates
- [mcp-hub](https://freemcp.space/featured/mcp-hub) — Serve multiple stdio MCP servers from one container: path routing, hub meta-tools, OAuth 2.1 + API tokens for ChatGPT, Claude, Cursor and other MCP clients
- [hicortex](https://freemcp.space/featured/hicortex) — Self-learning memory for AI agents — experience captured automatically, distilled into lessons overnight, shared across your whole fleet. Works with Hermes, OpenClaw, Claude Code, and Pi.
- [sandbox-as-a-service-mcp](https://freemcp.space/featured/sandbox-as-a-service) — MCP server for Sandbox as a Service: give an agent a real Linux VM — run commands, move files, expose a preview URL, destroy it.
- [mcp-oci](https://freemcp.space/featured/mcp-oci) — MCP server for Oracle Cloud (OCI) — live resource discovery, dependency mapping, and Terraform generation, with security modes and access-control flags.
- [cute-web-scraper](https://freemcp.space/featured/cute-web-scraper) — A free, local MCP server that gives Claude web scraping powers. 24 tools, four escalating fetch tiers, no API key.
- [evipedia-mcp](https://freemcp.space/featured/evipedia-mcp) — MCP Server for evipedia.ai
- [mcp-server](https://freemcp.space/featured/mcp-server-17) — MCP server for Tribeunal — 39 tools and 8 Agent Skills that put humans and AI agents on the same jury
- [plopino-mcp](https://freemcp.space/featured/plopino-mcp) — MCP server for Plopino — lets an AI agent publish a page, a file, or a folder and hand back a public link.
- [shiped-mcp](https://freemcp.space/featured/shiped-mcp) — Deploy AI-generated HTML/CSS/JS to an instant public HTTPS URL from any MCP agent (Claude Code, Codex, Cursor, Kiro, Copilot). Remote HTTP MCP endpoint with OAuth 2.1 device-flow login — no API key to mint or store.
- [superglookoquery](https://freemcp.space/featured/superglookoquery) — MCP server exposing Glooko diabetes device data (any pump/CGM combination) for clinical audit, with device-agnostic capability discovery. Forked from podquery-mcp.
- [architecture_viewer](https://freemcp.space/featured/architecture-viewer) — AI coding session architecture gate — local MCP (av_guard) + CLI diffs vs git HEAD for cross-layer deps. Apache-2.0.
- [scenef-mcp](https://freemcp.space/featured/scenef-mcp) — SceneF MCP server — verified California and Hawaii movie showtimes, every operating cinema in the covered states, checked twice daily. Remote, no key: https://scenef.com/mcp
- [opticquiz-mcp](https://freemcp.space/featured/opticquiz-mcp) — Two MCP servers for color-vision accessibility: check whether a palette or image is colorblind-safe, and see it recolored as protan/deutan/tritan. Machado 2009 + CIEDE2000, published method. Local stdio.
- [ergonia](https://freemcp.space/featured/ergonia) — Ergonia Works: verifiable work for AI agents. Work isn't done because an agent says so, it's done when anyone can verify it. Every task carries an acceptance condition a stranger can execute.
- [macaroonnetwork-mcp](https://freemcp.space/featured/macaroonnetwork-mcp) — MCP client for Macaroon Network -- discover and buy from a live marketplace where AI agents pay per query via Bitcoin Lightning (L402) or Base/USDC (x402).
- [neon-mcp-gateway](https://freemcp.space/featured/neon-mcp-gateway) — Enterprise Zero-Trust security gateway, token rate-limiter, and secure SSE proxy for Model Context Protocol (MCP) servers.
- [BotHireMCPServer](https://freemcp.space/featured/bothiremcpserver) — MCP server for BotHire — the machine-to-machine labor market where AI agents hire each other and pay agent-to-agent in USDT/USDC (x402, gasless, multi-chain: Base, Arbitrum, BNB, Solana) with ownerless on-chain escrow. Read-only discovery tools: search skills/agents, market stats, hire guide.
- [moltline-mcp](https://freemcp.space/featured/moltline-mcp) — Zero-dependency stdio bridge for the Moltline Studio MCP fleet - 19 hosted streamable-HTTP servers, 132 tools, 92 of them free with no signup.
- [veilbrowser](https://freemcp.space/featured/veilbrowser) — Stealth browser for AI agents — real Chrome over raw CDP, no Playwright/Puppeteer. TypeScript + MCP-native. Passes sannysoft 57/57, bypasses Cloudflare.
- [viber-mcp](https://freemcp.space/featured/viber-mcp) — MCP server for Viber messenger (Rakuten Viber Bot API) — TypeScript
- [ictpbx-mcp](https://freemcp.space/featured/ictpbx-mcp) — Read-only MCP server for ICTPBX — extensions, DIDs, SIP trunks, tenants and PBX statistics over ICTCore REST. By ICT Innovations.
- [komnet](https://freemcp.space/featured/komnet) — Git-backed message bus for AI coding agents — Claude Code, Cursor and Codex coordinate asynchronously, with no server
- [ntfy-mcp](https://freemcp.space/featured/ntfy-mcp-2) — MCP server for ntfy: publish notifications, read cached messages, manage users and topic access
- [smtp-mcp](https://freemcp.space/featured/smtp-mcp) — MCP server that sends mail over SMTP, gated behind an allowlist and a human confirmation
- [munim](https://freemcp.space/featured/munim) — A multi-account MCP server for people who look after other people's infrastructure. Built with the Strands Agents SDK.
- [portkey-admin-mcp](https://freemcp.space/featured/portkey-admin-mcp-2) — Portkey Admin API control-plane MCP server with Prisma AIRS interoperability guidance
- [jgs-magic-sysmlv1-mcp](https://freemcp.space/featured/jgs-magic-sysmlv1-mc) — Bring Claude Code and any MCP agent to your live SysML v1 models in CATIA Magic: 130+ tools to query, audit, and edit the real model over a local, air-gapped connection. No cloud, no export. FREE / PRO / ENTERPRISE.
- [magents](https://freemcp.space/featured/magents) — Shared session bus for Claude Code, Codex, and Cursor
- [AnkusDrive](https://freemcp.space/gchen19/ankusdrive) — CLI + MCP server that turns FreeCAD into a mechanical-design workbench for LLM agents — parametric CAD, drawings, FEM/CFD simulation, and manufacturing checks
- [drop2run-cli](https://freemcp.space/featured/drop2run-cli) — Source for the drop2run CLI and MCP server — publish a static site or an agent's output to an HTTPS link, no git and no build config.
- [elicitly](https://freemcp.space/featured/elicitly) — Elicitly Free Edition — human-in-the-loop for prompts and Agent Skills over MCP elicitation. Local MCP server (npx -y elicitly) + embeddable toolkit (@elicitly/tools).
- [K8s-AIops](https://freemcp.space/featured/k8s-aiops) — Standalone governed Kubernetes ops — 15 MCP tools with built-in audit/budget/undo/risk-tier harness
- [ottersnap-mcp](https://freemcp.space/featured/ottersnap-mcp) — MCP server for the OtterSnap rendering API — screenshots, PDFs, OG images and page extraction for AI agents.
- [svipall](https://freemcp.space/featured/svipall) — Local-first MCP server and CLI in Rust: any page as LLM-ready Markdown, whole-site crawls, keyless search, and local captcha solving. No cloud, no API keys.
- [x402-scraper-engine](https://freemcp.space/featured/x402-scraper-engine) — HTTP 402 pay-per-call web scraper & Llama-3 digest engine for autonomous AI agents on Base L2. No API keys, no subscriptions.
- [vitamind-mcp](https://freemcp.space/featured/vitamind-mcp) — MCP server for solar vitamin D — when the sun where you are can actually make vitamin D, for your skin type. Bridges any stdio MCP client to the hosted Vitamin D Explorer server.
- [nightmarquee-mcp](https://freemcp.space/antdevlab/nightmarquee-mcp) — Cinematic website prompts with live previews, inside your editor. MCP server for Claude Code, Claude Desktop and Cursor.
- [mcp-server](https://freemcp.space/featured/mcp-server-16) — MCP server for cogDepot, the anonymous broker where AI agents publish capabilities, negotiate, and form direct peer-to-peer deals. Keyless discovery, or the full trading loop with a key - post, browse, negotiate, seal, rate. Local via npx or the hosted remote server.
- [browser-mcp](https://freemcp.space/featured/browser-mcp) — Drive your real, logged-in Chrome from any AI agent (Claude Code, Codex, Cursor, VS Code) — works where headless dies. Reads emailed login codes from your Gmail, 40 tools, up to 20 concurrent sessions. MIT, local-only.
- [caldav-mcp](https://freemcp.space/featured/caldav-mcp-3) — MCP server for CalDAV calendars: events, tasks and journals over the open standard
- [carddav-mcp](https://freemcp.space/featured/carddav-mcp) — Model Context Protocol (MCP) server for CardDAV address books: contacts, groups and photos
- [engagelab-email-mcp](https://freemcp.space/featured/engagelab-email-mcp) — Official EngageLab Agent Email MCP server for AI agents to send, receive, monitor, and reply to email
- [mailflat-sdks](https://freemcp.space/featured/mailflat-sdks) — Official MailFlat SDKs for Python, TypeScript/JavaScript and Java. Real email inboxes your agent or test suite can create from code and read one-time codes from.
- [outlook-mcp](https://freemcp.space/featured/outlook-mcp-2) — MCP server for tidying a large Outlook / Hotmail mailbox via Microsoft Graph. Bulk moves, folder-tree surgery, inbox rules — no send tool, no permanent delete.
- [b2-mcp](https://freemcp.space/featured/b2-mcp) — MCP server for Backblaze B2 Cloud Storage: a focused, safe 40-tool surface (17 native B2 SDK, 19 S3 data-plane, 4 analytics) for any MCP-compatible AI client, currently incubating in Backblaze-Labs
- [x402-list-mcp](https://freemcp.space/featured/x402-list-mcp) — MCP server for x402-list.com: discover x402 payment services and on-chain-verified facilitator settlement volumes. Published on npm as x402-list-mcp.
- [pbx-mcp](https://freemcp.space/featured/pbx-mcp) — MCP server for Asterisk and FreeSWITCH. Lets AI assistants inspect channels, SIP registrations, trunk status and dialplan on a live PBX.
- [meet-live-assist-extension](https://freemcp.space/featured/meet-live-assist-ext) — Your own AI agent, live in a Google Meet or Zoom call: reads the captions, answers in a side panel, runs entirely on your machine over MCP.
- [fmsg-mcp](https://freemcp.space/featured/fmsg-mcp) — MCP server for fmsg: send and receive federated messages from any AI agent via a deployed fmsg Web API
- [agent-identity-mcp](https://freemcp.space/flovoice53/agent-identity-mcp) — MCP server that gives an AI agent a disposable email address and a real UK phone number to test signup/verification flows end to end
- [giggal-mcp](https://freemcp.space/featured/giggal-mcp) — Official MCP server for Giggal.ai: catch-all, accept-all, and SEG-protected email verification for Claude, ChatGPT, Cursor, and other MCP clients.
- [sms-florin-mcp](https://freemcp.space/flovoice53/sms-florin-mcp) — MCP server for sms-florin — rent a real UK phone number and receive SMS/OTP codes from AI coding agents (Claude, Cursor, Codex...)
- [aginxbrowser](https://freemcp.space/featured/aginxbrowser) — The browser built for AI agents — fetch live pages as markdown, render JS/SPAs with built-in V8, take screenshots without Chromium, meta-search 5 engines, and drive interactive login sessions. One Rust binary, stealth TLS fingerprints, MCP native for Claude Code & Cursor. Headless browser alternative to Puppeteer/Playwright.
- [domain-mcp](https://freemcp.space/featured/domain-mcp) — Manage Dynadot domains, DNS, renewals, and transfers from Claude, Cursor, or any MCP client.
- [Agent402](https://freemcp.space/featured/agent402) — agent402.tools: 500+ pay-per-call tools, metered models and finished reports for AI agents, paid per call in USDC over x402 and MPP or by card. Open source, self-hostable, MCP-native. The applied layer of agentic finance.
- [MCPEmails](https://freemcp.space/asgeiralbretsen/mcpemails) — Give your AI agent an inbox. Hosted remote MCP server: connect Gmail or any IMAP mailbox (Fastmail, iCloud, Yahoo, Zoho) and read, search, send, organize, schedule and auto-triage email from Claude, ChatGPT, Cursor or any MCP client. OAuth sign-in, per-key permission scopes, mail fetched live and never stored. Nothing to install or deploy. Setup guides: https://mcpemails.com/docs
- [gemini-antigravity-bridge](https://freemcp.space/nandhakumar-murugan/gemini-antigravity-b) — ⚡ Bridge connecting Google Gemini Spark & Cloud AI to your local machine via MCP with autonomous file creation, terminal execution, and subagent orchestration.
- [gigamail](https://freemcp.space/featured/gigamail) — Mail for AI agents ( and humans). MCP server giving Claude (or any agent) safe, permission-controlled access to email (Microsoft Graph + IMAP), calendar and your knowledge files. Two-phase confirmation for sends, audit log, local index. No built-in LLM: your agent brings the intelligence.
- [ssh-mcp-server](https://freemcp.space/featured/ssh-mcp-server-2) — SSH MCP server for AI agents: remote commands, file transfer, log search and server audits through OpenSSH.
- [SmartCLI](https://freemcp.space/featured/smartcli) — Three Agent Skills over one pluggable PTY + pyte core: drive TUIs, design terminal effects, and render cell-accurate UIs. pip install smartcli-toolkit
- [markdown-to-whatsapp](https://freemcp.space/featured/markdown-to-whatsapp) — Convert Markdown into WhatsApp formatting: tables drawn to fit the phone's monospace width. Web page, library, CLI and MCP server.
- [clawdcall-mcp](https://freemcp.space/dialgoodian/clawdcall-mcp) — Let AI agents place consent-based outbound phone calls and retrieve transcripts, summaries, and outcomes. Use the hosted Streamable HTTP server or install with `npx -y clawdcall-mcp`.
- [sendgrid-mcp-secure](https://freemcp.space/featured/sendgrid-mcp-secure) — Security-first MCP server for SendGrid — recipient allowlists, send caps, review-mode, audit log, no silent BCC. Hardened against the postmark-mcp incident class.
- [heliograph](https://freemcp.space/featured/heliograph) — Remote, captured, auditable execution on a machine you cannot log into. Control CLI, relay and transports around the heliograph method.
- [public-browser](https://freemcp.space/featured/public-browser) — Lets Claude Code and Cursor drive Chrome. Browse your real profile: -30% tokens, -25% cost, -41% tool calls, -34% tool defs, +40% faster. Direct CDP, a11y-tree refs, server-side plan executor. MIT, no paid tier.
- [claude-codex-bridge](https://freemcp.space/featured/claude-codex-bridge) — Use Codex agents from Claude Code with live progress, steering, and session continuation.
- [Nimbus](https://freemcp.space/featured/nimbus) — On-call intelligence for DevOps and platform teams. Local-first AI agent over your tools — HITL-gated, MCP-native, AGPL-3.0.
- [cursor-delegate-mcp](https://freemcp.space/featured/cursor-delegate-mcp) —  Stop burning your Claude or Codex limits on boilerplate. Delegate multi-file implementation to Cursor's Composer 2.5 over MCP — your frontier model writes the brief and reviews the diff; Composer does the typing, fast, on a separate quota.
- [unclick](https://freemcp.space/featured/unclick) — The universal remote for AI: one MCP install gives agents 450+ callable endpoints across 60+ integrations, plus persistent cross-session memory. Works with Claude, ChatGPT, Cursor, and any MCP client.
- [allmcps-server](https://freemcp.space/featured/allmcps-server) — Official MCP server for AllMCPs.com — submit MCP servers to the directory directly from your AI agent.
- [relayer-mcp](https://freemcp.space/featured/relayer-mcp) — MCP server for XNS S3-compatible storage — agent-driven Relayer install & management. Mirrored from GitLab.
- [mcp-server-vibes-coded](https://freemcp.space/featured/mcp-server-vibes-cod) — 26-tool MCP server for agent security, scanner consensus, x402 reliability, and Vibes-Coded's 344-resource commerce catalog.
- [LiuHe](https://freemcp.space/featured/liuhe) — LLM-native code toolkit: Rust multi-language parser (tree-sitter) + 44 MCP tools for atomic editing, impact analysis, reference tracing and deterministic zero-LLM code quality gates. Built for the handless, eyeless, memoryless LLM.
- [synapse-mcp](https://freemcp.space/featured/synapse-mcp) — Free, 100% local MCP server. Turns your codebase into an AST knowledge graph so AI coding agents (Claude, Cursor, Copilot) get exact caller trees, semantic search, and safe writes — 60% fewer tokens, zero data egress.
- [dochost-mcp](https://freemcp.space/featured/dochost-mcp) — Official MCP server for dochost (https://dochost.io) — publish Markdown or HTML to a shareable link from Claude, ChatGPT or Cursor. OAuth, no API keys.
- [mcp-azure](https://freemcp.space/featured/mcp-azure) — MCP server for Azure (Resource Manager) — inventory, tags, VM power, lifecycle — with governance controls (scoping, protected groups, location allowlist, delete gating, confirmation).
- [snapshot-site-mcp](https://freemcp.space/featured/snapshot-site-mcp) — Let Claude, ChatGPT, and other MCP clients capture, compare, and analyze any web page — hosted with OAuth, or local over stdio.
- [awarse-mcp](https://freemcp.space/featured/awarse-mcp) — Model Context Protocol (MCP) server for automated test heal, Playwright orchestration, and AI-assisted QA workflows.
- [traecnclaw-mcp-skill](https://freemcp.space/featured/traecnclaw-mcp-skill) — Public TRAECNclaw MCP Agent Skill and installable server package bundle.
- [opticparse-public](https://freemcp.space/featured/opticparse-public) — Stealth Multimodal Web Scraper & 0-Day Phishing Shield for AI Agents. Alternative to Firecrawl & Crawl4AI with zero-CSS vision extraction, 200 free trial credits, and native LangChain / ElizaOS / MCP support.
- [repo-cartographer](https://freemcp.space/featured/repo-cartographer) — Understand any codebase in 60 seconds - an MCP server, CLI and GitHub Action that turns any repo into an architecture diagram (Mermaid/Graphviz) and enforces architecture rules in CI. Works with Claude, Cursor, ChatGPT and any MCP client.
- [picoberry-mcp](https://freemcp.space/featured/picoberry-mcp) — PicoBerry MCP server — an AI 3D workspace for games, VR, and beyond. Generate, remesh, texture, and animate 3D assets from any MCP client. Multi-engine, one API.
- [lambdacad-mcp](https://freemcp.space/featured/lambdacad-mcp) — λ MCP server for any AutoLISP-capable CAD — AI drafting with 105 tools, 2D + 3D solids, STL export. BricsCAD® on Linux is the reference adapter. No COM, no SDK.
- [bridgenode-mcp](https://freemcp.space/featured/bridgenode-mcp) — BridgeNode — x402 pay-per-request AI inference. MCP server for AI agents.
- [minia2a-mcp](https://freemcp.space/featured/minia2a-mcp) — Remote MCP server for minia2a.uk — 1,680+ x402 pay-per-call agent tools. USDC on Base, 5 free trial calls per wallet.
- [k8s-mcp-server](https://freemcp.space/featured/k8s-mcp-server) — Model Context Protocol (MCP) server for debugging, analyzing, and diagnosing Kubernetes clusters directly from AI agents.
- [stacktree-mcp](https://freemcp.space/featured/stacktree-mcp) — MCP server for stacktr.ee — publish HTML privately from any AI agent (Claude Code, Codex, Cursor, Claude.ai). Seven tool calls for unguessable, replace-in-place URLs.
- [eqvps-mcp](https://freemcp.space/eqvps/eqvps-mcp) — Crypto-native VPS that AI agents rent and pay for autonomously via MCP — no KYC
- [krova-node](https://freemcp.space/featured/krova-node) — Monorepo for the Krova Cloud JS/TS packages — SDK, CLI, MCP, webhook verifier, n8n node.
- [noodle-mcp](https://freemcp.space/featured/noodle-mcp) — Noodle Biomedical Literature Discovery MCP — search papers and traverse citation or semantic literature graphs.
- [identityforge-mcp](https://freemcp.space/featured/identityforge-mcp) — Design systems, brand naming, and domain research for coding agents through MCP and CLI.
- [mcp-imslp](https://freemcp.space/featured/mcp-imslp) — MCP server for IMSLP, the Petrucci Music Library. Read works, scores and recordings. No API key required.
- [mcp-lrclib](https://freemcp.space/featured/mcp-lrclib) — MCP server for LRCLIB: search tracks and fetch plain or time-synced (LRC) lyrics. No API key.
- [runcomfy-mcp](https://freemcp.space/featured/runcomfy-mcp) — Remote MCP for RunComfy: ComfyUI deployments, hosted models, LoRA training. 31 tools.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
