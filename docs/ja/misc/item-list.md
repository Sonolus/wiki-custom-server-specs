# `ItemList`

`ItemList`は、アイテムのページ付けされたリストの情報を提供し、Sonolusアプリがアイテムリストビューにデータを入力するために使用します。

## 構文

```ts
type ItemList<T> = {
    pageCount: number
    items: T[]
}
```

### `pageCount`

`-1`を入力した場合、リストは無限のページネーションを持つものとして扱われます

## 例

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ]
}
```

## 備考

各ページはなるべく短く、最大でも20個のエントリまでを表示することをお勧めします。
