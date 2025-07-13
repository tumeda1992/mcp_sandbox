`~/Library/Application\ Support/Claude/claude_desktop_config.json`に以下のように記載

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "/path/to/dir/npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/Users/username/Desktop",
        "/Users/username/Downloads"
      ]
    }
  }
}
```

補足
- usernameについては要書き換え
- nodeが入っていなければ動かない
  - トラブルシューティング: `env: node: No such file or directory`
    - (原因)Claude Desktopを開くユーザがログインユーザのPATHを共用していないかもしれないため
    - (対応)ターミナルから、ログインユーザが`open -a "Claude"`を行ってPATHを引き継いだ状態で起動する
- [こちら](https://modelcontextprotocol.io/quickstart/user)を参照した