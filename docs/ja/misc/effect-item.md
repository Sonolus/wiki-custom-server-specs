# `EffectItem`

`EffectItem`は、エフェクトの情報を示します。

## 構文

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

エフェクトを識別する一意の名前(ID)。

## 例

```json
{
    "name": "bandori.skin00",
    "version": 2,
    "title": "SEスキン00",
    "subtitle": "BanG Dream! Girls Band Party!",
    "author": "BanG Dream! Girls Band Party!",
    "thumbnail": {
        // ...
    },
    "data": {
        // ...
    }
}
```
