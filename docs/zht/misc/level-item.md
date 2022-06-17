# `LevelItem`

`LevelItem`提供了關卡的資訊。

## 語法

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

用於識別關卡的獨特名稱。

### `UseItem<T>`

如果`useDefault`為`true`，關卡將使用關卡引擎的預設選項。

否則，`item`會被使用。

## 例子

```json
{
    "name": "bandori.1.expert",
    "version": 1,
    "rating": 20,
    "title": "Yes! BanG_Dream!",
    "artists": "Poppin'Party",
    "author": "BanG Dream! 少女樂團派對！",
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
