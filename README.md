# Self Care Log - Mobile

スマホからアクセスできるセルフケアログのフロントエンド。

## 概要

`https://take1998hikaru.github.io/selflog-mobile/` でアクセスできるPWA風アプリ。  
データは GitHub Gist に保存され、PCの本体（[selflogapp](https://github.com/take1998hikaru/selflogapp)）と同期される。

## 機能

- 朝ログ・夜ログ・つぶやき・日記の入力
- Gist 経由で PC ↔ スマホ間データ同期
- ローカル localStorage でオフラインも動作

## 制限事項（モバイル時）

- SwitchBot 連携はPCローカル限定（モバイルではSwitchBot UI動作せず）
- 週次レポート出力はPC限定
- 朝の天気自動取得は機能制限あり

## 設定方法（初回のみ）

1. このページを開く
2. GitHubの **Personal Access Token (gist スコープ)** を入力
3. PC側と同じ **Gist ID** を入力
4. 同期 → 既存ログが取得される

## ファイル構成

- `index.html` - メインアプリ（React + Babel CDN）
- `styles.css` - スタイル
- `gist-setup.html` - Gist 設定ヘルプ

## 注意

- 個人ログデータはこのリポジトリには含まれない（Gist で別途管理）
- API キー・トークン類はソースに含めない（localStorage 管理）
- リポジトリは Public だが、データへのアクセスは PAT を持つ本人のみ
