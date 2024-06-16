# `GET /sonolus/{type}/info`

`/sonolus/{type}/info` provides information of items, and is used by Sonolus app to populate server item info view.

## URL Parameters

| URL Parameter | Value    | Description                                                                                                       |
| :------------ | :------- | :---------------------------------------------------------------------------------------------------------------- |
| `type`        | `string` | `posts`, `playlists`, `levels`, `skins`, `backgrounds`, `effects`, `particles`, `engines`, `replays`, or `rooms`. |

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

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type ItemInfo<T> = {
    creates?: ServerForm[]
    searches?: ServerForm[]
    sections: ItemSection<T>[]
    banner?: SRL
}
```

## Examples

```json
{
    "creates": [
        // ...
    ],
    "searches": [
        // ...
    ],
    "sections": [
        // ...
    ],
    "banner": {
        // ...
    }
}
```
