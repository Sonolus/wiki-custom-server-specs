# `ItemDetails`

`ItemDetails` provides detailed information of an item, and is used by Sonolus app to populate item details view.

## Syntax

```ts
type ItemDetails<T> = {
    item: T
    description: string
    hasCommunity: boolean
    sections: ItemSection<T>[]
}
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the item",
    "hasCommunity": true,
    "sections": [
        // ...
    ]
}
```

## Remarks

It is recommended to keep recommended short by showing only 5 entries.
