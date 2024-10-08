# Vue3 Test App

## 使用技術

| 言語・フレームワーク・主要ライブラリ | その他、備考                 |
| ------------------------------------ | ---------------------------- |
| JavaScript                           | 開発言語                     |
| Vue.js (Vue3)                        | フロントエンドフレームワーク |
| Vite                                 | Vue.js のビルドツール        |
| Element UI Plus                      | UI コンポーネント            |
| Bootstrap                            | CSS フレームワーク           |
| Axios                                | API 通信ライブラリ           |
| Vuelidate                            | バリデーションライブラリ 　  |
| Pinia                                | データストアライブラリ 　    |
| Dayjs                                | 日付ライブラリ 　            |

## フォルダ構成

```
public/            # 静的アセットを配置するフォルダ。URLから直接アクセスが可能。
   ├ images/       # サイズが大きい画像、もしくはセキュリティ上公開しても問題ないものはこちらへ保管する (※1)
src/
 ├ assets/         # コンポーネント内で使用する画像ファイルやscssファイルを配置する
   ├ images/       # サイズが小さい画像はこちらへ保管する (※1)
 ├ components/     # コンポーネントを保管
   ├ common/       # ドメインに関心を持たないどこでも共通で使用できるコンポーネント
 ├ composables/    # 状態（ステートを管理）を持つ共通処理や一つの共通ではない処理を（CSVエクスポート等）ひとまとまりに記述する
 ├ constants/      # 定数を保管するフォルダ。axiosに渡すAPIエンドポイント情報も保管されている。
 ├ pages/          # Viteに処理されるアセットを格納するディレクトリ
 ├ router/         # Vue-Routerのルーティングファイル
 ├ store/          # データストアとしてPiniaを使用中
 ├ utils/          # ドメインに関心を持たないどこでも共通で使用できる関数を保管
 ├ main.js         # アプリケーションのエントリポイントのスクリプトファイル
 ├ config.dev.js   # アプリの設定ファイル。開発環境の環境変数をこちらへ格納している。
 ├ config.stg.js   # アプリの設定ファイル。STG環境の環境変数をこちらへ格納している。
 ├ config.prod.js  # アプリの設定ファイル。本番環境の環境変数をこちらへ格納している。
vite.config.js     # Viteの設定ファイル
```

※1 src/assets 内に配置した画像は Vite でコンパイルされて、base64 形式にエンコードされる。  
base64 形式のメリットは、HTTP リクエストが発生しない為、ページ内の HTTP リクエストの回数を減らすことができる。  
ただし、base64 形式にするとデータサイズが約 37%増加する、キャッシュされないといったデメリットもある。  
それを踏まえて、アイコン等の小さい画像のみ src/assets に配置する。(画像は基本 assets に保管する)

【base64 形式に変換するメリットの参考記事】  
https://thk.kanzae.net/net/itc/t1506/

## 環境構築

ルート直下にて下記コマンドを実行

```
npm i
npm run dev
```
