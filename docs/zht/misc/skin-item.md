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
    "name": "bandori.n00.f00.l00",
    "version": 2,
    "title": "類型1／類型1／佈景類型00",
    "subtitle": "BanG Dream! 少女樂團派對！",
    "author": "BanG Dream! 少女樂團派對！",
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
