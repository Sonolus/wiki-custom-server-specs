# `GET /sonolus/levels/{name}`

`/sonolus/levels/{name}` provides detailed information of level of name `{name}`, and is used by Sonolus app to populate server level details view.

## Headers

| Header            | Value    | Description                                                    |
| :---------------- | :------- | :------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version). |

## Query Parameters

| Query Parameter | Value    | Description                                             |
| :-------------- | :------- | :------------------------------------------------------ |
| `localization`  | `string` | See [`localization`](../query-parameters/localization). |

## Response Syntax

```ts
type LevelDetails = ItemDetails<LevelItem>
```

## Examples

```json
{
    "item": {
        // ...
    },
    "description": "Description of the level",
    "recommended": [
        // ...
    ]
}
```
