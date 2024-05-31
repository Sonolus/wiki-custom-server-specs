# `GET /sonolus/backgrounds/{name}/community`

`/sonolus/backgrounds/{name}/community` provides community information of background of name `{name}`, and is used by Sonolus app to populate server background details view's community section.

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
type BackgroundCommunity = ItemCommunity
```

## Examples

```json
{
    "actions": [
        // ...
    ],
    "topComments": [
        // ...
    ]
}
```
