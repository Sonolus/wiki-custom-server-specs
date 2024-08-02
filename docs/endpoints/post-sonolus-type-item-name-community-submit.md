# `POST /sonolus/{type}/{itemName}/community/submit`

`/sonolus/{type}/{itemName}/community/submit` allows Sonolus app to submit community actions to item of name `{itemName}`.

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

## Request Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Session` | `string` | Optional, see [`Sonolus-Session`](../headers/sonolus-session.md). |

## Request Body

```ts
type ServerSubmitItemCommunityActionRequest = {
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
type ServerSubmitItemCommunityActionResponse = {
    shouldUpdateCommunity?: boolean
    shouldNavigateCommentsToPage?: number
    key: string
    hashes: string[]
}
```

### `shouldUpdateCommunity`

Whether community section should update or not.

### `shouldNavigateCommentsToPage`

Whether comment list should navigate to specified page or not.

### `key`

Server defined upload key.

### `hashes`

Hashes of files needed to be uploaded.

Only files specified in request body `values` can be uploaded.

If not empty, files will be uploaded using [`POST /sonolus/{type}/{itemName}/community/upload`](./post-sonolus-type-item-name-community-upload.md).

## Examples

```json
{
    "shouldUpdateCommunity": true,
    "shouldNavigateCommentsToPage": 5,
    "key": "...",
    "hashes": [
        // ...
    ]
}
```
