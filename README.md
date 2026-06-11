# 麻雀点数計算アプリ（PWA）

点数計算・逆転条件・点数早見表・成績表（ウマオカ精算）・序盤方針・鳴き読みをサポートする麻雀アプリ。
スマホ（Pixel 9等）にインストールしてオフラインでも使えます。

## GitHub Pagesで公開する手順

1. GitHubで新しいリポジトリを作成（例: `mahjong-app`、Public）
2. このフォルダの全ファイルをアップロード
   （リポジトリページ → **Add file → Upload files** にドラッグ&ドロップ → Commit changes）
3. リポジトリの **Settings → Pages** を開き、
   Source: **Deploy from a branch** / Branch: **main** / フォルダ: **/(root)** → Save
4. 1〜2分待つと `https://ユーザー名.github.io/mahjong-app/` で公開されます

## Pixel 9にアプリとしてインストール

1. Pixel 9のChromeで上記URLを開く
2. 右上の「︙」メニュー → **「ホーム画面に追加」→「インストール」**
   （または自動で表示される「アプリをインストール」バナーをタップ）
3. ホーム画面の🀄アイコンから全画面アプリとして起動できます
4. 一度開けばオフライン（電波のない雀荘）でも動作します

## ファイル構成

- `index.html` — アプリ本体（単一ファイル）
- `manifest.webmanifest` — アプリ名・アイコン等の定義
- `sw.js` — オフラインキャッシュ（Service Worker）
- `icon-*.png` — アプリアイコン

## 更新方法

`index.html` を差し替えてコミットすれば反映されます。
キャッシュを確実に更新したい場合は `sw.js` の `CACHE = "mahjong-v1"` の番号を上げてください。
