# `GET /sonolus/effects/list`

`/sonolus/effects/list` provides information of effects, and is used by Sonolus app to populate server effect list view.

## Query Parameters

| Query Parameter         | Value    | Description                                                                    |
| :---------------------- | :------- | :----------------------------------------------------------------------------- |
| `localization`          | `string` | See [`localization`](../query-parameters/localization.md).                     |
| `page`                  | `number` | See [`page`](../query-parameters/page.md).                                     |
| Search Query Parameters | `any`    | See [Search Query Parameters](../query-parameters/search-query-parameters.md). |

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type EffectList = ItemList<EffectItem>
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
