# `ItemList`

`ItemList` provides information of a paginated list of items, and is used by Sonolus app to populate item list view.

## Syntax

```ts
type ItemList<T> = {
    pageCount: number
    items: T[]
}
```

### `pageCount`

If `-1` is used, the list is treated as having infinite pagination

## Examples

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ]
}
```

## Remarks

It is recommended to keep each page short by showing only 20 entries.
