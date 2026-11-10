# bgp-mcp

Stateless MCP server for BGP data, running on Cloudflare Workers. Each request builds a fresh `McpServer` via `createMcpHandler` from the Agents SDK — no Durable Objects or sessions.

## Usage

```sh
bun install
bun run dev      # http://localhost:8787/mcp
bun run deploy
```

Connect a client:

```sh
claude mcp add --transport http bgp https://bgp-mcp.<account>.workers.dev/mcp
```
