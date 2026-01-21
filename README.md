# morixx.dev

技術ブログ [morixx.dev](https://morixx.dev) のソースコードです。

## 技術スタック

- **Astro** - 静的サイト生成フレームワーク
- **MDX** - Markdown + JSX
- **Tailwind CSS** - スタイリング
- **Netlify** - ホスティング

## 開発

```bash
# 依存関係のインストール
npm install

# 開発サーバー起動 (http://localhost:4321)
npm run dev

# 本番ビルド
npm run build

# ビルドプレビュー
npm run preview
```

## 記事の追加

`src/blog/` に `.mdx` ファイルを作成:

```yaml
---
title: "記事タイトル"
description: "記事の説明"
pubDate: 2026-01-21
tags: ["tag1", "tag2"]
draft: false
---

本文をここに記述...
```

## ディレクトリ構成

```
src/
├── blog/           # MDX記事ファイル
├── components/     # UIコンポーネント
├── layouts/        # ページレイアウト
├── pages/          # ルーティング
└── styles/         # グローバルCSS
```
