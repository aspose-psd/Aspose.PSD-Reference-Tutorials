---
title: PSD ファイルで露出調整レイヤーをレンダリングする - Java
linktitle: PSD ファイルで露出調整レイヤーをレンダリングする - Java
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイル内の露出レイヤーをレンダリングおよび調整する方法を学びます。露出レイヤーを変更および追加するためのコード例を含むステップバイステップ ガイド。
weight: 15
url: /ja/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD ファイルで露出調整レイヤーをレンダリングする - Java

## 導入

Photoshop PSD ファイルで作業していて、露出を調整したり、露出調整レイヤーをプログラムで追加したりする必要がありますか? 既存のレイヤーを微調整する場合でも、新しいレイヤーを追加する場合でも、Aspose.PSD for Java はこれらのタスクを処理するための強力で直感的な方法を提供します。 このガイドでは、Aspose.PSD for Java を使用して PSD ファイルの露出調整レイヤーをレンダリングおよび変更する方法について説明します。 このチュートリアルの最後には、既存のレイヤーの露出設定を調整し、PSD ファイルに新しい露出調整レイヤーを追加する方法がわかります。 さあ、始めましょう!

## 前提条件

チュートリアルに進む前に、次の前提条件を満たしていることを確認してください。

1. Java 開発キット (JDK): マシンに JDK がインストールされている必要があります。このガイドでは、少なくとも JDK 8 がインストールされていることを前提としています。
2.  Aspose.PSD for Java: PSDファイルを扱うにはAspose.PSDライブラリが必要です。ここからダウンロードできます。[ここ](https://releases.aspose.com/psd/java/).
3. Java の基礎知識: Java プログラミングに精通していれば、簡単に理解できるようになります。
4. IDE またはテキスト エディター: IntelliJ IDEA、Eclipse などの IDE、または任意のテキスト エディターを使用して、Java コードを記述および実行します。

## パッケージのインポート

まず最初に、Aspose.PSD for Java から必要なパッケージをインポートしましょう。この手順により、コードが PSD ファイルの操作にライブラリの機能を利用できるようになります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## ステップ1: PSDファイルを読み込む

まず、PSD ファイルをアプリケーションに読み込む必要があります。手順は次のとおりです。

```java
String dataDir = "Your Document Directory";  //ドキュメントディレクトリを定義する
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  //ソースPSDファイルのパス

PsdImage im = (PsdImage) Image.load(sourceFileName);  //PSDファイルを読み込む
```

このコードスニペットでは、`"Your Document Directory"` PSDファイルが保存されているパスを入力します。`Image.load()`メソッドはPSDファイルをインスタンスにロードします`PsdImage`、レイヤーを操作できるようになります。

## ステップ2: 既存の露出調整レイヤーを編集する

PSD ファイルが読み込まれると、既存のレイヤーにアクセスして変更できます。ファイルに露出調整レイヤーが含まれている場合は、そのプロパティを調整できます。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  //露出レベルを調整する
        expLayer.setOffset(-0.25f);  //オフセットを設定する
        expLayer.setGammaCorrection(0.5f);  //ガンマ補正を調整する
    }
}
```

このループでは、PSDファイルのすべてのレイヤーを反復処理します。`ExposureLayer` 、我々はその`Exposure`, `Offset`、 そして`GammaCorrection`プロパティ。これにより、露出調整レイヤーの視覚的な出力を微調整できます。

## ステップ3: 変更したPSDファイルを保存する

変更を加えたら、更新された PSD ファイルを保存する必要があります。

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  //変更したPSDファイルを保存するパス

im.save(psdPathAfterChange);  //変更をPSDファイルに保存します
```

この行は、露出調整を保持しながら、変更された PSD ファイルを指定されたパスに保存します。

## ステップ4: PNGとしてエクスポート

更新された PSD ファイルを PNG としてエクスポートするには、次の手順に従います。

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // PNGファイルを保存するパス

PngOptions saveOptions = new PngOptions();  //PNGオプションの作成
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  //色の種類をアルファ付きのTruecolorに設定する

im.save(pngExportPath, saveOptions);  //PNGとして保存
```

ここ、`PngOptions`PNG エクスポート設定を構成するために使用されます。`PngColorType.TruecolorWithAlpha` PNG ファイルの色の深度と透明度が保持されます。

## ステップ5: 新しい露出調整レイヤーを追加する

既存の PSD ファイルに新しい露出調整レイヤーを追加する場合は、次のコードを使用します。

```java
String sourceFileName = dataDir + "PhotoExample.psd";  //ソースPSDファイルのパス

PsdImage img = (PsdImage) Image.load(sourceFileName);  //PSDファイルを読み込む

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  //新しい露出調整レイヤーを追加する

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  //変更したPSDファイルを保存するパス
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // PNGファイルを保存するパス

img.save(psdPathAfterChange);  //変更をPSDファイルに保存します

PngOptions options = new PngOptions();  //PNGオプションの作成
options.setColorType(PngColorType.TruecolorWithAlpha);  //色の種類をアルファ付きのTruecolorに設定する

img.save(pngExportPath, options);  //PNGとして保存
```

このステップでは、指定された露出、オフセット、ガンマ補正値を持つ新しい露出調整レイヤーが PSD ファイルに追加され、更新された PSD ファイルと PNG ファイルが保存されます。

## 結論

これで完了です。Aspose.PSD for Java を使用して PSD ファイルで露出レイヤーをレンダリングおよび調整する方法を学習しました。既存の露出レイヤーを変更する方法、新しい露出レイヤーを追加する方法、および作業を PNG ファイルとしてエクスポートする方法についても説明しました。写真の調整やデザイン アセットの準備など、これらのスキルにより、PSD ファイルをプログラムで管理する能力が向上します。コーディングを楽しんでください。

## よくある質問

### Aspose.PSD for Java とは何ですか?

Aspose.PSD for Java は、Java を使用してプログラム的に PSD ファイルを作成、編集、変換できるライブラリです。Photoshop ドキュメントを操作するための包括的な機能を提供します。

### Aspose.PSD for Java を使用して他の種類のレイヤーを操作できますか?

はい、Aspose.PSD for Java は、テキスト レイヤー、調整レイヤー、イメージ レイヤーなど、さまざまな種類のレイヤーをサポートしており、PSD ファイルの広範な操作が可能です。

### Aspose.PSD for Java を使い始めるにはどうすればよいですか?

まずはライブラリをダウンロードしてください。[Webサイト](https://releases.aspose.com/psd/java/)そして、[ドキュメント](https://reference.aspose.com/psd/java/)詳細なガイドと例については、こちらをご覧ください。

### Aspose.PSD for Java の無料試用版はありますか?

はい、無料トライアルをご利用いただけます。ダウンロードできます[ここ](https://releases.aspose.com/).

### Aspose.PSD for Java のサポートを受けるにはどうすればよいですか?

サポートについては、[Aspose サポート フォーラム](https://forum.aspose.com/c/psd/34)質問したり、コミュニティからサポートを受けたりできる場所です。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
