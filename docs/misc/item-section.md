# `ItemSection`

`ItemSection` provides information of a section of items.

## Syntax

```ts
type ItemSection<T> = {
    title: Text | (string & {})
    icon?: Icon
    items: T[]
}
```

## Examples

```json
{
    "title": "#RECOMMENDED",
    "items": [
        // ...
    ]
}
```
