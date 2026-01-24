# 貢献ガイドライン

チームマーケットプレイスへの貢献方法を説明します。

## スキルの追加

### 1. ディレクトリ作成

```bash
mkdir skills/your-skill-name
```

### 2. 必要なファイル

```
skills/your-skill-name/
├── skill.md      # スキル本体（必須）
└── README.md     # 使い方の説明（推奨）
```

### 3. skill.md の書き方

```markdown
# スキル名

スキルの説明と指示をここに記述します。

## 動作

- ルール1
- ルール2

## 例

具体的な使用例を記述します。
```

### 4. marketplace.json への登録

`.claude-plugin/marketplace.json` の `skills` 配列に追加：

```json
{
  "name": "your-skill-name",
  "version": "1.0.0",
  "description": "スキルの説明",
  "path": "skills/your-skill-name/skill.md",
  "category": "カテゴリ名"
}
```

## プラグインの追加

### 1. ディレクトリ作成

```bash
mkdir plugins/your-plugin-name
```

### 2. 必要なファイル

```
plugins/your-plugin-name/
├── plugin.json   # プラグイン設定（必須）
├── README.md     # 使い方の説明（推奨）
└── server.js     # MCPサーバー実装（必要な場合）
```

### 3. plugin.json の書き方

```json
{
  "name": "your-plugin-name",
  "version": "1.0.0",
  "description": "プラグインの説明",
  "type": "mcp",
  "mcp": {
    "command": "node",
    "args": ["server.js"],
    "cwd": "plugins/your-plugin-name"
  }
}
```

### 4. marketplace.json への登録

`.claude-plugin/marketplace.json` の `plugins` 配列に追加：

```json
{
  "name": "your-plugin-name",
  "version": "1.0.0",
  "description": "プラグインの説明",
  "path": "plugins/your-plugin-name",
  "category": "カテゴリ名"
}
```

## カテゴリ一覧

| カテゴリ | 用途 |
|---------|------|
| `examples` | サンプル・テンプレート |
| `coding` | コーディング支援 |
| `review` | コードレビュー |
| `documentation` | ドキュメント作成 |
| `testing` | テスト支援 |
| `team-specific` | チーム固有のワークフロー |

## レビュープロセス

1. 新しいブランチを作成
2. スキル/プラグインを追加
3. Pull Requestを作成
4. チームメンバーのレビューを受ける
5. マージ
