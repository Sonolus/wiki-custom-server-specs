# `EngineItem`

`EngineItem` provides information of a engine.

## Syntax

```ts
type EngineItem = {
    name: string
    version: 9
    title: string
    subtitle: string
    author: string
    skin: SkinItem
    background: BackgroundItem
    effect: EffectItem
    particle: ParticleItem
    thumbnail: SRL<'EngineThumbnail'>
    playData: SRL<'EnginePlayData'>
    tutorialData: SRL<'EngineTutorialData'>
    rom?: SRL<'EngineRom'>
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
    "version": 7,
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
    "tutorialData": {
        // ...
    },
    "playData": {
        // ...
    },
    "configuration": {
        // ...
    }
}
```
