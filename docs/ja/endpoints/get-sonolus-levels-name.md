# `GET /sonolus/levels/{name}`

`/sonolus/levels/{name}` `{name}`レベルの詳細情報を提供し、Sonolus アプリがサーバーのレベルの詳細ビューにデータを入力するために利用されます。

## クエリパラメータ

| クエリパラメータ | 値       | 説明                                                   |
| :--------------- | :------- | :----------------------------------------------------- |
| `localization`   | `string` | [`localization`](../query-parameters/localization)参照 |

## レスポンスヘッダー

| ヘッダー          | 値       | 説明                                                                      |
| :---------------- | :------- | :------------------------------------------------------------------------ |
| `Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)を参照してください。 |

## レスポンスボディ

```ts
type LevelDetails = ItemDetails<LevelItem>
```

## 例

```json
{
    "item": {
        // ...
    },
    "description": "Description of the level",
    "recommended": [
        // ...
    ]
}
```
