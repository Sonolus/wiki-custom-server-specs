# `ItemCommunityCommentList`

`ItemCommunityCommentList` provides comments information of an item, and is used by Sonolus app to populate item details view's community section's comment list.

## Syntax

```ts
type ItemCommunityCommentList = {
    pageCount: number
    comments: ItemCommunityComment[]
}
```

### `pageCount`

If `-1` is used, the list is treated as having infinite pagination.

## Examples

```json
{
    "pageCount": 5,
    "comments": [
        // ...
    ]
}
```

## Remarks

It is recommended to keep each page short by showing only 10 entries.
