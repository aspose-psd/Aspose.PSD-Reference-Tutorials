---
date: 2025-12-21
description: 學習如何使用 Aspose.PSD 透過調整影像伽瑪來執行 Java 圖像處理。一步一步的指南，將 PSD 轉換為 TIFF 並套用伽瑪校正。
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java 影像處理 – 使用 Aspose.PSD 調整 Gamma
url: /zh-hant/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像處理 – 使用 Aspose.PSD 調整 Gamma

## 介紹

如果您正在從事 **java image processing**，調整圖片的 gamma 是一項基本技術，可在不失去細節的情況下提升亮度與對比度。在本教學中，我們將示範如何使用 **Aspose.PSD for Java** 對 PSD 檔案套用 gamma 校正，然後將結果匯出為 TIFF 圖像。您將會了解此方法為何快速、可靠，且非常適合伺服器端的圖像處理管線。

## 快速解答
- **Gamma 校正的作用是什麼？** 它會重新映射亮度值，使暗部變亮或亮部變暗，同時保留整體細節。  
- **哪個函式庫負責處理？** Aspose.PSD for Java 提供專用的 `adjustGamma` 方法來處理點陣圖像。  
- **我可以在同一流程中將 PSD 轉換為 TIFF 嗎？** 可以 – 在 gamma 調整之後，直接使用 `TiffOptions` 將圖像儲存為 TIFF。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線則需購買商業授權。  
- **支援哪個 Java 版本？** Aspose.PSD 支援 Java 8 及以上版本。

## 什麼是 java 圖像處理？

Java 圖像處理是指使用 Java 函式庫對視覺資料進行操作、分析與轉換。常見工作包括調整尺寸、過濾、色彩校正與格式轉換——所有這些都可以在桌面或 Web 應用程式中自動化執行。

## 為什麼使用 Aspose.PSD 進行 Gamma 校正？

Aspose.PSD 提供高階 API，抽象化 PSD 格式的複雜性，讓您專注於實際的圖像調整。它會處理快取、色彩配置檔，並提供直觀的 `adjustGamma` 呼叫，非常適合 **image gamma correction** 與 **convert psd to tiff** 工作流程。

## 前置條件

在開始教學之前，請確保已完成以下設定：

1. **Java 開發環境** – 確認您的系統已安裝 Java 開發環境。  
2. **Aspose.PSD 函式庫** – 下載並將 Aspose.PSD 函式庫整合至您的 Java 專案。您可以在 [documentation](https://reference.aspose.com/psd/java/) 中找到相關資源。  
3. **範例圖像** – 準備一張用於套用 gamma 調整的 PSD 範例圖像。

## 匯入套件

先在 Java 專案中匯入所需的套件，為使用 Aspose.PSD 功能做好準備。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 步驟 1：載入圖像

先將範例 PSD 圖像載入 `RasterImage` 類別的實例，這是後續 gamma 調整的基礎。

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

## 步驟 2：調整 Gamma

使用 `adjustGamma` 方法調整已載入圖像的 gamma。依需求微調 gamma 值。

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 步驟 3：建立 TiffOptions

為最終圖像建立 `TiffOptions` 實例。設定每個樣本的位元數、光譜選項等屬性，以符合您的輸出規格。

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 步驟 4：儲存結果圖像

使用先前定義的 `TiffOptions`，將處理後的圖像儲存為 TIFF 格式。

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方法 |
|-------|----------------|------------|
| **圖像顯得過度淡化** | Gamma 值過高（例如 > 2.5） | 將 Gamma 因子降低至 1.8 至 2.2 之間的值。 |
| **`rasterImage.isCached()` returns false** | 圖像尚未載入記憶體 | 在調整 Gamma 之前呼叫 `rasterImage.cacheData()`。 |
| **TIFF 檔案大小過大** | 每個樣本位元設定為 16 位元 | 如範例所示，使用 8 位元樣本 (`{8,8,8}`)。 |

## 常見問答

**Q: 可以對每個顏色通道套用不同的 gamma 值嗎？**  
A: 可以 – `adjustGamma` 方法接受紅、綠、藍三個通道的獨立 float 值。

**Q: 是否可以在儲存之前串接多個圖像調整操作？**  
A: 當然可以。您可以在同一個 `RasterImage` 實例上依序執行調整大小、裁切或色彩校正等操作。

**Q: Aspose.PSD 是否支援多頁 PSD 檔案？**  
A: 支援，每個圖層都可以單獨存取與處理。

**Q: 除了 TIFF，還能匯出哪些格式？**  
A: Aspose.PSD 透過各自的 Options 類別支援 PNG、JPEG、BMP 以及其他多種格式。

## 結論

恭喜！您已成功透過 Aspose.PSD for Java，對 PSD 檔案執行 **java image processing**，調整 gamma 後再匯出為 TIFF 圖像。此工作流程提供對圖像亮度與對比度的精細控制，十分適合自動化圖形管線、Web 服務或桌面工具使用。

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## 常見問題

### Q1: 在哪裡可以找到 Aspose.PSD 文件？

A1: 您可以在 [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/) 取得文件。

### Q2: 如何下載 Aspose.PSD for Java？

A2: 請從 [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/) 下載函式庫。

### Q3: 哪裡可以購買 Aspose.PSD？

A3: 前往 [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) 購買 Aspose.PSD。

### Q4: 有免費試用版嗎？

A4: 有，您可以在 [https://releases.aspose.com/](https://releases.aspose.com/) 取得免費試用。

### Q5: 哪裡可以取得 Aspose.PSD 的支援？

A5: 請至 Aspose.PSD 論壇 [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34) 尋求協助。