# Awesome Remote MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of **remote & hosted** Model Context Protocol (MCP) servers — no local setup, no Docker, no configuration required.

[Model Context Protocol (MCP)](https://modelcontextprotocol.io) is an open standard that enables AI models to securely interact with external tools and data sources. This list focuses exclusively on **remote servers** — servers you can connect to instantly without installing anything locally.

## Why Remote MCP?

| | Local MCP | Remote MCP |
|---|---|---|
| Setup | Install + configure | Just a URL |
| Maintenance | You manage it | Provider manages it |
| Availability | Your machine must be on | Always-on |
| Team sharing | Difficult | Share a URL |

---

## Contents

- [Platforms](#platforms)
- [Developer Tools](#developer-tools)
- [Data & Databases](#data--databases)
- [Productivity](#productivity)
- [AI & LLMs](#ai--llms)
- [Finance](#finance)
- [Communication](#communication)
- [Infrastructure & DevOps](#infrastructure--devops)
- [Security](#security)
- [Contributing](#contributing)

---

## Legend

| Symbol | Meaning |
|--------|---------|
| ☁️ | Fully hosted, always-on |
| ⚡ | One-click deploy |
| 🆓 | Free tier available |
| 🔐 | Auth required |
| 🌐 | Open source |

---

## Platforms

> Platforms that let you host and deploy your own MCP servers remotely.

- **[freemcp.space](https://freemcp.space)** ☁️ ⚡ 🆓 — Deploy any MCP server from a Dockerfile or GitHub repo in seconds. Free tier includes 2 servers. No infrastructure management needed.
- **[Cloudflare Workers MCP](https://developers.cloudflare.com/agents/guides/remote-mcp-server/)** ☁️ 🌐 — Deploy MCP servers on Cloudflare's edge network globally.
- **[Smithery](https://smithery.ai)** ☁️ 🆓 — MCP server registry and remote hosting platform.

---

## Developer Tools

- **[GitHub MCP](https://github.com/github/github-mcp-server)** ☁️ 🔐 🌐 — Official GitHub MCP server. Access repos, issues, PRs, and code search.
- **[GitMCP](https://gitmcp.io)** ☁️ 🆓 — Turn any GitHub repository into an MCP server instantly.
- **[Sentry MCP](https://mcp.sentry.dev/sse)** ☁️ 🔐 — Query and manage Sentry issues directly from your AI assistant.

---

## Data & Databases

- **[Airtable MCP](https://airtable.com)** ☁️ 🔐 — Query and update Airtable bases remotely.
- **[Notion MCP](https://www.notion.so/product/notion-ai)** ☁️ 🔐 — Read and write Notion pages and databases.

---

## Productivity

- **[Linear MCP](https://linear.app/changelog/2025-03-18-mcp)** ☁️ 🔐 — Manage Linear issues, projects, and teams via AI.
- **[Atlassian MCP](https://www.atlassian.com)** ☁️ 🔐 — Jira and Confluence integration for AI assistants.

---

## AI & LLMs

- **[OpenAI MCP](https://openai.com)** ☁️ 🔐 — Access OpenAI models and fine-tuning APIs.
- **[Replicate MCP](https://replicate.com)** ☁️ 🔐 — Run thousands of AI models remotely.

---

## Finance

- **[Stripe MCP](https://docs.stripe.com/building-with-llms/mcp)** ☁️ 🔐 — Query Stripe payments, customers, and invoices.
- **[Coinbase MCP](https://www.coinbase.com)** ☁️ 🔐 — Crypto portfolio and market data.

---

## Communication

- **[Slack MCP](https://slack.com)** ☁️ 🔐 — Read and send Slack messages, manage channels.
- **[Resend MCP](https://resend.com/mcp)** ☁️ 🔐 — Send transactional emails via AI.

---

## Infrastructure & DevOps

- **[AWS MCP](https://github.com/awslabs/mcp)** ☁️ 🔐 🌐 — Official AWS MCP servers for S3, Lambda, CloudWatch and more.
- **[Azure MCP](https://github.com/microsoft/azure-mcp)** ☁️ 🔐 🌐 — Microsoft Azure resource management via MCP.
- **[Cloudflare MCP](https://github.com/cloudflare/mcp-server-cloudflare)** ☁️ 🔐 🌐 — Manage Cloudflare zones, workers, and KV remotely.
- **[Vercel MCP](https://vercel.com)** ☁️ 🔐 — Deploy and manage Vercel projects.

---

## Security

- **[Snyk MCP](https://snyk.io)** ☁️ 🔐 — Scan dependencies for vulnerabilities remotely.

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

### Criteria for inclusion

- **Must be remote** — The server must be accessible via a URL without local installation.
- **Must be functional** — No dead links or abandoned projects.
- **Must have a description** — Explain what the server does in one sentence.

### How to add a server

1. Fork this repository
2. Add your server to the appropriate category in `README.md`
3. Follow the existing format: `**[Name](URL)** badges — description`
4. Open a pull request

---

## Deploy Your Own

Want to host your own MCP server remotely?

👉 **[freemcp.space](https://freemcp.space)** — Deploy from Dockerfile or GitHub in seconds. Free tier available.

---

## Related Lists

- [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) — The original comprehensive list (local + remote)
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) — Official reference servers
- [best-of-mcp-servers](https://github.com/tolkonepiu/best-of-mcp-servers) — Weekly ranked list

---

## License

[CC0 1.0](LICENSE) — Public Domain
