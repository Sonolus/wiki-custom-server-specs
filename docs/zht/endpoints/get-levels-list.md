# `GET /levels/list`

`/skins/list`提供了關卡的資訊，會由Sonolus程式使用來生成伺服器關卡列表頁面。

## 標頭

標頭 | 數值 | 描述
:-- | :-- | :--
`Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。

## 查詢函數

查詢函數 | 數值 | 描述
:-- | :-- | :--
`localization` | `string` | 詳見[`localization`](../query-parameters/localization)。
`page` | `number` | 詳見[`page`](../query-parameters/page)。
`keywords` | `string` | 詳見[`keywords`](../query-parameters/keywords)。

## 響應語法

```ts
type LevelList = ItemList<LevelItem>
```

## 例子

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ]
}
```
