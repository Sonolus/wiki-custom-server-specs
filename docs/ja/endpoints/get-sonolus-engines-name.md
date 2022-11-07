# `GET /sonolus/engines/{name}`

`/sonolus/engines/{name}`は`{name}`に指定されたエンジンの詳細情報を提供し、Sonolus アプリがサーバーエンジンの詳細ビューにデータを入力するために利用されます。

## クエリパラメータ

| クエリパラメータ | 値       | 説明                                                      |
| :--------------- | :------- | :-------------------------------------------------------- |
| `localization`   | `string` | [`localization`](../query-parameters/localization.md)参照 |

## レスポンスヘッダー

| ヘッダー          | 値       | 説明                                                         |
| :---------------- | :------- | :----------------------------------------------------------- |
| `Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version.md)参照 |

## レスポンスボディ

```ts
type EngineDetails = ItemDetails<EngineItem>
```

## 例

```json
{
    "item": {
        // ...
    },
    "description": "Description of the engine",
    "recommended": [
        // ...
    ]
}
```
