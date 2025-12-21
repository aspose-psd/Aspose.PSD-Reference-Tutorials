---
date: 2025-12-21
description: 學習如何使用 Aspose.PSD for Java 這個領先的 Java 圖像處理函式庫來調整圖像對比度，並高效地將 PSD 轉換為 TIFF。
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 調整圖像的對比度
url: /zh-hant/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 調整圖像的對比度

## Introduction

如果您正在尋找 **如何調整對比度**，您來對地方了。Aspose.PSD for Java 是一個功能強大的 **java 圖像處理庫**，讓您可以微調圖像屬性，如對比度、亮度等。在本教學中，我們將逐步說明如何提升 PSD 檔案的對比度，然後 **將 PSD 轉換為 TIFF** 以供後續工作流程使用。

## Quick Answers
- **調整對比度** 是什麼意思？它改變最暗與最亮像素之間的差異，讓細節更突出。
- **哪個函式庫負責此功能？** Aspose.PSD for Java – 完整的圖像處理工具包。
- **我需要授權嗎？** 測試時可使用臨時授權；正式環境需購買完整授權。
- **我可以將結果儲存為 TIFF 嗎？** 可以，我們會使用 `TiffOptions` 匯出處理後的圖像。
- **程式執行需要多久？** 對於一般尺寸的 PSD 檔案，通常在一秒以內完成。

## What is Contrast Adjustment?
對比度調整是什麼？

對比度調整會改變圖像的色調範圍，增強亮部與暗部之間的差異。當掃描後的圖像顯得平淡，或在為印刷準備圖形時，這項功能特別有用。

## Why Use Aspose.PSD for Java?
- **豐富的格式支援** – 開啟、編輯並儲存 PSD、TIFF、PNG、JPEG 等多種格式。
- **高效能** – 快取與光柵圖像優化降低記憶體開銷。
- **直觀的 API** – 像 `adjustContrast` 這樣的單一方法呼叫，使程式碼易於閱讀。

## Prerequisites

在開始之前，請確保您已具備以下條件：

- 具備 Java 程式設計的基本知識。
- 已安裝 Aspose.PSD for Java 函式庫。您可以在[此處](https://releases.aspose.com/psd/java/)下載。

## Import Packages

匯入套件

Add the required imports to your Java class:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

步驟 1：載入圖像

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

我們將來源 PSD 檔案（`sample.psd`）載入 `Image` 物件，作為後續所有處理的入口點。

## Step 2: Cast to RasterImage and Cache Data

步驟 2：轉型為 RasterImage 並快取資料

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

將物件轉型為 `RasterImage` 後，我們即可進行像素層級的操作。快取可提升效能，尤其是處理大型檔案時。

## How to Adjust Contrast of an Image

如何調整圖像的對比度

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 方法接受一個表示百分比變化的整數。在此範例中，我們將對比度提升 **50 %**。

## Convert PSD to TIFF Using Aspose.PSD

使用 Aspose.PSD 將 PSD 轉換為 TIFF

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

此處我們設定 `TiffOptions`（每樣本位元、光譜解釋），並將增強對比度的圖像寫入 TIFF 檔案。

## Common Issues and Solutions
常見問題與解決方案
- **圖像未快取**：對於大型 PSD，務必呼叫 `cacheData()` 以避免 `OutOfMemoryError`。
- **顏色異常偏移**：確認 `setPhotometric` 與目標色彩空間（RGB 或 CMYK）相符。
- **找不到檔案**：確保 `dataDir` 指向正確的資料夾，且檔名拼寫正確。

## Frequently Asked Questions

常見問答

### Q1: Aspose.PSD 是否相容於不同的圖像格式？

A1: 是的，Aspose.PSD 支援多種圖像格式，為您的專案提供彈性。

### Q2: 如何取得 Aspose.PSD 的臨時授權？

A2: 您可以在[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q3: 哪裡可以找到 Aspose.PSD 的文件說明？

A3: 文件說明可於[此處](https://reference.aspose.com/psd/java/)取得。

### Q4: Aspose.PSD 提供哪些支援選項？

A4: 如需支援，請前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)。

### Q5: 我可以購買 Aspose.PSD 嗎？

A5: 可以，您可於[此處](https://purchase.aspose.com/buy)購買 Aspose.PSD。

## Conclusion
結論

現在您已了解如何使用 Aspose.PSD for Java **調整 PSD 圖像的對比度**，以及如何 **將 PSD 轉換為 TIFF** 以供後續處理。這些步驟讓您能細緻地控制圖像品質，同時保持程式碼簡潔易維護。歡迎嘗試其他圖像調整方法，如 `adjustBrightness` 或 `adjustGamma`，以符合您的特定需求。

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}