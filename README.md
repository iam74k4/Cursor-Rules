# Cursor Rules 設定

プロジェクト間で一貫した開発プラクティスを維持するためのCursor IDEルールです。

## フォルダ構造

```
.cursor/
├── rules/
│   ├── git-rules.mdc      # Gitルール
│   ├── coding-rules.mdc   # コーディングルール
│   ├── readme-rules.mdc   # READMEルール
│   └── ci-rules.mdc       # CI/CDルール
└── commands/
    └── github-build.md    # GitHub Actionsワークフロー生成
```

## ルール概要

| ファイル | 内容 |
|----------|------|
| `git-rules.mdc` | コミットメッセージ、ブランチ命名 |
| `coding-rules.mdc` | コード品質、ターミナル、言語設定 |
| `readme-rules.mdc` | README構造、Shields.ioバッジ、マークダウン記法 |
| `ci-rules.mdc` | GitHub Actions、CI/CDベストプラクティス |

## 使い方

ワークスペースにこのリポジトリを追加:

```json
{
  "folders": [
    { "name": "YourProject", "path": "../YourProject" },
    { "path": "." }
  ]
}
```

## 主要な規約

### コミットメッセージ
```
feat: 新機能
fix: バグ修正
docs: ドキュメント
refactor: リファクタリング
test: テスト
chore: メンテナンス
```

### 言語設定
- 応答: 日本語
- コード・コメント: 英語

### ターミナル（PowerShell）
- `&&`は使用不可、`;`か分割で対応

### README
- 必須セクション: バッジ、概要、インストール、使い方、ライセンス
- Shields.ioバッジをタイトル直下に配置
- コードブロックには言語指定を必須
- 画像にはaltテキストを設定

### CI/CD
- ワークフローファイルは `.github/workflows/` に配置
- タグベースのリリースを推奨
- バージョン管理: セマンティックバージョニング、タグから自動抽出
- セキュリティ: GITHUB_TOKENの適切な使用、権限の最小化
- パフォーマンス: キャッシュの活用、並列ビルド
