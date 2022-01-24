# `GET /effects/list`

`/effects/list` provides information of effects, and is used by Sonolus app to populate server effect list view.

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
type EffectList = ItemList<EffectItem>
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
