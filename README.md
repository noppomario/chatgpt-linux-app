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

- Node.js 18以上
- Rust 1.77.2以上
- 以下のLinuxパッケージ:
  - webkit2gtk-4.0
  - libwebkit2gtk-4.0-dev
  - libgtk-3-dev
  - libayatana-appindicator3-dev
  - librsvg2-dev
  - libsoup-3.0-dev
  - libjavascriptcoregtk-4.1-dev
  - libappindicator3-dev
  - libasound2-dev
  - libssl-dev

### インストール手順

1. 必要なパッケージのインストール:

   ```bash
   # Debian/Ubuntu系
   sudo apt-get update
   sudo apt-get install webkit2gtk-4.0 libwebkit2gtk-4.0-dev libgtk-3-dev libayatana-appindicator3-dev librsvg2-dev libsoup-3.0-dev libjavascriptcoregtk-4.1-dev libappindicator3-dev libasound2-dev libssl-dev

   # Fedora/RHEL系
   sudo dnf install webkit2gtk4.1-devel gtk3-devel libappindicator-gtk3-devel librsvg2-devel libsoup3-devel javascriptcoregtk4.1-devel alsa-lib-devel openssl-devel
   ```

2. リポジトリのクローン:

   ```bash
   git clone https://github.com/noppomario/chatgpt-linux-app.git
   cd chatgpt-linux-app
   ```

3. 依存関係のインストール:

   ```bash
   npm install
   ```

4. 開発モードで実行:

   ```bash
   npm run tauri dev
   ```

5. ビルド:

   ```bash
   npm run tauri build
   ```

## ライセンス

このプロジェクトは[MITライセンス](https://github.com/noppomario/chatgpt-linux-app/blob/main/LICENSE)の下で公開されています。

## 貢献

バグ報告や機能要望は[Issue](https://github.com/noppomario/chatgpt-linux-app/issues)にて受け付けています。
PRも歓迎です！
