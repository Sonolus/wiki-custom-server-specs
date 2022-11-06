# `GET /sonolus/effects/{name}`

`/sonolus/effects/{name}` provides detailed information of effect of name `{name}`, and is used by Sonolus app to populate server effect details view.

## Query Parameters

| Query Parameter | Value    | Description                                                |
| :-------------- | :------- | :--------------------------------------------------------- |
| `localization`  | `string` | See [`localization`](../query-parameters/localization.md). |

## Request Headers

| Header                 | Value    | Description                                                                 |
| :--------------------- | :------- | :-------------------------------------------------------------------------- |
| `Sonolus-Session-Id`   | `string` | Optional, see [`Sonolus-Session-Id`](../headers/sonolus-session-id.md).     |
| `Sonolus-Session-Data` | `string` | Optional, see [`Sonolus-Session-Data`](../headers/sonolus-session-data.md). |

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
type EffectDetails = ItemDetails<EffectItem>
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the effect",
    "recommended": [
        // ...
    ]
}
```
