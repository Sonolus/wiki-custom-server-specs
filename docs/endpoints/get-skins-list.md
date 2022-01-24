# `GET /skins/list`

`/skins/list` provides information of skins, and is used by Sonolus app to populate server skin list view.

## Headers

| Header            | Value    | Description                                                    |
| :---------------- | :------- | :------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version). |

## Query Parameters

| Query Parameter         | Value    | Description                                                                 |
| :---------------------- | :------- | :-------------------------------------------------------------------------- |
| `localization`          | `string` | See [`localization`](../query-parameters/localization).                     |
| `page`                  | `number` | See [`page`](../query-parameters/page).                                     |
| Search Query Parameters | `any`    | See [Search Query Parameters](../query-parameters/search-query-parameters). |

## Response Syntax

```ts
type SkinList = ItemList<SkinItem>
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
