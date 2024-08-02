# `POST /sonolus/{type}/upload`

`/sonolus/{type}/upload` allows Sonolus app to upload files when creating an item.

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

| Header               | Value    | Description                                                         |
| :------------------- | :------- | :------------------------------------------------------------------ |
| `Sonolus-Session`    | `string` | Optional, see [`Sonolus-Session`](../headers/sonolus-session.md).   |
| `Sonolus-Upload-Key` | `string` | See [`POST /sonolus/{type}/create`](./post-sonolus-type-create.md). |

## Request Body

`multipart/form-data` encoded data with `files` field.

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
type ServerUploadItemResponse = {}
```

## Examples

```json
{}
```
