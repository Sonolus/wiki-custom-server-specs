# `GET /sonolus/engines/{name}`

`/sonolus/engines/{name}`提供了名稱為`{name}`的引擎的詳細資訊，會由 Sonolus 程式使用來生成伺服器引擎資訊頁面。

## 查詢函數

| 查詢函數       | 數值     | 描述                                                        |
| :------------- | :------- | :---------------------------------------------------------- |
| `localization` | `string` | 詳見[`localization`](../query-parameters/localization.md)。 |

## 響應標頭

| 標頭              | 數值     | 描述                                                             |
| :---------------- | :------- | :--------------------------------------------------------------- |
| `Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version.md)。 |

## 響應主體

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
