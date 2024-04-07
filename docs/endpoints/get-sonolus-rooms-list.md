# `GET /sonolus/rooms/list`

`/sonolus/rooms/list` provides information of rooms, and is used by Sonolus app to populate server room list view.

## Query Parameters

| Query Parameter   | Value    | Description                                                                      |
| :---------------- | :------- | :------------------------------------------------------------------------------- |
| `localization`    | `string` | See [`localization`](../query-parameters/localization.md).                       |
| `page`            | `number` | See [`page`](../query-parameters/page.md).                                       |
| Search Parameters | `any`    | See [Options Query Parameters](../query-parameters/options-query-parameters.md). |

## Request Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Session` | `string` | Optional, see [`Sonolus-Session`](../headers/sonolus-session.md). |

## Request Body

None.

## Response Code

| Code               | Description                         |
| :----------------- | :---------------------------------- |
| `200 OK`           |                                     |
| `401 Unauthorized` | Authentication required or expired. |

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type RoomList = ItemList<RoomItem>
```

## Examples

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ],
    "searches": [
        // ...
    ]
}
```

## Remarks

When using quick search, search parameters of `?type=quick&keywords=...` will be sent.
