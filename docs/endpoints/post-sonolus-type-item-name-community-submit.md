# `POST /sonolus/{type}/{itemName}/community/submit`

`/sonolus/{type}/{itemName}/community/submit` allows Sonolus app to submit community actions to item of name `{itemName}`.

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

```ts
type SubmitItemCommunityActionRequest = {
    values: string
}
```

### `values`

Query parameters of submitted action.

See [Options Query Parameters](../query-parameters/options-query-parameters.md).

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
type SubmitItemCommunityActionResponse = {
    shouldUpdateCommunity?: boolean
    shouldNavigateCommentsToPage?: number
}
```

### `shouldUpdateCommunity`

Whether community section should update or not.

### `shouldNavigateCommentsToPage`

Whether comment list should navigate to specified page or not.

## Examples

```json
{
    "shouldUpdateCommunity": true,
    "shouldNavigateCommentsToPage": 5
}
```
