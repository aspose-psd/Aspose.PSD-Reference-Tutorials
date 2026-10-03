---
date: 2026-10-03
description: 了解如何使用 Aspose.PSD 在 Java 中提取 PSD 的縮圖。本分步指南涵蓋環境設定、程式碼範例，以及將縮圖儲存為 JPEG
  圖像。
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: 在 Java 中從 PSD 提取縮圖
og_description: 了解如何使用 Aspose.PSD 在 Java 中提取 PSD 縮圖。本指南將帶您完成環境設定、載入檔案、提取縮圖以及將其儲存為
  JPEG 圖像的步驟。
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: 使用 Aspose.PSD 在 Java 中提取 PSD 縮圖
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: 在 Java 中從 PSD 提取縮圖
url: /zh-hant/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 PSD 中提取縮圖（Java）

## 介紹
從 PSD 檔案提取縮圖可讓您在不載入完整高解析度影像的情況下快速產生預覽。在 Java 中，Aspose.PSD 使此流程簡單且效能佳。本教學將教您如何設定函式庫、定位縮圖資源，並將其儲存為 JPEG 檔案——只需幾行程式碼即可完成。

## 快速解答
- **哪個函式庫處理 PSD 縮圖？** Aspose.PSD for Java.
- **需要多少行程式碼？** 大約五行即可載入、提取並儲存。
- **可以從大型 PSD 檔案提取縮圖嗎？** 可以，Aspose.PSD 可處理高達 500 MB 的檔案，且不需完整載入記憶體。
- **開發時需要授權嗎？** 免費試用版可用於評估；正式環境需購買授權。
- **支援哪些輸出格式？** 提取的縮圖可儲存為 JPEG、PNG 或 BMP。

## 什麼是從 PSD 提取縮圖？
從 PSD 提取縮圖是指讀取嵌入於 Photoshop（PSD）文件內的小型預覽影像。此預覽以資源形式儲存，可獨立保存以供目錄或顯示用途。縮圖通常是低解析度的圖像，供應用程式在不載入完整尺寸影像的情況下快速顯示視覺摘要。

## 為何使用 Aspose.PSD 完成此任務？
Aspose.PSD 支援 **30+ 影像格式**，且可處理高達 **500 MB** 的 PSD 檔案，同時保持低記憶體使用，因為它會按需讀取資源。API 亦提供完善的錯誤處理機制，讓您即使面對損毀檔案也能可靠地提取縮圖。

## 前置條件
在開始之前，請確保您已具備：
- 已安裝 Java Development Kit（JDK）。
- 從 [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/) 下載 Aspose.PSD for Java 函式庫。
- 具備 Java 語法與專案設定的基本知識。

## 如何在 Java 中從 PSD 檔案提取縮圖？
使用 `PsdImage` 載入 PSD 檔案，定位 `ThumbnailResource`，並將其影像資料儲存為 JPEG。Aspose.PSD 抽象化了低階解析，您只需呼叫 `getResources()`，再對提取出的影像呼叫 `save()`。此方法適用於任何包含縮圖的 PSD，無論檔案大小。

## 匯入套件
`Image` 為載入影像的基礎類別。`PsdImage` 代表 PSD 文件。`ThumbnailResource` 與 `Thumbnail4Resource` 代表縮圖資源。`JpegOptions` 指定 JPEG 儲存選項。

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## 步驟 1：載入 PSD 檔案
首先，建立指向 PSD 檔案的 `PsdImage` 實例。建構子僅讀取標頭與必要資源，保持記憶體使用最小化。

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

將 `"Your_Document_Directory/"` 替換為 PSD 檔案所在的目錄路徑，將 `"your_file.psd"` 替換為您的 PSD 檔案名稱。

## 步驟 2：遍歷影像資源
Aspose.PSD 將縮圖儲存為 `ThumbnailResource` 物件於影像的資源集合中。遍歷集合，檢查資源類型，並擷取第一個遇到的縮圖。

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## 步驟 3：儲存提取的縮圖
取得縮圖影像後，呼叫其 `save` 方法寫入磁碟。您可選擇 JPEG、PNG 或 BMP；JPEG 為網頁預覽最常用的格式。

## 步驟 4：處理不同的縮圖類型
若 PSD 包含多種縮圖變體，例如 `Thumbnail4Resource`，請擴充遍歷邏輯以檢查每種型別。API 為每種資源提供獨立類別，讓您選擇所需的解析度。

## 常見問題與解決方案
- **未找到縮圖：** 並非所有 PSD 檔案都有嵌入預覽。請在 Photoshop 的「File → File Info」面板中檢查來源檔案。
- **不支援的格式錯誤：** 請確保使用最新的 Aspose.PSD 版本；舊版可能缺少較新的縮圖資源類型。
- **大型檔案記憶體不足：** 使用 `PsdImage.load(..., LoadOptions)` 並設定 `LoadOptions.setLoadResourcesOnly(true)`，以避免在僅需縮圖時載入完整影像資料。

## 常見問答

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一個 Java 函式庫，可在不需 Adobe Photoshop 的情況下，以程式方式建立、操作與轉換 PSD 及其他點陣圖格式。

**Q: 在哪裡可以找到 Aspose.PSD for Java 的更多文件？**  
A: 您可以參考 [documentation](https://reference.aspose.com/psd/java/) 取得詳細的 API 參考與範例。

**Q: 我可以在購買前免費試用 Aspose.PSD 嗎？**  
A: 可以，您可下載 [free trial](https://releases.aspose.com/) 以評估函式庫功能。

**Q: 如何取得 Aspose.PSD 的臨時授權？**  
A: 臨時授權可於 [temporary license](https://purchase.aspose.com/temporary-license/) 頁面取得。

**Q: Aspose.PSD 可用於商業用途嗎？**  
A: 可以，Aspose.PSD 可依其授權條款在個人與商業專案中使用。

---

**最後更新：** 2026-10-03  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose

## 相關教學

- [如何使用 Aspose.PSD for Java 將 PSD 轉換為點陣圖格式](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [使用 Aspose.PSD Java 將 PSD 儲存為 JPEG 並支援 RGB 顏色](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [使用 Aspose.PSD for Java 調整影像大小 – 繪製形狀與基本影像操作](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}