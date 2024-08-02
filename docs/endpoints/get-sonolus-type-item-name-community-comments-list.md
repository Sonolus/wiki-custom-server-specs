# `GET /sonolus/{type}/{itemName}/community/comments/list`

`/sonolus/{type}/{itemName}/community/comments/list` provides comments information of item of name `{itemName}`, and is used by Sonolus app to populate server item details view's community section's comment list.

## URL Parameters

| URL Parameter | Value    | Description                                                                                              |
| :------------ | :------- | :------------------------------------------------------------------------------------------------------- |
| `type`        | `string` | `posts`, `playlists`, `levels`, `skins`, `backgrounds`, `effects`, `particles`, `engines`, or `replays`. |
| `itemName`    | `string` | Name of item.                                                                                            |

## Query Parameters

| Query Parameter       | Value    | Description                                                                      |
| :-------------------- | :------- | :------------------------------------------------------------------------------- |
| `localization`        | `string` | See [`localization`](../query-parameters/localization.md).                       |
| Configuration Options | `any`    | See [Options Query Parameters](../query-parameters/options-query-parameters.md). |
| `page`                | `number` | See [`page`](../query-parameters/page.md).                                       |

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
type ServerItemCommunityCommentList = {
    pageCount: number
    comments: ServerItemCommunityComment[]
}
```

### `pageCount`

If `-1` is used, the list is treated as having infinite pagination.

### `comments`

It is recommended to keep each page short by showing only 10 comments.

## Examples

```json
{
    "pageCount": 5,
    "comments": [
        // ...
    ]
}
```
