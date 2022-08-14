# `GET /sonolus/particles/{name}`

`/sonolus/particles/{name}`提供了名稱為`{name}`的粒子的詳細資訊，會由 Sonolus 程式使用來生成伺服器粒子資訊頁面。

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
type ParticleDetails = ItemDetails<ParticleItem>
```

## 例子

```json
{
    "item": {
        // ...
    },
    "description": "粒子的描述",
    "recommended": [
        // ...
    ]
}
```
