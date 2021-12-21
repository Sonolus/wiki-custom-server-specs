# `SRL`

`SRL`（Sonolus Resource Locator）提供了為Sonolus程式定位、讀取和緩存資源的資訊。

## 語法

```ts
type ResourceType =
    | 'LevelCover'
    | 'LevelBgm'
    | 'LevelData'
    | 'SkinThumbnail'
    | 'SkinData'
    | 'SkinTexture'
    | 'BackgroundThumbnail'
    | 'BackgroundData'
    | 'BackgroundImage'
    | 'BackgroundConfiguration'
    | 'EffectThumbnail'
    | 'EffectData'
    | 'EffectClip'
    | 'ParticleThumbnail'
    | 'ParticleData'
    | 'ParticleTexture'
    | 'EngineThumbnail'
    | 'EngineData'
    | 'EngineConfiguration'

type SRL<T extends ResourceType> = {
    type: T
    hash: string
    url: string
}
```

### `type`

資源的類型。

### `hash`

非強制，用於緩存的資源SHA-1 hash。

擁有相同hash的緩存資源會被馬上使用。

### `url`

資源的絕對或相對url。

如果使用相對url（以`/`開頭的url），url是相對於伺服器地址（而不是域根）的。

## 例子

```json
{
    "type": "LevelCover",
    "hash": "...",
    "url": "https://..."
}
```

## 備註

雖然不強制使用，但仍然強烈建議加入`hash`以確保Sonolus程式可以使用緩存資源，來提高載入網絡請求的速度並降低頻寬使用量，改善玩家的遊玩體驗。
