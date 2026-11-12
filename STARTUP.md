# 起動と確認

既存の隔離済みチェックアウト `/workspace/SAMPLE-LP` を使用します。明示的な依頼がなければGit worktreeを新規作成しません。

```sh
cd /workspace/SAMPLE-LP
python3 -m http.server 4173 --bind 127.0.0.1
```

ZIPを展開した場合は `index.html` のあるディレクトリで同じサーバーコマンドを実行します。インストール・ビルド・シークレットは不要です。環境停止後はサーバーを再起動してください。他のサービスがポートを使用していれば勝手に停止せず確認してください。

内部確認:

```sh
python3 - <<'PY'
from pathlib import Path
from urllib.request import urlopen
response = urlopen('http://127.0.0.1:4173/', timeout=10)
assert response.status == 200
assert response.read() == Path('index.html').read_bytes()
print('NUTORY ready')
PY
```

ブラウザではレシピ切替、タブの左右/Home/End、商品変更時の数量リセット、数量1〜10、小計30,000ウォン以上の送料無料、注文サマリー、お気に入り保存・再読込・削除、保存不可時のページ内保持、Esc・背景クリック、FAQ、モバイルメニューを確認します。360/390/768/1440pxで横はみ出しがないことを確認してください。外部通信を必要とせずHTML単体でも表示できます。

同梱の environment-config.json は再利用用の設定内容です。読み込むだけで自動実行・公開されるものではありません。
