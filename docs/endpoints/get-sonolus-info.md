# `GET /sonolus/info`

`/sonolus/info` provides information of the server, and is used by Sonolus app to populate server home page.

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
    levels: Section<LevelItem>
    skins: Section<SkinItem>
    backgrounds: Section<BackgroundItem>
    effects: Section<EffectItem>
    particles: Section<ParticleItem>
    engines: Section<EngineItem>
}

type Section<T> = {
    items: T[]
    search: Search
}
```

## Examples

```json
{
    "levels": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "skins": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "backgrounds": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "effects": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "particles": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "engines": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    }
}
```

## Remarks

It is recommended to keep each category short by showing only 5 entries.
