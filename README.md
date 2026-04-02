# Awesome Remote MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Connect your AI assistant to the world — no installs, no Docker, no config files.

Remote MCP servers are accessible via a URL. Paste the endpoint into your AI client and start using it immediately.

**→ Want to host your own?** [freemcp.space](https://freemcp.space) deploys any MCP server from a Dockerfile or GitHub repo in seconds.

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

> Deploy and run your own MCP servers remotely.

- **[freemcp.space](https://freemcp.space)** 🆓 🌐 ✅ — Host any MCP server from a Dockerfile or GitHub repo. Free tier: 2 servers. Instant deploy, no infrastructure management. `{username}/{slug}/mcp`
- **[Cloudflare Workers MCP](https://developers.cloudflare.com/agents/guides/remote-mcp-server/)** 🆓 🌐 ✅ — Run MCP servers on Cloudflare's global edge network.
- **[Smithery](https://smithery.ai)** 🆓 ✅ — MCP server registry with remote hosting and one-click deploy.

---

## Code & Development

- **[GitHub MCP](https://github.com/github/github-mcp-server)** 🔑 🌐 ✅ — Repos, issues, PRs, code search, and file access. Official GitHub server.
  `https://api.githubcopilot.com/mcp/`
- **[GitMCP](https://gitmcp.io)** 🆓 ✅ — Any GitHub repo becomes an MCP server instantly. No setup needed.
  `https://gitmcp.io/{owner}/{repo}`
- **[Sentry](https://mcp.sentry.dev/sse)** 🔑 ✅ — Query issues, events, and releases from Sentry.

---

## Data & Search

- **[Brave Search](https://brave.com/search/api/)** 🆓 🔑 ✅ — Web and local search without tracking.
- **[Exa](https://exa.ai)** 🔑 ✅ — Semantic web search optimized for AI agents.
- **[Kagi](https://kagi.com)** 💰 🔑 — Privacy-first search with high-quality results.

---

## Productivity & Workspace

- **[Linear](https://linear.app/changelog/2025-03-18-mcp)** 🔑 ✅ — Issues, projects, and team management.
- **[Notion](https://www.notion.so)** 🔑 ✅ — Read and write pages, databases, and blocks.
- **[Airtable](https://airtable.com)** 🔑 — Bases, records, and views.

---

## Cloud Infrastructure

- **[AWS MCP](https://github.com/awslabs/mcp)** 🔑 🌐 ✅ — S3, Lambda, CloudWatch, and more. Official AWS servers.
- **[Azure MCP](https://github.com/microsoft/azure-mcp)** 🔑 🌐 ✅ — Azure resource management. Official Microsoft server.
- **[Cloudflare MCP](https://github.com/cloudflare/mcp-server-cloudflare)** 🔑 🌐 ✅ — Zones, Workers, KV, and R2. Official Cloudflare server.
- **[Vercel MCP](https://vercel.com/docs/mcp)** 🔑 ✅ — Deployments, domains, and project management.

---

## Finance & Payments

- **[Stripe MCP](https://docs.stripe.com/building-with-llms/mcp)** 🔑 ✅ — Customers, payments, invoices, and subscriptions. Official Stripe server.
- **[Resend MCP](https://resend.com/mcp)** 🆓 🔑 ✅ — Send transactional emails directly from your AI assistant.

---

## Communication

- **[Slack MCP](https://slack.com)** 🔑 — Channels, messages, and user management.
- **[Twilio](https://twilio.com)** 🔑 — SMS, calls, and messaging APIs.

---

## AI & Models

- **[Replicate MCP](https://replicate.com)** 🆓 🔑 ✅ — Run image generation, video, audio, and language models.
- **[OpenAI MCP](https://openai.com)** 🔑 — Models, fine-tuning, and assistants API.
- **[Anthropic MCP](https://anthropic.com)** 🔑 — Claude API access and prompt management.

---

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting.

**Only remote servers are listed here.** For local servers, see [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers).

---

## Related

- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) — Comprehensive list, local + remote
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) — Official reference implementations
- [PulseMCP](https://pulsemcp.com) — Discovery and rankings

---

*Maintained by [Appnova](https://freemcp.space) · [CC0 License](LICENSE)*
