# corporate-site

Learn Your Next 合同会社 のコーポレートサイト。

## 公開URL
- https://corp.learnyournext.com/ （独自ドメイン。SquarespaceのDNSに `CNAME corp → learnyournext.github.io` を追加後に有効化）
- https://learnyournext.github.io/corporate-site/ （GitHub Pagesの既定URL）

## 構成
- `index.html` — 1ページ構成（Hero / できること / 私たちについて / 会社概要 / お問い合わせ / フッター）
- `assets/css/style.css` — スタイル一式
- `assets/img/` — ブランドロゴ（[LYN-Brand-Logo](https://github.com/learnyournext/LYN-Brand-Logo)から取り込み）
- `robots.txt` / `llms.txt` — クロール・AI向けの最小セット

ビルド不要の静的HTMLのみで構成。ローカル確認は `index.html` をブラウザで直接開くか、
任意の静的サーバー（例: `npx serve .`）で確認する。

## デプロイ
現在: GitHub Pages（`main`ブランチ、リポジトリはpublic）で公開中。
最終的にはS3 + CloudFrontでの配信を想定。`index.html` を含む本ディレクトリ一式をS3バケットに配置し、
CloudFrontから配信する。

## 未確定
- `corp.learnyournext.com` のDNS（SquarespaceのCNAME追加）は要対応。追加済みならGitHub Pages側でEnforce HTTPSを有効化する。
- 「できること」3項目の文言は仮コピー。実際のサービス内容（会社概要の事業内容を参照）に合わせて要調整。
