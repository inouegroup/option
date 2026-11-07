# オプション単価表

社内共有の検索できる価格表。画面（`public/index.html`）は開くたびに `public/data.csv` を読み込みます。
**データを更新するときは `data.csv` を差し替えるだけ**で、画面の作り直しは不要です。

## データの更新手順
1. Excelで価格表を直し、「CSV UTF-8（コンマ区切り）」で保存する（列の並びと見出しはそのまま）。
2. GitHubでこのリポジトリを開き、「Add file → Upload files」から `public` フォルダに同じ名前の `data.csv` をアップロードして上書きする。
3. 「Commit changes」を押す。1〜2分でURLに反映される（Actionsタブで進行状況が見える）。

## 列
カテゴリ / サブカテゴリ / 商品 / 仕様 / 単位 / 追加金額 / 差額 / 仕入れ額 / 送料 / 定価 / 仕入先 / URL / 備考 / 画像

- 画像は `public/img/` に入れたファイルの名前（例 `img01.png`）を「画像」列に書く。
- 備考の改行はセル内改行のままでOK。

## 構成
- `public/index.html` 画面
- `public/data.csv` データ
- `public/img/` 商品画像
- `firebase.json` / `.github/workflows/deploy.yml` Firebase Hostingへの自動反映
