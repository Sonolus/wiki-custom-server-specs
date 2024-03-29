# `GET /sonolus/effects/list`

`/sonolus/effects/list`提供了效果的資訊，會由 Sonolus 程式使用來生成伺服器效果列表頁面。

## 查詢函數

| 查詢函數       | 數值     | 描述                                                                            |
| :------------- | :------- | :------------------------------------------------------------------------------ |
| `localization` | `string` | 詳見[`localization`](../query-parameters/localization.md)。                     |
| `page`         | `number` | 詳見[`page`](../query-parameters/page.md)。                                     |
| 搜尋的查詢函數 | `any`    | 詳見[Search Query Parameters](../query-parameters/search-query-parameters.md)。 |

## 響應標頭

| 標頭              | 數值     | 描述                                                             |
| :---------------- | :------- | :--------------------------------------------------------------- |
| `Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version.md)。 |

## 響應主體

```ts
type EffectList = ItemList<EffectItem>
```

## 例子

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
