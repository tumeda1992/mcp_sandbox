## MCP サーバーとしての weather の起動方法

このプロジェクトは [Claude Desktop](https://www.anthropic.com/products/claude-desktop) などのMCPクライアントから利用できます。

### 必要な準備

1. 依存パッケージのインストール
   - `uv` を使って依存関係をインストールしてください。
   - 例: `uv pip install -r requirements.txt` または `uv pip install .`

2. Claude Desktop の設定ファイルにMCPサーバーを追加
   - Macの場合: `~/Library/Application\ Support/Claude/claude_desktop_config.json` を編集します。
   - 以下のように `mcpServers` に `weather` サーバーを追加してください。

```json
{
  "mcpServers": {
    "weather": {
      "command": "uv",
      "args": [
        "--directory",
        "/ABSOLUTE/PATH/TO/PARENT/FOLDER/weather",
        "run",
        "weather.py"
      ]
    }
  }
}
```

> `/ABSOLUTE/PATH/TO/PARENT/FOLDER/weather` はこの `weather` ディレクトリの絶対パスに置き換えてください。

### 注意事項
- Python 3.13 以上が必要です。
- `uv` コマンドが必要です（`pip install uv` でインストール可能）。
- `weather.py` はMCPサーバーとして起動します。

### サーバーの手動起動例

```bash
uv --directory /ABSOLUTE/PATH/TO/PARENT/FOLDER/weather run weather.py
```

### 参考
- [Model Context Protocol (MCP)](https://modelcontextprotocol.org/)
