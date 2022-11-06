# `GET /sonolus/skins/list`

`/sonolus/skins/list`提供了佈景的資訊，會由 Sonolus 程式使用來生成伺服器佈景列表頁面。

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
type SkinList = ItemList<SkinItem>
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
