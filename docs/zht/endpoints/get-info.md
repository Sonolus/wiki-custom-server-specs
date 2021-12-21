# `GET /info`

`/info`提供了伺服器的資訊，會由Sonolus程式使用來生成伺服器的主頁。

## 標頭

標頭 | 數值 | 描述
:-- | :-- | :--
`Sonolus-Version` | `string` | 非強制，詳見[`Sonolus-Version`](../headers/sonolus-version)。

## 查詢函數

查詢函數 | 數值 | 描述
:-- | :-- | :--
`localization` | `string` | 詳見[`localization`](../query-parameters/localization)。

## 響應語法

```ts
type ServerInfo = {
    levels: LevelItem[]
    skins: SkinItem[]
    backgrounds: BackgroundItem[]
    effects: EffectItem[]
    particles: ParticleItem[]
    engines: EngineItem[]
}
```

## 例子

```json
{
    "levels": [
        // ...
    ],
    "skins": [
        // ...
    ],
    "backgrounds": [
        // ...
    ],
    "effects": [
        // ...
    ],
    "particles": [
        // ...
    ],
    "engines": [
        // ...
    ]
}
```

## 備註

建議每個分類僅顯示5個項目來保持頁面不會過長。
