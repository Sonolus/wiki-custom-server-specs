# `SkinItem`

`SkinItem` provides information of a skin.

## Syntax

```ts
type SkinItem = {
    name: string
    version: 3
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'SkinThumbnail'>
    data: SRL<'SkinData'>
    texture: SRL<'SkinTexture'>
}
```

### `name`

Unique name which identifies the skin.

## Examples

```json
{
    "name": "bandori-n00-f00-l00",
    "version": 3,
    "title": "TYPE1 / TYPE1 / レーンスキン00",
    "subtitle": "BanG Dream! Girls Band Party!",
    "author": "BanG Dream! Girls Band Party!",
    "thumbnail": {
        // ...
    },
    "data": {
        // ...
    },
    "texture": {
        // ...
    }
}
```
