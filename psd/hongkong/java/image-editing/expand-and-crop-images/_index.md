---
date: 2026-07-08
description: Java 圖像編輯函式庫教學：學習如何使用 Aspose.PSD for Java 裁剪圖像、調整大小、擴展畫布，並將 PSD 轉換為 JPEG。
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: 擴展與裁剪圖像
og_description: Java 圖像編輯函式庫教學示範如何在數分鐘內使用 Aspose.PSD for Java 裁剪、擴展畫布，並將 PSD 轉換為 JPEG。
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java 圖像編輯函式庫 – 使用 Aspose.PSD 裁剪圖像
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java 圖像編輯函式庫 – 使用 Aspose.PSD 裁剪圖像
url: /zh-hant/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像編輯函式庫：使用 Aspose.PSD 進行 Java 圖像裁剪

## 簡介

在本教學中，您將學習如何使用 **java image editing library**——具體而言是 Aspose.PSD for Java——來裁剪、擴展以及將 PSD 檔案轉換為 JPEG。無論您是為網站入口準備資產，或是自動化產生縮圖，下列步驟都提供可重複使用、可投入生產的工作流程，您可以將其整合到任何 Java 8 以上的專案中。

## 快速答覆

- **什麼函式庫處理 crop image java？** Aspose.PSD for Java.  
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **在裁剪時能同時將 PSD 轉換為 JPEG 嗎？** 可以，使用 `JpegOptions` 搭配裁剪矩形。  
- **支援 Java 8 嗎？** Aspose.PSD 支援 Java 8 及更新版本。  
- **實作需要多長時間？** 基本裁剪操作通常在 10 分鐘以內完成。

## 什麼是 “crop image java”？

crop image java 指的是從來源圖片中選取一個矩形區域，並捨棄該區域之外的所有內容。使用 Aspose.PSD 時，您會建立一個定義區域的 `Rectangle`，將其套用至 `RasterImage`，然後將結果儲存為任何支援的格式，例如 JPEG。

## 為什麼使用 Aspose.PSD 進行 Java 圖像裁剪？

Aspose.PSD 提供一個 **java image editing library**，能原生處理 PSD 檔案，支援超過 100 種圖層功能，且可處理最高 10 000 × 10 000 像素的影像，同時將記憶體使用量控制在 500 MB 以下。它亦內建 JPEG、PNG、BMP 等格式的轉換功能，無需外部工具。這使得大量批次處理流程快速、可靠且易於維護。

## 先決條件

1. **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。  
2. **Aspose.PSD for Java** – 從官方網站 **[here](https://releases.aspose.com/psd/java/)** 下載函式庫。

> **專業提示：** 將 Aspose.PSD JAR 加入專案的 classpath 或 Maven/Gradle 相依性，以避免 `ClassNotFoundException`。

## 匯入套件

在您的 Java 原始檔案中加入必要的匯入。這些類別讓您能存取圖像載入、光柵操作、矩形定義以及 JPEG 輸出選項。

## 如何使用 Aspose.PSD 進行 Java 圖像裁剪？

使用 `RasterImage` 載入來源 PSD，定義描述裁剪區域的 `Rectangle`（負座標可擴展畫布），最後以 `JpegOptions` 儲存結果。此三步流程同時處理裁剪與格式轉換，免除中間檔案的需求。

## 步驟 1：設定文件目錄

指定包含來源 PSD 檔案的資料夾。將佔位符替換為您機器上的實際路徑。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步驟 2：指定來源與目的路徑

定義 PSD 的讀取位置以及裁剪後 JPEG 的寫入位置。

```java
String dataDir = "Your Document Directory";
```

## 步驟 3：載入並快取影像

`RasterImage` 代表記憶體中 PSD 檔案的光柵化版本。  
將 PSD 載入 `RasterImage` 物件。快取可提升後續操作（如裁剪）的效能。

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## 步驟 4：建立裁剪矩形

`Rectangle` 定義裁剪區域的 X、Y 座標以及寬度/高度。  
建立一個描述您想保留區域的 `Rectangle`。座標可為負值，以在裁剪前 **expand** 畫布，這對於在原始圖像周圍加入邊框很有幫助。

> **為什麼使用負座標？**  
> 負的 X/Y 值會將裁剪區域向左/上移動，實際上在最終裁剪前於原始內容周圍加入空白空間（擴展）。

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## 步驟 5：儲存裁剪後的影像

`JpegOptions` 指定 JPEG 輸出的設定，例如品質與壓縮。  
最後，使用 `JpegOptions` 儲存產生的影像。此步驟同時示範在套用裁剪矩形時 **convert psd jpeg**。

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **結果：** `jpeg_out.jpg` 現在是一張 300 × 300 像素的影像，先在每側擴展了 200 像素，然後裁剪至定義的矩形。

恭喜！您已成功執行 **java image cropping**，擴展畫布，並將 PSD 檔案轉換為 JPEG——全部只需幾行簡潔的程式碼。

## 常見使用情境

- **為網頁準備資產** – 在上傳前裁剪並調整螢幕截圖或設計稿的大小。  
- **產生縮圖** – 從大型 PSD 中擷取特定區域作為預覽。  
- **自動化批次處理** – 迭代資料夾中的 PSD 檔案，對每個檔案套用相同的裁剪矩形。

## 故障排除與技巧

| 問題 | 建議解決方案 |
|-------|----------------|
| 載入大型 PSD 時出現 `OutOfMemoryError` | 盡早呼叫 `rasterImage.cacheData()`，並考慮增大 JVM 堆大小（`-Xmx`）。 |
| 裁剪區域偏離中心 | 檢查矩形的 X/Y 偏移；記得負值會擴展畫布。 |
| 輸出的 JPEG 看起來模糊 | 調整 `JpegOptions` 的品質設定（例如 `new JpegOptions { Quality = 90 }`）。 |

## 常見問題

### Q1：Aspose.PSD 是否相容於不同的 Java 版本？

A1：是的，Aspose.PSD 支援 Java 8、11、17 以及更新的版本，確保在各種開發環境中具有廣泛相容性。

### Q2：我可以在商業專案中使用 Aspose.PSD 嗎？

A2：當然可以，Aspose.PSD 為開發者提供商業授權，允許在個人與商業應用中使用。

### Q3：支援的影像檔案格式有任何限制嗎？

A3：Aspose.PSD 支援超過 30 種影像格式，包括 PSD、JPEG、PNG、BMP、TIFF 等。完整清單請參考 [documentation](https://reference.aspose.com/psd/java/)。

### Q4：如何取得 Aspose.PSD 相關問題的支援？

A4：前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 向社群或 Aspose 支援團隊尋求協助。

### Q5：是否提供免費試用？

A5：是的，您可以使用免費試用版探索 Aspose.PSD。點此下載 [here](https://releases.aspose.com/)。

---

**最後更新：** 2026-07-08  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## 相關教學

- [使用 Aspose.PSD 進行簡單調整大小 – Java 圖像處理函式庫](/psd/java/basic-image-operations/simple-resizing/)
- [如何使用 Aspose.PSD for Java 旋轉圖像 270 度](/psd/java/advanced-image-manipulation/rotate-image/)
- [如何使用 Aspose.PSD 在 Java 圖像處理中調整 Gamma](/psd/java/advanced-techniques/adjust-gamma/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}