# `SRL`

`SRL` （Sonolus Resource Locator）は、Sonolusアプリがリソースを検索、ロード、およびキャッシュするためのリソースの情報を提供します。

## 構文

```ts
type SRL<T extends ResourceType> = {
    type: T
    hash: string
    url: string
}

type ResourceType =
    | 'LevelCover'
    | 'LevelBgm'
    | 'LevelPreview'
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
    | 'EngineRom'
    | 'EngineConfiguration'
```

### `type`

リソースのタイプ。

### `hash`

キャッシングに使用される、リソースのSHA-1ハッシュ(オプション)。

一致するハッシュを持つリソースがキャッシュされていて利用可能な場合、即時にロードされます。

### `url`

リソースの絶対URLまたは相対URL。

相対URL（ `/`始まるURL）が使用されている場合、それはサーバーアドレス（ドメインルートではない）に相対的です。

## 例

```json
{
    "type": "LevelCover",
    "hash": "...",
    "url": "https://..."
}
```

## 備考

`hash`はオプションですが、Sonolusアプリがキャッシュされたリソースを使用できるようにするために利用することを強くお勧めします。これにより、帯域幅の使用量と読み込み時間を削減して、プレーヤーのエクスペリエンスを向上させます。
