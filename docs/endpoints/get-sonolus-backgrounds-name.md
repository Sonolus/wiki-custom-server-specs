# `GET /sonolus/backgrounds/{name}`

`/sonolus/backgrounds/{name}` provides detailed information of background of name `{name}`, and is used by Sonolus app to populate server background details view.

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
type BackgroundDetails = ItemDetails<BackgroundItem>
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the background",
    "recommended": [
        // ...
    ]
}
```
