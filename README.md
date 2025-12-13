# Cursor Rules 設定

プロジェクト間で一貫した開発プラクティスを維持するためのCursor IDEルールです。

## フォルダ構造

```
.cursor/
└── rules/
    ├── git-rules.mdc      # Gitルール
    └── coding-rules.mdc   # コーディングルール
```

## ルール概要

| ファイル | 内容 |
|----------|------|
| `git-rules.mdc` | コミットメッセージ、ブランチ命名 |
| `coding-rules.mdc` | コード品質、ターミナル、言語設定 |

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
