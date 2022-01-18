# `LevelItem`

`LevelItem`は、レベルの情報を示します。

## 構文

```ts
type UseItem<T> = {
    useDefault: boolean
    item?: T
}

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
    data: SRL<'LevelData'>
}
```

### `name`

レベルを識別する一意の名前(ID)。

### `UseItem<T>`

`useDefault`が`true`の場合、レベルはエンジンのデフォルト設定を使用します。

それ以外の場合は、 `item`が使用されます。

## 例

```json
{
    "name": "bandori.1.expert",
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
