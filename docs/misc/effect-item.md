# `EffectItem`

`EffectItem` provides information of a effect.

## Syntax

```ts
type EffectItem = {
    name: string
    version: 5
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'EffectThumbnail'>
    data: SRL<'EffectData'>
    audio: SRL<'EffectAudio'>
}
```

### `name`

Unique name which identifies the effect.

## Examples

```json
{
    "name": "bandori-00",
    "version": 5,
    "title": "SEスキン00",
    "subtitle": "BanG Dream! Girls Band Party!",
    "author": "BanG Dream! Girls Band Party!",
    "thumbnail": {
        // ...
    },
    "data": {
        // ...
    },
    "audio": {
        // ...
    }
}
```
