# Resources

リソースは、外観と動作を動的に変更するために使用できるSonolusアプリが理解できるファイルです。

## Image Resources

イメージリソースは`LevelCover`などのタイプに使用されます。

`.png`が、推奨形式です。

## Audio Resources

オーディオリソースは`LevelBgm`などのタイプに使用されます。

`.mp3`が、推奨形式です。

## JSON Resources

JSONリソースは`LevelData`などのタイプに使用されます。

`.json`のみがサポートされており、データはGZipで圧縮する必要があります。(zlibではなくgzipである必要があります)

## Archive Resources

アーカイブリソースは`EffectAudio`などのタイプに使用されます。

`.zip`のみがサポートされています。

## Binary Resources

バイナリリソースは、 `EngineRom`などのタイプに使用されます。

コンテンツは、それぞれのタイプで定義されたスキーマを持つバイナリデータであり、GZipで圧縮されている必要があります。
