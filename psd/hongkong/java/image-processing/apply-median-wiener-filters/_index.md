---
date: 2026-07-17
description: 學習一步一步的濾鏡技巧，使用 Aspose.PSD for Java 套用 Median 與 Wiener 濾鏡，並高效地將 PSD 轉換為
  GIF。
keywords:
- convert psd to gif
- remove salt pepper noise
- median filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: 套用 Median 與 Wiener 濾鏡
og_description: 使用 Aspose.PSD for Java 將 PSD 轉換為 GIF。學習如何套用 Median 與 Wiener 濾鏡、去除鹽與胡椒雜訊，並匯出高品質
  GIF。
og_image_alt: 'Developer guide: Convert PSD to GIF with Median and Wiener filters
  in Java using Aspose.PSD'
og_title: Convert PSD to GIF – 套用 Median 與 Wiener 濾鏡 (Java)
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  headline: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  type: TechArticle
- description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  name: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  steps:
  - name: Load the Image
    text: '`Image` is Aspose.PSD''s base class representing any supported image file.'
  - name: Cast Image into RasterImage
    text: '`RasterImage` extends `Image` and provides pixel‑level access for raster‑based
      operations.'
  - name: Create MedianFilterOptions Instance
    text: '`MedianFilterOptions` configures the median filter, allowing you to set
      the kernel size.'
  - name: Save the Resultant Image (Convert PSD to GIF)
    text: '`GifOptions` specifies settings for saving an image in GIF format, such
      as color depth and compression. `ExportFormat.Gif` is the enum value used to
      save an image as a GIF file. By following these steps you have successfully
      applied a Median filter and exported the cleaned image as a GIF.'
  type: HowTo
- questions:
  - answer: It reduces salt‑and‑pepper noise while preserving edges.
    question: What does the Median filter do?
  - answer: For adaptive noise reduction that considers local image variance.
    question: When should I use the Wiener filter?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the code?
  - answer: Yes—Aspose.PSD lets you **convert PSD to GIF** in a single step.
    question: Can I save the output as GIF?
  - answer: Typically under 10 minutes for a basic setup.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
- median filter
- wiener filter
title: Convert PSD to GIF – 逐步應用 Median 與 Wiener 濾鏡 (Java)
url: /zh-hant/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 轉換 PSD 為 GIF：套用中值與 Wiener 濾波器 (Java)

## 快速解答
- **Median 濾波器的作用是什麼？** 它在保留邊緣的同時減少鹽與胡椒噪點。  
- **什麼時候應該使用 Wiener 濾波器？** 用於考慮局部影像變異的自適應降噪。  
- **執行程式碼是否需要授權？** 免費試用可用於開發；商業授權則需於正式環境使用。  
- **可以將輸出儲存為 GIF 嗎？** 可以 — Aspose.PSD 允許您在單一步驟中 **convert PSD to GIF**。  
- **實作大約需要多久？** 基本設定通常在 10 分鐘以內。

## 什麼是逐步濾波？
*逐步濾波* 方法將影像處理拆分為明確、可管理的階段——載入影像、設定濾波選項、套用濾波，最後儲存結果。此系統化流程有助於除錯、重複使用程式碼，並可針對不同影像格式調整流程。

## 為什麼使用 Aspose.PSD for Java？
Aspose.PSD for Java 支援 **30+ 影像格式**，包括 PSD、PNG、JPEG、GIF、BMP 與 TIFF，且可在不將整個檔案載入記憶體的情況下處理上百頁文件。此函式庫 **零外部相依**，可直接嵌入任何 Java 專案，無需擔心原生二進位檔。內建的 Median 與 Wiener 濾波器即開箱即用，API 亦提供一鍵式轉換，可在處理後直接匯出為 GIF、PNG 或 JPEG。

## 前置條件

在開始之前，請確保您已具備：

1. **Aspose.PSD for Java Library** – 從 [here](https://releases.aspose.com/psd/java/) 下載並安裝。其他 Aspose 產品請參閱 [here](https://releases.aspose.com/)。  
2. **Java 開發環境** – JDK 8 以上，並在機器上配置好 IDE 或建置工具（Maven/Gradle）。

## 匯入套件

`Image`、`RasterImage` 以及濾波選項類別讓您完整掌控影像處理與降噪。

## 如何使用 Aspose.PSD (Java) 轉換 PSD 為 GIF

載入 PSD、套用所需濾波，然後以 GIF 格式呼叫 `save`——只需幾行簡潔程式碼。此直接回答模式讓您在深入每一步之前即可看到完整轉換流程。儲存時亦可指定顏色深度或壓縮等額外選項。

## 逐步濾波：如何套用 Median 濾波器

Median 濾波器可在保留邊緣的同時去除 **鹽與胡椒噪點**。它透過在每個像素上滑動視窗，將中心值替換為周圍值的中位數，從而在不模糊重要細節的前提下消除離群值。

### 步驟 1：載入影像

`Image` 為 Aspose.PSD 的基礎類別，代表任何支援的影像檔案。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

### 步驟 2：將 Image 轉型為 RasterImage

`RasterImage` 繼承自 `Image`，提供像素層級的存取以進行點陣圖操作。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### 步驟 3：建立 MedianFilterOptions 實例

`MedianFilterOptions` 用於設定 Median 濾波器，可調整核大小。

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### 步驟 4：套用 Median 濾波器

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### 步驟 5：儲存結果影像（轉換 PSD 為 GIF）

`GifOptions` 指定儲存為 GIF 格式的設定，例如顏色深度與壓縮。`ExportFormat.Gif` 為將影像儲存為 GIF 檔的列舉值。

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

遵循上述步驟，即可成功套用 Median 濾波器並將清理後的影像匯出為 GIF。

## 套用 Wiener 濾波器（可選擴充）

Wiener 濾波器透過估計局部變異來執行自適應降噪，特別適合噪點程度不一致的影像。只需將 Median 濾波器換成 `WienerFilterOptions`，其餘流程保持不變。

> **專業提示：** 嘗試不同的核大小，以在降噪與細節保留之間取得最佳平衡。

## 常見問題與故障排除

| 症狀 | 可能原因 | 解決方式 |
|------|----------|----------|
| `ClassCastException` 在轉型為 `RasterImage` 時發生 | 輸入檔案不是可點陣化的 PSD | 確認 PSD 包含點陣圖層，或先將圖層轉為點陣圖 |
| 輸出 GIF 為空白 | 目標路徑錯誤或資料夾缺乏寫入權限 | 確認 `dataDir` 指向已存在且可寫入的目錄 |
| 濾波似乎沒有作用 | 核大小對噪點而言過小 | 增大濾波器尺寸（例如 `new MedianFilterOptions(6)`） |

## 常見問答

**Q1：可以將這些濾波套用於任何格式的影像嗎？**  
A1：可以，Aspose.PSD 支援超過 30 種格式，您可以對 PSD、PNG、JPEG、BMP、TIFF 等進行濾波。

**Q2：Aspose.PSD for Java 有免費試用嗎？**  
A2：有，您可在 [here](https://releases.aspose.com/) 取得免費試用版。

**Q3：如何取得 Aspose.PSD for Java 的支援？**  
A3：請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 尋求社群協助。

**Q4：官方文件在哪裡可以找到？**  
A4：請參考文件 [here](https://reference.aspose.com/psd/java/)。

**Q5：如何購買商業授權？**  
A5：您可於 [here](https://purchase.aspose.com/buy) 購買產品。

## 結論

本教學示範了使用 Aspose.PSD for Java 進行 **逐步濾波** 的完整流程，涵蓋 Median（以及可選的 Wiener）濾波器的套用，並說明了 **convert PSD to GIF** 的後處理步驟。透過這些基礎組件，您可以將強大的影像處理管線整合至任何 Java 應用程式，無論是清理相片、為網站準備素材，或是自動化批次轉換。

---

**最後更新：** 2026-07-17  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [轉換 PSD 為 GIF - 使用 Aspose.PSD for Java 套用高斯與 Wiener 濾波器於彩色影像](/psd/java/image-processing/apply-gaussian-wiener-filters-color-image/)
- [逐步濾波 - 使用 Aspose.PSD for Java 套用動態 Wiener 濾波器](/psd/java/image-processing/apply-motion-wiener-filters/)
- [如何使用 Aspose.PSD for Java 轉換 PSD 為 GIF – 有損壓縮器](/psd/java/advanced-image-manipulation/implement-lossy-gif-compressor/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```