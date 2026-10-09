# Installing BoardMark for Cline

BoardMark is a hosted MCP server; there is nothing to clone, build or run locally.

1. Ask the user to create a personal access token at https://app.boardmark.ai/agents (Agent & MCP → New token). Optionally give the token the role the agent works as (Developer, QA, …). Do not ask them to paste the token into the chat if you can avoid it; it starts with `board_pat_`.
2. Add this server to Cline's MCP settings (`cline_mcp_settings.json`), replacing `<token>`:

```json
{
  "mcpServers": {
    "boardmark": {
      "type": "streamableHttp",
      "url": "https://mcp.boardmark.ai/mcp",
      "headers": { "Authorization": "Bearer <token>" }
    }
  }
}
```

3. Verify: list the tools (expect `list_projects`, `get_issue`, …) and call `list_projects`.
4. Before working on a project, call `get_docs_context` with its key for the project's briefs, notes, handoffs and status meanings.

Full guide for every client: https://mcp.boardmark.ai/connect.md
