# `SRL`

`SRL` (Sonolus Resource Locator) provides information of a resource for Sonolus app to locate, load, and cache it.

## Syntax

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
    | 'EngineConfiguration'
```

### `type`

Type of the resource.

### `hash`

Optional SHA-1 hash of the resource, used for caching.

If a cached resource with matching hash is available, it is immediately used.

### `url`

Absolute or relative URL of the resource.

If a relative URL (a URL starting with `/`) is used, it is relative to the server address (not domain root).

## Examples

```json
{
    "type": "LevelCover",
    "hash": "...",
    "url": "https://..."
}
```

## Remarks

While `hash` is optional, it is strongly recommended to allow Sonolus app to use cached resources, thus improving player experience by reducing bandwidth usage and loading time.
