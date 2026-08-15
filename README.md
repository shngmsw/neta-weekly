# neta-weekly

週次トレンドダイジェストの公開用リポジトリ。GitHub Pages でダイジェストを HTML 公開する。

**これは公開リポジトリです。秘匿情報・取引先固有名詞を絶対に含めないでください。**

## 構成

```
docs/
  index.html          バックナンバー一覧
  assets/
    digest.css         共通スタイル
    template.html       週次ダイジェスト生成用テンプレート
  YYYY-MM-DD.html       週次ダイジェスト本体（号ごとに追加）
```

## GitHub Pages の設定

1. GitHub の当該リポジトリで Settings > Pages を開く
2. Source を `Deploy from a branch` に設定
3. Branch を `main` / フォルダを `/docs` に設定
4. Save 後、`https://<user>.github.io/neta-weekly/` で公開される

## 運用

週次ダイジェストの生成・公開は `neta-trend`（private repo）側の Claude Routines スキル
`neta-trend-weekly-digest` から行う。このリポジトリへの直接編集は基本的に発生しない。

- 新しい号は `docs/YYYY-MM-DD.html` として追加
- `docs/index.html` の一覧に新しい号へのリンクを先頭（新しい号が上）に追加
