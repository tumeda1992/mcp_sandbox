# MCP登録方法
## ローカルMCP（npm経由で取得済みのものの実行も含む）
基本
```sh
claude mcp add notion_api -e OPENAPI_MCP_HEADERS="{\"Authorization\": \"Bearer ******\", \"Notion-Version\": \"2022-06-28\" }" -- "/Users/username/.n/bin/node" "/Users/username/.n/lib/node_modules/@notionhq/notion-mcp-server/bin/cli.mjs"
```

既にClaudeDesktopとかで登録済みの場合、そのjsonを直接登録([参考](https://docs.anthropic.com/ja/docs/claude-code/mcp#json%E8%A8%AD%E5%AE%9A%E3%81%8B%E3%82%89%E3%81%AEmcp%E3%82%B5%E3%83%BC%E3%83%90%E3%83%BC%E3%81%AE%E8%BF%BD%E5%8A%A0))
```sh
claude mcp add-json local_code '{"type":"stdio","command": "/Users/username/.n/bin/node","args": ["/Users/username/.n/lib/node_modules/@modelcontextprotocol/server-filesystem/dist/index.js","/Users/username/Desktop","/Users/username/Downloads"]}'
```

## リモートMCP
Coming Soon