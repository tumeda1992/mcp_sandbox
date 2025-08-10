以下のライブラリを入れて、指示に従ってインストール
https://github.com/doriandarko/claude-search-mcp

ClaudeDesktopへの入れ方
```json
    "web_search": {
      "command": "/Users/username/.n/bin/node",
      "args": ["/Users/username/.n/lib/node_modules/claude-search-mcp/dist/index.js"],
      "env": {
        "ANTHROPIC_API_KEY": "sk-ant-api***"
      }
    }
```

ClaudeCodeでの組み込み
```sh
claude mcp add web_search -e ANTHROPIC_API_KEY="sk-ant-api***" -- "/Users/username/.n/bin/node" "/Users/username/.n/lib/node_modules/claude-search-mcp/dist/index.js"
```

- CLAUDE.mdの記法とか、自身でルール調べてもらって書いてもらうとかのため
- でも結構馬鹿だから、ChatGPTとかで調べた結果とかを載せたほうが早いな
  - 直接公式サイトのURL見に行くこととかできずに検索だけでなんとかしようとする
  - 下手な調べ方をするから、かなりトークンを食う