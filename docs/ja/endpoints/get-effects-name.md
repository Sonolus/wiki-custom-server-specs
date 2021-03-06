# `GET /effects/{name}`

`/effects/{name}`は`{name}`に指定されたエフェクトの詳細情報を提供し、Sonolusアプリがサーバー効果の詳細ビューにデータを入力するために利用されます。

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
type EffectDetails = ItemDetails<EffectItem>
```

## 例

```json
{
    "item": {
        // ...
    },
    "description": "Description of the effect",
    "recommended": [
        // ...
    ]
}
```
