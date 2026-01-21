# CLAUDE.md

morixx.dev 技術ブログプロジェクトの開発ガイドライン

## 実装計画

- **詳細計画**: `plans/soft-zooming-plum.md`
- **メモリ**: `.claude/skills/agent-memory/memories/project-context/morixx-dev-blog-plan.md`

## プロジェクト概要

- **サイト名**: morixx.dev
- **種類**: 技術ブログ
- **フレームワーク**: Astro
- **コンテンツ管理**: MDXファイルベース
- **デプロイ先**: Netlify

## 技術スタック

- **フレームワーク**: Astro (コンテンツ重視の静的サイト生成)
- **コンテンツフォーマット**: MDX (Markdown + JSX)
- **スタイリング**: 未定 (Tailwind CSS推奨)
- **ホスティング**: Netlify

## ディレクトリ構成 (予定)

```
morixx_dev/
├── src/
│   ├── components/     # 再利用可能なUIコンポーネント
│   ├── layouts/        # ページレイアウト
│   ├── pages/          # ルーティング用ページ
│   └── content/        # MDXブログ記事
│       └── blog/       # ブログ記事 (.mdx)
├── public/             # 静的アセット (画像など)
├── astro.config.mjs    # Astro設定
├── netlify.toml        # Netlify設定
└── package.json
```

## 開発コマンド

```bash
# 依存関係のインストール
npm install

# 開発サーバー起動
npm run dev

# 本番ビルド
npm run build

# ビルドプレビュー
npm run preview
```

## ブログ記事の追加方法

1. `src/content/blog/` に新しい `.mdx` ファイルを作成
2. frontmatterにタイトル、日付、タグなどのメタデータを記載
3. 本文をMarkdown/MDX形式で記述

### frontmatter例

```yaml
---
title: "記事タイトル"
description: "記事の説明"
pubDate: 2026-01-21
tags: ["astro", "blog"]
draft: false
---
```

## デプロイフロー

- mainブランチへのプッシュでNetlifyが自動デプロイ
- プルリクエスト時にプレビューデプロイが作成される

## 開発方針

- シンプルで高速な読み込みを重視
- SEO対策を意識したメタタグの設定
- アクセシビリティを考慮したマークアップ
- モバイルファーストのレスポンシブデザイン
