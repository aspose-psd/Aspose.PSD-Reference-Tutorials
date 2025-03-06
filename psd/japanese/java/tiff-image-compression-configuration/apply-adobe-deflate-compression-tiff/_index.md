---
title: Adobe Deflate 圧縮を TIFF に適用する - Java
linktitle: Adobe Deflate 圧縮を TIFF に適用する - Java
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して Adobe Deflate 圧縮を TIFF 画像に適用する方法を学びます。効率的な画像処理のためのステップバイステップ ガイド。
weight: 12
url: /ja/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adobe Deflate 圧縮を TIFF に適用する - Java

## 導入

品質を落とさずに TIFF 画像を効率的に圧縮する方法を考えたことはありませんか? 大きな画像ファイルを扱っている場合、読み込み時間が遅くなったり、ストレージの問題に悩まされたことがあるでしょう。そこで役立つのが Adobe Deflate 圧縮です。Aspose.PSD for Java を使用すると、プロジェクトに簡単に実装できます。このチュートリアルでは、Adobe Deflate 圧縮を TIFF 画像に適用する手順を段階的に説明します。準備はできましたか? さあ、始めましょう!

## 前提条件

実際のコードに進む前に、すべてが設定されていることを確認しましょう。必要なものは次のとおりです。

1. Java 開発キット (JDK): マシンに最新バージョンの JDK がインストールされていることを確認してください。
2.  Aspose.PSD for Java: Aspose.PSD for Javaライブラリをダウンロードしてプロジェクトに統合します。[ここ](https://releases.aspose.com/psd/java/).
3. 開発環境: IntelliJ IDEA、Eclipse、NetBeans などの IDE。
4. 一時ライセンス（オプション）：購入の準備ができていない場合は、[一時ライセンス](https://purchase.aspose.com/temporary-license/)機能を試してみましょう。

## パッケージのインポート

まず、Java プロジェクトに必要なパッケージをインポートします。これらのインポートは、Aspose.PSD ライブラリと Java ユーティリティを操作できるようにするため、非常に重要です。

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

基本事項を説明したので、プロセスをわかりやすい手順に分解してみましょう。

## ステップ1: TIFFオプションを設定する

まず最初に、インスタンスを作成する必要があります`TiffOptions`必要に応じて設定します。これらのオプションは、解像度、配色、圧縮など、TIFF ファイルの処理方法を定義します。

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

ここでは、`TiffOptions`デフォルトの形式でオブジェクトを作成します。しかし、これはほんの始まりに過ぎません。 

## ステップ2: イメージのプロパティを構成する

次に、TIFF画像のさまざまなプロパティを設定する必要があります。`BitsPerSample`, `Photometric`, `Resolution`、 そして`PlanarConfiguration`これらの設定により、画像データの保存方法と表示方法が決まります。

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

各プロパティの機能は次のとおりです。
- BitsPerSample: 各カラー チャネルのサンプルあたりのビット数を設定します。
- フォトメトリック: カラー モデル (この場合は RGB) を定義します。
- 解像度: 画像の水平解像度と垂直解像度を指定します。
- PlanarConfiguration: ピクセル データの保存方法を決定します。

## ステップ3: Adobe Deflate圧縮を適用する

ここで魔法の登場です! TIFF 画像に Adobe Deflate 圧縮を適用します。これにより、画像の品質を損なうことなくファイル サイズを縮小できます。

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

Adobe Deflate は、ファイル サイズを縮小しながら高品質を維持する必要がある画像に最適なロスレス圧縮方式です。

## ステップ4: TIFF画像の作成と編集

オプションを設定したら、新しい TIFF 画像を作成して操作します。この手順では、単純な 100 x 100 の画像を作成し、赤いピクセルで塗りつぶします。

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

ここでは、画像の各ピクセルをループして、その色を赤に設定しています。もちろん、この部分をカスタマイズして、より複雑な画像を作成することもできます。

## ステップ5: 圧縮されたTIFF画像を保存する

最後に、イメージを設定して作成したら、圧縮を適用して保存します。正しいディレクトリ パスを指定してください。

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

これで完了です。Aspose.PSD for Java を使用して、TIFF 画像に Adobe Deflate 圧縮を正常に適用できました。

## 結論

これで完了です。Adobe Deflate 圧縮を TIFF 画像に適用するのは、Aspose.PSD for Java を使用すると簡単です。Web サイト、デジタル メディア、またはその他のプロジェクト用の大きな画像を扱う場合でも、この方法を使用すると、ファイルのサイズを管理しやすくしながら、高品質を維持できます。Aspose.PSD for Java の強みは、そのシンプルさと効率性にあり、複雑な画像形式を扱う開発者にとって頼りになるツールとなっています。

## よくある質問

### Adobe Deflate 圧縮とは何ですか?
Adobe Deflate は、品質を損なうことなく TIFF 画像のサイズを縮小するために使用されるロスレス圧縮方式です。

### Aspose.PSD for Java で他の圧縮方法を使用できますか?
はい、Aspose.PSD は LZW、CCITT、JPEG などのさまざまな圧縮方式をサポートしています。

### Aspose.PSD ライブラリは無料ですか?
 Aspose.PSDは無料トライアルを提供していますが、フル機能を使用するにはライセンスが必要です。[一時ライセンス](https://purchase.aspose.com/temporary-license/)試してみる。

### 解像度設定は TIFF 画像にどのような影響を与えますか?
解像度によって、印刷または表示される画像の鮮明さが決まります。解像度が高いほど品質は向上しますが、ファイル サイズが大きくなります。

### Aspose.PSD for Java で他の画像形式を操作できますか?
もちろんです! Aspose.PSD は、PSD、PNG、JPEG など、さまざまな形式をサポートしています。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
