# 
[こちら](https://modelcontextprotocol.io/quickstart/user)を参考に作成

```/Users/username/Library/Application Support/Claude/claude_desktop_config.json
{
  "mcpServers": {
    "local_code": {
      "command": "/Users/username/.n/bin/node",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem/dist/index.js",
        "/Users/username/Desktop",
        "/Users/username/Downloads"
      ]
    }
  }
}
```



## トラブルシューティング
### env: node: No such file or directory
エラー発生時の書き方

```/Users/username/Library/Application Support/Claude/claude_desktop_config.json
{
  "mcpServers": {
    "local_code": {
      "command": "/Users/username/.n/bin/npx",
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

#### 原因
npxの場所はわかるけど、裏で動くnodeがわからなかったとのこと。
ログインユーザと違うユーザが実行しているからPATHが違うのだろう

#### 対応
npxを使わずに、直接nodeを指定する。

`npm install -g @modelcontextprotocol/server-filesystem`

```/Users/username/Library/Application Support/Claude/claude_desktop_config.json
{
  "mcpServers": {
    "local_code": {
      "command": "/Users/username/.n/bin/node",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem/dist/index.js",
        "/Users/username/Desktop",
        "/Users/username/Downloads"
      ]
    }
  }
}
```

ターミナルから、ログインユーザが`open -a "Claude"`を行ってPATHを引き継いだ状態で起動する、という一時的な対策もある。