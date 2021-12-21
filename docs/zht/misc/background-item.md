# `BackgroundItem`

`BackgroundItem`提供了背景的資訊。

## 語法

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

用於識別背景的獨特名稱。

## 例子

```json
{
    "name": "bandori.live.00",
    "version": 2,
    "title": "默認背景",
    "subtitle": "BanG Dream! 少女樂團派對！",
    "author": "BanG Dream! 少女樂團派對！",
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
