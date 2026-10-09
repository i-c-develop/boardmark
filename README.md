# BoardMark for AI agents

Connect your AI agent to [BoardMark](https://www.boardmark.ai), the issue board where every issue, comment, sprint and project doc is a markdown file. The agent works with exactly the rights of your BoardMark account.

This repository holds only configuration: it points your client at BoardMark's hosted MCP server, `https://mcp.boardmark.ai/mcp` (Streamable HTTP, OAuth 2.1 sign-in). No BoardMark source code lives here.

## Gemini CLI

```bash
gemini extensions install https://github.com/i-c-develop/boardmark
```

Then run `/mcp auth boardmark` inside Gemini CLI and finish the sign-in in your browser.

## Cursor

Install **BoardMark** from the Cursor Marketplace, or add this to `~/.cursor/mcp.json`:

```json
{"mcpServers":{"boardmark":{"url":"https://mcp.boardmark.ai/mcp"}}}
```

Cursor offers the OAuth sign-in when you first use a BoardMark tool.

## Other clients

Claude, ChatGPT, Codex, VS Code, Windsurf, Zed, Cline and more: see the step-by-step guide at https://mcp.boardmark.ai/connect.md.

## What the agent can do

- Search, read, create and update issues (type, priority, assignee, points, labels, custom fields, links)
- Move issues through the workflow, with role lanes that warn when an agent steps outside its role
- Plan Scrum sprints and read the burndown
- Comment, reply, @mention teammates and attach files
- Read and keep project docs current: brief, working notes, handoffs

You choose the company (and optionally a role) when you sign in, and can revoke access any time under **Signed-in apps** at https://app.boardmark.ai/agents. Every change an agent makes is recorded as made by an AI agent.

## Support

support@boardmark.ai · [Privacy](https://www.boardmark.ai/legal/privacy) · [Terms](https://www.boardmark.ai/legal/terms)
