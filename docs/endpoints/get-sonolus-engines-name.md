# `GET /sonolus/engines/{name}`

`/sonolus/engines/{name}` provides detailed information of engine of name `{name}`, and is used by Sonolus app to populate server engine details view.

## Query Parameters

| Query Parameter | Value    | Description                                                |
| :-------------- | :------- | :--------------------------------------------------------- |
| `localization`  | `string` | See [`localization`](../query-parameters/localization.md). |

## Request Headers

| Header                 | Value    | Description                                                                 |
| :--------------------- | :------- | :-------------------------------------------------------------------------- |
| `Sonolus-Session-Id`   | `string` | Optional, see [`Sonolus-Session-Id`](../headers/sonolus-session-id.md).     |
| `Sonolus-Session-Data` | `string` | Optional, see [`Sonolus-Session-Data`](../headers/sonolus-session-data.md). |

## Request Body

None.

## Response Code

| Code               | Description                         |
| :----------------- | :---------------------------------- |
| `200 OK`           |                                     |
| `401 Unauthorized` | Authentication required or expired. |
| `404 Not Found`    |                                     |

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

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
