# NUTORY / 너토리

韓国向けの架空のピーナッツパウダーブランドLPです。韓国語原稿、CSS、JavaScript、画像を `index.html` に埋め込んでいます。外部CDN・フォント・画像への依存、パッケージのインストール、ビルドは不要です。

## 閲覧・ダウンロード

納品専用ブランチ `delivery/nutory-cm-20261112` の `delivery/NUTORY.zip` を保存して展開し、`index.html` をChromeなどのブラウザで開いてください。GitHubのファイル画面では **Download raw file**（↓）で取得できます。HTML単体はブランチのルートにもあります。サーバーでの閲覧手順は `STARTUP.md` に記載しています。file://ではブラウザによって永続保存が制限されることがあります。

`delivery/revision-preview.jpg` は今回のFV・人物写真・ブランドメッセージ・ラテ作りの実画面です。

## 今回の修正：POP FOOD CAMPAIGN

- FVを独立したオレンジ瓶・緑瓶・クリーム背景・背景文字・ステッカーのレイヤーへ作り替え、浮遊、回転、マウスに反応する傾き、粉の動きを追加。
- FVのモーション停止／再開ボタンを追加。端末のprefers-reduced-motion設定時は動きを止め、ボタンにも適用状態を表示。
- ヨーグルトを食べる女性、パウダーを振りかける男性、トーストを楽しむ友人2人、ラテを作るバリスタの4場面を新規AI生成。商品が写る写真は既存パッケージを参照して制作。
- FV直後に食べる／使う人物写真を大きく配置。ブランドメッセージとホームカフェにも人物を追加。
- 鮮やかなオレンジ・深緑・イエローと、大きな見出し、ステッカー、太い縁取り、斜めの写真、立体的な影を全体へ展開。
- 原料の細かな粉、各味の単独商品写真、料理写真が変わるレシピ、3つの器の工程写真、ラテの湯気、夜のデザート、FAQ等の内容は引き続き掲載。

`delivery/hero-motion.gif` は実ブラウザから取得した32フレームのアニメーション確認画像、`delivery/revision-preview.jpg` はFVと人物写真の画面確認画像です。GIFは動作イメージであり、HTML本体はCSSとJavaScriptで動きます。

## 機能・検証

レシピの左右/Home/Endキー、商品3種、数量1〜10、商品変更時の数量リセット、小計30,000ウォン以上の送料無料、デモ注文、コレクション保存・再読込・削除・保存不可時のページ内保持、ダイアログのEsc/背景クリック、FAQ、モバイルメニュー、prefers-reduced-motionに対応しています。保存キーは `nutory-collection-v1`、形式は `{"flavor":"original"}` などです。

Chromium/Playwrightで全21画像のデコード、料理写真の切替、360/390/768/1440pxの横はみ出しなし、主要操作、JavaScriptエラー0件を確認済みです。PC・スマホ画像、浮遊アニメーションの時間変化、停止でフレームが止まること、再開、マウスへの反応、動きを減らす設定も確認しました。

## 架空の設定について

実在の商品・販売事業者ではありません。価格・風味・原料・製法・保存・栄養数値は架空の設定であり、実製品の分析・認証結果ではありません。画像はAI生成です。実際の注文・決済・配送・個人情報取得・アクセス解析は行いません。コレクションはブラウザ内だけで保存します。

旧環境の完成物は取得できず、引き継ぎ仕様から再構築したものを改修しています。制作前のcocori HTMLは `/tmp/nutory/previous-index.html` に退避済みです（ZIPには含めません）。NUTORYを`main`の公開対象にし、既存の `.github/workflows/pages.yml` を利用してGitHub Pagesへデプロイします。以前のmainのPadobulサイトは `archive/padobul/` とGit履歴に保存しています。


## GitHub Pagesへの公開

公開先: https://kenkenta51-max.github.io/SAMPLE-LP/

`main`へのpushで既存の「Deploy to GitHub Pages」が実行されます。公開アーティファクトは `index.html` と `.nojekyll` のみです。納品ZIP、GIF、旧サイトの保存ファイルはサイトへ含めません。


## 併設LP：Padobul

パドブルの人物・光沢背景を追加した版は [padobul/index.html](padobul/index.html) に保存しています。公開URLは https://kenkenta51-max.github.io/SAMPLE-LP/padobul/ です。
トップページのNUTORYおよび旧版の保存領域 `archive/padobul/` は変更せず、GitHub Pagesの公開アーティファクトへ `padobul/index.html` を追加しています。


## LP Collection

全LPのサムネイル・公開リンク・検索・お気に入りを備えたコレクションを https://kenkenta51-max.github.io/SAMPLE-LP/collection/ に追加しました。NUTORYとPadobulの現行版に加え、Git履歴から復元したcocoriを掲載しています。Padobulは現行版1件に統一しています。詳細は [collection/README.md](collection/README.md) を参照してください。既存のNUTORY・PadobulのHTMLとURLは維持しています。公開アーティファクトには、上記LPに加えて`collection/`と`archive/cocori/index.html`、`archive/padobul/index.html`を含めます。
