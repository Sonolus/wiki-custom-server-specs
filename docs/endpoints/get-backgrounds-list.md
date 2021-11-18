# `GET /backgrounds/list`

`/backgrounds/list` provides information of backgrounds, and is used by Sonolus app to populate server background list view.

## Headers

| Header            | Value    | Description                                                    |
| :---------------- | :------- | :------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version). |

## Query Parameters

| Query Parameter | Value    | Description                                             |
| :-------------- | :------- | :------------------------------------------------------ |
| `localization`  | `string` | See [`localization`](../query-parameters/localization). |
| `page`          | `number` | See [`page`](../query-parameters/page).                 |
| `keywords`      | `string` | See [`keywords`](../query-parameters/keywords).         |

## Response Syntax

```ts
type BackgroundList = ItemList<BackgroundItem>
```

## Examples

```json
{
    "pageCount": 5,
    "items": [
        // ...
    ]
}
```
