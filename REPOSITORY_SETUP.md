# GitHub リポジトリセットアップ計画

## ディレクトリ構造
```
.github/
├── ISSUE_TEMPLATE/
│   ├── bug_report.md
│   └── feature_request.md
├── workflows/
│   └── build.yml
└── pull_request_template.md
```

## 作成すべきファイルの内容

### 1. バグ報告テンプレート (.github/ISSUE_TEMPLATE/bug_report.md)
```markdown
---
name: バグ報告
about: アプリケーションの問題点を報告
title: '[BUG] '
labels: bug
assignees: ''
---

## バグの説明
問題の内容を明確かつ簡潔に説明してください。

## 再現手順
1. '...' に移動
2. '....' をクリック
3. '....' をスクロール
4. エラーの確認

## 期待される動作
何が起こるべきだったのかを説明してください。

## スクリーンショット
可能であれば、問題を説明するスクリーンショットを追加してください。

## 実行環境
- OS: [例: Fedora 37]
- アプリケーションバージョン: [例: 0.1.0]
```

### 2. 機能リクエストテンプレート (.github/ISSUE_TEMPLATE/feature_request.md)
```markdown
---
name: 機能リクエスト
about: このプロジェクトへのアイデアの提案
title: '[FEATURE] '
labels: enhancement
assignees: ''
---

## 関連する問題
この機能リクエストは問題に関連していますか？説明してください。

## 解決策の提案
実現したい機能について説明してください。

## 代替案の検討
検討した他の解決策や機能があれば説明してください。

## その他の文脈
機能リクエストに関する他の文脈やスクリーンショットをここに追加してください。
```

### 3. PRテンプレート (.github/pull_request_template.md)
```markdown
## 変更の種類
- [ ] バグ修正
- [ ] 新機能
- [ ] 破壊的変更
- [ ] ドキュメント更新

## 変更内容
変更の内容とその理由を説明してください。

## 影響範囲
この変更によって影響を受ける部分を説明してください。

## チェックリスト
- [ ] テストを追加/更新しました
- [ ] ドキュメントを更新しました
- [ ] コードレビューを依頼しました
```

### 4. GitHub Actionsワークフロー (.github/workflows/build.yml)
```yaml
name: Build

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Setup Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '18'

    - name: Install Rust
      uses: actions-rs/toolchain@v1
      with:
        toolchain: stable
        override: true

    - name: Install dependencies
      run: |
        sudo apt-get update
        sudo apt-get install -y webkit2gtk-4.0 libayatana-appindicator3-dev librsvg2-dev

    - name: Install npm dependencies
      run: npm install

    - name: Build
      run: npm run tauri build

    - name: Upload artifacts
      uses: actions/upload-artifact@v2
      with:
        name: linux-build
        path: src-tauri/target/release/bundle/
```

## 実装手順

1. `.github`ディレクトリの作成
2. 上記の各テンプレートファイルの作成
3. GitHubリポジトリでの設定確認
   - Issuesの有効化
   - GitHub Actionsの有効化
   - ブランチ保護ルールの設定

## セキュリティ設定

1. 依存関係の自動更新
   - Dependabotの有効化
   - セキュリティアラートの有効化

2. ブランチ保護
   - メインブランチへの直接プッシュを禁止
   - PRのレビュー必須化
   - CIパス必須化