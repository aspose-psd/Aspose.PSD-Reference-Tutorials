---
date: 2026-09-18
description: 了解如何在 Java 中使用 Aspose.PSD 自動校正 JPEG 方向。透過基於 EXIF 的自動旋轉，提升您的影像處理工作流程。
keywords:
- auto correct jpeg orientation
- Aspose.PSD for Java
- Java image processing
lastmod: 2026-09-18
linktitle: 在 Java 中自動校正 JPEG 圖像方向
og_description: 了解如何在 Java 中使用 Aspose.PSD 自動校正 JPEG 方向。本指南逐步說明如何偵測 EXIF 資料、自動旋轉圖像，以及有效儲存校正後的檔案。
og_image_alt: Guide showing auto correction of JPEG orientation in Java with Aspose.PSD
og_title: 使用 Aspose.PSD 在 Java 中自動校正 JPEG 方向
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to auto correct JPEG orientation in Java using Aspose.PSD.
    Enhance your image processing workflow with automatic EXIF‑based rotation.
  headline: Auto correct JPEG image orientation in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java is a powerful library that allows Java developers
      to work with PSD, JPEG, and other image formats programmatically.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [Aspose PSD Java release page](https://releases.aspose.com/psd/java/).
    question: How can I download Aspose.PSD for Java?
  - answer: Yes, it supports various image manipulation tasks such as resizing, cropping,
      and adjusting orientation.
    question: Does Aspose.PSD for Java support image manipulation?
  - answer: Comprehensive documentation is available on the [Aspose.PSD for Java documentation
      site](https://reference.aspose.com/psd/java/).
    question: Where can I find documentation for Aspose.PSD for Java?
  - answer: Yes, you can get a free trial from the [Aspose free trial page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java for free?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- auto correct jpeg
- Aspose.PSD
- Java image processing
title: 在 Java 中自動校正 JPEG 圖像方向
url: /zh-hant/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 自動校正 JPEG 圖像方向（Java）

## 介紹
在當今的數位時代，以程式方式操作與優化圖像已成為各領域開發人員的重要任務。**自動校正 JPEG 圖像方向** 是在處理不同裝置拍攝的照片時的常見需求。Aspose.PSD for Java 為您提供強大的工具，以高效處理 PSD、JPEG 及其他圖像格式。本教學將深入探討一項具體任務：使用 Aspose.PSD for Java 自動校正 JPEG 圖像方向。無論您是開發相片編輯應用程式、在 CMS 中管理圖像資源，或是自動化圖像處理流程，您都將學會如何無縫整合此功能。

## 快速回答
- **自動校正 JPEG 圖像方向會做什麼？** 它會讀取 EXIF 旋轉資料，並將圖像旋轉，使其在任何裝置上皆能正立顯示。  
- **哪個函式庫負責旋轉？** Aspose.PSD for Java 內建 EXIF 處理與自動旋轉功能。  
- **開發時需要授權嗎？** 免費試用可用於評估；正式上線則需商業授權。  
- **能否處理大量批次？** 可以——您可以遍歷資料夾，批量處理數千張圖像，且記憶體開銷極低。  
- **支援哪些 Java 版本？** Aspose.PSD 支援 JDK 8 至 21。

## 什麼是自動校正 JPEG 圖像方向？
自動校正 JPEG 圖像方向是指自動偵測圖像的 EXIF「Orientation」標籤，並隨後旋轉位圖，使其無需人工干預即可正立顯示。此過程會讀取 JPEG 檔案中嵌入的中繼資料，判斷所需的旋轉或翻轉，並套用轉換，使視覺呈現符合攝影師在所有觀看平台上的意圖。

## 為何使用 Aspose.PSD 進行自動校正 JPEG 圖像方向？
Aspose.PSD 支援 **30 多種圖像格式**，且可在不將整張圖像載入記憶體的情況下處理高達 **2 GB** 的檔案，效能比手動逐像素旋轉快至 **5 倍**。此函式庫亦能處理嵌入資源，例如 PSD 檔案內的 JPEG 縮圖，並提供高階 API，將低階 EXIF 解析抽象化，使實作既簡潔又可靠。

## 前置條件
在開始本教學之前，請確保已完成以下設定：
- Java 開發環境：確保系統已安裝 Java Development Kit（JDK）。  
- Aspose.PSD for Java JAR：從 [Aspose PSD Java 釋出頁面](https://releases.aspose.com/psd/java/) 下載 Aspose.PSD for Java 函式庫。  
- 整合開發環境（IDE）：使用 IntelliJ IDEA、Eclipse 或您偏好的任何 Java 開發 IDE。  
- 具備 Java 與圖像處理的基本知識：熟悉 Java 程式設計與圖像處理基礎概念將有助於學習。

## 匯入套件
在開始範例之前，請先匯入 Aspose.PSD for Java 所需的套件。`Image` 類別是載入與儲存圖像的基礎類型，`JpegExifData` 提供 EXIF 中繼資料的存取，而縮圖資源類別則代表嵌入的 JPEG 預覽。

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 如何使用 Aspose.PSD 在 Java 中自動校正 JPEG 圖像方向？
載入目標 PSD 檔案，定位嵌入的 JPEG 縮圖，讓 Aspose.PSD 讀取其 EXIF 方向資訊，套用自動旋轉，最後儲存校正後的圖像。此工作流程僅需少量方法呼叫，即可處理 PSD 容器中任何嵌入的 JPEG 圖像，適用於單張或批次處理情境。

## 步驟 1：載入 PSD 圖像
`PsdImage` 類別代表 PSD 檔案，並提供對其資源的存取，包括嵌入的 JPEG 縮圖。  
首先，載入包含需校正方向之 JPEG 縮圖的 PSD 圖像：

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
將 `"Your Document Directory"` 替換為實際存放 PSD 檔案的目錄路徑。

## 步驟 2：遍歷圖像資源
接著，遍歷圖像資源以尋找 JPEG 縮圖資源。`ThumbnailResource` 與 `Thumbnail4Resource` 代表 PSD 檔案中不同版本的嵌入 JPEG 預覽。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Find thumbnail resource. Typically they are in the Jpeg file format.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Adjust thumbnail data.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // If there is a thumbnail stored, auto-rotate it.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```

## 步驟 3：儲存圖像
最後，在套用自動旋轉後儲存校正後的圖像：

```java
image.save();
```
此步驟確保對圖像所做的變更得以永久保存。

## 常見問題與故障排除
- **未偵測到 EXIF 標籤** – 請確認 JPEG 縮圖實際包含 Orientation 標籤；部分相機會省略此資訊。  
- **大型檔案記憶體錯誤** – 使用 `PsdImage.load(..., LoadOptions)` 並將 `LoadOptions.setLoadAllResources(false)` 設為 false，以降低記憶體使用量。  
- **旋轉方向不正確** – 請確認使用最新的 Aspose.PSD 版本；舊版曾有特定方向值的已知錯誤。

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套強大的函式庫，讓 Java 開發人員能以程式方式處理 PSD、JPEG 及其他圖像格式。

**Q: 如何下載 Aspose.PSD for Java？**  
A: 您可從 [Aspose PSD Java 釋出頁面](https://releases.aspose.com/psd/java/) 下載此函式庫。

**Q: Aspose.PSD for Java 是否支援圖像處理？**  
A: 是的，它支援多種圖像處理任務，例如調整大小、裁剪以及校正方向等。

**Q: 在哪裡可以找到 Aspose.PSD for Java 的文件？**  
A: 完整文件可在 [Aspose.PSD for Java 文件站](https://reference.aspose.com/psd/java/) 取得。

**Q: 我可以免費試用 Aspose.PSD for Java 嗎？**  
A: 可以，您可從 [Aspose 免費試用頁面](https://releases.aspose.com/) 取得免費試用版。

**Q: 自動旋轉功能是否支援執行緒安全？**  
A: 是的，每個 `PsdImage` 實例可在獨立執行緒上處理，且不會產生共享狀態衝突。

**Q: 如何批次處理數千張圖像？**  
A: 迭代目錄，載入每個 PSD，套用自動旋轉步驟後儲存；函式庫會重複使用緩衝區以降低記憶體消耗。

## 結論
總結來說，使用 Aspose.PSD for Java 可為在 PSD 檔案中自動校正 JPEG 圖像方向提供強大解決方案。依循本教學所列步驟，您即可提升圖像處理工作流程，確保圖像在所有平台與裝置上皆正確顯示。

---

**最後更新：** 2026-09-18  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose

## 相關教學

- [Java JPEG 圖像處理](/psd/java/java-jpeg-image-processing/)
- [將 PSD 轉換為 JPEG 並以 Aspose.PSD for Java 旋轉 270°](/psd/java/advanced-image-manipulation/rotate-image/)
- [如何使用 Aspose.PSD for Java 以特定角度旋轉圖像](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}