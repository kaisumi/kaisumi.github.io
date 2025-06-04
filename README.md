# ITエンジニア向け最新AIニュース

このリポジトリは、AI 関連の最新ニュースを表示するシンプルな静的サイトです。サイト本体は `index.html`、ニュースデータは `ai-news.json` に保存されます。

## ローカルで実行する

ページは JSON ファイルを HTTP 経由で取得するため、ローカルサーバーを立てて閲覧します。以下のコマンドで簡易サーバーを起動してください。

```bash
python -m http.server
```

起動後、ブラウザで `http://localhost:8000/` を開きます。

## ニュースデータの自動更新

`ai-news.json` は GitHub Actions ワークフロー `.github/workflows/fetch-ai-news.yml` により自動生成されます。ワークフローは Gemini API を利用してニュースを取得し、生成した JSON をコミットします。手動で編集しても次回実行時に上書きされます。

## ファイル構成

- `index.html` – ニュースを読み込み表示するメインページ
- `ai-news.json` – 自動生成されるニュースデータ
- `.github/workflows/fetch-ai-news.yml` – ニュース更新用のワークフロー

## ライセンス

このリポジトリに `LICENSE` ファイルが存在する場合はそちらを参照してください。
