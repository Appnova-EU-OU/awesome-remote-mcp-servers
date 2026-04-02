# Contributing

## The one rule

**Only remote servers.** If someone needs to run `npx`, `pip install`, or `docker run` on their own machine, it doesn't belong here. That's what [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) is for.

## What qualifies

- Accessible via a public URL (SSE or HTTP transport)
- Active and responding
- Has a stable endpoint (not a personal demo)

## Entry format

```
- **[Name](https://url.com)** badges — One sentence. What can you do with it?
  `https://the-actual-mcp-endpoint/path`
```

Include the actual MCP endpoint URL if it's different from the homepage.

## Badges

| Badge | Use when |
|-------|---------|
| 🆓 | Free tier exists |
| 💰 | Paid only |
| 🔑 | Requires API key or auth |
| 🌐 | Source code is public |
| ✅ | You've personally verified it works |

## Pull request

Title: `Add [Server Name]`

Check before submitting:
- [ ] The endpoint URL responds
- [ ] It's in the right category
- [ ] Alphabetical order within the category
- [ ] Description is one sentence max
