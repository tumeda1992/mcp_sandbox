https://github.com/makenotion/notion-mcp-server?tab=readme-ov-file

以下を追加

```/Users/username/Library/Application Support/Claude/claude_desktop_config.json
{
  "mcpServers": {
    "notion_api": {
      "command": "/Users/takahiroumeda/.n/bin/node",
      "args": ["/Users/takahiroumeda/.n/lib/node_modules/@notionhq/notion-mcp-server/bin/cli.mjs"],
      "env": {
        "OPENAPI_MCP_HEADERS": "{\"Authorization\": \"Bearer ntn_****\", \"Notion-Version\": \"2022-06-28\" }"
      }
    }
  }
}
```

