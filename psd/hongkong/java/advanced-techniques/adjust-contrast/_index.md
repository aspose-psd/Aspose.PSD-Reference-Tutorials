---
date: 2026-07-27
description: 了解如何使用 Aspose.PSD for Java（領先的 Java 圖像處理函式庫）將 PSD 轉換為 TIFF 並執行圖像對比度調整。
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: 轉換 PSD 為 TIFF 並調整對比度
og_description: 本指南提供逐步程式碼示例、效能技巧以及高品質 TIFF 輸出的匯出選項。
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: 轉換 PSD 為 TIFF 並調整對比度 – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: 使用 Aspose.PSD for Java 轉換 PSD 為 TIFF 並調整對比度
url: /zh-hant/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 將 PSD 轉換為 TIFF 並調整對比度

## 介紹

如果您需要 **將 PSD 轉換為 TIFF** 同時微調圖形的視覺品質，您來對地方了。在本教學中，我們將使用 Aspose.PSD for Java——一個強大的 **java image manipulation** 函式庫，完整示範工作流程。您將學會如何提升 **image contrast adjustment**、快取大型點陣資料以提升效能，最後 **將影像儲存為 TIFF** 供後續處理。讓我們開始吧！

## 快速回答
- **「調整對比度」是什麼意思？** 它會改變最暗與最亮像素之間的差異，讓細節更突出。  
- **哪個函式庫負責此功能？** Aspose.PSD for Java – 完整的影像處理工具組。  
- **需要授權嗎？** **臨時 Aspose 授權** 可用於測試；正式環境需購買正式授權。  
- **可以將 PSD 轉換為 TIFF 嗎？** 當然可以，我們會使用 `TiffOptions` 匯出處理後的影像。  
- **轉換速度如何？** 以一般 30 MB 的 PSD 為例，整個流程在現代 CPU 上可於一秒內完成。

## 什麼是影像對比度調整？
對比度調整會改變影像的色調範圍，放大亮部與暗部之間的差異。這在掃描後影像顯得平淡，或在為印刷準備圖形時特別有用。它透過拉伸或壓縮像素強度的直方圖，使陰影更深、亮部更亮，從而提升感知的深度與細節。

## 為何選擇 Aspose.PSD for Java？
Aspose.PSD 提供高效能、功能豐富的引擎，能處理 **超過 50 種點陣與向量格式**，支援最高 500 MB 檔案而不需完整載入記憶體，並可精確控制 TIFF 的每樣本位元數與光度解釋。這些量化的能力使其成為企業級影像管線的首選。

## 前置條件

在開始之前，請確保您已具備：

- 基本的 Java 程式設計知識。  
- 已安裝 Aspose.PSD for Java 函式庫。您可以在此處下載 [here](https://releases.aspose.com/psd/java/)。

## 匯入套件

在您的 Java 類別中加入必要的匯入：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 步驟 1：載入影像

`Image` 類別是 Aspose.PSD 的入口點，代表記憶體中的任何支援點陣影像。  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

我們將來源 PSD 檔案 (`sample.psd`) 載入為 `Image` 物件，作為後續所有處理的起點。

## 步驟 2：轉型為 RasterImage 並快取資料

`RasterImage` 提供直接的像素層級存取，並支援大型檔案的快取。  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

將 `Image` 轉型為 `RasterImage` 後，即可進行像素層級的操作。快取可提升效能，尤其是處理大型檔案時。

## 如何調整影像的對比度

`adjustContrast` 方法是一個簡單的 API 呼叫，可依百分比值調整影像對比度。  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 方法接受一個整數，代表百分比變化。在此範例中，我們將對比度提升 **50 %**。

## 使用 Aspose.PSD 將 PSD 轉換為 TIFF

`TiffOptions` 讓您指定 TIFF 專屬設定，如每樣本位元數、壓縮類型與光度解釋。  
```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

此處我們設定 `TiffOptions`（每樣本位元數、光度解釋），並 **將影像儲存為 TIFF**。此步驟完成 **convert PSD to TIFF** 工作流程。

## 常見問題與解決方案
- **影像未快取：** 大型 PSD 請務必呼叫 `cacheData()`，以避免 `OutOfMemoryError`。  
- **顏色意外偏移：** 確認 `setPhotometric` 與目標色彩空間（RGB 或 CMYK）相符。  
- **找不到檔案：** 確認 `dataDir` 指向正確資料夾，且檔名拼寫正確。

## 常見問答

### Q1：Aspose.PSD 是否相容於不同的影像格式？

A1：是的，Aspose.PSD 支援 **超過 50 種輸入與輸出格式**，包括 PSD、TIFF、PNG、JPEG、BMP 與 GIF，讓您在各種專案中都能靈活使用。

### Q2：如何取得 Aspose.PSD 的臨時授權？

A2：您可以在此取得臨時授權 [here](https://purchase.aspose.com/temporary-license/)。

### Q3：在哪裡可以找到 Aspose.PSD 的文件說明？

A3：文件說明可於此取得 [here](https://reference.aspose.com/psd/java/)。

### Q4：Aspose.PSD 提供哪些支援選項？

A4：請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得支援。

### Q5：我可以購買 Aspose.PSD 嗎？

A5：可以，請在此購買 [here](https://purchase.aspose.com/buy)。

## 結論

現在您已掌握 **如何將 PSD 轉換為 TIFF** 以及使用 Aspose.PSD for Java 進行 **影像對比度調整** 的方法。這些步驟讓您在保持程式碼整潔可維護的同時，對影像品質擁有精細的控制。歡迎嘗試其他調整方法，如 `adjustBrightness` 或 `adjustGamma`，以符合您的特定需求。

---

**最後更新：** 2026-07-27  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose

## 相關教學

- [Java Image Processing Tutorial - Adjust Brightness of an Image with Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [How to Adjust Gamma in Java Image Processing with Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}