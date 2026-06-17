---
date: 2026-04-05
description: Aspose.PSD for Java を使用して PSD ファイルの露出調整レイヤーをレンダリングする方法を学びます。露出レイヤーの変更と追加に関するコード例付きのステップバイステップガイド。
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: PSDファイルで露出調整レイヤーをレンダリングする - Java
second_title: Aspose.PSD Java API
title: PSDファイルの露出調整レイヤーをレンダリング - Java
url: /ja/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD ファイルの露出調整レイヤーをレンダリングする - Java

## 概要

Photoshop PSD ファイルを扱っていて、プログラムで **露出調整レイヤーをレンダリング** する必要がありますか？既存のレイヤーを調整する場合でも新しいレイヤーを追加する場合でも、Aspose.PSD for Java はこれらのタスクを強力かつ直感的に処理する方法を提供します。このガイドでは、Aspose.PSD for Java を使用して PSD ファイル内の露出調整レイヤーをレンダリングおよび変更する方法を順を追って説明します。チュートリアルの最後までに、既存のレイヤーの露出設定を調整し、PSD ファイルに新しい露出調整レイヤーを追加する方法が分かります。それでは始めましょう！

## クイック回答
- **必要なライブラリは何ですか？** Aspose.PSD for Java
- **既存の露出レイヤーを編集できますか？** はい、露出、オフセット、ガンマ補正を変更できます。
- **新しい露出調整レイヤーを追加するには？** `PsdImage` インスタンスで `addExposureAdjustmentLayer()` を使用します。
- **PNG エクスポートはサポートされていますか？** もちろんです – `PngOptions` を使用して結果を PNG として保存します。
- **本番環境でライセンスが必要ですか？** 本番利用には商用ライセンスが必要です。無料トライアルが利用可能です。

## レンダリングされた露出調整レイヤーとは何ですか？

露出調整レイヤーは、基になる画像の明るさ、オフセット、ガンマを変更する非破壊的な Photoshop レイヤーです。これをレンダリングするとは、設定を適用して視覚的な結果が調整を反映するようにし、PNG などの形式でエクスポートできるようにすることを意味します。

## なぜ Aspose.PSD for Java を使用して露出調整レイヤーをレンダリングするのか？

- **完全なコントロール** – Photoshop を開かずにレイヤー属性を操作できます。
- **バッチ処理** – 多数のファイルに対して調整を自動化できます。
- **クロスプラットフォーム** – JDK があればどのシステムでも実行できます。
- **PSD 構造を保持** – 将来の編集のためにレイヤーを編集可能なままに保ちます。

## 前提条件

1. **Java Development Kit (JDK)** – 少なくとも JDK 8 が必要です。
2. **Aspose.PSD for Java** – こちらからダウンロードしてください [here](https://releases.aspose.com/psd/java/)。
3. **基本的な Java の知識** – 標準的な Java 構文に慣れている必要があります。
4. **IDE またはテキストエディタ** – IntelliJ IDEA、Eclipse、VS Code、またはお好みのエディタ。

## パッケージのインポート

まず、必要な Aspose.PSD クラスをインポートします:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 露出調整レイヤーをレンダリングする方法 – ステップバイステップガイド

### ステップ 1: PSD ファイルをロードする

`"Your Document Directory"` を PSD ファイルが格納されているフォルダーに置き換えてください。`Image.load()` メソッドは `PsdImage` オブジェクトを返し、ドキュメントのレイヤーにフルアクセスできます。

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

### ステップ 2: 既存の露出調整レイヤーを編集する

ループはすべてのレイヤーを走査し、`ExposureLayer` を見つけて 3 つの主要パラメータを更新します。これはカスタム値で **露出調整レイヤーをレンダリング** する核心部分です。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

### ステップ 3: 変更された PSD ファイルを保存する

変更された PSD は元のレイヤーをすべて保持しますが、露出調整は新しい設定を反映しています。

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

### ステップ 4: 結果を PNG としてエクスポートする

`TruecolorWithAlpha` を使用した `PngOptions` により、エクスポートされた PNG はフルカラー深度と PSD からの透過情報を保持します。

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

### ステップ 5: 新しい露出調整レイヤーを追加する

既存のドキュメントに **新しい露出調整レイヤーを追加** する必要がある場合は、以下のコードを使用してください:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

`addExposureAdjustmentLayer` メソッドは指定された露出、オフセット、ガンマ値で新しい調整レイヤーを作成し、以前と同様にレンダリングおよびエクスポートできます。

## 一般的な問題とヒント

- **レイヤーが見つからない** – PSD に実際に `ExposureLayer` が含まれていることを確認してください。`instanceof ExposureLayer` を使用して `ClassCastException` を回避します。
- **ファイルパスエラー** – 絶対パスを使用するか、`dataDir` がファイル区切り文字（`/` または `\`）で終わっていることを確認してください。
- **ライセンス例外** – 有効なライセンスなしで実行すると、出力に透かしが追加されます。コードの早い段階でライセンスを登録してください (`License license = new License(); license.setLicense("Aspose.PSD.lic");`)。

## FAQ

### Aspose.PSD for Java とは何ですか？

Aspose.PSD for Java は、Java を使用してプログラム的に PSD ファイルを作成、編集、変換できるライブラリです。Photoshop ドキュメントの操作に必要な包括的な機能を提供します。

### Aspose.PSD for Java を使用して他の種類のレイヤーを操作できますか？

はい、Aspose.PSD for Java はテキストレイヤー、調整レイヤー、画像レイヤーなどさまざまなレイヤータイプをサポートしており、PSD ファイルの広範な操作が可能です。

### Aspose.PSD for Java の使い方を始めるには？

ライブラリを [website](https://releases.aspose.com/psd/java/) からダウンロードし、詳細なガイドやサンプルコードは [documentation](https://reference.aspose.com/psd/java/) を参照してください。

### Aspose.PSD for Java の無料トライアルはありますか？

はい、無料トライアルが利用可能です。こちらからダウンロードしてください [here](https://releases.aspose.com/)。

### Aspose.PSD for Java のサポートはどこで受けられますか？

サポートが必要な場合は、[Aspose support forum](https://forum.aspose.com/c/psd/34) にアクセスして質問し、コミュニティから助けを得ることができます。

**追加の質問**

**Q: 複数の PSD ファイルをバッチ処理できますか？**  
A: もちろんです。ロード、編集、保存ロジックをループで囲み、ファイルパスのリストを反復処理します。

**Q: 新しい露出レイヤーを追加したときにライブラリはレイヤー階層を保持しますか？**  
A: はい。新しいレイヤーは既存レイヤーの上に追加され、元の階層構造を維持します。

**Q: PNG 以外にエクスポートできる画像形式は何ですか？**  
A: Aspose.PSD は JPEG、BMP、TIFF など、対応する `*Options` クラスを介して複数の形式をサポートしています。

---

**最終更新日:** 2026-04-05  
**テスト環境:** Aspose.PSD for Java 24.10  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}