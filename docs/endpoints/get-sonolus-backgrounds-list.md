# `GET /sonolus/backgrounds/list`

`/sonolus/backgrounds/list` provides information of backgrounds, and is used by Sonolus app to populate server background list view.

## Query Parameters

| Query Parameter         | Value    | Description                                                                    |
| :---------------------- | :------- | :----------------------------------------------------------------------------- |
| `localization`          | `string` | See [`localization`](../query-parameters/localization.md).                     |
| `page`                  | `number` | See [`page`](../query-parameters/page.md).                                     |
| Search Query Parameters | `any`    | See [Search Query Parameters](../query-parameters/search-query-parameters.md). |

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

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type BackgroundList = ItemList<BackgroundItem>
```

## Examples

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ],
    "search": {
        //...
    }
}
```
