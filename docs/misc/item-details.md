# `ItemDetails`

`ItemDetails` provides detailed information of an items, and is used by Sonolus app to populate item details view.

## Syntax

```ts
type ItemDetails<T> = {
    item: T
    description: string
    recommended: T[]
}
```

## Examples

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

## Remarks

It is recommended to keep recommended short by showing only 5 entries.
