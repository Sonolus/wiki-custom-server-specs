# `GET /sonolus/particles/{name}`

`/sonolus/particles/{name}` provides detailed information of particle of name `{name}`, and is used by Sonolus app to populate server particle details view.

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
type ParticleDetails = ItemDetails<ParticleItem>
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the particle",
    "recommended": [
        // ...
    ]
}
```
