---
date: 2026-02-25
description: 學習如何使用 Aspose.PSD for Java（領先的 Java 圖像處理庫）將 PSD 轉換為 TIFF 並執行圖像對比度調整。
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 將 PSD 轉換為 TIFF 並調整對比度
url: /zh-hant/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 將 PSD 轉換為 TIFF 並調整對比度

## 介紹

如果您需要 **convert PSD to TIFF** 同時微調圖形的視覺品質，您來對地方了。在本教學中，我們將使用 Aspose.PSD for Java——一個功能強大的 **java image manipulation** 函式庫，完整說明工作流程。您將學會如何提升 **image contrast adjustment**、快取大型點陣資料以提升效能，最後 **save image as TIFF** 以供後續處理。讓我們開始吧！

## 快速答覆
- **「調整對比度」是什麼意思？** 它會改變最暗與最亮像素之間的差異，讓細節更突出。  
- **哪個函式庫負責這項工作？** Aspose.PSD for Java – 完整的影像處理工具組。  
- **需要授權嗎？** **temporary aspose license** 可用於測試；正式環境需購買正式授權。  
- **我可以 **convert PSD to TIFF** 嗎？** 當然可以，我們會使用 `TiffOptions` 來匯出處理後的影像。  
- **程式執行需要多久？** 在現代硬體上，標準尺寸的 PSD 檔案通常在一秒內完成。

## 什麼是影像對比度調整？

對比度調整會改變影像的色調範圍，放大明暗區域之間的差異。當影像在掃描後顯得平淡，或在列印前需要加強視覺衝擊時，這項功能特別有用。

## 為什麼選擇 Aspose.PSD for Java？

- **豐富的格式支援** – 可開啟、編輯並 **save image as TIFF**、PNG、JPEG 等多種格式。  
- **高效能** – 快取與點陣影像最佳化可減少記憶體開銷，對大型 PSD 檔案尤為關鍵。  
- **簡潔的 API** – 像 `adjustContrast` 這樣的單一方法呼叫，使程式碼易讀且易於維護。  
- **完整的 java image manipulation 能力**，適用於簡單腳本與企業級應用。

## 前置條件

在開始之前，請確保您已具備：

- 基本的 Java 程式設計知識。  
- 已安裝 Aspose.PSD for Java 函式庫。您可以在[此處](https://releases.aspose.com/psd/java/)下載。

## 匯入套件

將必要的匯入加入您的 Java 類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 步驟 1：載入影像

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

我們將來源 PSD 檔案 (`sample.psd`) 載入為 `Image` 物件，作為後續所有處理的入口點。

## 步驟 2：轉型為 RasterImage 並快取資料

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

將物件轉型為 `RasterImage` 後，即可進行像素層級的操作。快取可提升效能，特別是處理大型檔案時。

## 如何調整影像的對比度

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 方法接受一個代表百分比變化的整數。在此範例中，我們將對比度提升 **50 %**。

## 使用 Aspose.PSD 將 PSD 轉換為 TIFF

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

此處我們設定 `TiffOptions`（每樣本位元、光度解釋），並 **save image as TIFF**。此步驟完成 **convert PSD to TIFF** 工作流程。

## 常見問題與解決方案
- **影像未快取：** 大型 PSD 必須呼叫 `cacheData()`，以避免 `OutOfMemoryError`。  
- **顏色異常：** 請確認 `setPhotometric` 與目標色彩空間（RGB 或 CMYK）相符。  
- **找不到檔案：** 請確保 `dataDir` 指向正確資料夾，且檔名拼寫正確。

## 常見問答

### Q1：Aspose.PSD 是否相容於不同的影像格式？

A1：是的，Aspose.PSD 支援多種影像格式，為您的專案提供彈性。

### Q2：如何取得 Aspose.PSD 的臨時授權？

A2：您可以在[此處](httpshttps://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q3：在哪裡可以找到 Aspose.PSD 的文件說明？

A3：文件說明位於[此處](https://reference.aspose.com/psd/java/)。

### Q4：Aspose.PSD 提供哪些支援管道？

A4：請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得支援。

### Q5：我可以購買 Aspose.PSD 嗎？

A5：可以，請在[此處](https://purchase.aspose.com/buy)購買。

## 結論

現在您已了解 **how to convert PSD to TIFF** 以及使用 Aspose.PSD for Java 進行 **image contrast adjustment** 的方法。這些步驟讓您能細緻控制影像品質，同時保持程式碼簡潔易維護。歡迎嘗試其他調整方法，例如 `adjustBrightness` 或 `adjustGamma`，以符合您的特定需求。

---

**最後更新：** 2026-02-25  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}