# `GET /info`

`/info` provides information of the server, and is used by Sonolus app to populate server home page.

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
type ServerInfo = {
    levels: LevelItem[]
    skins: SkinItem[]
    backgrounds: BackgroundItem[]
    effects: EffectItem[]
    particles: ParticleItem[]
    engines: EngineItem[]
}
```

## Examples

```json
{
    "levels": [
        // ...
    ],
    "skins": [
        // ...
    ],
    "backgrounds": [
        // ...
    ],
    "effects": [
        // ...
    ],
    "particles": [
        // ...
    ],
    "engines": [
        // ...
    ]
}
```

## Remarks

It is recommended to keep each category short by showing only 5 entries.
