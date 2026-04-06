---
date: 2026-01-07
description: 學習逐步的濾波技術，使用 Aspose.PSD for Java 套用中值濾波器與 Wiener 濾波器，並高效地將 PSD 轉換為 GIF。
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
title: 逐步濾波 - 應用中位數與維納濾波器（Java）
url: /zh-hant/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 逐步濾鏡：在 Java 中套用中值與 Wiener 濾鏡

## 介紹

如果你正在尋找 **逐步濾鏡** 工作流程來清理 Java 中的噪點圖像，你來對地方了。Aspose.PSD for Java 讓套用中值與 Wiener 濾鏡變得簡單，甚至還能在處理完畢後 **將 PSD 轉換為 GIF**。在本教學中，我們將一步步說明從設定函式庫到儲存濾鏡結果的全部流程，讓你能自信地將高品質影像去噪整合到應用程式中。

## 快速問答
- **中值濾鏡的作用是什麼？** 它可減少鹽與胡椒雜訊，同時保留邊緣。  
- **什麼時候該使用 Wiener 濾鏡？** 需要考慮局部影像變異的自適應降噪時。  
- **執行程式碼需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **可以將輸出儲存為 GIF 嗎？** 可以——Aspose.PSD 允許 **將 PSD 轉換為 GIF**，一步完成。  
- **實作需要多長時間？** 基本設定通常在 10 分鐘以內完成。

## 什麼是逐步濾鏡？

*逐步濾鏡* 方法將影像處理拆解為明確、易於管理的階段——載入影像、設定濾鏡選項、套用濾鏡，最後儲存結果。這種有條理的流程有助於除錯、重複使用程式碼，並能依不同影像格式調整流程。

## 為什麼選擇 Aspose.PSD for Java？

- **廣泛的格式支援** – 支援 PSD、PNG、JPEG、GIF 等多種格式。  
- **無外部相依** – 純 Java 實作，輕鬆嵌入任何專案。  
- **內建濾鏡選項** – 中值、Wiener 以及其他進階濾鏡即開箱即用。  
- **一鍵轉換** – 處理完畢後可直接匯出為 GIF、PNG 或 JPEG。

## 前置作業

在開始之前，請確保你已具備以下項目：

1. **Aspose.PSD for Java 函式庫** – 從 [此處](https://releases.aspose.com/psd/java/) 下載並安裝。  
2. **Java 開發環境** – JDK 8 以上，並在機器上配置好 IDE 或建置工具（Maven/Gradle）。

## 匯入套件

先匯入必要的類別，以取得影像處理與濾鏡選項的存取權。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## 逐步濾鏡：如何套用中值濾鏡

### 步驟 1：載入影像

先將 API 指向要清理的 PSD 檔案。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### 步驟 2：將影像轉型為 RasterImage

濾鏡作用於點陣資料，需將通用的 `Image` 轉型為 `RasterImage`。

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### 步驟 3：建立 MedianFilterOptions 例項

設定中值核心的大小。**4** 的大小對中等噪點效果不錯。

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### 步驟 4：套用中值濾鏡

將濾鏡套用至整個影像範圍。

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### 步驟 5：儲存結果影像（將 PSD 轉換為 GIF）

濾鏡完成後，我們將輸出儲存為 GIF，示範 **將 PSD 轉換為 GIF** 的功能。

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

依照上述步驟，你已成功套用中值濾鏡並將清理後的影像匯出為 GIF。

## 套用 Wiener 濾鏡（可選延伸）

若專案需要自適應降噪，可將中值濾鏡換成 Wiener 濾鏡。程式結構相同，只需匯入 `WienerFilterOptions` 並以所需半徑建立實例。

> **小技巧：** 為兩種濾鏡嘗試不同的核心大小，以找出噪點去除與細節保留之間的最佳平衡點。

## 常見問題與除錯

| 症狀 | 可能原因 | 解決方式 |
|------|----------|----------|
| `ClassCastException` 在轉型為 `RasterImage` 時發生 | 輸入檔案不是點陣相容的 PSD | 確認 PSD 包含點陣圖層，或先將圖層轉為點陣 |
| 輸出 GIF 為空白 | 目標路徑錯誤或資料夾缺乏寫入權限 | 確認 `dataDir` 指向已存在且可寫入的目錄 |
| 濾鏡似乎沒有作用 | 核心大小對噪點程度太小 | 增大濾鏡大小（例如 `new MedianFilterOptions(6)`） |

## 常見問答

**Q1：這些濾鏡可以套用於任何格式的影像嗎？**  
A1：可以，Aspose.PSD 支援多種影像格式，適用於各種專案。

**Q2：Aspose.PSD for Java 有提供免費試用嗎？**  
A2：有，請至 [此處](https://releases.aspose.com/) 取得免費試用版。

**Q3：如何取得 Aspose.PSD for Java 的技術支援？**  
A3：請前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 尋求社群協助。

**Q4：在哪裡可以找到 Aspose.PSD for Java 的文件說明？**  
A4：文件位於 [此處](https://reference.aspose.com/psd/java/)。

**Q5：如何購買 Aspose.PSD for Java？**  
A5：可於 [此處](https://purchase.aspose.com/buy) 直接購買。

## 結論

本指南示範了使用 Aspose.PSD for Java 進行 **逐步濾鏡** 的完整流程，涵蓋中值（以及可選的 Wiener）濾鏡的套用，並說明了 **將 PSD 轉換為 GIF** 的後續處理。掌握這些基礎，你即可在任何 Java 應用程式中整合強大的影像處理管線，無論是清理照片、為網站準備素材，或是自動化批次轉換，都能得心應手。

---

**最後更新：** 2026-01-07  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}