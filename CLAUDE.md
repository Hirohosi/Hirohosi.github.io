# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 概要

GitHub Pages で公開される静的サイト。2つのiOSアプリ（Kokorolog / Yumetoki）のサポートページ・法的ドキュメントをホスティングする。ビルドツール・パッケージマネージャー・テストフレームワークは存在しない。

## デプロイ

```bash
git add <files>
git commit -m "message"
git push origin main
```

`main` ブランチへのプッシュで GitHub Pages に自動反映される。

## プロジェクト構成

```
kokorolog/          # ココロログ（感情ジャーナルアプリ）
  index.html        # トップ（サポートページ）
  support.html      # サポートページ（index.htmlと同内容）
  privacy-policy.html
  terms-of-service.html

Yumetoki/           # 夢解きアプリ
  index.html        # トップ（サポートページ）
  privacy-policy.html
  terms-of-service.html

app-ads.txt         # Google Ad Publisher 設定
DOCS/               # .gitignore済み。Markdown原稿（git管理外）
```

## コードの特徴

- 全ファイルがインラインCSSを持つ単体HTMLファイル（共有CSSなし）
- 外部依存はGoogleフォントのみ（kokorolog/index.htmlのみ）
- privacy-policy.html / terms-of-service.html は日本語・英語の2言語構成
- kokorolog カラー: `#667eea` → `#764ba2`（紫グラデーション）
- Yumetoki カラー: `#4F46E5` → `#7C3AED`（インディゴグラデーション）

## 注意事項

- `DOCS/` はgit管理外（.gitignoreで除外）。Markdown原稿が置かれているが公開はされない
- ルートに `gitignore`（先頭ドットなし）という古いファイルが残っている。実際の設定は `.gitignore`
