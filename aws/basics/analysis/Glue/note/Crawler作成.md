# 概要
コンソール上で「Crawler作成」を実施する際の各種項目を解説する。

# 前提知識
## データソース
### Subsequent crawler runs （初期クローリング以降のクローラー）
- Crawl all sub-folders
  - ソースを全て読み込む
  - 処理時間がかかり、費用がかさむ
- Crawl new sub-folders only
  - 追加した分だけ読み込む
- Crawl based on events

[**分かりやすい記事**](https://techblog.nhn-techorus.com/archives/21903)

# 作成手順
TBD

# メモ（後で手順に追加）
- Table prefix
クローラーでテーブルを作成する際、生成されるテーブル名は「Table prefix + S3のフォルダ名」となる。

