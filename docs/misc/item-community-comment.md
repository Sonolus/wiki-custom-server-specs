# `ItemCommunityComment`

`ItemCommunityComment` provides information of an item community comment.

## Syntax

```ts
type ItemCommunityComment = {
    author: string
    time: number
    content: string
    actions: ServerForm[]
}
```

## Examples

```json
{
    "author": "Username",
    "time": 1640995200000,
    "content": "...",
    "actions": [
        // ...
    ]
}
```
