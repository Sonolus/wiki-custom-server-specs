# `EffectItem`

`EffectItem`は、エフェクトの情報を示します。

## 構文

```ts
type EffectItem = {
    name: string
    version: 3
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'EffectThumbnail'>
    data: SRL<'EffectData'>
    audio: SRL<'EffectAudio'>
}
```

### `name`

エフェクトを識別する一意の名前(ID)。

## 例

```json
{
    "name": "bandori-00",
    "version": 3,
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
