---
date: 2025-12-21
description: Aspose.PSD を使用して画像のガンマを調整し、Java で画像処理を行う方法を学びましょう。PSD を TIFF に変換し、ガンマ補正を適用するステップバイステップガイド。
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java画像処理 – Aspose.PSDでガンマを調整
url: /ja/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Processing – Adjust Gamma with Aspose.PSD

## Introduction

**java image processing** に取り組む際、画像のガンマを調整することは、ディテールを失わずに明るさとコントラストを向上させる基本的なテクニックです。このチュートリアルでは、**Aspose.PSD for Java** を使用して PSD ファイルにガンマ補正を適用し、結果を TIFF 画像としてエクスポートする方法を順を追って解説します。このアプローチが高速で信頼性が高く、サーバーサイドの画像パイプラインに最適である理由もご紹介します。

## Quick Answers
- **What does gamma correction do?** It remaps luminance values to make dark areas brighter or bright areas darker while preserving overall detail.  
- **Which library handles the processing?** Aspose.PSD for Java provides a dedicated `adjustGamma` method for raster images.  
- **Can I convert PSD to TIFF in the same flow?** Yes – after gamma adjustment you can save the image directly to TIFF using `TiffOptions`.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production use.  
- **What Java version is supported?** Aspose.PSD supports Java 8 and later.

## What is java image processing?

Java image processing とは、Java ライブラリを使用して視覚データの操作、分析、変換を行うことを指します。リサイズ、フィルタリング、カラー補正、フォーマット変換などのタスクを、デスクトップアプリや Web アプリケーションで自動化できます。

## Why use Aspose.PSD for gamma correction?

Aspose.PSD は PSD フォーマットの複雑さを抽象化したハイレベル API を提供し、実際の画像調整に集中できるようにします。キャッシュ処理やカラープロファイルの管理を行い、シンプルな `adjustGamma` 呼び出しだけで **image gamma correction** や **convert psd to tiff** のワークフローを実現できるため、最適です。

## Prerequisites

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

1. **Java Development Environment** – システムに Java 開発環境がインストールされていること。  
2. **Aspose.PSD Library** – Aspose.PSD ライブラリをダウンロードし、Java プロジェクトに組み込むこと。必要なリソースは [documentation](https://reference.aspose.com/psd/java/) にあります。  
3. **Sample Image** – ガンマ調整に使用するサンプル PSD 画像を用意すること。

## Import Packages

プロセスを開始するために、Java プロジェクトで必要なパッケージをインポートします。これにより Aspose.PSD の機能をシームレスに利用できるようになります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

サンプル PSD 画像を `RasterImage` クラスのインスタンスに読み込みます。これが以降のガンマ調整の基盤となります。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Step 2: Adjust Gamma

読み込んだ画像に対して `adjustGamma` メソッドを使用し、ガンマを調整します。必要に応じてガンマ値を微調整してください。

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Step 3: Create TiffOptions

結果画像用に `TiffOptions` のインスタンスを作成します。ビット深度やフォトメトリックオプションなど、出力を希望通りに設定します。

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Step 4: Save the Resultant Image

先ほど定義した `TiffOptions` を使用して、操作した画像を TIFF 形式で保存します。

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Image appears washed out** | Gamma value too high (e.g., > 2.5) | Lower the gamma factor to a value between 1.8 and 2.2. |
| **`rasterImage.isCached()` returns false** | Image not yet loaded into memory | Call `rasterImage.cacheData()` before adjusting gamma. |
| **TIFF file size is large** | Bits per sample set to 16‑bit | Use an 8‑bit sample (`{8,8,8}`) as shown in the example. |

## Frequently Asked Questions

**Q: Can I apply different gamma values to each colour channel?**  
A: Yes – the `adjustGamma` method accepts separate float values for red, green, and blue channels.

**Q: Is it possible to chain multiple image adjustments before saving?**  
A: Absolutely. You can perform resizing, cropping, or colour corrections sequentially on the same `RasterImage` instance.

**Q: Does Aspose.PSD support multi‑page PSD files?**  
A: Yes, each layer can be accessed and processed individually.

**Q: What format can I export to besides TIFF?**  
A: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective options classes.

## Conclusion

Congratulations! You’ve successfully performed **java image processing** by adjusting the gamma of a PSD file and exporting it as a TIFF image using Aspose.PSD for Java. This workflow gives you fine‑grained control over image brightness and contrast, making it ideal for automated graphics pipelines, web services, or desktop utilities.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## FAQ's

### Q1: Where can I find the Aspose.PSD documentation?

A1: You can access the documentation at [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: How do I download Aspose.PSD for Java?

A2: Download the library from [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Where can I purchase Aspose.PSD?

A3: Visit [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) to purchase Aspose.PSD.

### Q4: Is there a free trial available?

A4: Yes, you can explore a free trial at [https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Where can I seek support for Aspose.PSD?

A5: For support, visit the Aspose.PSD forum at [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).

---