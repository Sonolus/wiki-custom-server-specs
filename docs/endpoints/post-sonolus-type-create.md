# `POST /sonolus/{type}/create`

`/sonolus/{type}/create` allows Sonolus app to create an item.

## URL Parameters

| URL Parameter | Value    | Description                                                                                              |
| :------------ | :------- | :------------------------------------------------------------------------------------------------------- |
| `type`        | `string` | `posts`, `playlists`, `levels`, `skins`, `backgrounds`, `effects`, `particles`, `engines`, or `replays`. |

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
type ServerCreateItemRequest = {
    values: string
}
```

### `values`

Query parameters of create.

See [Options Query Parameters](../query-parameters/options-query-parameters.md).

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
type ServerCreateItemResponse = {
    key: string
    hashes: string[]
    shouldUpdateInfo?: boolean
    shouldNavigateToItem?: string
}
```

### `key`

Server defined upload key.

### `hashes`

Hashes of files needed to be uploaded.

Only files specified in request body `values` can be uploaded.

If not empty, files will be uploaded using [`POST /sonolus/{type}/upload`](./post-sonolus-type-upload.md).

## Examples

```json
{
    "key": "...",
    "hashes": [
        // ...
    ],
    "shouldUpdateInfo": true,
    "shouldNavigateToItem": "..."
}
```
