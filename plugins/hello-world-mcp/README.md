# Hello World MCP Plugin

シンプルな挨拶機能を提供するMCPサーバーのサンプルです。

## 概要

このプラグインは、MCPプロトコルを使用してClaude Codeに挨拶ツールを追加します。

## 提供ツール

### `greet`

指定した名前で挨拶を返します。

**パラメータ:**
- `name` (string, required): 挨拶する相手の名前

**使用例:**
```
greet({ name: "Alice" })
// => "Hello, Alice! Welcome to the team marketplace!"
```

## インストール

```bash
# プラグインをインストール
/plugin install hello-world-mcp
```

## 開発

```bash
# ローカルでテスト
echo '{"jsonrpc":"2.0","id":1,"method":"tools/list"}' | node server.js
```
