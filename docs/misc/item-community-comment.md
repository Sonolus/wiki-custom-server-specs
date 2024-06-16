# `ItemCommunityComment`

`ItemCommunityComment` provides information of an item community comment.

## Syntax

```ts
type ItemCommunityComment = {
    name: string
    author: string
    time: number
    content: string
    actions: ServerForm[]
}
```

## Examples

```json
{
    "name": "...",
    "author": "Username",
    "time": 1640995200000,
    "content": "...",
    "actions": [
        // ...
    ]
}
```
