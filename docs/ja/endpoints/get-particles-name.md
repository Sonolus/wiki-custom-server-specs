# `GET /particles/{name}`

`/particles/{name}`は`{name}`に指定されたパーティクルの詳細情報を提供し、Sonolusアプリがサーバーのパーティクルの詳細ビューにデータを入力するために利用されます。

## ヘッダー

ヘッダー | 値 | 説明
:-- | :-- | :--
`Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)参照

## クエリパラメータ

クエリパラメータ | 値 | 説明
:-- | :-- | :--
`localization` | `string` | [`localization`](../query-parameters/localization)参照

## レスポンスの構文

```ts
type ParticleDetails = ItemDetails<ParticleItem>
```

## 例

```json
{
    "item": {
        // ...
    },
    "description": "Description of the particle",
    "recommended": [
        // ...
    ]
}
```
