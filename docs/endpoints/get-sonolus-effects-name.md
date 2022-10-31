# `GET /sonolus/effects/{name}`

`/sonolus/effects/{name}` provides detailed information of effect of name `{name}`, and is used by Sonolus app to populate server effect details view.

## Query Parameters

| Query Parameter | Value    | Description                                             |
| :-------------- | :------- | :------------------------------------------------------ |
| `localization`  | `string` | See [`localization`](../query-parameters/localization). |

## Response Headers

| Header            | Value    | Description                                                    |
| :---------------- | :------- | :------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version). |

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
