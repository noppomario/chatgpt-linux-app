<div align="center">
  <img src="src-tauri/icons/128x128.png" alt="ChatGPT for Linux" width="128" height="128">

  # ChatGPT for Linux

  [![Version](https://img.shields.io/github/v/release/noppomario/chatgpt-linux-app?style=flat-square)](https://github.com/noppomario/chatgpt-linux-app/releases) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT) [![Tauri](https://img.shields.io/badge/Built%20with-Tauri-blue?style=flat-square)](https://tauri.app)

  🚀 ChatGPTをLinuxデスクトップで快適に使用するためのネイティブアプリケーション
</div>

> 🤖 **注意** 🤖
> このリポジトリの内容は基本的にすべてAIによって作成されています

## 📝 概要

ChatGPTをLinux向けデスクトップアプリケーションとして提供するプロジェクトです。TauriフレームワークとWebViewを使用して、軽量かつネイティブな体験を実現しています。

## ✨ クイックスタート

### 📥 パッケージからインストール

[リリースページ](https://github.com/noppomario/chatgpt-linux-app/releases/latest)からダウンロードしてインストールしてください。

## ⭐ 主な機能

- 🌐 ChatGPTのウェブインターフェースをネイティブアプリケーションとして提供
- 📱 ウィンドウサイズは1200x800でリサイズ可能
- 🐧 Debian/RedHat系Linuxディストリビューションに対応
- 🔒 プライバシーを重視したローカルでの動作
- 🚀 軽量で高速な動作を実現

## 🛠️ 開発環境のセットアップ

### 📋 必要な環境

- 📦 **Node.js** 18以上
- ⚙️ **Rust** 1.77.2以上
- 🐧 **Linuxパッケージ**:

  ```bash
  # 📥 Debian/Ubuntu系
  sudo apt-get install webkit2gtk-4.0 \
                       libwebkit2gtk-4.0-dev \
                       libgtk-3-dev \
                       libayatana-appindicator3-dev \
                       librsvg2-dev \
                       libsoup-3.0-dev \
                       libjavascriptcoregtk-4.1-dev \
                       libappindicator3-dev \
                       libasound2-dev \
                       libssl-dev

  # 📥 Fedora/RHEL系
  sudo dnf install webkit2gtk4.1-devel \
                   gtk3-devel \
                   libappindicator-gtk3-devel \
                   librsvg2-devel \
                   libsoup3-devel \
                   javascriptcoregtk4.1-devel \
                   alsa-lib-devel \
                   openssl-devel
  ```

### 🚀 開発の始め方

1. 📥 **リポジトリのクローン**

   ```bash
   git clone https://github.com/noppomario/chatgpt-linux-app.git
   cd chatgpt-linux-app
   ```

2. 📦 **依存関係のインストール**

   ```bash
   npm install
   ```

3. 🔧 **開発モードで実行**

   ```bash
   npm run tauri dev
   ```

4. 📦 **ビルド**

   ```bash
   npm run tauri build
   ```

## 📜 ライセンス

このプロジェクトは [MIT License](LICENSE) の下で公開されています。詳細は[ライセンスファイル](LICENSE)をご確認ください。

## 🤝 コントリビューション

私たちはオープンソースコミュニティからのコントリビューションを歓迎します！

- 🐛 **バグを見つけた場合**: [Issue](https://github.com/noppomario/chatgpt-linux-app/issues) を作成してください
- 💡 **新機能の提案**: [Issue](https://github.com/noppomario/chatgpt-linux-app/issues) で機能の提案をしてください
- 🔧 **コードの改善**: プルリクエストを送信してください
- 📖 **ドキュメントの改善**: タイプミスや説明の改善など、ドキュメントの質を高めるPRを歓迎します

**開発プロセス**:

1. このリポジトリをフォーク
2. `main`ブランチから作業用ブランチを作成
3. 変更を加えてコミット
4. プルリクエストを作成

すべてのコントリビューションに感謝いたします！ 🙏
