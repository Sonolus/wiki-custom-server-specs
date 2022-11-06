# `GET /sonolus/backgrounds/{name}`

`/sonolus/backgrounds/{name}` provides detailed information of background of name `{name}`, and is used by Sonolus app to populate server background details view.

## Query Parameters

| Query Parameter | Value    | Description                                                |
| :-------------- | :------- | :--------------------------------------------------------- |
| `localization`  | `string` | See [`localization`](../query-parameters/localization.md). |

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

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
