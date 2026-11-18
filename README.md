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
- [Handmade](https://freemcp.space/hhiramkarogo/handmade) — **Build AI-generated interfaces that look intentionally engineered, not generated.**
- [handmade](https://freemcp.space/featured/handmade) — Handmade is a Model Context Protocol (MCP) server tailored to eliminate generic AI output by enforcing comprehensive prompt coverage and proactively clarifying ambiguities before generation.
- [m4r-data](https://freemcp.space/featured/m4r-data) — Structured data from Music For Robots — music composed for machines, reviewed by AI critics
- [gpt-image-studio](https://freemcp.space/featured/gpt-image-studio) — Let your AI agent generate images with OpenAI gpt-image-2.5 or any OpenAI-compatible relay — live web gallery, cost tracking, MCP, 5 languages
- [spotify-data-mcp](https://freemcp.space/featured/spotify-data-mcp) — MCP server for Spotify data: play counts, monthly listeners, charts, artist stats, playlists and ISRC lookup for Claude, Cursor and VS Code
- [bayze-mcp](https://freemcp.space/featured/bayze-mcp) — Local-first AI model-routing core: waterfall workflows with structured cross-vendor review (draft → review → revise). BYOK or unified API. MCP stdio. npm: bayze-mcp
- [kitden](https://freemcp.space/featured/kitden) — See the MCP servers, plugins and skills Claude Code, Codex and Cursor load, and which skills got cut
- [mcp-b2b-prospect-engine](https://freemcp.space/featured/mcp-b2b-prospect-eng) — MCP server for the Mamba Labs Prospect Engine actor on Apify
- [verify-atom](https://freemcp.space/featured/verify-atom) — Give AI agents cryptographically signed proof of web observations: Ed25519-signed proof packets (HTTP status, page title, body SHA-256, DNS, TLS) for any public URL. Install: `uvx verify-atom-mcp`.
- [dagon-mcp](https://freemcp.space/featured/dagon-mcp) — MCP server for Dagon Inference: uncensored LLMs, pay with Solana USDC
- [multi-mail-mcp](https://freemcp.space/featured/multi-mail-mcp) — MCP server for searching, reading and writing mail across several Gmail accounts (Claude Desktop, Claude Code, ChatGPT)
- [xonta-max-mcp](https://freemcp.space/featured/xonta-max-mcp) — MCP server for building bots and mini-apps for the MAX messenger (max.ru): current Bot API facts, code checks, Telegram migration hints, bot templates, deep links, ad tracking and test fixtures. English and Russian.
- [proton-mail-mcp](https://freemcp.space/featured/proton-mail-mcp-2) — Unofficial MCP server for Proton Mail Bridge: search and read mail, write drafts, guarded cleanup. Not affiliated with Proton AG.
- [whatsapp-messaging-api-mcp](https://freemcp.space/jevil257/whatsapp-messaging-a) — Send WhatsApp messages from Claude and any MCP client. No Meta Business approval or WhatsApp Business account.
- [discord-management-mcp](https://freemcp.space/featured/discord-management-m) — Safe-by-default Discord management MCP server with JSON backups, restore planning and guarded mutations
- [hellohop-mcp](https://freemcp.space/socialground/hellohop-mcp) — MCP server for the HelloHop WhatsApp API. Read chats, groups and communities from Claude, Cursor or any MCP client.
- [blueticks-mcp](https://freemcp.space/featured/blueticks-mcp) — Blueticks MCP server for Claude Desktop / Cursor / Cline
- [gmail-tidy-mcp](https://freemcp.space/featured/gmail-tidy-mcp) — MCP server that reads and organizes several Gmail accounts (labels, filters, archiving, drafts) and can never send or delete mail.
- [mail-mcp-server](https://freemcp.space/featured/mail-mcp-server) — Read-only mail for AI agents: on-premises Exchange and any IMAP mailbox, with local search inside PDF, Office and ZIP attachments.
- [mac-terminal-mcp](https://freemcp.space/featured/mac-terminal-mcp) — A sandboxed terminal for Claude on your Mac. No dialogs, no dependencies, no telemetry.
- [spm](https://freemcp.space/featured/spm) — A simple, cross-platform manager for native system services.
- [model-worker-mcp](https://freemcp.space/featured/model-worker-mcp) — MCP server delegating bounded coding tasks to an OpenAI-compatible model: explicit read/write paths, diff validation, risk-based routing.
- [contextsmith](https://freemcp.space/featured/contextsmith) — Give your coding agent the right code, not more code. Local context engine for Claude Code, Cursor & Codex: code graph + hybrid search + embeddings + git history, packed into a token budget. Held-out SWE-bench: right file in 4k tokens 92% vs 29% for search + whole files. MIT, no API keys.
- [onlinecompiler-mcp](https://freemcp.space/featured/onlinecompiler-mcp) — MCP server for OnlineCompiler.io: run and judge code in 46 languages from AI assistants and coding tools such as Claude, ChatGPT, Gemini CLI, Cursor and Codex.
- [Viewport-iq](https://freemcp.space/featured/viewport-iq) — Production-grade Browser Inspection & Responsive Testing MCP Server. Inspect websites, test across viewports, detect layout overflow, capture screenshots, and run audits via Playwright & MCP.
- [softglaze-claude-plugin](https://freemcp.space/featured/softglaze-claude-plu) — SoftGlaze Browser plugin for Claude Code and Cowork: isolated browser profiles, proxies and macros, with your approval for every change.
- [nullprint-mcp](https://freemcp.space/featured/nullprint-mcp) — MCP server for Nullprint, the AI antidetect browser: let Claude, Codex, DeepSeek and other AI agents create, launch, check and drive browser profiles.
- [cat-burglar](https://freemcp.space/featured/cat-burglar) — A stealth browser MCP for agents: three engines, diff observations, site memory, a human CAPTCHA handoff, and a benchmark harness.
- [roomvana-mcp](https://freemcp.space/featured/roomvana-mcp) — MCP server for Roomvana — browse room types & design styles and get a direct link to the Roomvana AI interior-design studio at https://roomvana.ai
- [uwarp-mcp](https://freemcp.space/featured/uwarp-mcp) — WCAG contrast checks, HSL palette + :root CSS generation, and search over 500+ free Uwarp UI design tools.
- [omniverse-mcp](https://freemcp.space/featured/omniverse-mcp) — MCP server + Kit extension that lets AI assistants drive NVIDIA Omniverse apps (Isaac Sim, USD Composer): inspect and edit USD scenes, capture viewports with segmentation, control robots, physics and recordings.
- [tag-per-track-mcp](https://freemcp.space/featured/tag-per-track-mcp) — Model Context Protocol (MCP) server enabling AI agents to perform musical audio analysis, lyrics transcription, and Spotify A&R tracking via x402 USDC micropayments on Base.
- [dinoctor-mcp](https://freemcp.space/featured/dinoctor-mcp) — MCP server for Dinoctor: let Claude, Cursor or any MCP app direct animated videos in the free Dinoctor app.
- [pour-cli](https://freemcp.space/featured/pour-cli) — Audit any URL against WCAG 2.2 from the terminal, in CI, and from AI agents over MCP.
- [penlydoc-mcp](https://freemcp.space/featured/penlydoc-mcp) — MCP server for PenlyDoc e-signatures: send documents for signature, see who signed, download sealed PDFs
- [mcpgate](https://freemcp.space/wensun1217/mcpgate) — MCP production gateway: API-key auth, per-key rate limiting, response caching, circuit breakers, and Prometheus metrics for MCP servers.
- [swarmnest-mcp](https://freemcp.space/featured/swarmnest-mcp) — Swarmnest MCP server: search AI agent tools, APIs, MCP servers and Agent Skills from Claude, Cursor, VS Code or any MCP client. Remote endpoint https://swarmnest.ai/mcp
- [x402-router-mcp](https://freemcp.space/featured/x402-router-mcp) — MCP server + free API for x402 Router: search and route to ~21k live, reliability-scored x402 pay-per-call endpoints (Base, Solana, USDC)
- [agent-data-tools](https://freemcp.space/featured/agent-data-tools) — Focused APIs by monthly plan or pay per call: company check (EU VAT, Nordic and French registers, sanctions), PDF to text, web page to Markdown, plus 700 pay-per-call tools for AI agents over HTTP and MCP. Card, x402 or MPP.
- [nexusgrid-mcp](https://freemcp.space/featured/nexusgrid-mcp) — Official MCP server providing edge-native AI agent tools: Web-to-Markdown scraper (NexusScrape), email deliverability & RFC 7208 auditor (MailAuthGuard), and disposable email fraud detector (FraudShield).
- [onaa-protocol](https://freemcp.space/featured/onaa-protocol) — Open directory of stores where AI agents reached checkout (payment not tested), plus payment, escrow and shipping providers. Links only; ONAA never pays.
- [SignsofAI](https://freemcp.space/featured/signsofai) — A free, privacy-first tool that flags the tells of AI-generated writing, overused vocabulary, rhetorical crutches, robotic sentence rhythm and, for every finding, tells you how to fix it.
- [amazon-mcp](https://freemcp.space/featured/amazon-mcp) — Amazon MCP server by HasData: keyword search, product details, seller profiles and seller catalogues, as JSON.
- [walmart-mcp](https://freemcp.space/featured/walmart-mcp) — MCP server for Walmart: keyword and category search, product pages with the buy box and other sellers, and the review feed with its filter block. 1,000 free credits every month.
- [pktctl](https://freemcp.space/featured/pktctl) — The MCP server that puts Cisco Packet Tracer under your AI agent's control. Native PTMP, 72 tools, one static binary.
- [mcp-yandex-merchants](https://freemcp.space/featured/mcp-yandex-merchants) — MCP server for Yandex Merchants (Yandex Tovary): change prices, discounts and product visibility without re-uploading the YML feed
- [mcp-google-merchants](https://freemcp.space/featured/mcp-google-merchants) — MCP server for Google Merchant Center (Merchant API): diagnose disapproved products, manage product data, feeds and promotions, read performance reports
- [shopscout-mcp](https://freemcp.space/featured/shopscout-mcp) — Let your agent shop and compare: Shopify catalog search, offer ranking and shipping-plan comparison, $0.01 USDC per call via x402 on Base.
- [paxaver-mcp](https://freemcp.space/featured/paxaver-mcp) — Paxaver school community platform: student lunch ordering with allergy and dietary checks, wallets, school calendars, volunteering, memberships and payments.
- [brightspace-mcp-server](https://freemcp.space/featured/brightspace-mcp-serv) — MCP server for Brightspace (D2L). Works with any school.
- [pronounce](https://freemcp.space/featured/pronounce) — 🔊 Hear how developers actually pronounce kubectl, nginx, GIF & 1,900+ tech terms. Sourced dictionary + CLI + VS Code + GitHub Action + MCP + Agent Skill.
- [ictexam-mcp](https://freemcp.space/featured/ictexam-mcp) — MCP server for ICTExam — read exams, gradebooks and item analysis; parse papers with AI and publish exams. By ICT Innovations.
- [scorm-mcp-server](https://freemcp.space/featured/scorm-mcp-server) — Turn HTML, Claude Design bundles or mobile-learning exports into LMS-ready SCORM 2004/1.2 packages — and validate any SCORM zip. Offline, tracked, MIT.
- [learn-shell](https://freemcp.space/featured/learn-shell) — An agent-native teaching OS — a classroom that remembers, for you and your AI. MCP server + self-hosted web app.
- [mcp-server-pronunciation](https://freemcp.space/featured/mcp-server-pronuncia) — Local MCP voice coach with English pronunciation, grammar, and fluency feedback.
- [voice-coach-mcp](https://freemcp.space/featured/voice-coach-mcp) — Local voice coach: records the mic and measures singing pitch accuracy (cents, vibrato, MIDI melody), phoneme-level English pronunciation and public-speaking pace, pauses and filler words, with a coaching skill and progress log.
- [geogebra-mcp](https://freemcp.space/featured/geogebra-mcp) — MCP server that lets AI (Claude, Cursor…) draw, check and fix plane-geometry figures live on GeoGebra Calculator
- [esp-mcp](https://freemcp.space/featured/esp-mcp) — Centralize ESP32 related commands and simplify getting started with seamless, LLM-driven interaction and help.
- [usb-rea](https://freemcp.space/featured/usb-rea) — Reverse Engineer any USB gadget: capture vendor-app traffic, infer the protocol with evidence, generate an open Python/libusb driver. CLI + MCP server.
- [campus-cli](https://freemcp.space/featured/campus-cli) — CLI no oficial para UPC Aula Virtual (Blackboard Learn) — terminal + MCP para Claude
- [brightspace-d2l-mcp](https://freemcp.space/featured/brightspace-d2l-mcp) — Brightspace D2L MCP server for Claude, ChatGPT, Cursor and Copilot. Knows what you already handed in, so it only tells you what is actually left. Due dates, grades and course files at any school with normal SSO sign-in.
- [canvas-mcp](https://freemcp.space/featured/canvas-mcp) — Local-first Canvas LMS MCP server. Stdio transport, ~125 lines of Python.
- [moodle-mcp-server](https://freemcp.space/featured/moodle-mcp-server) — Open-source MCP server that connects AI agents to Moodle LMS data through Moodle Web Services.
- [ent1-mcp](https://freemcp.space/featured/ent1-mcp) — Serveur MCP (Model Context Protocol) en Rust pour l'ENT ONE / Edifice : messagerie avec les enseignants, carnet de liaison, cahier de texte, actualités… depuis Claude ou ChatGPT.
- [servomotor-mcp](https://freemcp.space/featured/servomotor-mcp) — Drive Gearotons M17 open-source servomotors from natural language (MCP server).
- [gnuradioMCP](https://freemcp.space/featured/gnuradiomcp) — MCP server for GNU Radio
- [mcp-server-kicad](https://freemcp.space/featured/mcp-server-kicad) — Maintenance mode: security and KiCad compatibility fixes only (see README for why). KiCad MCP server: 100+ Model Context Protocol tools that let an AI assistant do schematic capture and PCB layout, run ERC and DRC, and export Gerbers, BOM and 3D models.
- [sheetsdata-mcp](https://freemcp.space/featured/sheetsdata-mcp) — sheetsdata-mcp
- [misterclaw](https://freemcp.space/featured/misterclaw) — 👾🦀 MiSTerClaw — MCP Remote Control for MiSTer-FPGA
- [fw-context-mcp](https://freemcp.space/featured/fw-context-mcp) — C/C++ semantic index for AI coding assistants — powered by your compile_commands.json. Query the program your compiler actually builds, not just the source files.
- [platformio.mcp](https://freemcp.space/featured/platformio-mcp) — MCP server that lets AI coding agents drive PlatformIO: build, flash, serial monitor, tests, crash decoding, size reports
- [ugs-mcp](https://freemcp.space/featured/ugs-mcp) — MCP server for controlling CNC machines via Universal GCode Sender
- [stm32-gdb-mcp](https://freemcp.space/302875837/stm32-gdb-mcp) — MCP server that lets AI agents debug STM32 firmware on real hardware (GDB + OpenOCD/ST-Link/J-Link): HardFault triage, FreeRTOS, SWO/RTT, decoded structured results.
- [serial-mcp-server](https://freemcp.space/featured/serial-mcp-server) — Rust MCP server and CLI for serial/UART devices, with JSON macro automation and agent skills for repeatable timed workflows.
- [opcua-mcp](https://freemcp.space/featured/opcua-mcp) — An MCP server that connects to OPC UA-enabled industrial systems.
- [modbus-mcp](https://freemcp.space/featured/modbus-mcp) — An MCP server that standardizes and contextualizes industrial Modbus data.
- [ByteAsk-Embedded-MCP](https://freemcp.space/featured/byteask-embedded-mcp) — The open-source MCP server behind ByteAsk Embedded Docs: a source-grounded, page-cited evidence-retrieval server for coding agents (Claude Code, Codex, Cursor) that write firmware / driver / protocol code and need exact facts.
- [redcon](https://freemcp.space/featured/redcon) — Context budgeting layer for coding agents: selects, compresses, caches and budgets repository context. Public benchmark (context-eval), MCP. Open source.
- [openbaud](https://freemcp.space/featured/openbaud) — Turn serial devices into reusable, auditable tools for coding agents — discover, decode, visualize, capture, and replay.
- [obsbot-mcp](https://freemcp.space/featured/obsbot-mcp) — Cross-platform MCP server for OBSBOT Tiny 2 (UVC) camera control
- [smolmux](https://freemcp.space/featured/smolmux) — C11 device multiplexer: share serial UART / GDB SWD across humans, scripts, and AI agents (MCP). MIT.
- [Comparador Luz Gas](https://freemcp.space/nuncaeslupus/comparador-luz-gas) — **El comparador oficial de tarifas de luz y gas de la CNMC, como librería, CLI y servidor MCP.**
- [Numerador Facturas](https://freemcp.space/nuncaeslupus/numerador-facturas) — **Numera facturas PDF en lote desde el navegador.** Estampa un número correlativo (`F-0001`, `F-0002`…) en **todas las páginas** de cada factura y te devuelve un ZIP listo para entregar. Todo ocurre del lado del cliente: **los PDFs nunca salen de tu equipo.**
- [Doc Control](https://freemcp.space/nuncaeslupus/doc-control) — **Lets AI agents edit Word documents as tracked changes the writer can accept or reject.**
- [Drawspec](https://freemcp.space/nuncaeslupus/drawspec) — **Diagrams from a JSON description — no coordinates, so nothing to misplace.** You say what the diagram *means*: the boxes, the arrows, the labels, and a role for each. drawspec decides every position, size, route and colour, and draws a clean SVG, PNG or plain-text diagram.
- [mcp-server-atlassian-bitbucket](https://freemcp.space/featured/mcp-server-atlassian-3) — Node.js/TypeScript MCP server for Atlassian Bitbucket. Enables AI systems (LLMs) to interact with workspaces, repositories, and pull requests via tools (list, get, comment, search). Connects AI directly to version control workflows through the standard MCP interface.
- [csvglow](https://freemcp.space/featured/csvglow) — Generate beautiful interactive HTML dashboards from CSV/Excel files
- [Glyphic](https://freemcp.space/featured/glyphic) — Glyphic is an open source diagram engine that lets AI agents generate production-quality diagrams from structured JSON, without SVG, Mermaid, or a browser.
- [matter-controller-mcp](https://freemcp.space/featured/matter-controller-mc) — An MCP server for Matter Controller, enabling AI agents to control and interact with Matter devices.
- [cli](https://freemcp.space/featured/cli) — cli & mcp-server package for Push To Display
- [telinksdk-builder-mcp](https://freemcp.space/featured/telinksdk-builder-mc) — Build Telink and other embedded SDKs (Eclipse headless, Make or generic) via natural language, with automatic build pattern detection.
- [chartlink-agents](https://freemcp.space/featured/chartlink-agents) — chartlink for agents: Claude Code plugin, MCP bridge and listing kit for charts with live-updating embeds
- [drawspec](https://freemcp.space/featured/drawspec) — Declarative diagram spec → clean, themeable SVG. JSON with no coordinates, so an LLM can write it correctly.
- [mcp-server-weaviate](https://freemcp.space/featured/mcp-server-weaviate) — MCP (Model Context Protocol) server for Weaviate
- [mcp-dashboards](https://freemcp.space/featured/mcp-dashboards) — Turn your data into interactive dashboards inside any AI client - MCP Apps powered
- [ply-visualizer](https://freemcp.space/featured/ply-visualizer) — Inspect, compare and export point clouds, meshes and depth data with interactive 3D previews, measurements, NumPy/PyTorch inputs and COLMAP depth.
- [charted](https://freemcp.space/featured/charted) — Zero-dependency Python SVG chart generator. Generate beautiful, customisable charts in SVG from Python data structures. Inspired by mermaid.js.
- [axiom-advanced-math-mcp](https://freemcp.space/featured/axiom-advanced-math) — Exact symbolic math for LLMs: integrals, equations, matrices, and claim verification via Giac/Xcas. MCP server + CLI.
- [renoun-mcp](https://freemcp.space/featured/renoun-mcp) — Structural observability for AI conversations. Detects loops, stuck states, breakthroughs, and convergence patterns across 17 channels without analyzing content. MCP server + REST API.
- [mcp-gnu-units](https://freemcp.space/featured/mcp-gnu-units) — Unit converter for AI agents, powered by the GNU units database — convert 3000+ units of measurement, evaluate compound unit expressions, reduce to SI base units, dimensional analysis. Offline, deterministic.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
