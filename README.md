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
- [fixgraph-mcp](https://freemcp.space/featured/fixgraph-mcp) — Search and contribute to a community-verified knowledge base of engineering issues and fixes, with trust scores and fix verification.
- [onlinecybertools-mcp-server](https://freemcp.space/featured/onlinecybertools-mcp) — MCP stdio server for onlinecybertools.com API
- [readystack-mcp](https://freemcp.space/featured/readystack-mcp) — 45 regulation-and-deadline linters that run as MCP servers (npx @readystack/<name> --mcp) - CRA/CSAF, PCI DSS 6.4.3, WCAG 2.1 AA, DORA, NIS2, EU AI Act, KSeF, NF-e
- [mcp-factory](https://freemcp.space/featured/mcp-factory) — Manifest-driven engine that scaffolds MCP servers from one mcp.yaml, plus a runtime hub serving tools from every registered bot through a single endpoint.
- [Nexus-MCP](https://freemcp.space/featured/nexus-mcp) — Unified MCP server: hybrid search + code graph + semantic memory. 10 tools, <350MB RAM, fully local. No API keys.
- [google-health-mcp](https://freemcp.space/featured/google-health-mcp) — Local-first MCP server for Google Health API v4 (Fitbit + Pixel Watch) — Claude/Cursor/Hermes
- [mcp-server-atlassian-confluence](https://freemcp.space/featured/mcp-server-atlassian) — Node.js/TypeScript MCP server for Atlassian Confluence. Provides tools enabling AI systems (LLMs) to list/get spaces & pages (content formatted as Markdown) and search via CQL. Connects AI seamlessly to Confluence knowledge bases using the standard MCP interface.
- [mcp-superset](https://freemcp.space/featured/mcp-superset) — MCP server for managing Apache Superset — 128+ tools for dashboards, charts, datasets, SQL Lab, access control
- [dati](https://freemcp.space/featured/dati) — Turn your database into secure, semantically rich MCP tools for agents.
- [adx-mcp-server](https://freemcp.space/featured/adx-mcp-server-2) — A Model Context Protocol (MCP) server that enables AI assistants to query and analyze Azure Data Explorer databases through standardized interfaces.
- [bruno-mcp](https://freemcp.space/featured/bruno-mcp) — MCP Server for running Bruno Collections
- [insforge-mcp](https://freemcp.space/featured/insforge-mcp) — Backend-as-a-service for agents building full-stack apps: auth, PostgreSQL database, storage and functions.
- [mcp-image-compression](https://freemcp.space/featured/mcp-image-compressio) — A high-performance image compression microservice based on MCP (Modal Context Protocol)
- [ThumbGate](https://freemcp.space/featured/thumbgate) — ThumbGate Pre-Action Checks self-improve from ranked lessons and repeated failures, hard-block detected secret leaks, and block matches in strict mode.
- [mcp-zuul](https://freemcp.space/featured/mcp-zuul) — MCP server for Zuul CI - debug build failures, search logs, manage pipelines, and monitor jobs from Claude, Cursor, or any MCP client
- [adb-mcp](https://freemcp.space/featured/adb-mcp) — MCP server for Android — drive emulators and real devices over adb from Claude Code, Cursor, or VS Code. 73 tools: screenshots, UI hierarchy, tap/swipe/type, logcat, device locks, Gradle builds and tests. The Android counterpart to XcodeBuildMCP.
- [podium-mcp](https://freemcp.space/featured/podium-mcp) — One MCP server, 51 tools for AI agents on mobile + canvas UIs: iOS & Android automation, Maestro E2E, evidenced assertions, React Native/Metro debugging — plus a no-vision canvas/WebGL brain (Pixi/Konva/Fabric/Phaser/Three/Babylon) that drives game UIs like DOM elements, ~5x cheaper than screenshot loops.
- [media-mcp](https://freemcp.space/featured/media-mcp) — Local image and video processing: resize, convert, compress, crop, thumbnails, metadata extraction, rotate, flip, filters and ffmpeg-based video operations.
- [cubelife](https://freemcp.space/featured/cubelife) — Give your AI agent a persistent pixel-art character. Node SDK, Python SDK, CLI, and MCP server.
- [homespun](https://freemcp.space/featured/homespun) — Homespun: apps your AI builds and hosts. Client CLI, MCP server, SDK core, agent skill and Claude plugin. MIT.
- [sonar-mcp-server](https://freemcp.space/featured/sonar-mcp-server) — Read-only MCP server for self-hosted SonarQube Community Build 26.4+: lets AI agents (Claude Code, Cursor, Copilot) read issues, security hotspots, rules and code snippets to fix findings locally
- [codesentinel](https://freemcp.space/featured/codesentinel) — AI-Powered Codebase Health Agent for Slack — dead code, circular deps, coupling, architectural drift
- [open-task-relay-public](https://freemcp.space/featured/open-task-relay-publ) — Open-source task commons where AI agents do bounded public-good work, publish evidence, and review results.
- [react-analyzer-mcp](https://freemcp.space/featured/react-analyzer-mcp) — MCP server for analyzing & generating docs for React code locally
- [icloud-mcp](https://freemcp.space/featured/icloud-mcp-2) — MCP server for Apple services — Mail, Calendar, Contacts, Reminders, Notes, Messages, Safari — via AppleScript (local) or iCloud IMAP/CalDAV/CardDAV (cloud)
- [buildkite-mcp-server](https://freemcp.space/featured/buildkite-mcp-server) — Official MCP Server for Buildkite.
- [icon-composer-mcp](https://freemcp.space/featured/icon-composer-mcp) — Apple Icon Composer CLI & MCP server: create and manipulate .icon bundles and images with Liquid Glass rendering
- [agentmako](https://freemcp.space/featured/agentmako) — Local-first MCP server that gives coding agents structured context packets, code/schema facts, and diagnostics - backed by a local SQLite store.
- [credit-optimizer-v5](https://freemcp.space/featured/credit-optimizer-v5) — Save 47% on Manus AI credits automatically. Zero downsides. Pays for itself in ~27 prompts. Free MCP Server (PyPI) + $12 Manus Skill bundle with Fast Navigation (115x speed boost).
- [postmancer](https://freemcp.space/featured/postmancer) — An experimental MCP server Rest Client intended to be a replacement of tools postman & insomnia
- [higress-ops-mcp-server](https://freemcp.space/featured/higress-ops-mcp-serv) — A Model Context Protocol (MCP) server implementation that enables comprehensive configuration and management of Higress.
- [firefly-mcp](https://freemcp.space/featured/firefly-mcp) — Firefly MCP
- [unified-diff-mcp](https://freemcp.space/featured/unified-diff-mcp) — Generate and visualize unified diffs as HTML or PNG, with side-by-side and line-by-line views for filesystem dry runs.
- [mcp-gitlab-jira](https://freemcp.space/featured/mcp-gitlab-jira) — GitLab and Jira: manage projects, merge requests, files, releases and tickets.
- [gavel](https://freemcp.space/featured/gavel) — Code quality platform for Bazel monorepos — static analyzers as aspects, SARIF, quality gates
- [stacksfinder-mcp](https://freemcp.space/featured/stacksfinder-mcp) — MCP server for StacksFinder - deterministic tech stack recommendations for LLM clients
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
