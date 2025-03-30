# ChatGPT for Linux

ChatGPTをLinux向けデスクトップアプリケーションとして提供するプロジェクトです。TauriフレームワークとWebViewを使用して実装されています。

## 機能

- ChatGPTのウェブインターフェースをネイティブアプリケーションとして提供
- ウィンドウサイズは1200x800でリサイズ可能
- Debian/RedHat系Linuxディストリビューションに対応

## 開発環境のセットアップ

### 必要なソフトウェア

- Node.js 16以上
- Rust
- 以下のLinuxパッケージ:
  - webkit2gtk4.1-devel
  - libsoup3-devel
  - その他Tauriの依存パッケージ

### インストール手順

1. リポジトリのクローン:
```bash
git clone https://github.com/[username]/chatgpt-linux-app.git
cd chatgpt-linux-app
```

2. 依存関係のインストール:
```bash
npm install
```

3. 開発モードで実行:
```bash
npm run tauri dev
```

4. ビルド:
```bash
npm run tauri build
```

## GitHub登録前の作業項目

1. ファイル整理
   - [x] プロジェクト構造の確認
   - [ ] .gitignoreの更新（Code modeで実施）
     - Tauriビルド成果物の除外
     - Rust関連ファイルの除外
   - [ ] 不要なファイルの削除

2. ドキュメント作成
   - [x] README.mdの作成（基本情報）
   - [ ] インストール手順の詳細化
   - [ ] トラブルシューティングガイドの追加

3. ライセンス
   - [ ] オープンソースライセンスの選択（MIT推奨）
   - [ ] LICENSE.mdファイルの作成

4. リポジトリ設定
   - [ ] GitHub Actionsワークフローの作成
   - [ ] Issue・PRテンプレートの作成

## ライセンス

このプロジェクトは[MITライセンス](LICENSE.md)の下で公開されています。

## 貢献

バグ報告や機能要望は[Issue](https://github.com/[username]/chatgpt-linux-app/issues)にて受け付けています。
PRも歓迎です！
