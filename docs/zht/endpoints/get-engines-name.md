# `GET /engines/{name}`

`/particles/{name}`提供了名稱為`{name}`的引擎的詳細資訊，會由Sonolus程式使用來生成伺服器引擎資訊頁面。

## 標頭

標頭 | 數值 | 描述
:-- | :-- | :--
`Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。

## 查詢函數

查詢函數 | 數值 | 描述
:-- | :-- | :--
`localization` | `string` | 詳見[`localization`](../query-parameters/localization)。

## 響應語法

```ts
type EngineDetails = ItemDetails<EngineItem>
```

## 例子

```json
{
    "item": {
        // ...
    },
    "description": "引擎的描述",
    "recommended": [
        // ...
    ]
}
```
