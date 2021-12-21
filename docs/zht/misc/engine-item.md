# `EngineItem`

`EngineItem`提供了引擎的資訊。

## 語法

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
    configuration: SRL<'EngineConfiguration'>
}
```

### `name`

用於識別引擎的獨特名稱。

### `skin` / `background` / `effect` / `particle`

引擎使用的預設項目。

## 例子

```json
{
    "name": "bandori",
    "version": 4,
    "title": "BanG Dream!",
    "subtitle": "BanG Dream! 少女樂團派對！",
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
