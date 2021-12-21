# `ItemList`

`ItemList`提供了已分頁項目的資訊，會由Sonolus程式使用來生成列表的頁面。

## 語法

```ts
type ItemList<T> = {
    pageCount: number
    items: T[]
}
```

### `pageCount`

如果數值等於`-1`，列表將被視為擁有無限分頁。

## 例子

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ]
}
```

## 備註

建議僅顯示20個項目來保持每個頁面不會過長。
