# Claude Code Marketplace

個人的なClaude Codeマーケットプレイス - スキルのコレクション

## インストール

```bash
# ローカルディレクトリから
/plugin marketplace add /path/to/claude-code-marketplace

# GitHubリポジトリから（公開している場合）
/plugin marketplace add owner/repo
```

## ディレクトリ構造

```
claude-code-marketplace/
├── .claude-plugin/
│   └── marketplace.json
└── skills/
```

## スキルの追加

```bash
# skill-creatorで作成
/skill-creator

# リポジトリに追加
cp -r /path/to/created-skill skills/your-skill-name
```

## プラグインの追加

プラグインは別のGitHubリポジトリで管理し、`.claude-plugin/marketplace.json`から参照します:

```json
{
  "plugins": [
    {
      "name": "your-plugin-name",
      "source": {
        "source": "github",
        "repo": "owner/plugin-repo"
      },
      "description": "プラグインの説明",
      "version": "1.0.0"
    }
  ]
}
```

## 参考資料

- [Claude Code - プラグインマーケットプレイス](https://code.claude.com/docs/ja/plugin-marketplaces)
- [Anthropic公式スキルリポジトリ](https://github.com/anthropics/skills)
