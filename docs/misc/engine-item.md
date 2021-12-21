# `EngineItem`

`EngineItem` provides information of a engine.

## Syntax

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

Unique name which identifies the engine.

### `skin` / `background` / `effect` / `particle`

Default items to use with the engine.

## Examples

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