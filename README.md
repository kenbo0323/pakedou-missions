# pakedou-missions

パケ道「今日の障害」の配信データです。Cloudflare Workers の静的アセットとして https://pakedou-missions.com/ に公開されます。

- `public/missions/index.json` — 配信中のミッション一覧 (`latest` は最新の日付)
- `public/missions/<日付>.json` — その日の問題 (構成、チェック、ルール、16言語の本文)
- `public/m/<番号>/index.html` — 共有リンクの着地ページ (タイトルと状況だけ。ヒントと解説はアプリの中)
- `public/index.html`, `public/404.html`, `public/robots.txt`, `public/_headers`
- `wrangler.jsonc`, `package.json` — Workers Builds が `npx wrangler deploy` で使う (アセットのみ、スクリプトなし)

ブランチ `main` が本番、`staging` はプレビュー URL で確認するためのものです。ファイルは自動生成されるので手で編集しません。
