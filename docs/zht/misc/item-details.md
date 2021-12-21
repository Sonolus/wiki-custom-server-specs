# `ItemDetails`

`ItemDetails`提供了每一個項目的詳細資訊，會由Sonolus程式使用來生成資訊頁面。

## 語法

```ts
type ItemDetails<T> = {
    item: T
    description: string
    recommended: T[]
}
```

## 例子

```json
{
    "item": {
        // ...
    },
    "description": "項目的描述",
    "recommended": [
        // ...
    ]
}
```

## 備註

建議僅顯示5個項目來保持每個頁面不會過長。
