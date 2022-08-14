# `GET /sonolus/backgrounds/list`

`/sonolus/backgrounds/list`提供了背景的資訊，會由 Sonolus 程式使用來生成伺服器背景列表頁面。

## 標頭

| 標頭              | 數值     | 描述                                                          |
| :---------------- | :------- | :------------------------------------------------------------ |
| `Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。 |

## 查詢函數

| 查詢函數       | 數值     | 描述                                                                         |
| :------------- | :------- | :--------------------------------------------------------------------------- |
| `localization` | `string` | 詳見[`localization`](../query-parameters/localization)。                     |
| `page`         | `number` | 詳見[`page`](../query-parameters/page)。                                     |
| 搜尋的查詢函數 | `any`    | 詳見[Search Query Parameters](../query-parameters/search-query-parameters)。 |

## 響應語法

```ts
type BackgroundList = ItemList<BackgroundItem>
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
