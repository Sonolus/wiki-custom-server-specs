# `GET /sonolus/backgrounds/{name}`

`/sonolus/backgrounds/{name}`提供了名稱為`{name}`的背景的詳細資訊，會由 Sonolus 程式使用來生成伺服器背景資訊頁面。

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
type BackgroundDetails = ItemDetails<BackgroundItem>
```

## 例子

```json
{
    "item": {
        // ...
    },
    "description": "背景的描述",
    "recommended": [
        // ...
    ]
}
```
