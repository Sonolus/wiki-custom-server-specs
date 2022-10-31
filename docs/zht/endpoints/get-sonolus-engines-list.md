# `GET /sonolus/engines/list`

`/sonolus/engines/list`提供了引擎的資訊，會由 Sonolus 程式使用來生成伺服器引擎列表頁面。

## 查詢函數

| 查詢函數       | 數值     | 描述                                                                         |
| :------------- | :------- | :--------------------------------------------------------------------------- |
| `localization` | `string` | 詳見[`localization`](../query-parameters/localization)。                     |
| `page`         | `number` | 詳見[`page`](../query-parameters/page)。                                     |
| 搜尋的查詢函數 | `any`    | 詳見[Search Query Parameters](../query-parameters/search-query-parameters)。 |

## 響應標頭

| Header            | 數值     | 描述                                                          |
| :---------------- | :------- | :------------------------------------------------------------ |
| `Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。 |

## 響應主體

```ts
type EngineList = ItemList<EngineItem>
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
