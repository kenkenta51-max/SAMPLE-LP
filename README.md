# cocori — ひとくち、夏をほどく。

架空のココナッツミルクラテブランド「cocori」の日本語LPです。
HTML・CSS・JavaScriptと画像を `index.html` にまとめています。ビルドや依存パッケージのインストールは不要です。

## 閲覧・編集

`index.html` をブラウザで開いてください。ローカルサーバーを使う場合は、このディレクトリで以下を実行します。

```sh
python3 -m http.server 4173
```

## GitHub Pages

公開先の予定URL: https://kenkenta51-max.github.io/SAMPLE-LP/

初回はリポジトリの **Settings → Pages → Build and deployment → Source** を **GitHub Actions** に設定します。
その後 **Actions → Deploy to GitHub Pages → Run workflow → main** で初回の公開を実行できます。
以後は `main` へのプッシュで自動更新されます。Pagesの利用可否はリポジトリの公開範囲とGitHubプランに依存します。

ワークフローは `index.html` と `.nojekyll` だけを公開用アーティファクトへコピーします。

## 実装

- スマートフォン対応、動きを減らす設定への対応
- スクロール・ホバー演出とレシピ写真の切り替え
- コレクション保存（ブラウザのローカルストレージ）
- 数量・送料の計算とデモ注文
- 栄養成分・配合比率と架空の開発ストーリー

商品、価格、人物、成分値、開発ストーリーは架空の設定です。写真はAI生成のイメージです。
注文・決済・発送や個人情報の取得は行いません。
