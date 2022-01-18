# `GET /particles/list`

`/particles/list`はパーティクルの情報を提供し、Sonolusアプリがサーバーのパーティクルリストビューにデータを入力するために利用されます。

## ヘッダー

ヘッダー | 値 | 説明
:-- | :-- | :--
`Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)参照

## クエリパラメータ

クエリパラメータ | 値 | 説明
:-- | :-- | :--
`localization` | `string` | [`localization`](../query-parameters/localization)参照
`page` | `number` | [`page`](../query-parameters/page)参照
`keywords` | `string` | [`keywords`](../query-parameters/keywords)参照

## レスポンスの構文

```ts
type ParticleList = ItemList<ParticleItem>
```

## 例

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ]
}
```
