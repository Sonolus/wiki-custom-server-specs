# `SkinItem`

`SkinItem`提供了佈景的資訊。

## 語法

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

用於識別佈景的獨特名稱。

## 例子

```json
{
    "name": "bandori-n00-f00-l00",
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
