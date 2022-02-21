# `EngineItem`

`EngineItem`は、エンジンの情報を示します。

## 構文

```ts
type EngineItem = {
    name: string
    version: 4
    title: string
    subtitle: string
    author: string
    skin: SkinItem
    background: BackgroundItem
    effect: EffectItem
    particle: ParticleItem
    thumbnail: SRL<'EngineThumbnail'>
    data: SRL<'EngineData'>
    rom?: SRL<'EngineRom'>
    configuration: SRL<'EngineConfiguration'>
}
```

### `name`

エンジンを識別する一意の名前(ID)。

### `skin` / `background` / `effect` / `particle`

エンジンで使用するデフォルトのアイテム。

## 例

```json
{
    "name": "bandori",
    "version": 4,
    "title": "BanG Dream!",
    "subtitle": "BanG Dream! Girls Band Party!",
    "author": "Burrito",
    "skin": {
        // ...
    },
    "background": {
        // ...
    },
    "effect": {
        // ...
    },
    "particle": {
        // ...
    },
    "thumbnail": {
        // ...
    },
    "data": {
        // ...
    },
    "configuration": {
        // ...
    }
}
```
