# `GET /sonolus/skins/{name}`

`/sonolus/skins/{name}` provides detailed information of skin of name `{name}`, and is used by Sonolus app to populate server skin details view.

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
