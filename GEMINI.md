# BoardMark

BoardMark is an issue board: projects, issues, comments, sprints and project docs stored as markdown files. The `boardmark` MCP server works with exactly the rights of the signed-in user.

- First use: run `/mcp auth boardmark` and finish the sign-in in the browser (pick the company, optionally a role).
- Find work with `list_projects`, `list_my_issues` and `search_issues`; read an issue with `get_issue`.
- Every change takes the `version` from your latest read (`get_issue` before `update_issue`). On `409 version_conflict`, read again and re-apply.
- Status ids come from `get_project`; never guess them.
- Before working on an unfamiliar project, `get_docs_context` gives its briefs, notes, handoffs and what each status means.

Full guide: https://mcp.boardmark.ai/connect.md
