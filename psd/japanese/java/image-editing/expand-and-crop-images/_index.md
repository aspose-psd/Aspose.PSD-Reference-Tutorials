---
date: 2026-01-07
description: Aspose.PSD for Java を使用した Java の画像トリミング方法を学びましょう。画像のトリミング、リサイズ、PSD から
  JPEG への変換に関するステップバイステップガイドです。
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: '画像のトリミング Java: Aspose.PSD for Javaで画像を拡大・トリミング'
url: /ja/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Aspose.PSD for Java で画像の拡張とトリミング

## Introduction

このチュートリアルでは、Aspose.PSD ライブラリを使用して **crop image java** を実現する方法を紹介します。キャンバスを拡張したり不要な端をトリミングしたり、PSD ファイルを JPEG に変換したりする必要がある場合でも、以下の手順に従えばクリーンで再現性のあるプロセスを実行できます。前提条件、インポート文、各コーディングステップをわかりやすく解説するので、実務プロジェクトにすぐ適用できます。

## Quick Answers
- **What library handles crop image java?** Aspose.PSD for Java.
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.
- **Can I convert PSD to JPEG while cropping?** Yes, using `JpegOptions` together with a cropping rectangle.
- **Is Java 8 supported?** Aspose.PSD supports Java 8 and newer versions.
- **How long does the implementation take?** Typically under 10 minutes for a basic crop operation.

## What is “crop image java”?

Java で画像をトリミングするとは、元画像の矩形領域を選択し、残りの部分を破棄することを指します。Aspose.PSD を使用すると、この領域を `Rectangle` オブジェクトで定義し、JPEG など別の形式で結果を保存できます。

## Why use Aspose.PSD for Java image cropping?

- **Full PSD support** – 変換せずにレイヤー構造を持つ PSD ファイルを直接操作できます。  
- **High‑performance raster handling** – 大容量画像でもメモリ使用量を抑えて高速に処理できます。  
- **Built‑in conversion** – トリミングやキャンバス拡張を行いながら、JPEG、PNG、BMP などに簡単にエクスポートできます。  
- **Cross‑platform** – Java が動作するあらゆる環境で利用可能です。

## Prerequisites

1. **Java Development Kit (JDK)** – Java 8 以降がインストールされていること。  
2. **Aspose.PSD for Java** – 公式サイト **[here](https://releases.aspose.com/psd/java/)** からライブラリをダウンロードしてください。  

> **Pro tip:** Add the Aspose.PSD JAR to your project’s classpath or Maven/Gradle dependencies to avoid `ClassNotFoundException`.

## Import Packages

Add the required imports to your Java source file. These classes give you access to image loading, raster manipulation, rectangle definition, and JPEG export options.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step 1: Set Your Document Directory

Specify the folder that contains the source PSD file. Replace the placeholder with the actual path on your machine.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Specify Source and Destination Paths

Define where to read the PSD from and where to write the cropped JPEG.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Step 3: Load and Cache the Image

Load the PSD into a `RasterImage` object. Caching improves performance for subsequent operations such as cropping.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Step 4: Create Rectangle for Cropping

Create a `Rectangle` that describes the region you want to keep. The coordinates can be negative to **expand** the canvas before cropping, which is useful for adding a border around the original image.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Why use negative coordinates?**  
> Negative X/Y values shift the crop area left/up, effectively adding empty space (expanding) around the original content before the final crop.

## Step 5: Save the Cropped Image

Finally, save the resulting image using `JpegOptions`. This step also demonstrates **convert psd jpeg** while applying the cropping rectangle.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Result:** `jpeg_out.jpg` now contains a 300 × 300 pixel image that has been expanded by 200 px on each side and then cropped to the defined rectangle.

Congratulations! You've successfully performed **java image cropping**, expanded the canvas, and converted a PSD file to JPEG—all in a few concise lines of code.

## Common Use Cases

- **Preparing assets for web** – アップロード前にスクリーンショットやデザインをトリミング・リサイズできます。  
- **Generating thumbnails** – 大きな PSD から特定領域を抽出してサムネイルとして利用できます。  
- **Automated batch processing** – フォルダー内の PSD ファイルを一括で処理し、同一のトリミング矩形を適用できます。

## Troubleshooting & Tips

| Issue | Suggested Fix |
|-------|----------------|
| `OutOfMemoryError` when loading large PSDs | Call `rasterImage.cacheData()` early and consider increasing the JVM heap size (`-Xmx`). |
| Cropped area is off‑center | Verify the rectangle’s X/Y offsets; remember negative values expand the canvas. |
| Output JPEG looks blurry | Adjust `JpegOptions` quality setting (e.g., `new JpegOptions { Quality = 90 }`). |

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with different Java versions?

A1: Yes, Aspose.PSD supports various Java versions, ensuring compatibility with a wide range of development environments.

### Q2: Can I use Aspose.PSD for commercial projects?

A2: Absolutely, Aspose.PSD provides commercial licenses for developers, allowing its use in both personal and commercial projects.

### Q3: Are there any limitations on the image file formats supported?

A3: Aspose.PSD supports a variety of image file formats, including PSD, JPEG, PNG, and more. Refer to the [documentation](https://reference.aspose.com/psd/java/) for a complete list.

### Q4: How can I get support for Aspose.PSD-related queries?

A4: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to seek assistance from the community or the Aspose support team.

### Q5: Is there a free trial available?

A5: Yes, you can explore Aspose.PSD with a free trial. Download it [here](https://releases.aspose.com/).

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}