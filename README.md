# 零層ダイブ

近未来の地下都市「旧第七アーコロジー」を降りていく、不思議のダンジョン風ローグライクです。スマホのブラウザで遊べ、ホーム画面に追加するとアプリのように全画面で起動し、オフラインでも遊べます。

## GitHub Pages で公開する手順

1. GitHub で新しいリポジトリを作る（例：`zero-dive`、Public）。
2. このフォルダの中身（`index.html`、`manifest.webmanifest`、`sw.js`、`icons/`、`README.md`）をすべてアップロードする。ブラウザなら「Add file → Upload files」にドラッグするだけでよい。
3. リポジトリの「Settings → Pages」を開き、「Source」を「Deploy from a branch」、ブランチを `main`、フォルダを `/ (root)` にして保存する。
4. 1〜2分後、`https://<ユーザー名>.github.io/zero-dive/` で遊べるようになる。

コマンドラインを使う場合：

```bash
cd zero-dive
git init && git add . && git commit -m "零層ダイブ"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/zero-dive.git
git push -u origin main
```

## スマホにアプリとして保存する

- **iPhone（Safari）**：公開したURLを開き、共有ボタン →「ホーム画面に追加」。
- **Android（Chrome）**：公開したURLを開き、メニュー →「アプリをインストール」または「ホーム画面に追加」。

一度開けば、以降は電波がなくても起動できます。セーブデータと図鑑は端末のブラウザ内に保存されます。

## 更新するとき

`index.html` を差し替えてアップロードし直すだけで反映されます。古い画面が残る場合は、`sw.js` の `CACHE = 'zero-dive-v1'` の数字を上げてからアップロードしてください。

## その他

- バランス調整メニューはパスワードで保護されています（開発・テスト用）。
- 音はブラウザ内で合成しており、外部の音声ファイルは使っていません。
