# `GET /sonolus/skins/{name}`

`/sonolus/skins/{name}`は`{name}`に指定されたスキンの詳細情報を提供し、Sonolus アプリがサーバーのスキンの詳細ビューにデータを入力するために利用されます。

## クエリパラメータ

| クエリパラメータ | 値       | 説明                                                   |
| :--------------- | :------- | :----------------------------------------------------- |
| `localization`   | `string` | [`localization`](../query-parameters/localization)参照 |

## レスポンスヘッダー

| ヘッダ            | 値       | 説明                                                      |
| :---------------- | :------- | :-------------------------------------------------------- |
| `Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)参照 |

## レスポンスボディ

```ts
type SkinDetails = ItemDetails<SkinItem>
```

## 例

```json
{
    "item": {
        // ...
    },
    "description": "Description of the skin",
    "recommended": [
        // ...
    ]
}
```
