# オプション単価表

社内共有の検索できる価格表。

- 見る：https://inouegroup.github.io/option/
- 更新：https://inouegroup.github.io/option/admin.html

画面（index.html）は開くたびに Firebase（Firestore）から最新データを読み込みます。
データを変えるときに HTML の作り直しは不要です。

## データの更新手順
1. 価格表の Excel を直す（「価格表」シート、1行目の見出しはそのまま）。
2. 更新ページを開き、Google でログインする（Firestore のルールに登録したアカウントのみ）。
3. Excel を選ぶ → 追加・削除・変更の一覧を確認 →「この内容で更新する」。
4. 単価表を開き直すと反映されている。

## 構成
- index.html 見る用ページ（商品画像10点はこの中に入っている）
- admin.html 更新用ページ
- データ：Firebase プロジェクト option-807c5 の Firestore（meta/info と prices）
