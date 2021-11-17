# `BackgroundItem`

`BackgroundItem` provides information of a background.

## Syntax

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

Unique name which identifies the background.

## Examples

```json
{
    "name": "bandori.live.00",
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
