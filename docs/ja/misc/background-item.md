# `BackgroundItem`

`BackgroundItem`は、背景の情報を示します。

## 構文

```ts
type BackgroundItem = {
    name: string
    version: 2
    title: string
    subtitle: string
    author: string
    thumbnail: SRL<'BackgroundThumbnail'>
    data: SRL<'BackgroundData'>
    image: SRL<'BackgroundImage'>
    configuration: SRL<'BackgroundConfiguration'>
}
```

### `name`

背景を識別する一意の名前(ID)。

## 例

```json
{
    "name": "bandori-live-00",
    "version": 2,
    "title": "デフォルト背景",
    "subtitle": "BanG Dream! Girls Band Party!",
    "author": "BanG Dream! Girls Band Party!",
    "thumbnail": {
        // ...
    },
    "data": {
        // ...
    },
    "image": {
        // ...
    },
    "configuration": {
        // ...
    }
}
```
