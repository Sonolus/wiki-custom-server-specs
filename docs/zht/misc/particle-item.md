# `ParticleItem`

`ParticleItem`提供了粒子的資訊。

## 語法

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

用於識別粒子的獨特名稱。

## 例子

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
