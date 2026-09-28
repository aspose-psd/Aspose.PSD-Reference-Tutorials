---
date: 2026-09-28
description: 本 Java 圖像處理教學示範如何使用 Aspose.PSD for Java 調整圖像亮度。透過逐步程式碼載入、修改並儲存 PSD 或
  TIFF 檔案。
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: 調整圖像亮度
og_description: 本 Java 圖像處理教學示範如何使用 Aspose.PSD for Java 調整圖像亮度。透過逐步程式碼載入、修改並儲存 PSD
  或 TIFF 檔案。
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: Java 圖像處理：使用 Aspose.PSD 調整亮度
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
title: Java 圖像處理：使用 Aspose.PSD 調整亮度
url: /zh-hant/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 調整影像亮度

## 簡介

在本 **java image processing** 教學中，您將學習如何直接從 Java 程式碼調整圖片的亮度。亮度調整是平面設計師、攝影師以及任何建立影像處理管線的人常見的任務。在本 **java image manipulation** 指南中，我們將逐步說明完整工作流程——載入 PSD/TIFF、套用亮度偏移，並儲存結果——使用 Aspose.PSD for Java 函式庫。

## 快速解答
- **哪個函式庫處理亮度？** Aspose.PSD for Java.  
- **哪個方法變更亮度？** `RasterImage.adjustBrightness()`.  
- **我可以處理 PSD 與 TIFF 檔案嗎？** Yes, the API supports both formats and 10+ additional image types.  
- **生產環境需要授權嗎？** A commercial license is required for non‑evaluation use.  
- **實作需要多長時間？** Typically under 10 minutes for a basic adjustment.

## 什麼是 java image processing？

`Java image processing` 指的是一組技術，讓您能以 Java 程式化地讀取、轉換與寫入影像資料。調整亮度是核心操作之一，會改變每個像素的整體亮度，使暗部變亮或亮部變暗。

## 為什麼使用 Aspose.PSD for Java？

Aspose.PSD for Java 提供完整的純 Java 解決方案，支援廣泛的點陣圖與向量格式，消除原生相依性，並為大型檔案提供高效能快取。其廣泛的 API 讓開發者能以最少程式碼執行複雜的顏色校正與圖層編輯，使其同時適用於簡單的調整與進階的影像處理管線。

- **支援 10+ 點陣圖與向量格式** – PSD、TIFF、JPEG、PNG、BMP、GIF 等。  
- **Pure‑Java 實作** – 無原生 DLL 或外部相依性，因而可在任何 JVM 上執行。  
- **高效能快取** – 點陣資料可被快取，使大型檔案的重複編輯速度提升至最高 2 倍。  
- **豐富的 API** – 超過 150 個方法，用於顏色校正、圖層處理、遮罩與合成。

## 前置條件

在開始本教學之前，請確保您已具備以下前置條件：

- Aspose.PSD for Java 函式庫：從 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 下載並安裝函式庫。  
- 已在您的機器上安裝 Java Development Kit (JDK) 8 或更高版本。  
- 開發環境 (IDE)，例如 IntelliJ IDEA、Eclipse 或 VS Code。

## 匯入套件

首先，將必要的套件匯入您的 Java 專案。以下範例中，我們將使用下列套件：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

現在，讓我們將調整影像亮度的過程分解為簡單的步驟：

## 如何使用 Aspose.PSD 調整亮度？

載入來源影像、套用亮度偏移、設定儲存選項，並將結果寫入磁碟——全部只需四個簡潔步驟。以下各節提供清晰的逐步說明，您可直接複製到自己的專案中。此方式確保每個操作高效執行，且最終影像在保留原始品質的同時，呈現所需的亮度變化。

### 步驟 1：載入影像

`RasterImage` 類別代表記憶體中 PSD 或 TIFF 檔案的點陣化版本，提供直接的像素存取以進行顏色校正操作。

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

在此步驟中，我們載入目標影像，並將其轉型為 `RasterImage` 以便後續處理。

### 步驟 2：調整亮度

`adjustBrightness(int value)` 會依指定的整數值改變每個像素的亮度。正數會使影像變亮，負數則使其變暗。此方法直接在原影像上處理，無需額外建立物件。

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

此處，我們使用 `adjustBrightness` 方法來調整影像的亮度。在此範例中，我們將亮度降低 50 單位，您亦可依需求自行設定此值。

### 步驟 3：設定 TiffOptions

`TiffOptions` 指定 TIFF 輸出的編碼參數，例如每樣本位元數與光譜解釋。它讓您控制最終檔案的編碼方式。

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

設定 `TiffOptions` 以儲存調整後的影像。根據您的需求調整 `bitsPerSample` 與 `photometric` 屬性。

### 步驟 4：儲存結果影像

呼叫 `save` 會使用先前定義的選項，將處理後的點陣資料寫入檔案。此操作具原子性，確保輸出檔案為有效的 TIFF 影像。

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

最後，使用指定的 `TiffOptions` 儲存已修改的影像。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|--------|----------|
| **`ClassCastException` when casting Image** | 檔案不是點陣圖（例如向量 PSD）。 | 在轉型前驗證來源檔案格式或使用 `image instanceof RasterImage`。 |
| **Brightness change has no effect** | 調整前影像未被快取。 | 如步驟 1 所示，呼叫 `rasterImage.cacheData()`。 |
| **Saved file appears corrupted** | `TiffOptions` 設定不正確。 | 確認 `bitsPerSample` 與來源影像深度相符（通常為每通道 8 位元）。 |

## 常見問答

**Q: 我可以在除 PSD 之外的其他影像格式調整亮度嗎？**  
A: 可以，Aspose.PSD for Java 除支援 PSD 與 TIFF 外，亦支援 JPEG、PNG、BMP、GIF 等多種點陣格式。

**Q: 如何在影像調整過程中處理錯誤？**  
A: 將處理程式碼包在 try‑catch 區塊中，捕捉 `IOException` 或 `ImageProcessingException` 以管理檔案存取與點陣操作錯誤。

**Q: 亮度調整的範圍有上限嗎？**  
A: 此方法接受 –255 至 +255 的整數值；超出此範圍的值會被限制在最近的界限。

**Q: 我可以在商業專案中使用 Aspose.PSD for Java 嗎？**  
A: 可以，生產環境需要商業授權。請於 [此處](https://purchase.aspose.com/buy) 購買授權。

**Q: 有提供免費試用嗎？**  
A: 有，您可從 [此處](https://releases.aspose.com/) 取得免費試用版。

**Q: `adjustBrightness` 方法會影響圖層可見性嗎？**  
A: 此方法作用於點陣化的合成影像，隱藏的圖層在點陣化時會被忽略，保留預期的視覺結果。

**Q: 我可以串接多個調整（例如對比、飽和度）嗎？**  
A: 當然可以。調整亮度後，您可以在同一個 `RasterImage` 實例上呼叫 `adjustContrast`、`adjustSaturation` 或其他顏色校正方法。

---

**最後更新：** 2026-09-28  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose

## 相關教學

- [Image Processing Java Library：使用 Aspose.PSD 反轉圖層](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [使用 Aspose.PSD for Java 將影像轉為灰階](/psd/java/advanced-techniques/grayscale-image/)
- [使用 Aspose.PSD for Java 以特定角度旋轉影像](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}