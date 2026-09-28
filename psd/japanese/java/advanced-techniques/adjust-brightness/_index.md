---
date: 2026-09-28
description: Java 画像処理チュートリアルでは、Aspose.PSD for Java を使用して画像の明るさを調整する方法を示します。ステップバイステップのコードに従って、PSD
  または TIFF ファイルを読み込み、変更し、保存します。
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: 画像の明るさを調整
og_description: Java 画像処理チュートリアルでは、Aspose.PSD for Java を使用して画像の明るさを調整する方法を示します。ステップバイステップのコードに従って、PSD
  または TIFF ファイルを読み込み、変更し、保存します。
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Java 画像処理: Aspose.PSD で明るさを調整'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Java 画像処理: Aspose.PSD で明るさを調整'
url: /ja/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した画像の明るさ調整

## はじめに

この **java image processing** チュートリアルでは、Javaコードから直接画像の明るさを調整する方法を学びます。明るさの調整は、グラフィックデザイナー、写真家、画像処理パイプラインを構築するすべての人に頻繁に必要とされる作業です。この **java image manipulation** ガイドでは、PSD/TIFF の読み込み、明るさオフセットの適用、結果の保存という完全なワークフローを Aspose.PSD for Java ライブラリを使用して解説します。

## クイック回答
- **明るさを扱うライブラリは何ですか？** Aspose.PSD for Java.  
- **どのメソッドが明るさを変更しますか？** `RasterImage.adjustBrightness()`.  
- **PSD と TIFF ファイルを扱えますか？** はい、API は両方のフォーマットと 10 以上の追加画像タイプをサポートしています。  
- **本番環境でライセンスが必要ですか？** 評価版以外の使用には商用ライセンスが必要です。  
- **実装にどれくらい時間がかかりますか？** 基本的な調整で通常 10 分未満です。

## java image processing とは何ですか？
`Java image processing` は、Java を使用して画像データをプログラムで読み取り、変換し、書き込むための技術群を指します。明るさの調整は、すべてのピクセルの全体的な明度を変える基本的な操作の一つで、暗い領域を明るくしたり、明るい領域を暗くしたりします。

## なぜ Aspose.PSD for Java を使用するのか？
Aspose.PSD for Java は、幅広いラスタおよびベクタ形式をサポートし、ネイティブ依存性を排除し、大きなファイル向けに高性能キャッシュを提供する包括的な純粋な Java ソリューションです。豊富な API により、開発者は最小限のコードで複雑なカラー補正やレイヤーベースの編集を実行でき、シンプルな調整から高度な画像処理パイプラインまで幅広く活用できます。

- **10 以上のラスタおよびベクタ形式をサポート** – PSD、TIFF、JPEG、PNG、BMP、GIF など。  
- **Pure‑Java 実装** – ネイティブ DLL や外部依存性がなく、任意の JVM で動作します。  
- **高性能キャッシュ** – ラスタデータをキャッシュでき、大きなファイルでの繰り返し編集が最大 2 倍速くなります。  
- **豊富な API** – カラー補正、レイヤー処理、マスク、合成などに 150 以上のメソッドがあります。

## 前提条件

チュートリアルに入る前に、以下の前提条件が揃っていることを確認してください。

- Aspose.PSD for Java ライブラリ: [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) からライブラリをダウンロードしてインストールしてください。  
- Java Development Kit (JDK) 8 以上がマシンにインストールされていること。  
- IntelliJ IDEA、Eclipse、VS Code などの開発環境 (IDE)。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。この例では、以下を使用します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

それでは、画像の明るさを調整するプロセスをシンプルな手順に分解しましょう。

## Aspose.PSD を使用した明るさの調整方法は？

ソース画像を読み込み、明るさオフセットを適用し、保存オプションを設定し、結果をディスクに書き出す—これらを4つの簡潔な手順で行います。以下のセクションでは、プロジェクトにコピーできる明確なステップバイステップの手順を示します。このアプローチにより、各操作が効率的に実行され、最終画像は元の品質を保ちつつ希望の明るさ変更が反映されます。

### ステップ 1: 画像の読み込み

`RasterImage` クラスは、メモリ内の PSD または TIFF ファイルのラスタライズされたバージョンを表します。カラー補正操作のためにピクセルへ直接アクセスできます。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

このステップでは、対象画像を読み込み、さらに処理するために `RasterImage` にキャストします。

### ステップ 2: 明るさの調整

`adjustBrightness(int value)` は、指定された整数値で各ピクセルの明度を変更します。正の数は画像を明るくし、負の数は暗くします。このメソッドはインプレースで画像を処理するため、追加のオブジェクト作成は不要です。

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

ここでは、`adjustBrightness` メソッドを使用して画像の明るさを変更します。この例では明るさを 50 ユニット下げていますが、要件に応じてこの値はカスタマイズ可能です。

### ステップ 3: TiffOptions の設定

`TiffOptions` は、サンプルあたりのビット数やフォトメトリック解釈など、TIFF 出力のエンコードパラメータを指定します。結果ファイルのエンコード方法を制御できます。

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

調整した画像を保存するために `TiffOptions` を設定します。`bitsPerSample` と `photometric` プロパティは、特定のニーズに合わせて調整してください。

### ステップ 4: 結果画像の保存

`save` を呼び出すと、前述のオプションを使用して処理されたラスタデータがファイルに書き込まれます。この操作は原子的で、出力ファイルが有効な TIFF 画像であることを保証します。

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

最後に、指定した `TiffOptions` を使用して変更された画像を保存します。

## 一般的な問題と解決策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| **`ClassCastException` が Image をキャストするときに発生** | ファイルがラスタ画像ではありません（例: ベクタ PSD）。 | ソースファイル形式を確認するか、キャスト前に `image instanceof RasterImage` を使用してください。 |
| **明るさの変更が効果なし** | 調整前に画像がキャッシュされていませんでした。 | ステップ 1 のように `rasterImage.cacheData()` を呼び出してください。 |
| **保存されたファイルが破損しているように見える** | `TiffOptions` の設定が正しくありません。 | `bitsPerSample` がソース画像の深度（通常はチャンネルあたり 8 ビット）と一致していることを確認してください。 |

## よくある質問

**Q: PSD 以外の他の画像形式でも明るさを調整できますか？**  
A: はい、Aspose.PSD for Java は PSD と TIFF に加えて JPEG、PNG、BMP、GIF など多くのラスタ形式をサポートしています。

**Q: 画像調整プロセス中のエラーはどのように処理できますか？**  
A: `try‑catch` ブロックで処理コードを囲み、`IOException` または `ImageProcessingException` を捕捉してファイルアクセスやラスタ操作のエラーを管理してください。

**Q: 明るさ調整の範囲に制限はありますか？**  
A: このメソッドは –255 から +255 の整数値を受け付けます。この範囲外の値は最も近い限界にクランプされます。

**Q: 商用プロジェクトで Aspose.PSD for Java を使用できますか？**  
A: はい、本番使用には商用ライセンスが必要です。ライセンスは [here](https://purchase.aspose.com/buy) から購入してください。

**Q: 無料トライアルは利用可能ですか？**  
A: はい、[here](https://releases.aspose.com/) から無料トライアルでライブラリを試すことができます。

**Q: `adjustBrightness` メソッドはレイヤーの可視性に影響しますか？**  
A: このメソッドはラスタライズされた合成画像に対して動作するため、ラスタライズ時に非表示レイヤーは無視され、意図したビジュアル結果が保たれます。

**Q: 複数の調整（例: コントラスト、彩度）を連続して適用できますか？**  
A: もちろんです。明るさを調整した後、同じ `RasterImage` インスタンスで `adjustContrast`、`adjustSaturation`、その他のカラー補正メソッドを呼び出すことができます。

---

**最終更新日:** 2026-09-28  
**テスト環境:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**作者:** Aspose

## 関連チュートリアル

- [画像処理 Java ライブラリ: Aspose.PSD を使用したレイヤーの反転](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Aspose.PSD for Java を使用した画像のグレースケール変換](/psd/java/advanced-techniques/grayscale-image/)
- [Aspose.PSD for Java で特定の角度で画像を回転する方法](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}