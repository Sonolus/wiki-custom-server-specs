# `GET /sonolus/particles/list`

`/sonolus/particles/list`はパーティクルの情報を提供し、Sonolus アプリがサーバーのパーティクルリストビューにデータを入力するために利用されます。

## クエリパラメータ

| クエリパラメータ     | 値       | 説明                                                                       |
| :------------------- | :------- | :------------------------------------------------------------------------- |
| `localization`       | `string` | [`localization`](../query-parameters/localization.md)参照                  |
| `page`               | `number` | [`page`](../query-parameters/page.md)参照                                  |
| 検索クエリパラメータ | `any`    | [検索クエリパラメータ](../query-parameters/search-query-parameters.md)参照 |

## レスポンスヘッダー

| ヘッダー          | 値       | 説明                                                         |
| :---------------- | :------- | :----------------------------------------------------------- |
| `Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version.md)参照 |

## レスポンスボディ

```ts
type ParticleList = ItemList<ParticleItem>
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
