# discord-persona-icons

Discord の Webhook で、投稿ごとにアイコンを切り替えるための画像置き場です。

## 使い方

Webhook に送る JSON の `avatar_url` に、下の形の URL を入れます。

    https://raw.githubusercontent.com/taroatwork/discord-persona-icons/main/icons/<ファイル名>

ペルソナの一覧（表示名とアイコンの対応）は `personas.json` にあります。

## 決まりごと

- 画像は正方形の PNG、256〜512px
- 画像を差し替えるときは、上書きせず、ファイル名の番号を上げる（例：`claude-code-v1.png` → `claude-code-v2.png`）。
  Discord は一度読んだ画像を覚えているため、同じ URL のまま中身を変えても古い絵が出続けることがある
- 表示名に `discord`、`clyde` を入れない
- Webhook の URL（合鍵）は、このリポジトリに書かない
