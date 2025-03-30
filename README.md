# ChatGPT for Linux

> 🤖 **注意** 🤖  
> このリポジトリの内容は基本的にすべてAIによって作成されています

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
   git clone https://github.com/noppomario/chatgpt-linux-app.git
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

## ライセンス

このプロジェクトは[MITライセンス](https://github.com/noppomario/chatgpt-linux-app/blob/main/LICENSE)の下で公開されています。

## 貢献

バグ報告や機能要望は[Issue](https://github.com/noppomario/chatgpt-linux-app/issues)にて受け付けています。
PRも歓迎です！
