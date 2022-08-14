# `LevelItem`

`LevelItem` provides information of a level.

## Syntax

```ts
type LevelItem = {
    name: string
    version: 1
    rating: number
    title: string
    artists: string
    author: string
    engine: EngineItem
    useSkin: UseItem<SkinItem>
    useBackground: UseItem<BackgroundItem>
    useEffect: UseItem<EffectItem>
    useParticle: UseItem<ParticleItem>
    cover: SRL<'LevelCover'>
    bgm: SRL<'LevelBgm'>
    preview?: SRL<'LevelPreview'>
    data: SRL<'LevelData'>
}

type UseItem<T> = {
    useDefault: boolean
    item?: T
}
```

### `name`

Unique name which identifies the level.

### `UseItem<T>`

If `useDefault` is `true`, the level will use the default item of level's engine.

Otherwise, `item` is used.

## Examples

```json
{
    "name": "bandori-1-expert",
    "version": 1,
    "rating": 20,
    "title": "Yes! BanG_Dream!",
    "artists": "Poppin'Party",
    "author": "BanG Dream! Girls Band Party!",
    "engine": {
        // ...
    },
    "useSkin": {
        "useDefault": true
    },
    "useBackground": {
        "useDefault": true
    },
    "useEffect": {
        "useDefault": false,
        "item": {
            // ...
        }
    },
    "useParticle": {
        "useDefault": false,
        "item": {
            // ...
        }
    },
    "cover": {
        // ...
    },
    "bgm": {
        // ...
    },
    "data": {
        // ...
    }
}
```
