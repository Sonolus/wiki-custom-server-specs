# `GET /sonolus/{type}/{itemName}`

`/sonolus/{type}/{itemName}` provides detailed information of item of name `{itemName}`, and is used by Sonolus app to populate server item details view.

## URL Parameters

| URL Parameter | Value    | Description                                                                                              |
| :------------ | :------- | :------------------------------------------------------------------------------------------------------- |
| `type`        | `string` | `posts`, `playlists`, `levels`, `skins`, `backgrounds`, `effects`, `particles`, `engines`, or `replays`. |
| `itemName`    | `string` | Name of item.                                                                                            |

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
type ItemDetails<T> = {
    item: T
    description: string
    hasCommunity: boolean
    leaderboards: ItemLeaderboard[]
    sections: ItemSection<T>[]
}
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the item.",
    "hasCommunity": true,
    "leaderboards": [
        // ...
    ],
    "sections": [
        // ...
    ]
}
```
