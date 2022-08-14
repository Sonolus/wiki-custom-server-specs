# `GET /sonolus/levels/{name}`

`/sonolus/levels/{name}`提供了名稱為`{name}`的關卡的詳細資訊，會由 Sonolus 程式使用來生成伺服器關卡資訊頁面。

## 標頭

| 標頭              | 數值     | 描述                                                          |
| :---------------- | :------- | :------------------------------------------------------------ |
| `Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。 |

## 查詢函數

| 查詢函數       | 數值     | 描述                                                     |
| :------------- | :------- | :------------------------------------------------------- |
| `localization` | `string` | 詳見[`localization`](../query-parameters/localization)。 |

## 響應語法

```ts
type LevelDetails = ItemDetails<LevelItem>
```

## 例子

```json
{
    "item": {
        // ...
    },
    "description": "關卡的描述",
    "recommended": [
        // ...
    ]
}
```
