# `GET /sonolus/engines/{name}`

`/sonolus/engines/{name}` provides detailed information of engine of name `{name}`, and is used by Sonolus app to populate server engine details view.

## Query Parameters

| Query Parameter | Value    | Description                                             |
| :-------------- | :------- | :------------------------------------------------------ |
| `localization`  | `string` | See [`localization`](../query-parameters/localization). |

## Response Headers

| Header            | Value    | Description                                                    |
| :---------------- | :------- | :------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version). |

## Response Body

```ts
type EngineDetails = ItemDetails<EngineItem>
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the engine",
    "recommended": [
        // ...
    ]
}
```
