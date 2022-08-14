# `GET /sonolus/backgrounds/{name}`

`/sonolus/backgrounds/{name}`は `{name}`に指定された背景の詳細情報を提供し、Sonolus アプリがサーバーの背景の詳細ビューにデータを入力するために利用されます。

## ヘッダー

| ヘッダー          | 値       | 説明                                                      |
| :---------------- | :------- | :-------------------------------------------------------- |
| `Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)参照 |

## クエリパラメータ

| クエリパラメータ | 値       | 説明                                                   |
| :--------------- | :------- | :----------------------------------------------------- |
| `localization`   | `string` | [`localization`](../query-parameters/localization)参照 |

## レスポンスの構文

```ts
type BackgroundList = ItemList<BackgroundItem>
```

## 例

```json
{
    "item": {
        // ...
    },
    "description": "Description of the background",
    "recommended": [
        // ...
    ]
}
```
