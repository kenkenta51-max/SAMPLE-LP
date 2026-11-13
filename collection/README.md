# LP Collection

公開URL: https://kenkenta51-max.github.io/SAMPLE-LP/collection/

SAMPLE-LPの全4ブランチ、main内のHTML、納品データとGit履歴を確認し、3ブランド・3ページを収録しています。Padobulは現行版1件に統一し、保存版は一覧から除外しました。同一HTMLのブランチやZIP、制作途中の修正履歴は重複掲載していません。

| LP | 公開パス（/SAMPLE-LP/配下） | 出典 |
| --- | --- | --- |
| NUTORY / 너토리 | `/` | mainの`index.html`。delivery/nutory-cm-20261112の完成版と同一 |
| Padobul / パドブル / 파도불 | `/padobul/` | mainの`padobul/index.html`。codex/padobul-lp-previewの完成版と同一 |
| cocori / ココリ | `/archive/cocori/` | 初回コミット`9dfbd70`の`index.html`を変更せず復元 |

`codex/padobul-people-enamel`はmainと同じ収録LPです。制作途中のNUTORY・PadobulのリビジョンはGit履歴に残っています。

## 機能

- 各LPの実ブラウザ画面から作成したWebPサムネイルと公開リンク
- ブランド名、説明、タグ、関連キーワードの検索。大文字小文字・全角半角・ひらがなカタカナを正規化し、空白区切りの複数語で絞り込み
- お気に入りの追加・削除・一覧・再読込後の復元。キー`sample-lp-favorites-v1`を使用し、既存LPの保存領域から独立
- 保存できない環境ではメッセージを表示し、ページを開いている間だけ保持
- 名前順、検索結果0件、お気に入り0件、キーボード操作、スマートフォン表示、動きを減らす設定に対応
- 外部フォント・CDN・API・アクセス解析に依存しない静的HTML

## 公開

既存のGitHub Pagesワークフローで、従来のNUTORY・Padobulに加えて`collection/`と2つの`archive/`ページを配信します。既存LPのHTMLは変更していません。納品ZIP、設定ファイル、Git履歴は公開アーティファクトに含めません。

## 更新

`collection/index.html`内の`pages`配列にカードを追加し、`collection/thumbnails/`へ900×625pxのWebPを追加してください。ヘッダーの件数と「すべて」の総数も更新します。新規LPの公開パスは`.github/workflows/pages.yml`のコピー対象にも追加してください。

## 確認

Chromium/Playwrightで、画像の読み込み、検索・複数語検索、0件表示、お気に入りの追加・削除・再読込、名前順、全3リンク、360/390/768/1440pxの横幅、保存領域が使用できない場合を確認。JavaScriptエラーなし。
