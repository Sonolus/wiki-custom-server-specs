# `EffectItem`

`EffectItem`提供了效果的資訊。

## 語法

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

用於識別效果的獨特名稱。

## 例子

```json
{
    "name": "bandori.skin00",
    "version": 2,
    "title": "SE佈景00",
    "subtitle": "BanG Dream! 少女樂團派對！",
    "author": "BanG Dream! 少女樂團派對！",
    "thumbnail": {
        // ...
    },
    "data": {
        // ...
    }
}
```
