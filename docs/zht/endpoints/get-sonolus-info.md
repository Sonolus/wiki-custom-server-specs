# `GET /sonolus/info`

`/sonolus/info`提供了伺服器的資訊，會由 Sonolus 程式使用來生成伺服器的主頁。

## 標頭

| 標頭              | 數值     | 描述                                                          |
| :---------------- | :------- | :------------------------------------------------------------ |
| `Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。 |

## 查詢函數

| 查詢函數       | 數值     | 描述                                                     |
| :------------- | :------- | :------------------------------------------------------- |
| `localization` | `string` | 詳見[`localization`](../query-parameters/localization)。 |

## 響應語法

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

## 例子

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

## 備註

建議每個分類僅顯示 5 個項目來保持頁面不會過長。
