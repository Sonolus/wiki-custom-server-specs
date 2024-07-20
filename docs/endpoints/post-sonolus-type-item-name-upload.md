# `POST /sonolus/{type}/{itemName}/upload`

`/sonolus/{type}/{itemName}/upload` allows Sonolus app to upload files when submitting actions to item of name `{itemName}`.

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

| Header               | Value    | Description                                                                              |
| :------------------- | :------- | :--------------------------------------------------------------------------------------- |
| `Sonolus-Session`    | `string` | Optional, see [`Sonolus-Session`](../headers/sonolus-session.md).                        |
| `Sonolus-Upload-Key` | `string` | See [`POST /sonolus/{type}/{itemName}/submit`](./post-sonolus-type-item-name-submit.md). |

## Request Body

`multipart/form-data` encoded data with `files` field.

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
type ServerUploadItemActionResponse = {}
```

## Examples

```json
{}
```
