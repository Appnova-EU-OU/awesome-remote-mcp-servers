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
- [mcp-telegram](https://freemcp.space/featured/mcp-telegram) — Telegram MCP Server — connect Telegram to Claude AI & ChatGPT. 181 tools: messages, media, reactions, polls, stories & more. MTProto userbot. Self-host (npx) or hosted at mcp-telegram.com.
- [discord-mcp](https://freemcp.space/featured/discord-mcp) — MCP server to control Discord — messages, channels, roles, permissions, members, and moderation
- [cv-mcp-server](https://freemcp.space/featured/cv-mcp-server) — Carbon Voice MCP Server
- [chatterboxio-mcp-server](https://freemcp.space/featured/chatterboxio-mcp-ser-2) — A Model Context Protocol server implementation for ChatterBox, enabling AI agents to interact with online meetings and generate meeting summaries
- [Omnicord](https://freemcp.space/featured/omnicord) — Discord server management MCP for AI agents. Chat, moderation, administration, and full server building from one brief. 150+ tools, with destructive actions gated behind a preview.
- [mcp-server](https://freemcp.space/featured/mcp-server-13) — MCP server for Postcard.bot — let AI agents send real printed postcards. Works with Claude, Cursor, Windsurf, and any MCP client.
- [aiogram-mcp](https://freemcp.space/featured/aiogram-mcp-2) — MCP server middleware for aiogram Telegram bots — expose your bot to AI agents via the Model Context Protocol
- [outlook-assistant](https://freemcp.space/featured/outlook-assistant) — MCP server for Outlook email, calendar, and contacts — let your AI assistant manage your inbox directly from the conversation.
- [better-email-mcp](https://freemcp.space/featured/better-email-mcp) — IMAP/SMTP email for AI agents -- read, send, organize folders, and manage attachments across multiple accounts, with auto-discovery.
- [ringback](https://freemcp.space/featured/ringback) — Let your AI agent call your phone and talk to you — MCP servers for live, interruptible voice calls + tiered alerts, using free self-hosted pieces (pjsua2 + whisper.cpp + Linphone). No paid telephony, no extra API key.
- [email-mcp](https://freemcp.space/featured/email-mcp-2) — Unified MCP server for email access across Gmail, Outlook, iCloud, and IMAP
- [caldav-mcp](https://freemcp.space/featured/caldav-mcp-2) — Universal MCP server for CalDAV protocol integration. Works with any CalDAV-compatible calendar server including Yandex Calendar, Google Calendar (via CalDAV), Nextcloud, ownCloud, Apple iCloud, and others. Supports creating events with recurrence, categories, priority, attendees, reminders, searching events, and retrieving events by UID.
- [mingle-mcp](https://freemcp.space/featured/mingle-mcp) — Your AI meets other people's AIs. You meet the people. Agent-native networking via MCP.
- [Xadeus-QQ-MCP](https://freemcp.space/xadeus/xadeus-qq-mcp) — QQ MCP Server - connect AI agents to QQ via NapCatQQ. Auto-wake, messaging, group management, file sharing, cross-platform.
- [mcp-server](https://freemcp.space/featured/mcp-server-12) — MCP server for MultiMail — Verifiable identity email for AI agents
- [leximo-ai-call-assistant-mcp-server](https://freemcp.space/featured/leximo-ai-call-assis) — An MCP (Model Context Protocol) server that lets you schedule AI phone calls and manage Leximo assignments directly from Claude Desktop or Claude Code — no app switching needed.
- [qorami-sdk](https://freemcp.space/featured/qorami-sdk) — Official Qorami SDK — JS/Python clients, tool schemas and an MCP server so AI agents check email before sending. https://qorami.fr
- [alibaba-cloud-ops-mcp-server](https://freemcp.space/featured/alibaba-cloud-ops-mc-2) — AlibabaCloud CloudOps MCP Server
- [roundtable](https://freemcp.space/featured/roundtable) — Zero-configuration MCP server that unifies multiple AI coding assistants (Codex, Claude Code, Cursor, Gemini) through intelligent auto-discovery and standardized interface
- [codex-control-plane-mcp](https://freemcp.space/featured/codex-control-plane) — Durable MCP control plane for long-running Codex Desktop tasks
- [neurolink](https://freemcp.space/featured/neurolink) — One TypeScript interface for 24+ LLM providers — swap providers without rewriting. MCP-native (connect any MCP server), voice (TTS/STT/realtime), RAG, memory, file processors. Production-origin: powers Tara, Yama, and Clairvoyance at Juspay.
- [join.cloud](https://freemcp.space/featured/join-cloud) — Join.cloud lets AI agents work together in real-time rooms. Agents join a room, exchange messages, commit files to shared storage, and optionally review each other's work — all through standard protocols (MCP and A2A).
- [local-mcp-releases](https://freemcp.space/lmcp/local-mcp-releases) — 215+ local tools for Claude, ChatGPT, Cursor & Grok — Mail, iMessage, Teams, Slack, WhatsApp, OneDrive, Google Drive, Zoom, Outlook, Office. Native macOS, 100% local, no API keys.
- [bluesky-context-server](https://freemcp.space/featured/bluesky-context-serv) — Bluesky MCP server
- [slack-mcp-server](https://freemcp.space/featured/slack-mcp-server) — Catch up on Slack without reading it. Unreads, threads, search. Browser-session or hosted OAuth. 21 tools.
- [telephony-mcp-server](https://freemcp.space/featured/telephony-mcp-server) — A very simple no-fuss minimalist MCP Server with telephony tools like voice call and sms. This MCP Server can be integrated with LLM applications. Vonage API is used for calls, SMS, Speech-to-Text and Speech Recognition.
- [agent-comm-hub](https://freemcp.space/featured/agent-comm-hub) — Let multiple AI agents talk, schedule tasks, share memory and self-evolve — zero external services, 5-minute Docker deploy.
- [whatsapp-mcp](https://freemcp.space/featured/whatsapp-mcp) — WhatsApp MCP Server — Manage templates & send messages via Claude, Cursor, or any MCP client. Meta Cloud API.
- [producthunt-mcp-server](https://freemcp.space/featured/producthunt-mcp-serv) — MCP server for Product Hunt. Interact with trending posts, comments, collections, users, and more.
- [mattermost-mcp-host](https://freemcp.space/featured/mattermost-mcp-host) — A Mattermost integration that connects to Model Context Protocol (MCP) servers, leveraging a LangGraph-based Agent.
- [mcp-server](https://freemcp.space/featured/mcp-server-11) — MCP server for account verification: SMS verification, number rentals and matching-country proxies on carrier-issued mobile numbers. 40 tools, 2500+ services, 145+ countries. Works with Claude, Cursor, Codex, Windsurf, Cline, Zed, OpenClaw, Hermes and Continue.
- [inxmail-mcp](https://freemcp.space/featured/inxmail-mcp) — MCP server for the Inxmail Commerce transactional API — events, sendings, bounces, blocklist, blacklist, reactions, and delivery tracking from Claude.
- [proton-mail-mcp](https://freemcp.space/featured/proton-mail-mcp) — Unofficial MCP server for Proton Mail (not affiliated with Proton AG) — send, read, search & organize email over SMTP/IMAP
- [mcp-discord-bridge](https://freemcp.space/featured/mcp-discord-bridge) — AI assistant control a Discord server - reading messages, creating/deleting channels, sending messages ,All via the MCP protocol
- [joltsms-mcp-server](https://freemcp.space/featured/joltsms-mcp-server) — MCP server for JoltSMS — provision real-SIM US phone numbers and receive SMS/OTP codes
- [qmailing-mcp-server](https://freemcp.space/featured/qmailing-mcp-server) — MCP server for QMailing - AI agents read & send email, manage mailboxes, custom domains and webhooks via the QMailing API.
- [shipmail-mcp](https://freemcp.space/featured/shipmail-mcp) — Official Shipmail MCP server for AI-agent custom-domain business email, REST API, and webhooks
- [ox-mcp](https://freemcp.space/featured/ox-mcp) — MCP server for Open-Xchange & standards-based mail: email (IMAP/SMTP), Sieve filters, CalDAV calendar, CardDAV contacts, free/busy.
- [radmail-mcp](https://freemcp.space/featured/radmail-mcp) — Email OS for agents over MCP: two-axis triage, a Right Now lane, commitment follow-through, reviewable drafts, and a machine-verifiable BEC hard-stop (money/banking-change/first-contact = human-only). Zero-auth sandbox.
- [discogs-mcp-server](https://freemcp.space/featured/discogs-mcp-server) — MCP Server for Discogs
- [imessage-query-fastmcp-mcp-server](https://freemcp.space/featured/imessage-query-fastm) — An MCP server that provides safe access to your iMessage database through Model Context Protocol (MCP). This server is built with the FastMCP framework and the imessagedb library, enabling LLMs to query and analyze iMessage conversations with proper phone number validation and attachment handling.
- [ntfy-me-mcp](https://freemcp.space/featured/ntfy-me-mcp) — An ntfy MCP server for sending/fetching ntfy notifications to self-hosted or ANY ntfy.sh server from AI Agents 📤 (supports secure token auth & more - use with npx or docker!)
- [apple-mail-mcp](https://freemcp.space/featured/apple-mail-mcp) — Apple Mail MCP server with full-coverage FTS5 body search. Reliable on large mailboxes where AppleScript-based servers timeout.
- [wechat-fastbridge](https://freemcp.space/featured/wechat-fastbridge) — 让 Codex 秒级、低 token、安全地读写 macOS 微信 | Fast, token-efficient WeChat bridge for Codex
- [telegram-archive-mcp](https://freemcp.space/featured/telegram-archive-mcp) — MCP Server for Telegram-Archive — search messages, browse chats, and access archived Telegram history via MCP
- [iletimerkezi-mcp-server](https://freemcp.space/featured/iletimerkezi-mcp-ser) — iletiMerkezi MCP Server
- [signal-mcp](https://freemcp.space/featured/signal-mcp) — Ask Claude about your Signal conversations. Persistent history, full-text search, and complete signal-cli coverage — 100% local.
- [resend-email-mcp](https://freemcp.space/featured/resend-email-mcp) — The most complete MCP server for the Resend email API — full API coverage plus a unique debug/diagnostics layer.
- [pingwa-client](https://freemcp.space/featured/pingwa-client) — Text your phone from any agent, script or CI - and tap to reply. Python/CLI/MCP client for   pingwa.
- [mcp-server-notmuch](https://freemcp.space/featured/mcp-server-notmuch) — Read-first MCP server for a local notmuch mail database: search, threads, attachments, drafts. Sending email via Drafts/ 
- [covalent-bond](https://freemcp.space/featured/covalent-bond) — Peer-to-peer, end-to-end-encrypted collaboration channel for AI coding agents over MCP. The relay never sees your data.
- [discourse-mcp](https://freemcp.space/featured/discourse-mcp) — MCP client for Discourse sites
- [docs-mcp](https://freemcp.space/featured/docs-mcp) — CometChat docs search + implementation bundles: add chat, voice, video & moderation to your app through your AI coding agent.
- [callcenter.js-mcp](https://freemcp.space/featured/callcenter-js-mcp) — Callcenter.JS AI Voice Agent VOIP Connector, MCP + CLI
- [calcom-mcp](https://freemcp.space/featured/calcom-mcp) — A FastMCP server for interacting with the Cal.com API. This enables LLMs to manage event types, create bookings, and access Cal.com scheduling data programmatically.
- [feishu-user-plugin](https://freemcp.space/featured/feishu-user-plugin) — 飞书 MCP 服务器 + CLI 工具：让 Claude Code/Codex/脚本 直接接管你的飞书工作流 — 84 个工具、3 层鉴权 cookie / 官方 API / OAuth，以你本人身份发消息、读取群和私聊、操作文档 / 多维表格 / 知识库 / 云空间 / 日历 / 任务 / OKR
- [telegram-bot-mcp](https://freemcp.space/featured/telegram-bot-mcp) — Full-featured Telegram Bot API MCP server with 174 tools for Claude Code and AI agents
- [xtapdown-mcp](https://freemcp.space/featured/xtapdown-mcp) — XTapDown MCP Server — 14 X (Twitter) creator tools for Claude, ChatGPT, Gemini and any MCP client
- [mcp-server](https://freemcp.space/featured/mcp-server-10) — Official Model Context Protocol (MCP) server for FastAlert. This server allows AI agents (like Claude, ChatGPT, and Cursor) to list of your channels and send notifications directly through the FastAlert API.
- [mattermost-mcp](https://freemcp.space/featured/mattermost-mcp) — Mattermost MCP server to enable Claude to interact with Mattermost Workspaces
- [doubletick-cli](https://freemcp.space/featured/doubletick-cli) — CLI and MCP server for DoubleTick email read tracking
- [instapdown-mcp](https://freemcp.space/featured/instapdown-mcp) — 16 Instagram creator tools as an MCP server — Reels/Story/carousel downloaders, engagement audit, hashtag search, Reels hook generator, best-time-to-post and content calendar.
- [solmail-mcp](https://freemcp.space/featured/solmail-mcp) — MCP server for sending physical mail with Solana cryptocurrency. Colosseum Agent Hackathon submission.
- [mailwarden](https://freemcp.space/csitte/mailwarden) — A reliable, native Gmail MCP server with full mailbox control — including snooze.
- [openai-gpt-image-mcp](https://freemcp.space/featured/openai-gpt-image-mcp) — A Model Context Protocol (MCP) tool server for OpenAI's GPT-4o/gpt-image-1 image generation and editing APIs.
- [medical-mcp](https://freemcp.space/featured/medical-mcp) — An MCP server that provides comprehensive medical information by querying multiple authoritative medical APIs including FDA, WHO, PubMed, Google Scholar, and RxNorm
- [posecode](https://freemcp.space/featured/posecode) — An open-source text language, parser, validator and Three.js renderer for inspectable 3D human movement.
- [email-mcp](https://freemcp.space/featured/email-mcp) — Email MCP server with full IMAP + SMTP support — read, search, send, manage, and organize email from any AI assistant via the Model Context Protocol
- [tsgram-mcp](https://freemcp.space/featured/tsgram-mcp) — TSGram - Telegram MCP Server for local Claude Code integration - debug and vibe code on the go!
- [mcp_server_notify](https://freemcp.space/featured/mcp-server-notify) — Send system notification when Agent task is done.
- [mcp-googletasks](https://freemcp.space/featured/mcp-googletasks) — This Model Context Protocol (MCP) server provides a bridge between LLMs and Google Tasks, allowing you to manage your task lists and tasks directly through Claude.
- [wecom-docs-mcp-server](https://freemcp.space/featured/wecom-docs-mcp-serve) — MCP server for WeCom (Enterprise WeChat) document operations — create, read, edit Docs and Smartsheets. Fills the doc-CRUD gap in the WeCom MCP ecosystem.
- [dead-letter](https://freemcp.space/featured/dead-letter) — Convert .eml email exports to Markdown with YAML front matter
- [content-distribution-mcp](https://freemcp.space/featured/content-distribution) — Multi-channel content distribution MCP server with idempotent state. Auto-publish to DEV.to, Hashnode, GitHub Discussions, Reddit, Bluesky; browser-fallback for Medium, LinkedIn, X/Twitter.
- [clawaimail](https://freemcp.space/featured/clawaimail) — Email infrastructure for AI agents. Create inboxes on the fly, send and receive real emails, search messages, and manage threads via API. Install with `npx clawaimail-mcp`.
- [agent-mq](https://freemcp.space/featured/agent-mq-2) — Message queue for AI coding assistants. Let your AI agents talk to each other.
- [mailbox-mcp](https://freemcp.space/featured/mailbox-mcp) — Official MCP server for mailbox.bot — physical postal mail API for AI agents.
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
- [tui-mcp](https://freemcp.space/nvms/tui-mcp) — What Chrome DevTools MCP is for the browser, tui-mcp is for the terminal. Launch, screenshot, and interact with any TUI app.
- [infrabroker](https://freemcp.space/featured/infrabroker) — Infrastructure access broker for AI agents — SSH & Kubernetes. Per-operation ephemeral credentials minted by a separate signer; the model never touches one. MCP stdio / HTTP+OIDC.
- [mcp-remote-ssh](https://freemcp.space/featured/mcp-remote-ssh) — MCP server for remote SSH operations -- persistent sessions, structured command output, SFTP file transfer, port forwarding, and secret-safe environment variable injection with automatic output redaction.
- [sysknife](https://freemcp.space/featured/sysknife) — Your sysadmin co-pilot — an AI that administers Linux through typed, approval-gated, Ed25519-audited actions instead of shell strings. Reference implementation of the LACS standard.
- [cygnus-ssh-mcp](https://freemcp.space/featured/cygnus-ssh-mcp) — MCP server for SSH remote server management
- [trinity-lite](https://freemcp.space/featured/trinity-lite) — Local AgentOps for cross-vendor CLI coding agents: route work, recover state, and accept only with evidence.
<!-- freemcp:end -->

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

## License

[CC0-1.0](./LICENSE)
