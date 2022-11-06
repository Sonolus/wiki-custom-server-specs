# `GET /sonolus/info`

`/sonolus/info` provides information of the server, and is used by Sonolus app to populate server home page.

## Query Parameters

| Query Parameter | Value    | Description                                                |
| :-------------- | :------- | :--------------------------------------------------------- |
| `localization`  | `string` | See [`localization`](../query-parameters/localization.md). |

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
