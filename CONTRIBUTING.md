# Contributing to awesome-remote-mcp-servers

Thank you for contributing to the registry! This repo is a curated list of MCP servers that can be automatically imported into [freemcp.space](https://freemcp.space).

## Quick Start

1. Fork this repository
2. Create a new JSON file under `servers/<category>/`
3. Validate your JSON against `schemas/server.schema.json`
4. Open a Pull Request using the provided template

## Directory Structure

```
servers/
  ai-agents/
  cloud-infra/
  communication/
  databases/
  data-processing/
  developer-tools/
  media/
  productivity/
  search/
  security/
```

Place your file as `servers/<category>/<kebab-case-name>.json`.

## JSON Schema

Required fields:
- `name` — Human-readable server name
- `description` — 10-500 characters describing what it does
- `git_url` — Canonical `https://github.com/owner/repo` URL
- `author_github` — GitHub username or org that **owns** the repository
- `category` — Must match one of the directories above
- `tags` — 1-10 lowercase tags
- `license` — SPDX identifier or license name
- `status` — `active` or `archived`

Optional fields:
- `npm_package` — Published npm package name
- `homepage` — Documentation or marketing site
- `env_keys` — Array of environment variable specs

### Environment Key Spec

```json
{
  "key": "API_KEY",
  "kind": "required",
  "description": "API key for authentication"
}
```

Kinds:
- `required` — Must be set for the server to run
- `optional` — Has a safe default; can be omitted
- `client` — Goes into the user's MCP client config, NOT the hosted container

## Ownership & Claims

You **do not** need a freemcp.space account to submit a server here. However:

- Only the real GitHub repo owner can **claim** the server on freemcp.space
- Claiming transfers ownership and marks the server as verified
- If you submit a server you don't own, the real owner can still claim it later

## Validation

Our CI checks every PR for:
- JSON Schema validity
- `git_url` returns HTTP 200
- `author_github` is present
- No duplicate `git_url` entries

## Sync to freemcp.space

After merge, all manifests are automatically synced to freemcp.space via `sync-freemcp.yml`.
