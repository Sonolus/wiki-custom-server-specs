# `GET /sonolus/replays/{name}`

`/sonolus/replays/{name}` provides detailed information of replay of name `{name}`, and is used by Sonolus app to populate server replay details view.

## Query Parameters

| Query Parameter | Value    | Description                                                |
| :-------------- | :------- | :--------------------------------------------------------- |
| `localization`  | `string` | See [`localization`](../query-parameters/localization.md). |

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
| `404 Not Found`    |                                     |

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type ReplayDetails = ItemDetails<ReplayItem>
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the replay",
    "sections": [
        // ...
    ]
}
```
