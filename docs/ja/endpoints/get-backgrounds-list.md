# `GET /backgrounds/list`

`/backgrounds/list`は背景の情報を提供し、Sonolusアプリがサーバーの背景リストビューにデータを入力するために利用されます。

## ヘッダー

ヘッダ | 値 | 説明
:-- | :-- | :--
`Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)を参照してください。

## クエリパラメータ

クエリパラメータ | 値 | 説明
:-- | :-- | :--
`localization` | `string` | [`localization`](../query-parameters/localization)参照
`page` | `number` | [`page`](../query-parameters/page)参照
検索クエリパラメータ | `any` | [検索クエリパラメータ](../query-parameters/search-query-parameters)参照

## レスポンスの構文

```ts
type BackgroundList = ItemList<BackgroundItem>
```

## 例

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ],
    "search": {
        //...
    }
}
```
