# `ItemCommunity`

`ItemCommunity` provides community information of an item, and is used by Sonolus app to populate item details view's community section.

## Syntax

```ts
type ItemCommunity = {
    actions: ServerForm[]
    topComments: ItemCommunityComment[]
}
```

## Examples

```json
{
    "actions": [
        // ...
    ],
    "topComments": [
        // ...
    ]
}
```
