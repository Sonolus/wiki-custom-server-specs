# `GET /sonolus/{type}/{itemName}/leaderboards/{leaderboardName}/records/list`

`/sonolus/{type}/{itemName}/leaderboards/{leaderboardName}/records/list` provides detailed information of leaderboard of name `{leaderboardName}` in item of name `{itemName}`, and is used by Sonolus app to populate server item details view's leaderboard section's record list.

## URL Parameters

| URL Parameter     | Value    | Description                                                                                              |
| :---------------- | :------- | :------------------------------------------------------------------------------------------------------- |
| `type`            | `string` | `posts`, `playlists`, `levels`, `skins`, `backgrounds`, `effects`, `particles`, `engines`, or `replays`. |
| `itemName`        | `string` | Name of item.                                                                                            |
| `leaderboardName` | `string` | Name of leaderboard.                                                                                     |

## Query Parameters

| Query Parameter | Value    | Description                                                |
| :-------------- | :------- | :--------------------------------------------------------- |
| `localization`  | `string` | See [`localization`](../query-parameters/localization.md). |
| `page`          | `number` | See [`page`](../query-parameters/page.md).                 |

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
type ItemLeaderboardRecordList = {
    pageCount: number
    records: ItemLeaderboardRecord[]
}
```

### `pageCount`

If `-1` is used, the list is treated as having infinite pagination.

### `comments`

It is recommended to keep each page short by showing only 10 records.

## Examples

```json
{
    "pageCount": 5,
    "records": [
        // ...
    ]
}
```
