---
date: 2026-08-01
description: Aspose.PSD を使用した Java 画像処理でガンマを調整し、PSD を TIFF に変換し、色あせた画像を修正する方法を簡潔なチュートリアルで学びましょう。
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: 画像のガンマを調整する
og_description: Aspose.PSD を使用した Java 画像処理でガンマを調整する方法を学びましょう – 高速な server‑side ライブラリで、色あせた画像を修正し、数行のコードで
  PSD を TIFF に変換できます。
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: ガンマの調整方法 – Aspose.PSD を使用した Java 処理
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Aspose.PSD を使用した Java 画像処理でガンマを調整する方法
url: /ja/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD を使用した Java 画像処理におけるガンマ調整方法

## はじめに

If you’re working on **java image processing**, learning **ガンマ調整方法** is a fundamental technique to improve brightness and contrast without losing detail. In this tutorial we’ll walk through how to use **Aspose.PSD for Java** to apply gamma correction to a PSD file, **PSD を TIFF に変換**, and avoid a **色あせた画像**. You’ll see why this approach is fast, reliable, and perfect for **server‑side image processing** pipelines.

## クイック回答
- **ガンマ補正は何を行いますか？** It remaps luminance values to make dark areas brighter or bright areas darker while preserving overall detail.  
- **どのライブラリが処理を担当しますか？** Aspose.PSD for Java provides a dedicated `adjustGamma` method for raster images.  
- **同じフローで PSD を TIFF に変換できますか？** Yes – after gamma adjustment you can save the image directly to TIFF using `TiffOptions`.  
- **開発にライセンスは必要ですか？** A free trial works for testing; a commercial license is required for production use.  
- **サポートされている Java バージョンは何ですか？** Aspose.PSD supports Java 8 and later.

## Java のガンマ補正とは？

Gamma correction changes the nonlinear relationship between the encoded pixel values and the displayed brightness. By tweaking the gamma curve you can **色あせた画像** problems or enhance details in shadows without over‑exposing highlights. It works by applying a power‑law function to each pixel, which brightens dark tones and compresses highlights, resulting in a more natural visual appearance.

## ガンマ補正に Aspose.PSD を使用する理由

Aspose.PSD is a **java image processing library** that abstracts away the complexities of the PSD format. It supports processing files up to 2 GB, handles over 50 different image formats, and provides a simple `adjustGamma` call, making it ideal for **java gamma correction** and **convert PSD to TIFF** workflows.

## 前提条件

1. **Java 開発環境** – Java 8 以降がインストールされていること。  
2. **Aspose.PSD ライブラリ** – JAR をダウンロードしてプロジェクトに追加してください。公式の[ドキュメント](https://reference.aspose.com/psd/java/)をご覧ください。  
3. **サンプル画像** – 処理したい PSD ファイル（例: `sample.psd`）。  

## パッケージのインポート

Before you start, import the essential namespaces that give you access to raster handling and file‑format options.

## 手順 1: 画像の読み込み

The `RasterImage` class represents the rasterized pixel data of a PSD layer in memory. Loading the image once and caching it reduces memory churn for subsequent adjustments.

## 手順 2: ガンマの調整

Load your PSD with `new RasterImage("sample.psd")` and call `rasterImage.adjustGamma(2.0f)` — that single line applies a gamma of 2.0 across all colour channels, brightening shadows while keeping highlights intact. You can pass separate values for red, green, and blue if channel‑specific tweaks are required.

## 手順 3: TiffOptions の作成

`TiffOptions` lets you control compression, bits per sample, and other TIFF‑specific settings. Setting an 8‑bit sample (`{8,8,8}`) keeps the TIFF file size reasonable while preserving colour fidelity.

## 手順 4: 結果画像の保存

Call `rasterImage.save("output.tif", tiffOptions)` to write the processed image to disk. After saving, you can feed the TIFF into downstream systems such as print services or web APIs.

## 一般的な使用例

- **自動化されたグラフィックパイプライン** – サムネイル生成前にリアルタイムでガンマを調整します。  
- **バッチ変換ツール** – 明るさを正規化しながら大規模な PSD アーカイブを TIFF に変換します。  
- **Web サービス** – PSD を受け取りガンマ補正を適用し、クライアントに TIFF を返すエンドポイントを公開します。

## 一般的な問題と解決策

| 問題 | 発生理由 | 解決策 |
|-------|----------------|------------|
| **画像が色あせて見える** | Gamma 値が高すぎる（例: > 2.5） | ガンマ係数を 1.8〜2.2 の範囲に下げてください。 |
| **`rasterImage.isCached()` が false を返す** | 画像がまだメモリにロードされていない | ガンマ調整前に `rasterImage.cacheData()` を呼び出してください。 |
| **TIFF ファイルサイズが大きい** | サンプルあたりのビット数が 16 ビットに設定されている | 例に示すように 8 ビットサンプル（`{8,8,8}`）を使用してください。 |

## よくある質問

**Q: 各色チャンネルに異なるガンマ値を適用できますか？**  
A: Yes – the `adjustGamma` method accepts separate float values for red, green, and blue channels.

**Q: 保存前に複数の画像調整をチェーンできますか？**  
A: Absolutely. You can perform resizing, cropping, or colour corrections sequentially on the same `RasterImage` instance.

**Q: Aspose.PSD はマルチページ PSD ファイルをサポートしていますか？**  
A: Yes, each layer can be accessed and processed individually.

**Q: TIFF 以外にエクスポートできる形式はありますか？**  
A: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective options classes.

**Q: ガンマ補正後に色あせた画像を防ぐにはどうすればよいですか？**  
A: Start with a moderate gamma (around 2.0) and preview the result; adjust downwards if the image looks too bright.

## 結論

Congratulations! You’ve successfully learned **how to adjust gamma** in a **java image processing** workflow, converted a PSD to TIFF, and avoided common pitfalls such as a **色あせた画像**. This pattern gives you fine‑grained control over brightness and contrast, making it ideal for automated graphics pipelines, web services, or desktop utilities.

---

**最終更新日:** 2026-08-01  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Java 画像処理チュートリアル - Aspose.PSD for Java を使用した画像の明るさ調整](/psd/java/advanced-techniques/adjust-brightness/)
- [Aspose.PSD for Java を使用した PSD から TIFF への変換とコントラスト調整方法](/psd/java/advanced-techniques/adjust-contrast/)
- [Java で PSD を画像に変換 – Aspose.PSD で調整レイヤーを適用](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

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

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```