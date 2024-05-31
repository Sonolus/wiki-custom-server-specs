# `GET /sonolus/levels/{name}/community/comments/list`

`/sonolus/levels/{name}/community/comments/list` provides comments information of a level, and is used by Sonolus app to populate server level details view's community section's comment list.

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

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type LevelCommunityCommentList = ItemCommunityCommentList
```

## Examples

```json
{
    "pageCount": 5,
    "comments": [
        // ...
    ]
}
```
