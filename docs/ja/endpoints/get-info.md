# `GET /info`

`/info`はサーバーの情報を提供し、Sonolusアプリがサーバーのトップページにデータを入力するために利用されます。

## ヘッダー

ヘッダー | 値 | 説明
:-- | :-- | :--
`Sonolus-Version` | `string` | 任意、[`Sonolus-Version`](../headers/sonolus-version)参照

## クエリパラメータ

クエリパラメータ | 値 | 説明
:-- | :-- | :--
`localization` | `string` | [`localization`](../query-parameters/localization)参照

## レスポンスの構文

```ts
type ServerInfo = {
    levels: Section<LevelItem>
    skins: Section<SkinItem>
    backgrounds: Section<BackgroundItem>
    effects: Section<EffectItem>
    particles: Section<ParticleItem>
    engines: Section<EngineItem>
}

type Section<T> = {
    items: T[]
    search: Search
}
```

## 例

```json
{
    "levels": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "skins": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "backgrounds": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "effects": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "particles": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    },
    "engines": {
        "items": [
            // ...
        ],
        "search": {
            // ...
        }
    }
}
```

## 備考

recommendはなるべく短く、最大でも5つのエントリのみを表示することをお勧めします。
