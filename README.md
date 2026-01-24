# Claude Code Marketplace

個人用のClaude Codeスキル・プラグインマーケットプレイス

## インストール

```bash
# ローカルディレクトリから
/plugin marketplace add /path/to/claude-code-marketplace

# GitHubリポジトリから
/plugin marketplace add owner/claude-code-marketplace
```

## ディレクトリ構造

```
claude-code-marketplace/
├── .claude-plugin/
│   └── marketplace.json    # マーケットプレイス設定
├── skills/                 # スキル（プロンプトテンプレート）
│   └── hello-world/
│       ├── skill.md
│       └── README.md
├── plugins/                # プラグイン（MCPサーバー等）
│   └── hello-world-mcp/
│       ├── plugin.json
│       ├── server.js
│       └── README.md
├── CONTRIBUTING.md         # 貢献ガイドライン
└── README.md
```

## 利用可能なスキル

| 名前 | 説明 | カテゴリ |
|------|------|----------|
| hello-world | シンプルな挨拶スキル | examples |

## 利用可能なプラグイン

| 名前 | 説明 | カテゴリ |
|------|------|----------|
| hello-world-mcp | シンプルな挨拶MCPサーバー | examples |

## 貢献方法

新しいスキルやプラグインを追加する場合は、[CONTRIBUTING.md](./CONTRIBUTING.md) を参照してください。

## 参考資料

- [Claude Code - プラグインマーケットプレイス](https://code.claude.com/docs/ja/plugin-marketplaces)
- [Anthropic公式スキルリポジトリ](https://github.com/anthropics/skills)
