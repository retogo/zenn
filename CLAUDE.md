# zenn-content repo

Zenn (zenn.dev) の記事と本を GitHub integration 経由で同期するコンテンツリポジトリ。

## 構成

- `articles/<slug>.md` — 記事。slug は `[a-z0-9_-]{12,50}`
- `books/<slug>/` — 本。`config.yaml` + チャプター `.md`
- 本文ライセンス: CC BY 4.0（`LICENSE`）

## 記事 frontmatter

`title` / `emoji` / `type` (`tech` | `idea`) / `topics` (string[]) / `published` (bool)

## コマンド

- 新規作成: `bunx zenn new:article --slug <slug> --title <title> --type tech --emoji 🐕`
  - 手動で `articles/*.md` を作らない（slug 命名と frontmatter 規約のため）
- プレビュー: `bunx zenn preview`
- 整形: `bun run fmt` / `bun run fmt:check`（dprint）
- 校正: `bun run lint`（textlint: ja-technical-writing / ja-spacing / ai-writing）
