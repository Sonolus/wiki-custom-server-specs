# `ItemInfo`

`ItemInfo` provides information of items, and is used by Sonolus app to populate item info view.

## Syntax

```ts
type ItemInfo<T> = {
    searches?: ServerForm[]
    sections: ItemSection<T>[]
    banner?: SRL
}
```

## Examples

```json
{
    "searches": [
        // ...
    ],
    "sections": [
        // ...
    ],
    "banner": {
        // ...
    }
}
```
