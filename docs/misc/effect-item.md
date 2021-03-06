# `EffectItem`

`EffectItem` provides information of a effect.

## Syntax

```ts
type EffectItem = {
    name: string
    version: 2
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'EffectThumbnail'>
    data: SRL<'EffectData'>
}
```

### `name`

Unique name which identifies the effect.

## Examples

```json
{
    "name": "bandori.skin00",
    "version": 2,
    "title": "SEスキン00",
    "subtitle": "BanG Dream! Girls Band Party!",
    "author": "BanG Dream! Girls Band Party!",
    "thumbnail": {
        // ...
    },
    "data": {
        // ...
    }
}
```
