# `ParticleItem`

`ParticleItem` provides information of a particle.

## Syntax

```ts
type ParticleItem = {
    name: string
    version: 2
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'ParticleThumbnail'>
    data: SRL<'ParticleData'>
    texture: SRL<'ParticleTexture'>
}
```

### `name`

Unique name which identifies the particle.

## Examples

```json
{
    "name": "bandori-1",
    "version": 2,
    "title": "Effect Type 1",
    "subtitle": "BanG Dream! Girls Band Party!",
    "author": "Sonolus",
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
