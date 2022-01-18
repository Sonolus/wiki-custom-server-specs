# `ItemDetails`

`ItemDetails`はアイテムの詳細情報の型で、Sonolusアプリがアイテムの詳細ビューにデータを入力するために使用します。

## 構文

```ts
type ItemDetails<T> = {
    item: T
    description: string
    recommended: T[]
}
```

## 例

```json
{
    "item": {
        // ...
    },
    "description": "Description of the item",
    "recommended": [
        // ...
    ]
}
```

## 備考

recommendはなるべく短く、最大でも5つのエントリのみを表示することをお勧めします。
