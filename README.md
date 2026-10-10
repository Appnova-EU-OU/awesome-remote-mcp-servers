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
- [SmartDB_MCP](https://freemcp.space/featured/smartdb-mcp) — Universal database MCP server connecting to MySQL, PostgreSQL, SQL Server, MariaDB,DM8,Oracle,not only provides basic database connection such as OAuth 2.0 authentication , health checks, SQL optimization, and index health detection
- [nvim-mcp](https://freemcp.space/featured/nvim-mcp-2) — A Model Context Protocol (MCP) server that provides seamless integration with Neovim instances, enabling AI assistants to interact with your editor through connections and access diagnostic information via structured resources.
- [nvim-mcp](https://freemcp.space/featured/nvim-mcp) — MCP server that connects AI agents to your running Neovim instance via msgpack-RPC — no plugins required.
- [logisheets-mcp](https://freemcp.space/featured/logisheets-mcp) — give your AI agent a spreadsheet it can actually think in: deterministic Excel-compatible math + structured memory (blocks), real .xlsx out. Open source, self-hostable.
- [markview](https://freemcp.space/featured/markview) — Native macOS markdown preview + MCP server for Claude Code. Swift/SwiftUI, GFM, Mermaid, syntax highlighting. No Electron.
- [kivgraph](https://freemcp.space/featured/kivgraph) — A local MCP server for cross-repository semantic code intelligence in TypeScript and Go, backed by a persistent LadybugDB graph.
- [DevDocs-MCP](https://freemcp.space/featured/devdocs-mcp) — Documentation Authority for AI Agents based upon Devdocs
- [clarifyprompt-mcp](https://freemcp.space/featured/clarifyprompt-mcp-2) — Turns vague prompts into platform-optimized prompts for AI tools across image, video, voice, music, code, chat and document categories.
- [memorylens-mcp](https://freemcp.space/featured/memorylens-mcp) — MCP server for .NET memory profiling with AI-actionable code fix suggestions, powered by JetBrains dotMemory
- [LynxMCP](https://freemcp.space/featured/lynxmcp) — LynxMCP: local MCP server for the code questions grep can't answer. Call graph and blast radius, hybrid semantic + lexical code search on ONNX Runtime, library docs and PDFs as sources. No cloud, no PyTorch.
- [atest-mcp-server](https://freemcp.space/featured/atest-mcp-server) — MCP Server of API Testing
- [loopsense](https://freemcp.space/featured/loopsense) — LoopSense is an open-source MCP server that closes the feedback loop for AI coding agents — giving them real-time visibility into CI results, deployments, test outcomes, and file system changes. 
- [gptzero-mcp](https://freemcp.space/featured/gptzero-mcp) — Detect AI-generated text via the GPTZero API, with confidence scores, probability breakdowns and French and Spanish support.
- [localfig](https://freemcp.space/featured/localfig) — The Figma desktop app as an MCP server. Gives AI agents the full Figma Plugin API on your open file: read, write, tokens, components, exports, undo. Runs locally with no cloud API, no token and no quota. One command registers it with Claude Code, Cursor, VS Code, Windsurf, Cline, Gemini CLI, Codex and more. Zero dependencies.
- [mcp-server](https://freemcp.space/featured/mcp-server-23) — MCP server for Underground Cultural District — 23 tools, 218+ digital goods for AI agents. Free dev tools + paid catalog + Stripe checkout. npm: @underground-cultural-district/mcp-server
- [overseer-nvim-mcp](https://freemcp.space/featured/overseer-nvim-mcp) — MCP server giving coding agents visibility and control over overseer.nvim tasks: list, tail, run, restart, stop, dispose
- [mcp-openapi-schema-explorer](https://freemcp.space/featured/mcp-openapi-schema-e) — MCP server providing token-efficient access to OpenAPI/Swagger specs via MCP Resource Templates for client-side exploration.
- [nocodb-mcp-server](https://freemcp.space/featured/nocodb-mcp-server) — nocodb mcp server
- [altium-designer-mcp](https://freemcp.space/featured/altium-designer-mcp) — MCP server for AI-assisted management of Altium Designer component libraries
- [mcp-design-system-extractor](https://freemcp.space/featured/mcp-design-system-ex) — MCP (Model Context Protocol) server that enables AI assistants to interact with Storybook design systems. Extract component HTML, analyze styles, and help with design system adoption and refactoring.
- [aicanvas](https://freemcp.space/featured/aicanvas) — Open-core registry of animated React components, blocks, design systems, and templates. Real, editable code: install with one shadcn CLI command or let your AI agent pull it over MCP.
- [globalping-mcp-server](https://freemcp.space/featured/globalping-mcp-serve) — Remote MCP server that gives LLMs access to run network commands
- [roslyn-codelens-mcp](https://freemcp.space/featured/roslyn-codelens-mcp) — Roslyn-based MCP server giving AI agents deep semantic understanding of .NET/C# codebases — 67 tools for navigation, call graphs, diagnostics & code fixes, safe refactoring, code-quality auditing, test intelligence, DI graphs, and IL/external-assembly inspection.
- [mcp-ai-server-visual-studio](https://freemcp.space/featured/mcp-ai-server-visual) — MCP AI Server - Roslyn-powered MCP server for Visual Studio. 20 tools for AI assistants.
- [mk-qa-master](https://freemcp.space/featured/mk-qa-master) — AI 測試大師 — MCP server driving pytest / Jest / Cypress / Go / Maestro. Analyze, generate, run, advise. Web + Mobile (iOS/Android/BlueStacks).
- [metatron](https://freemcp.space/featured/metatron) — Git-native context layer for AI coding agents. Your team's real engineering decisions — patterns, pitfalls, conventions — live as reviewed markdown files in your repo; agents consult them before writing code and record what they learn. Files-first, no server required; MCP as an optional serving layer.
- [agent-tool](https://freemcp.space/featured/agent-tool) — MCP tool server for AI coding agents -- encoding-aware file tools, binary analysis, DAP debugger, SSH/SFTP, process memory, and more
- [xcode-studio-mcp](https://freemcp.space/featured/xcode-studio-mcp) — Unified MCP server for AI-assisted iOS development — build, deploy, screenshot, and interact with iOS Simulator from Claude Code, Cursor, or any MCP client
- [design-token-bridge-mcp](https://freemcp.space/featured/design-token-bridge) — MCP server that translates design tokens between platforms — Tailwind, Figma, CSS to Material 3, SwiftUI, and CSS Variables. Built for the v0 → Figma → Claude Code pipeline.
- [mcp-server](https://freemcp.space/featured/mcp-server-22) — MCP server for Jungle Grid lets agents submit, monitor, and retrieve logs from AI workloads.
- [mushi-mushi](https://freemcp.space/featured/mushi-mushi) — 🦖Know why your AI-built app broke — plain-English diagnosis + ready fix, in your editor. Open source. Sentry optional.
- [compound-mcp](https://freemcp.space/featured/compound-mcp) — OpenLookup, an MCP server from Compound Labs: eleven read-only lookups over live public data, including AI model pricing and routing, dependency maintenance and service pricing
- [arno](https://freemcp.space/julian/arno) — The IDE for agents. An MCP server: read by symbol, edit against a revision, validate with your own build, revert. Go, Java, Scala, TypeScript, Python, Rust, Ruby.
- [Cognigy Ai Mcp Management Server](https://freemcp.space/tsvetangerginovv/cognigy-ai-mcp-manag) — > Model Context Protocol server for managing Cognigy.AI virtual agents through the Management API > > This is an independent, open-source MCP server and is not affiliated with, endorsed by, or sponsored by Cognigy or NiCE. It requires your own valid Cognigy.AI account and API key, used in accordance
- [agentmail-mcp](https://freemcp.space/featured/agentmail-mcp) — Email for AI agents: create inboxes on the fly to send, receive and act on email.
- [go-mcp-mysql](https://freemcp.space/zhwt/go-mcp-mysql) — Zero burden, ready-to-use Model Context Protocol (MCP) server for interacting with MySQL and automation. No Node.js or Python environment needed.
- [codebase-context](https://freemcp.space/featured/codebase-context) — Codebase Context gives AI agents understanding of your codebase through semantic code search, team conventions, patterns, and memory, so they use fewer tokens, spend less time, and produce better, more familiar output.
- [repo-graph](https://freemcp.space/featured/repo-graph) — Structural graph memory for AI coding assistants — MCP server for codebase navigation
- [simulator-mcp-server](https://freemcp.space/featured/simulator-mcp-server) — Control iOS Simulators.
- [vercel-ai-docs-mcp](https://freemcp.space/featured/vercel-ai-docs-mcp) — A Model Context Protocol (MCP) server that provides AI-powered search and querying capabilities for the Vercel AI SDK documentation. This project enables developers to ask questions about the Vercel AI SDK and receive accurate, contextualized responses based on the official documentation.
- [mcp-server-sql-analyzer](https://freemcp.space/featured/mcp-server-sql-analy) — MCP server for SQL static analysis.
- [lightcms](https://freemcp.space/featured/lightcms) — Self-hosted CMS that works human or headless: full admin UI plus REST and MCP APIs, built-in semantic search and site chat, and content forking, versioning, diff/merge review, templates, approvals, and static page generation.
- [codewiki-mcp](https://freemcp.space/featured/codewiki-mcp-2) — MCP server for codewiki.google — search, fetch docs, and ask questions about any open-source repo
- [RestCsvMcpServer](https://freemcp.space/featured/restcsvmcpserver) — MCP Server for RestCSV, Generated using MCPGen
- [system-prompts-mcp-server](https://freemcp.space/featured/system-prompts-mcp-s) — Model Context Protocol server exposing system prompt files and summaries.
- [tnl](https://freemcp.space/featured/tnl) — Structured English contracts for AI coding agents — proposed by the agent, approved by you, saved on disk, read by every future session.
- [PatchWarden](https://freemcp.space/featured/patchwarden) — Turn your ChatGPT conversations into safe, auditable local execution. PatchWarden lets you discuss ideas and plans with ChatGPT, then hand the approved plan to local AI agents for guarded, traceable implementation—with scoped permissions, independent verification, and a complete execution record.Turn your ChatGPT conversations into safe, auditable 
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
