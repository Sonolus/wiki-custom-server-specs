# `ParticleItem`

`ParticleItem`は、パーティクルの情報を提供します。

## 構文

```ts
type ParticleItem = {
    name: string
    version: 1
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'ParticleThumbnail'>
    data: SRL<'ParticleData'>
    texture: SRL<'ParticleTexture'>
}
```

### `name`

パーティクルを識別する一意の名前(ID)。

## 例

```json
{
    "name": "bandori-1",
    "version": 1,
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
