---
date: 2026-09-28
description: Aspose.PSD for Java を使用して、PSD のカラーモードを 16 ビットグレースケールに設定しながら PSD を PNG
  にエクスポートする方法を学びます。コード例付きのステップバイステップ ガイドです。
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: PSD を PNG にエクスポート – 16ビットグレースケール – Java
og_description: Aspose.PSD for Java を使用して、16ビットグレースケールで PSD を PNG にエクスポートします。65,536
  のグレー階調を保持するステップバイステップのチュートリアルをご覧ください。
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Javaで16ビットグレースケールで PSD を PNG にエクスポート – Aspose.PSD ガイド
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Javaで16ビットグレースケール カラーモードのPSDをPNGにエクスポートする方法
url: /ja/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaで16ビットグレースケールカラー モードのPSDをPNGにエクスポートする

## はじめに
PSDをPNGにエクスポートしながら16ビットグレースケールカラー モードを保持すると、プロの写真のような階調の深さとPNGの汎用的な互換性を両立できます。このガイドでは、Aspose.PSD for Java を使用して **PSDのカラー モードを16ビットグレースケールに設定**し、続いて **PSDをPNGとしてエクスポート**する方法を学びます。チュートリアルは前提条件からトラブルシューティングまで網羅しているので、任意のJavaベースの画像パイプラインにワークフローを組み込むことができます。

## クイック回答
- **「PSDをPNGにエクスポートする」とは何ですか？** PSD を読み込み、必要に応じてカラー モードを変更し、PNG ファイルとして保存します。  
- **変換を担当する Aspose クラスはどれですか？** `PsdImage` が PSD を読み込み、`PngOptions` が PNG の出力設定を定義します。  
- **本番環境でライセンスは必要ですか？** はい – トライアルはテストに使用できますが、商用利用には有料ライセンスが必要です。  
- **16ビット深度は PNG で保持できますか？** もちろんです。`PngColorType.GrayscaleWithAlpha` を使用します。  
- **サポートされている IDE はどれですか？** 任意の Java IDE – IntelliJ IDEA、Eclipse、VS Code、または NetBeans が使用可能です。

## PSDをPNGにエクスポートするとは？
PSDをPNGにエクスポートするとは、Adobe Photoshop ドキュメント（PSD）を Portable Network Graphics（PNG）ファイルに変換し、画像のピクセルデータとカラー深度を保持するプロセスです。この変換は、ウェブ上で高品質なグレースケール資産をトーンの詳細を失わずに共有する際に一般的に使用されます。

## なぜ16ビットグレースケールでPSDをPNGにエクスポートするのか？
PNG にエクスポートしながら16ビットグレースケールを保持すると、65 536 色階調のグレーが得られ、8ビット画像よりはるかに豊かな階調表現が可能になります。PNG の普遍的なサポートにより、ブラウザ、モバイルアプリ、デスクトップエディタでファイルをロスなく表示でき、Aspose.PSD のロスレス圧縮によりアーティファクトが一切発生しません。

## 前提条件
開始する前に、以下の項目を用意してください。

1. **Java Development Kit (JDK)** – 最新の JDK を [Oracle のサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からインストールします。  
2. **Aspose.PSD for Java ライブラリ** – [Aspose ダウンロードページ](https://releases.aspose.com/psd/java/) から JAR をダウンロードします。  
3. **IDE** – IntelliJ IDEA、Eclipse、または Visual Studio Code が完全に動作します。  
4. **基本的な Java 知識** – クラス作成、例外処理、ファイルパス操作に慣れていることが望ましいです。  
5. **サンプル PSD ファイル** – Adobe Photoshop で作成するか、オンラインで無料サンプルを取得してください。

## PSDをPNGにエクスポートする手順

## PSDのカラー モードを16ビットグレースケールに設定するには？
`PsdImage` は Aspose.PSD のクラスで、PSD ファイルをメモリにロードして表現します。  
`ColorMode` は PSD 画像のカラー モードを定義する列挙型です。  

`PsdImage` で PSD を読み込み、`ColorMode` プロパティでカラー モードを変更し、変更後のファイルを保存します。この操作はすべてメモリ上で完結するため、中間ファイルが不要で高速かつ効率的です。

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

これらのインポートにより、PSD ファイルの操作、カラー モードの設定、PNG へのエクスポートに必要な機能が利用可能になります。

## ソースと出力ディレクトリを定義するには？
`File` は java.io のクラスで、ファイルシステム上のファイルまたはディレクトリパスを表します。  

プログラムに元の PSD を読む場所と、変換後の PNG を書き込む場所を指示する必要があります。絶対パスでも相対パスでも構いませんが、環境間で一貫性を保ち、パス解決エラーを防ぎましょう。

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

プレースホルダー文字列を実際のマシン上のパスに置き換えてください。

## 再利用可能なメソッドに変換ロジックをカプセル化するには？
`convertPsdToPng` は、PSD ファイルを PNG に変換するためのすべての手順をカプセル化したカスタムメソッドです。  

専用メソッドを作成することで、複数のファイルや異なる設定に対して同じ変換手順を再利用できます。ソースパス、出力フォルダー、オプションの圧縮レベルなどのパラメータを渡すことで、ワークフローを柔軟かつ保守しやすくなります。

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

このメソッドにより、**PSD のカラー モードを設定**し、続いて **PSD を PNG にエクスポート**する一連の流れを実現できます。

## PSDをロードして16ビットグレースケールモードを適用するには？
`PsdImage` は PSD ファイルをメモリにロードする Aspose.PSD のクラスです。  
`ColorMode.GRAYSCALE_16` は画像を 16 ビットグレースケールに設定する列挙値です。  
`channelBitsCount` はチャンネルあたりのビット数を指定するプロパティです。  

変換メソッド内でフルパスを構築し、`PsdImage` をインスタンス化して `ColorMode` を `ColorMode.GRAYSCALE_16` に変更します。`channelBitsCount` プロパティは 16 に設定し、高ビット深度を保持して画像がすべてのトーン情報を保持できるようにします。

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` は各エクスポートファイルに使用した設定を追跡するのに役立ちます。

## 画像に薄い枠線を描くには（オプション）？
`Graphics` は `PsdImage` キャンバス上で描画機能を提供するクラスです。  

テスト時に出力を見やすくするため、画像の周囲にグレーの矩形をオプションで描画できます。このステップはレイヤーやグラフィックオブジェクトの扱い方を示すもので、矩形は画像サイズに関係なく中央に配置されるよう動的に計算されます。

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

矩形は画像サイズに関係なく中央に配置されるよう動的に計算されます。

## 新しいカラー モードで変更されたPSDを保存するには？
`PsdOptions` は PSD ファイルの保存方法（カラー モードやビット深度設定など）を制御するクラスです。  

描画（またはスキップ）後、`PsdImage` インスタンスの `save` を呼び出し、16 ビットグレースケール構成を保持する `PsdOptions` オブジェクトを渡します。これにより、保存された PSD がデータロスなしに目的のカラー モードを保持します。

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## 16ビット深度を保持したままPSDをPNGに変換するには？
`PngOptions` は PNG の出力設定（カラー タイプや圧縮レベルなど）を定義するクラスです。  
`PngColorType.GrayscaleWithAlpha` は 16 ビットグレースケールデータをアルファ チャネル付きで保存する列挙値です。  

新たに保存した PSD をロードし、`PngOptions` に `PngColorType.GrayscaleWithAlpha` を設定して `save` を呼び出します。これにより、PNG ファイル内に 16 ビットグレースケールデータが保持され、ロスレスで高品質な画像が得られ、さらなる処理や配布に適します。

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

これで **PSDをPNGにエクスポート**し、高品質な 16 ビットグレースケール データを保持できました。

## 一般的な問題と解決策
| 問題 | 発生理由 | 解決策 |
|-------|----------------|-----|
| **“Unsupported color type” 例外** | サポートされていないチャンネル構成で PSD を保存しようとしたため。 | `channelBitsCount` が実際のビット深度（16）と一致していること、`channelsCount` がグレースケール（1）に正しく設定されていることを確認してください。 |
| **ファイルが見つからない** | ソースディレクトリのパスが間違っているため。 | `sourceDir` 文字列を再確認し、指定位置に PSD ファイルが存在することを確認してください。 |
| **出力 PNG が黒くなる** | アルファ処理が正しく行われずに PNG が保存されたため。 | 上記のように `PngColorType.GrayscaleWithAlpha` を使用してください。 |
| **大容量 PSD でメモリオーバーフロー** | ファイル全体をメモリにロードしたため。 | `PsdImage.load(inputStream, new LoadOptions())` でストリーミングモードを有効にし、大きなファイルを効率的に処理してください。 |

## よくある質問

**Q: 16ビットグレースケールカラー モードとは何ですか？**  
A: 65 536 色階調のグレーを提供し、標準的な 8 ビット（256 色階調）よりはるかに豊かなトーンディテールを実現します。

**Q: Aspose.PSD をグレースケール以外の画像でも使用できますか？**  
A: もちろんです！Aspose.PSD は RGB、CMYK、Lab、Indexed など多数のカラー モードをサポートしています。

**Q: Aspose.PSD のトライアル版はありますか？**  
A: はい、無料トライアル版をご利用いただけます。詳しくは [Aspose ダウンロードページ](https://releases.aspose.com/) をご覧ください。

**Q: さらに多くの Aspose.PSD のサンプルはどこで見つかりますか？**  
A: 公式 [ドキュメンテーション](https://reference.aspose.com/psd/java/) で詳細なチュートリアル、API リファレンス、サンプルプロジェクトが提供されています。

**Q: Aspose.PSD のライセンスはどのように購入できますか？**  
A: [Aspose 購入ページ](https://purchase.aspose.com/buy) からライセンスをご購入いただけます。

**最終更新日:** 2026-09-28  
**テスト環境:** Aspose.PSD for Java 24.12（執筆時点での最新バージョン）  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java を使用して指定ビット深度で PSD を PNG に変換する](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Aspose.PSD for Java を使用してレイヤー効果付きで PSD を PNG にエクスポートする](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD Java で PSD を JPEG として保存し、RGB カラーをサポートする](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}