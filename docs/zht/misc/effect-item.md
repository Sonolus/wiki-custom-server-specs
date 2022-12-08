# `EffectItem`

`EffectItem`提供了效果的資訊。

## 語法

```ts
type EffectItem = {
    name: string
    version: 4
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'EffectThumbnail'>
    data: SRL<'EffectData'>
    audio: SRL<'EffectAudio'>
}
```

### `name`

用於識別效果的獨特名稱。

## 例子

```json
{
    "name": "bandori-00",
    "version": 4,
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
