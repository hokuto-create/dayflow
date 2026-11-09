# DayFlow — 作業メモ

- `index.html` 1ファイルのアプリ（React + Babel standalone）。GitHub Pages で `main` から公開
- **`index.html` を変更したら、先頭の `APP_VERSION` も必ず更新する**
  - 起動時・アプリに戻ったときに公開中の版と比べ、違えば自動で読み込み直す仕組み（ホーム画面アプリの古いキャッシュ対策）
  - 形式: `'YYYYMMDD-連番'`（例: `'20261109-1'`）
- データ移行（作り直しなど）は起動時に一度だけ走る effect で行う。クラウド同期が有効なら初回取得（`syncStatus === "synced"`）の後に実行する
