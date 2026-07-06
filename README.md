# corporate-site

Learn Your Next LLC のコーポレートサイト。

## 構成
- `index.html` — 1ページ構成（Hero / できること / 私たちについて / お問い合わせ / フッター）
- `assets/css/style.css` — スタイル一式
- `assets/img/` — ブランドロゴ（[LYN-Brand-Logo](https://github.com/learnyournext/LYN-Brand-Logo)から取り込み）
- `robots.txt` / `llms.txt` — クロール・AI向けの最小セット

ビルド不要の静的HTMLのみで構成。ローカル確認は `index.html` をブラウザで直接開くか、
任意の静的サーバー（例: `npx serve .`）で確認する。

## デプロイ（予定）
S3 + CloudFront での配信を想定。`index.html` を含む本ディレクトリ一式をS3バケットに配置し、
CloudFrontから配信する。

## 未確定・要差し替え
- `index.html` 内のお問い合わせ用メールアドレス（`contact@example.com`）は仮の値。実際の連絡先に差し替えが必要。
- 「できること」3項目の文言は [second-brain#453](https://github.com/n-guitar/second-brain/issues/453) の骨格案に基づく仮コピー。実際のサービス内容に合わせて要調整。
- 独自ドメイン確定後、`index.html` のJSON-LDに `url` プロパティを追加する。
