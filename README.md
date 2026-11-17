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
- [jevx-mcp](https://freemcp.space/featured/jevx-mcp) — MCP server for Jevx (jevx.org): run Jev AI typed decisions from any MCP client
- [optuna-mcp](https://freemcp.space/featured/optuna-mcp) — The Optuna MCP Server is a Model Context Protocol (MCP) server to interact with Optuna APIs.
- [MCPR](https://freemcp.space/featured/mcpr) —  MCPR enables AI agents to participate in interactive R sessions for professional analysis workflows.
- [oraclaw](https://freemcp.space/featured/oraclaw) — Deterministic decision-intelligence MCP server for AI agents — 17 tools (bandits/LinUCB, HiGHS LP/MIP, PageRank, Monte Carlo, CMA-ES, conformal). Sub-25ms. Zero LLM cost. 11 free, no key. Listed on the MCP Registry & Glama.
- [code-guardian](https://freemcp.space/featured/code-guardian) — Code Guardian Studio – AI-powered code refactor engine for large repositories, built on Claude Code + MCP.
- [mcp-turboquant](https://freemcp.space/featured/mcp-turboquant) — MCP server for LLM quantization. Compress any model to GGUF/GPTQ/AWQ in one tool call. First MCP server for model compression.
- [kaggle-mcp-server](https://freemcp.space/featured/kaggle-mcp-server) — This project provides an MCP (Model Context Protocol) server for interacting with Kaggle competitions from Claude Desktop (or any MCP-compatible client)
- [mcp-compress](https://freemcp.space/featured/mcp-compress) — First MCP server for data compression. 60x compression on docs, 30x on SQL, 20x on logs. Zero dependencies. Lossless. Auto-picks best algorithm. 7 tools for any AI agent.
- [ephemeris-mcp](https://freemcp.space/featured/ephemeris-mcp) — MCP server for time-series foundation model (TSFM) forecasting: probabilistic forecasts from Chronos-2, TimesFM 2.5, Toto 2, TiRex-2 and IBM Granite models, or an accuracy-weighted ensemble.
- [jupyter-notebook-mcp](https://freemcp.space/featured/jupyter-notebook-mcp) — A Model Context Protocol (MCP) for Jupyter Notebook
- [label-studio-mcp-server](https://freemcp.space/featured/label-studio-mcp-ser) — Create, manage and automate Label Studio projects, tasks and predictions for data labeling workflows.
- [WaveGuardClient](https://freemcp.space/featured/waveguardclient) — Python SDK for WaveGuard  physics-based anomaly detection API. One call. Any data.
- [data-profiler-mcp](https://freemcp.space/featured/data-profiler-mcp) — MCP server that profiles tabular data files (CSV, Parquet, Excel, JSON) for LLM agents like Claude.
- [rigor](https://freemcp.space/featured/rigor) — Verified statistical inference for AI agents -- classical and non-parametric hypothesis testing, correlation/regression, effect sizes, power/sample-size, multiple-comparisons correction, a test-recommendation helper, and a batch pairwise-comparison tool, as a CLI and an MCP server
- [gnomon-mcp](https://freemcp.space/featured/gnomon-mcp) — Deterministic date, math and unit tools: time snapshots, calendar math with natural-language parsing, expression evaluation and Pint-based unit conversion.
- [cortexcloud-mcp](https://freemcp.space/featured/cortexcloud-mcp) — x402 pay-per-call MCP server — 22 AI/data/RPC tools, USDC on Base, no API keys
- [polymath-megablaster-mcp](https://freemcp.space/featured/polymath-megablaster) — Local MCP toolkit giving AI agents deterministic calculation instead of guessing: 15 free tools for exact math, dates, unit conversion, hashing, networking. 100% local, no network calls, no API keys, no telemetry.
- [website-downloader](https://freemcp.space/featured/website-downloader) — MCP server to download entire websites
- [chronulus-mcp](https://freemcp.space/featured/chronulus-mcp) — MCP Server for Chronulus AI Forecasting and Prediction Agents
- [growthbook-mcp](https://freemcp.space/featured/growthbook-mcp) — Official GrowthBook MCP server for creating flags, getting experiments, and more.
- [networkx-mcp-server](https://freemcp.space/featured/networkx-mcp-server) — 🕸️ First NetworkX MCP server for graph analysis in AI conversations | Community & Enterprise editions | Graph algorithms • Network analysis • MCP integration
- [math-mcp-learning-server](https://freemcp.space/featured/math-mcp-learning-se) — Educational MCP server with math operations, matrix algebra, data visualization, and persistent workspace
- [llm-advisor-mcp](https://freemcp.space/featured/llm-advisor-mcp) — Real-time LLM and VLM comparison with benchmarks, prices and personalized recommendations from multiple data sources.
- [filter-mcp-server](https://freemcp.space/featured/filter-mcp-server) — MCP server comparing approximate filters (Bloom, Counting Bloom, Cuckoo, SuRF). Listed in awesome-mcp-servers.
- [neurocode](https://freemcp.space/featured/neurocode) — In-memory Code Property Graph context slicer for local models (Ollama, Cursor, Claude Desktop): extracts sub-1,200 token reachability closures for autonomous repository bug repair on consumer edge hardware (4GB–8GB VRAM) without cloud API dependency.
- [kaggle-mcp](https://freemcp.space/featured/kaggle-mcp-2) — MCP server for Kaggle
- [fermat-mcp](https://freemcp.space/featured/fermat-mcp) — 🚀 Fermat MCP: The Ultimate Math Engine - Unifying SymPy, NumPy & Matplotlib in one powerful server! Perfect for devs & researchers. 
- [mathlas](https://freemcp.space/featured/mathlas) — Airtight math tools an AI uses over MCP — 3.7M-theorem search, PSLQ constant ID, OEIS, real Lean kernel checks, applicability checklists. No LLM inside, no API key.
- [calculator-server](https://freemcp.space/featured/calculator-server) — A comprehensive Go-based MCP server for mathematical computations with 13+ tools
- [stella-mcp](https://freemcp.space/featured/stella-mcp) — MCP server for Stella
- [dataloupe](https://freemcp.space/featured/dataloupe) — Offline data explorer + MCP server: turn CSV/Parquet/Excel into ONE self-contained interactive HTML file, or let your AI assistant query local data — nothing leaves your machine.
- [mathmethods-mcp](https://freemcp.space/featured/mathmethods-mcp) — MCP server for numerical methods and dynamic systems: root finding, integration, ODEs, Monte Carlo, 1D/2D dynamical systems, and combat models.
- [decisionmatrix-mcp](https://freemcp.space/featured/decisionmatrix-mcp) — Deterministic multi-criteria decision analysis (MCDA) for AI agents over MCP — score, rank & explain options against weighted criteria. Weighted-sum, weighted-product, TOPSIS. Exact decimals. Live remote server + self-host.
- [otakit](https://freemcp.space/featured/otakit) — Push updates directly to your Capacitor app without app store reviews.
- [mcp-architect](https://freemcp.space/featured/mcp-architect) — Give any AI assistant real architectural understanding of a codebase — local, private, zero-config MCP serve
- [Unfour](https://freemcp.space/featured/unfour) — Local-first backend troubleshooting workspace for tracing failures across API, SSH, and databases, with MCP-assisted runtime evidence.
- [qa-probe](https://freemcp.space/featured/qa-probe) — Local QA agent — maps frontend routes to backend APIs, probes every endpoint live, scores pages 0–100, and explains why data is missing. Built for LightShield SIEM. Works with any FastAPI / Express / Next.js app.
- [amendor-mcp](https://freemcp.space/featured/amendor-mcp) — Connect your coding agent to Amendor. Pulls change requests into your agent so it builds them and opens PRs.
- [codemagic-mcp](https://freemcp.space/featured/codemagic-mcp) — Build, sign, and publish iOS & Android apps through AI agents — Codemagic CI/CD + App Store Connect + Google Play
- [mcp-laya](https://freemcp.space/featured/mcp-laya) — Fast, local, non-autoregressive System-1 decision engine as MCP tools — typed decisions (classify / score / yes-no) over text, email, tickets or JSON in 100+ languages, with calibrated confidence and no text generation, so nothing to hallucinate. Offloads routing/triage/gating judgment calls from the main model; runs on-device, offline by default. `pipx install mcp-laya`
- [proxykit-mcp](https://freemcp.space/featured/proxykit-mcp) — MCP server for ProxyKit — drive a local HTTP(S) debugging proxy from Claude, Cursor, and any MCP host.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
