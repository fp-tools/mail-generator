# Mail Generator

メールマーケティング原稿作成支援ツール（GitHub Pages版）

## 機能

- 媒体ごとのヘッダー/フッター自動挿入
- 配信日付の一括置換
- 本文入力・名前タグ挿入
- 差分表示（置換前後の比較）
- テキスト/HTML形式でダウンロード
- クリップボードコピー
- 機種依存文字チェック
- 媒体の追加・編集・削除（管理画面）
- データのJSON形式インポート/エクスポート

## データの保存先

ブラウザの `localStorage` に保存されます。サーバー不要。

## GitHub Pages へのデプロイ手順

### 1. GitHubリポジトリを作成

1. [github.com](https://github.com) にログイン
2. 右上の `+` → `New repository`
3. Repository name に好きな名前を入力（例: `mail-generator`）
4. `Public` を選択
5. `Create repository` をクリック

### 2. ファイルをアップロード

**方法A: GitHub Web UI（簡単）**
1. リポジトリページで `uploading an existing file` をクリック
2. このフォルダの全ファイルをドラッグ＆ドロップ
3. `Commit changes` をクリック

**方法B: Git CLI**
```bash
cd mail-generator-pages
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### 3. GitHub Pages を有効化

1. リポジトリの `Settings` タブ → `Pages`
2. Source: `Deploy from a branch`
3. Branch: `main` / フォルダ: `/ (root)`
4. `Save` をクリック
5. 数分後に `https://YOUR_USERNAME.github.io/YOUR_REPO/` でアクセス可能

## 注意事項

- 読み込めなかったテンプレート（6件以降）は管理画面から修正してください
- データはブラウザのlocalStorageに保存されるため、異なるブラウザ・端末では共有されません
- 定期的にJSONエクスポートでバックアップすることを推奨します
