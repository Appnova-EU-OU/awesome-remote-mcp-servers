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
- [unitree-go2-mcp-server](https://freemcp.space/featured/unitree-go2-mcp-serv) — The Unitree Go2 MCP Server is a server built on the MCP that enables users to control the Unitree Go2 robot using natural language commands interpreted by a LLM.
- [airtable-mcp](https://freemcp.space/featured/airtable-mcp-2) — Airtable integration for AI-powered applications via Anthropic's Model Context Protocol (MCP)
- [just-mcp](https://freemcp.space/featured/just-mcp) — mcp server for just
- [pagecast](https://freemcp.space/featured/pagecast) — Record any browser page as GIF or video via MCP — powered by Playwright + ffmpeg
- [mac-monitor-mcp](https://freemcp.space/featured/mac-monitor-mcp) — Identifies resource-intensive processes on macOS and suggests performance improvements.
- [docket](https://freemcp.space/featured/docket) — Local-first, self-hostable coordination workspace for AI coding agents. Shared tasks, claims, sync and MCP integration.
- [pipepie](https://freemcp.space/featured/pipepie) — Self-hosted encrypted tunnel for webhooks, AI pipelines, and local development. End-to-end Noise encryption, pipeline tracing, web dashboard, MCP server for AI tools.
- [claude-critical-rules-mcp](https://freemcp.space/featured/claude-critical-rule-2) — MCP server for Claude AI providing automatic enforcement of critical rules - Prevents 96 documented failure patterns
- [pmpt-cli](https://freemcp.space/featured/pmpt-cli) — Record and share your AI-driven product development journey
- [devutils-mcp-server](https://freemcp.space/featured/devutils-mcp-server) — An open-source DevUtils MCP Server — a comprehensive developer utilities toolkit for the Docker MCP Catalog. It provides 36 tools across 8 categories that AI assistants can invoke directly.
- [P-Link-MCP](https://freemcp.space/featured/p-link-mcp) — x402 client implementation (x402-fetch), HTTP 402 server implementation and Model Context Protocol (MCP) for P-Link.io : pay, send and receive money with agents
- [pylon-mcp](https://freemcp.space/featured/pylon-mcp) — MCP server for Pylon AI — 10 pay-per-request APIs as AI agent tools. Powered by x402 on Base.
- [pincushion-plugin](https://freemcp.space/featured/pincushion-plugin) — Cursor marketplace plugin for Pincushion — MCP server + slash commands
- [promethic-mcp](https://freemcp.space/featured/promethic-mcp) — Hosted MCP docs and packaging for Promethic prompt library (Streamable HTTP at mcp.getpromethic.com/v1)
- [asc-mcp](https://freemcp.space/featured/asc-mcp) — MCP server for App Store Connect — check review status, read reviews, download sales reports from Claude Code, Cursor, or any AI agent. Free tier included.
- [gin-mcp](https://freemcp.space/featured/gin-mcp) — Enable MCP features for any Gin API with a line of code
- [agent-droid-bridge](https://freemcp.space/featured/agent-droid-bridge) — Agent Droid Bridge gives AI agents programmatic control over Android devices and emulators via ADB, exposed as an MCP server.
- [mcp-server-markdown](https://freemcp.space/featured/mcp-server-markdown) — MCP server for markdown — search, extract sections, list headings, find code blocks
- [jitapi](https://freemcp.space/featured/jitapi) — Just-in-Time API Orchestration for LLMs - An MCP server for dynamic API discovery and execution
- [mcp-server-scraper](https://freemcp.space/featured/mcp-server-scraper) — MCP server for web scraping — extract clean markdown, links, metadata from any URL
- [mcp-server-github-actions](https://freemcp.space/featured/mcp-server-github-ac) — MCP server for GitHub Actions — view runs, read logs, re-run jobs, trigger workflows
- [mcp-server-devutils](https://freemcp.space/featured/mcp-server-devutils) — Zero-auth MCP server with everyday developer utilities: base64, UUID, hash, JWT decode, cron, timestamps, JSON, regex
- [spring-boot-starter-swagger-mcp](https://freemcp.space/featured/spring-boot-starter) — Turn SpringDoc OpenAPI into production-ready MCP tools for Spring Boot: discovery, validation, workflows, and guardrails.
- [mcp-server-docker](https://freemcp.space/featured/mcp-server-docker) — MCP server for Docker — manage containers, images, volumes from your IDE
- [mcp-server-dns](https://freemcp.space/featured/mcp-server-dns) — MCP server for DNS — lookups, reverse DNS, WHOIS, zero auth
- [hird](https://freemcp.space/featured/hird) — A typed language for LLM agent systems on BEAM: effect-row tracking, auditable tool effects, typed actors, and OTP supervision, queryable by agents over MCP.
- [mcp-toolkit](https://freemcp.space/featured/mcp-toolkit) — 59 MCP servers for React + TypeScript automation — component scaffolding, CRUD feature factory, WCAG checks, test gen, TS enforcement, render/perf analysis, CRA→Vite migration, legacy analysis. npx-installable.
- [mcp-server-github-gist](https://freemcp.space/featured/mcp-server-github-gi) — MCP server to create, read, update, list, and search GitHub Gists from your IDE
- [mcp-server-npm-plus](https://freemcp.space/featured/mcp-server-npm-plus) — MCP server for npm - search, bundle sizes, vulnerabilities, download trends, dependency trees
- [rhizome-mcp](https://freemcp.space/featured/rhizome-mcp) — Crash-safe task tracking for AI coding agents over MCP: expiring leases, resumable attempts, version-pinned reviews. One Go binary, one SQLite file per project.
- [woodpecker-ci-mcp](https://freemcp.space/featured/woodpecker-ci-mcp) — MCP server for Woodpecker CI: read repositories, pipelines and logs, and drive builds, secrets and crons
- [vscode-tailwindshades](https://freemcp.space/featured/vscode-tailwindshade) — Tailwind CSS palettes (50–950) from any color, for Tailwind v4, v3, v2 and v1. A VS Code extension, a CLI, and an MCP server for AI agents.
- [dav-mcp](https://freemcp.space/featured/dav-mcp) — Transform AI agents into orchestrating assistants managing calendars, contacts, and tasks
- [dotpals](https://freemcp.space/featured/dotpals) — See what your coding agent actually did. A desktop pal and notch for Claude Code, Codex, Cursor, Gemini CLI and any agent: test results read from the output, faked passes caught, Claude Code sent back to fix what it broke, and an MCP server any AI tool can ask.
- [naja-scope](https://freemcp.space/featured/naja-scope) — MCP server for AI agents to explore SystemVerilog/Verilog netlists: trace connectivity, walk hierarchy, jump to source - without pasting RTL into context. Built on najaeda.
- [n8n-mcp](https://freemcp.space/featured/n8n-mcp) — Debugging-first MCP server for n8n. Tools for workflow generation, linting, per-node execution diagnosis, and driving live n8n instances. Built for AI agents.
- [gitingest-mcp](https://freemcp.space/featured/gitingest-mcp) — Convert any Git repository into a text digest of its codebase using gitingest.
- [editorconfig_mcp](https://freemcp.space/featured/editorconfig-mcp) — Formats files using .editorconfig rules so AI-generated code follows project formatting standards.
- [proton-safe-mcp](https://freemcp.space/featured/proton-safe-mcp) — Draft-only Proton Mail MCP server with attachment support and out-of-band human approval.
- [cos-codex-bridge](https://freemcp.space/featured/cos-codex-bridge) — Local MCP for Chief of Staff agents to run Codex and Claude Code CLI project sessions with scoped access and durable receipts.
- [android-mcp-server](https://freemcp.space/featured/android-mcp-server-2) — MCP server that lets AI assistants (Claude, OpenCode, VS Code) control Android devices securely via ADB
- [n8n-workflow-tester-safe](https://freemcp.space/featured/n8n-workflow-tester) — Safe MCP server + CLI for testing, inspecting, and operating n8n workflows with a constrained scope
- [stellify-mcp](https://freemcp.space/featured/stellify-mcp) — MCP server for Stellify - AI-native code generation platform
- [aso-score-mcp](https://freemcp.space/featured/aso-score-mcp) — MCP server that calculates an Agent Signal Optimization score across discovery, trust, commerce, interoperability, Google AI Search guidance, and browser-agent UX.
- [mcp-review-board](https://freemcp.space/featured/mcp-review-board) — MCP review board that lets different coding agents review each other — object → revise → pass, append-only audit trail. For Claude Code, Codex, OpenCode, Trae, ZCode.
- [portveil-mcp](https://freemcp.space/featured/portveil-mcp) — Portveil MCP server — let AI assistants manage your Portveil VPN network
- [zerodom](https://freemcp.space/featured/zerodom) — Terminal-native DOM perception layer for AppSec and AI. Hook into live Chrome sessions, compress HTML tokens by 98.9%, and map attack surfaces deterministically.
- [Precis](https://freemcp.space/featured/precis) — 🧪 Alpha — Local-first visual data quality platform. Visual DAG editor + schema-aware validation for Excel/CSV. Feedback welcome.
- [4DA](https://freemcp.space/featured/4da-2) — Privacy-first developer intelligence — surfaces what matters from the noise
- [osnova](https://freemcp.space/featured/osnova) — Deterministic code map for AI coding agents: a tree-sitter symbol and call graph served over MCP and a CLI, with no embeddings, network or telemetry.
- [mcp-keycloak](https://freemcp.space/featured/mcp-keycloak) — MCP server for Keycloak — multi-realm admin with security modes (read-only/read-write/admin) and access-control flags.
- [yandex-music-mcp](https://freemcp.space/featured/yandex-music-mcp) — Description: Unofficial Yandex Music MCP server for Claude: search, likes, history, My Wave, playlists
- [whichlib](https://freemcp.space/featured/whichlib) — The dependency picker for coding agents: an MCP server that recommends, compares and scores GitHub repos with a verdict. npx -y whichlib
- [buildtree-mcp](https://freemcp.space/featured/buildtree-mcp) — MCP server for buildtree: share Android and iOS builds with testers via install links and QR codes
- [dev-error-explainers](https://freemcp.space/featured/dev-error-explainers) — Paste a developer error, get the real cause and the fix. Offline, zero-dependency explainers for CORS, ESM/CJS, npm ERESOLVE, ChunkLoadError, Postgres/Supabase DATABASE_URL and Next.js build errors.
- [runecho](https://freemcp.space/featured/runecho) — Stops your AI coding agent from writing calls to functions that don't exist, before the edit lands. Deterministic, no LLM, no API keys.
- [json-mcp-lite](https://freemcp.space/featured/json-mcp-lite) — Turn any JSON file into an MCP server in one command: list, search and get tools for Claude Desktop, Claude Code and Cursor. MIT.
- [bitrix24-mcp](https://freemcp.space/featured/bitrix24-mcp) — MCP server for Bitrix24 CRM: deals, leads, contacts, tasks, timeline and sales analytics for Claude and Cursor
- [mcp-gtm-signals-aggregator](https://freemcp.space/featured/mcp-gtm-signals-aggr) — MCP server for GTM Signals Aggregator. Combines hiring and tech stack detection into one composite GTM score via Apify. Clay-ready output.
- [discp](https://freemcp.space/featured/discp) — The feature-complete Discord MCP Server for AI assistants (Claude, Cursor, Antigravity, OpenCode). 117 native tools, dual user/bot account support, anti-abuse human pacing, dynamic symbol search.
- [line-bot-ops-mcp](https://freemcp.space/featured/line-bot-ops-mcp) — MCP server to operate your own LINE bot: webhook queue health, failed jobs and retries, push, Rich Menu, follower insight.
- [mcp-google-gmail](https://freemcp.space/featured/mcp-google-gmail) — MCP server for the Gmail API — search, read and send email, manage drafts, labels and the trash. For Claude, Cursor, Codex and other AI clients.
- [usable-browser-agent-free](https://freemcp.space/featured/usable-browser-agent) — Usable Browser Agent, free personal/evaluation tier: an MCP server plus Firefox/Chrome extension that lets your AI agent drive your real, logged-in browser. Commercial license at savvytechsphere.com/usable-browser-agent
- [aetumi-mcp](https://freemcp.space/featured/aetumi-mcp) — AETumi MCP — install premium, production-ready Three.js/WebGL 3D web components into Claude Code, Cursor & Codex. Premium 3D web you own, from AETumi (aetumi.app).
- [3dtexel-mcp](https://freemcp.space/featured/3dtexel-mcp) — MCP server for 3D Texel: search and download 7,000+ PBR materials, HDRIs, decals and 3D assets, and generate PBR materials, HDRIs and textures from Claude, Cursor, ChatGPT and other AI agents.
- [autodesk-inventor-mcp](https://freemcp.space/featured/autodesk-inventor-mc) — Autodesk Inventor MCP server: connect Claude, Cursor or Codex to a live Inventor session (COM). Find sliver faces, test Unwrap, script the Inventor API. Zero dependencies.
- [market-pulse-mcp](https://freemcp.space/featured/market-pulse-mcp) — MCP server for T3rnel Market Pulse: evidence-graded agent-work lanes, should-I-bid advice, live agent jobs, hash-chained evidence ledger. Free without a key.
- [ios-agent-skill](https://freemcp.space/featured/ios-agent-skill) — Swift source, Apple guides and MCP tools for AI coding agents. Review iOS code, scaffold apps, and build/run/preview with Xcode Simulator. 
- [maven-mcp](https://freemcp.space/featured/maven-mcp) — Maven dependency intelligence MCP server and Claude Code / Grok Build plugin
- [Porkbun-MCP](https://freemcp.space/featured/porkbun-mcp) — Official Porkbun MCP server — exposes the Porkbun v3 API as native tools for Claude Desktop, Cursor, and other AI agents. Idempotency-safe writes, full domain lifecycle.
- [Telebrief](https://freemcp.space/featured/telebrief) — Personal digests from Telegram channels and chats: summarizes threads, extracts key points, and delivers a clean daily/weekly brief with links and context.
- [archprint](https://freemcp.space/featured/archprint) — Infers architecture rules from your TypeScript repo's real import graph, gates each on statistical evidence, and emits them into the tools you already use (ESLint, dependency-cruiser, ts-arch). Turns the boundaries your code already follows into enforcement, so architecture drift gets caught, not just documented.
- [agenthop](https://freemcp.space/featured/agenthop) — Let your AI agent talk directly to someone else's. One pairing code, end-to-end encrypted, no public IP. MCP server for Claude Code, Codex, Cursor, Gemini CLI and grok.
- [duplex](https://freemcp.space/featured/duplex) — One browser shared by a human and an AI: visual for the human, source-level for the AI
- [genomics-mcp](https://freemcp.space/featured/genomics-mcp) — Unified MCP access to genomic archives, reference databases and indexed sequencing files
- [RulesetMCP](https://freemcp.space/featured/rulesetmcp) — Weight-On-Wheels for AI: MCP server that keeps every agent grounded in your project's rules
- [ballmac-ui](https://freemcp.space/vamsiy/ballmac-ui) — Ballmac UI: accessible React + Tailwind components your AI agent can install. shadcn registry at ui.ballmac.com
- [namegender-mcp](https://freemcp.space/featured/namegender-mcp) — Model Context Protocol server for the NameGender API: gender from names, emails and usernames, with probability, sample size and source on every answer.
- [mailprobe-mcp](https://freemcp.space/featured/mailprobe-mcp) — Official Claude Code plugin and agent skill for the MailProbe MCP server: an AI assistant verifies email addresses in real time (deliverability, disposable and role-based detection). Hosted in France.
- [claude-session-relay](https://freemcp.space/spekbroodje/claude-session-relay) — Let Claude Code sessions on different machines share a board, message each other and avoid colliding git pushes. Teams, private sessions, and an MCP connector for claude.ai and Cowork.
- [cloudflare-mcp-go](https://freemcp.space/featured/cloudflare-mcp-go) — Cloudflare MCP server in Go
- [browser-buddy](https://freemcp.space/featured/browser-buddy) — Let your coding agent read your real, logged-in Chrome: MV3 extension + native host + MCP server (read_active_tab, open_and_read_url). Zero dependencies, MIT.
- [tactab](https://freemcp.space/featured/tactab) — Tactile browser control and multimodal visual vision bridge for AI agents (Cursor, Claude, etc.) via Model Context Protocol (MCP) & Chrome Extension.
- [keboola-mcp-server](https://freemcp.space/featured/keboola-mcp-server) — Model Context Protocol (MCP) Server for the Keboola Platform
- [django-orm-lens](https://freemcp.space/featured/django-orm-lens) — Django ER diagrams, N+1 detection, schema drift & migration-risk linting — in VS Code, a CLI and an MCP server. Static analysis: no database, no django.setup(). Free & MIT.
- [mcp-server-multiverse](https://freemcp.space/featured/mcp-server-multivers) — A middleware server that enables multiple isolated instances of the same MCP servers to coexist independently with unique namespaces and configurations.
- [android-mcp-server](https://freemcp.space/featured/android-mcp-server) — MCP server for controlling Android emulators via ADB — screenshots, UI interaction, logcat, and bug documentation for Claude Code
- [mdma](https://freemcp.space/featured/mdma) — Interactive documents from Markdown. Extends MD with forms, approvals, webhooks, and more — built for next gen apps
- [mcp-codebase-index](https://freemcp.space/featured/mcp-codebase-index) — 17 MCP query tools for codebase navigation — functions, classes, imports, dependency graphs, change impact. Zero dependencies. 87% token reduction.
- [user-feedback-mcp](https://freemcp.space/featured/user-feedback-mcp) — Simple MCP Server to enable a human-in-the-loop workflow in tools like Cline and Cursor.
- [mneme](https://freemcp.space/featured/mneme) — Architectural drift prevention for the agentic AI SDLC.
- [ui-annotator-mcp](https://freemcp.space/featured/ui-annotator-mcp) — MCP server that annotates any web page with hover labels — zero extensions, works in any browser
- [npm-package-docs-mcp](https://freemcp.space/featured/npm-package-docs-mcp) — A Model Context Protocol (MCP) tool that provides up-to-date documentation for npm packages directly in your IDE. This tool fetches the latest README documentation from either the package's GitHub repository or the README bundled with the npm package itself.
- [swarmia-mcp](https://freemcp.space/featured/swarmia-mcp) — A read-only local MCP server for to interact with swarmia.com
- [devplan-mcp-server](https://freemcp.space/featured/devplan-mcp-server) — MCP server for generating development plans, project roadmaps, and task breakdowns for Claude Code. Turn project ideas into paint-by-numbers implementation plans.
- [mobile-device-mcp](https://freemcp.space/featured/mobile-device-mcp) — MCP server for AI-powered mobile device control — 26 tools for screenshots, UI inspection, touch interaction, and AI visual analysis. Supports Anthropic Claude & Google Gemini.
- [ollama-handoff](https://freemcp.space/featured/ollama-handoff) — MCP server that offloads cheap work from your cloud LLM agent to a local Ollama model — summaries, drafts, extractions, first-pass reviews — at zero cloud cost.
- [git-context-mcp](https://freemcp.space/featured/git-context-mcp) — MCP server that answers why code exists - git blame, PR descriptions, and linked issues
- [mockhero](https://freemcp.space/featured/mockhero) — Synthetic test data generation: detect schemas from SQL or JSON and generate JSON, CSV or SQL data.
- [mcp-server-atlassian-jira](https://freemcp.space/featured/mcp-server-atlassian-2) — Node.js/TypeScript MCP server for Atlassian Jira. Equips AI systems (LLMs) with tools to list/get projects, search/get issues (using JQL/ID), and view dev info (commits, PRs). Connects AI capabilities directly into Jira project management and issue tracking workflows.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
