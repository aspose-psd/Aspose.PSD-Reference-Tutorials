---
date: 2026-02-27
description: 學習如何在 Java 圖像處理中使用 Aspose.PSD 調整 gamma、將 PSD 轉換為 TIFF，並在簡短教學中修復顏色淡化的圖像。
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: 如何在 Java 圖像處理中使用 Aspose.PSD 調整 Gamma
url: /zh-hant/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 圖像處理中使用 Aspose.PSD 調整 Gamma

## 簡介

如果您正在從事 **java image processing**，學習 **how to adjust gamma** 是提升亮度與對比度而不失細節的基本技巧。在本教學中，我們將示範如何使用 **Aspose.PSD for Java** 對 PSD 檔案套用 gamma 校正、**convert PSD to TIFF**，並避免 **washed‑out image**。您將了解此方法為何快速、可靠，且非常適合伺服器端圖像流水線。

## 快速解答
- **Gamma 校正的作用是什麼？** 它會重新映射亮度值，使暗部變亮或亮部變暗，同時保留整體細節。  
- **哪個函式庫負責處理？** Aspose.PSD for Java 提供專用的 `adjustGamma` 方法來處理光柵圖像。  
- **我可以在同一流程中將 PSD 轉換為 TIFF 嗎？** 可以 — 在 gamma 調整之後，您可以直接使用 `TiffOptions` 將圖像儲存為 TIFF。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線需購買商業授權。  
- **支援哪個 Java 版本？** Aspose.PSD 支援 Java 8 及以上版本。

## 如何在 Java 圖像處理中調整 Gamma
調整 gamma 是任何涉及亮度或對比度的 **java image processing tutorial** 的核心部分。以下我們將分步說明每個步驟的意義，並示範如何將此流程整合到現有程式碼中。

## 什麼是 Java Gamma 校正？
Gamma 校正改變編碼像素值與顯示亮度之間的非線性關係。透過微調 gamma 曲線，您可以 **fix washed out image** 問題，或在不過度曝光高光的前提下增強陰影細節。

## 為什麼使用 Aspose.PSD 進行 Gamma 校正？
Aspose.PSD 作為一個強大的 **java image processing library**，抽象化了 PSD 格式的複雜性。它處理色彩配置檔、快取，並提供簡單的 `adjustGamma` 呼叫，使其成為 **java gamma correction** 與 **convert PSD to TIFF** 工作流程的理想選擇。

## 先決條件

1. **Java 開發環境** – 已安裝 Java 8 或更新版本。  
2. **Aspose.PSD 函式庫** – 下載並將 JAR 加入專案。請參閱官方[文件](https://reference.aspose.com/psd/java/)。  
3. **範例圖像** – 您想要處理的 PSD 檔案（例如 `sample.psd`）。  

## 匯入套件

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 步驟 1：載入圖像

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

**小技巧：** 先快取光柵資料一次，可減少在連續套用多項調整時的記憶體波動。

## 步驟 2：調整 Gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

如果需要針對特定通道微調，您可以為紅、綠、藍通道分別傳入不同的值。

## 步驟 3：建立 TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

設定 8 位元樣本 (`{8,8,8}`) 可在保持色彩忠實度的同時，使 TIFF 檔案大小保持在合理範圍。

## 步驟 4：儲存結果圖像

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

儲存後，您可以將 TIFF 檔案送入下游系統，例如列印服務或 Web API。

## 常見使用情境

- **自動化圖形流水線** – 在產生縮圖前即時調整 gamma。  
- **批次轉換工具** – 在標準化亮度的同時，將大量 PSD 檔案轉換為 TIFF。  
- **Web 服務** – 提供一個端點，接收 PSD、套用 gamma 校正，並回傳 TIFF 給客戶端使用。  

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方法 |
|------|----------|----------|
| **圖像顯得過度漂白** | Gamma 值過高（例如 > 2.5） | 將 gamma 因子降低至 1.8 至 2.2 之間的值。 |
| **`rasterImage.isCached()` 回傳 false** | 圖像尚未載入記憶體 | 在調整 gamma 前呼叫 `rasterImage.cacheData()`。 |
| **TIFF 檔案大小過大** | 每樣本位元設定為 16 位元 | 如範例所示，使用 8 位元樣本 (`{8,8,8}`)。 |

## 常見問答

**問：我可以對每個顏色通道套用不同的 gamma 值嗎？**  
答：可以 — `adjustGamma` 方法接受紅、綠、藍通道的獨立 float 值。

**問：是否可以在儲存前串接多個圖像調整？**  
答：當然可以。您可以在同一個 `RasterImage` 實例上依序執行調整大小、裁切或顏色校正等操作。

**問：Aspose.PSD 是否支援多頁 PSD 檔案？**  
答：支援，您可以分別存取與處理每個圖層。

**問：除了 TIFF，還能匯出哪些格式？**  
答：Aspose.PSD 透過相應的選項類別支援 PNG、JPEG、BMP 以及其他多種格式。

**問：如何避免 gamma 校正後圖像過度漂白？**  
答：先以適中的 gamma（約 2.0）開始，預覽結果；若圖像過亮則降低 gamma 值。

## 結論

恭喜！您已成功學會在 **java image processing** 工作流程中 **how to adjust gamma**，將 PSD 轉換為 TIFF，並避免常見的 **washed‑out image** 問題。此模式讓您對亮度與對比度擁有精細的控制，十分適合自動化圖形流水線、Web 服務或桌面工具。

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}