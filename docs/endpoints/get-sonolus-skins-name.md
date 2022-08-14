# `GET /sonolus/skins/{name}`

`/sonolus/skins/{name}` provides detailed information of skin of name `{name}`, and is used by Sonolus app to populate server skin details view.

## Headers

| Header            | Value    | Description                                                    |
| :---------------- | :------- | :------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version). |

## Query Parameters

| Query Parameter | Value    | Description                                             |
| :-------------- | :------- | :------------------------------------------------------ |
| `localization`  | `string` | See [`localization`](../query-parameters/localization). |

## Response Syntax

```ts
type SkinDetails = ItemDetails<SkinItem>
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the skin",
    "recommended": [
        // ...
    ]
}
```
