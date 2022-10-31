# `GET /sonolus/engines/list`

`/sonolus/engines/list`はエンジンの情報を提供し、Sonolus アプリがサーバーエンジンリストビューにデータを入力するために利用されます。

## クエリパラメータ

| クエリパラメータ     | 値       | 説明                                                                    |
| :------------------- | :------- | :---------------------------------------------------------------------- |
| `localization`       | `string` | [`localization`](../query-parameters/localization)参照                  |
| `page`               | `number` | [`page`](../query-parameters/page)参照                                  |
| 検索クエリパラメータ | `any`    | [検索クエリパラメータ](../query-parameters/search-query-parameters)参照 |

## レスポンスヘッダー

| ヘッダー          | 値       | 説明                                                      |
| :---------------- | :------- | :-------------------------------------------------------- |
| `Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)参照 |

## レスポンスボディ

```ts
type EngineList = ItemList<EngineItem>
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
