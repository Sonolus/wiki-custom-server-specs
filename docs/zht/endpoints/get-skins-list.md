# `GET /skins/list`

`/skins/list`提供了佈景的資訊，會由Sonolus程式使用來生成伺服器佈景列表頁面。

## 標頭

標頭 | 數值 | 描述
:-- | :-- | :--
`Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。

## 查詢函數

查詢函數 | 數值 | 描述
:-- | :-- | :--
`localization` | `string` | 詳見[`localization`](../query-parameters/localization)。
`page` | `number` | 詳見[`page`](../query-parameters/page)。
搜尋的查詢函數 | `any` | 詳見[Search Query Parameters](../query-parameters/search-query-parameters)。

## 響應語法

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
