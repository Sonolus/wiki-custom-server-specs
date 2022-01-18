# `SkinItem`

`SkinItem`は、スキンの情報を示します。

## 構文

```ts
type SkinItem = {
    name: string
    version: 2
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'SkinThumbnail'>
    data: SRL<'SkinData'>
    texture: SRL<'SkinTexture'>
}
```

### `name`

スキンを識別する一意の名前(ID)。

## 例

```json
{
    "name": "bandori.n00.f00.l00",
    "version": 2,
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
