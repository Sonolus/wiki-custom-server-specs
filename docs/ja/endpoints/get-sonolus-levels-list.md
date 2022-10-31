# `GET /sonolus/levels/list`

`/sonolus/levels/list`はレベルの情報を提供し、Sonolus アプリがサーバーのレベルリストビューにデータを入力するために利用されます。

## クエリパラメータ

| クエリパラメータ     | 値       | 説明                                                                    |
| :------------------- | :------- | :---------------------------------------------------------------------- |
| `localization`       | `string` | [`localization`](../query-parameters/localization)参照                  |
| `page`               | `number` | [`page`](../query-parameters/page)参照                                  |
| 検索クエリパラメータ | `any`    | [検索クエリパラメータ](../query-parameters/search-query-parameters)参照 |

## レスポンスヘッダー

| ヘッダ            | 値       | 説明                                                                      |
| :---------------- | :------- | :------------------------------------------------------------------------ |
| `Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)を参照してください。 |

## レスポンスボディ

```ts
type LevelList = ItemList<LevelItem>
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
