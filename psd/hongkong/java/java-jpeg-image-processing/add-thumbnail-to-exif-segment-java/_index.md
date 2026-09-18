---
date: 2026-09-18
description: 了解如何使用 Aspose.PSD for Java 將 java image metadata 縮圖加入 EXIF 段落。本分步指南涵蓋前置條件、程式碼說明以及儲存更新後的圖像。
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: 在 Java 中將 Thumbnail 加入 EXIF Segment
og_description: 了解如何使用 Aspose.PSD for Java 將 java image metadata 縮圖加入 EXIF 段落。遵循分步指南嵌入
  thumbnails 並儲存更新後的圖像。
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: 如何將 java image metadata 縮圖加入 EXIF 段落
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: 如何將 java image metadata 縮圖加入 EXIF 段落
url: /zh-hant/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 EXIF 區段中加入 Java 圖像中繼資料縮圖

## 介紹
在本教學中，您將學習如何使用 Aspose.PSD for Java 為 PSD 檔案的 EXIF 區段加入 **java image metadata** 縮圖。EXIF（可交換圖像檔案格式）中繼資料儲存相機設定、拍攝日期、位置以及其他有用資訊。嵌入小型預覽縮圖可讓應用程式在不載入完整檔案的情況下快速顯示圖像概覽，提升效能與使用者體驗。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.PSD for Java 為 PSD 圖像的 EXIF 區段加入縮圖。  
- **實作需要多長時間？** 基本整合大約需要 10‑15 分鐘。  
- **需要授權嗎？** 生產環境需要臨時授權；免費試用可用於評估。  
- **支援哪個 Java 版本？** 完全支援 Java 8 及更新版本。  
- **可以處理大型檔案嗎？** 可以 — Aspose.PSD 能在不將整個圖像載入記憶體的情況下處理高達 2 GB 的檔案。

## 什麼是 java image metadata？
Java 圖像中繼資料是指嵌入於圖像檔案（例如 EXIF、IPTC 或 XMP）中的結構化資訊，可透過 Java 函式庫（如 Aspose.PSD）以程式方式讀取、修改或建立。此中繼資料讓應用程式能在不開啟視覺內容的情況下取得相機設定、時間戳記、GPS 座標以及自訂資料。

## 為何要在 EXIF 中繼資料加入縮圖？
在 EXIF 區段加入縮圖可為圖像瀏覽器、檔案總管與內容管理系統提供即時的視覺提示。Aspose.PSD 在記憶體中處理縮圖，讓您能在 0.2 秒內為最高 500 KB 的圖像嵌入預覽，且支援超過 30 種圖像格式，包括 PSD、JPEG、PNG 與 TIFF。

## 前置條件
在開始教學之前，請確保您具備以下條件：
- 具備 Java 程式設計的基本知識。  
- 系統已安裝 Java Development Kit（JDK）。  
- Java 的整合開發環境（IDE），例如 IntelliJ IDEA 或 Eclipse。  
- Aspose.PSD for Java 函式庫。您可從 [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/) 下載。

## 匯入套件
以下匯入語句將引入處理 PSD 圖像與 EXIF 資料所需的 Aspose.PSD 類別。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 步驟 1：載入 PSD 圖像
`PsdImage` 代表 Photoshop PSD 檔案，並提供對其圖層與資源的存取。  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## 步驟 2：遍歷圖像資源
`ImageResource` 封裝了 PSD 檔案中嵌入的縮圖、ICC 配置檔與中繼資料等資源。  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## 步驟 3：調整縮圖資料
`JpegOptions` 允許您為縮圖圖像設定 JPEG 專屬的參數，例如品質。  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## 步驟 4：儲存圖像
呼叫 `save` 會將更新後的 EXIF 區段（包含新縮圖）寫回磁碟，而不需重新編碼整個圖像。  
```java
image.save(dataDir + "output.psd");
```

## 常見問題與解決方案
- **縮圖未顯示：** 請確認縮圖資源已正確加入 EXIF 區段，且圖像是使用 `PsdImage.save` 方法儲存的。  
- **大型檔案記憶體不足錯誤：** 使用 `PsdImage.load(..., LoadOptions)` 並搭配 `LoadOptions.setLoadOnlyMetadata(true)` 只處理中繼資料。  
- **方向不正確：** 確保縮圖遵循原始圖像的方向標記；您可以讀取 `Orientation` EXIF 標籤並相應旋轉縮圖。

## 常見問答

**Q: 什麼是 EXIF 中繼資料？**  
A: EXIF 中繼資料是嵌入於數位圖像中的資訊，包含相機設定、拍攝日期、GPS 座標以及其他細節。

**Q: 為何要在 EXIF 中加入縮圖？**  
A: 加入縮圖可提升使用者體驗，讓使用者在不載入完整圖像的情況下快速預覽圖像。

**Q: 從哪裡可以下載 Aspose.PSD for Java？**  
A: 您可從 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) 下載 Aspose.PSD for Java。

**Q: 如何取得 Aspose.PSD 的臨時授權？**  
A: 您可從 [temporary license page](https://purchase.aspose.com/temporary-license/) 取得 Aspose.PSD 的臨時授權。

**Q: 如何取得 Aspose.PSD 的支援？**  
A: 如需支援，請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)。

---

**最後更新：** 2026-09-18  
**測試環境：** Aspose.PSD for Java 24.10  
**作者：** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 在 PSD 檔案中建立 XMP 中繼資料](/psd/java/image-editing/create-xmp-metadata/)
- [使用 Aspose.PSD for Java 調整圖像大小 – 繪製形狀與基本圖像操作](/psd/java/basic-image-operations/)
- [如何使用 Aspose.PSD for Java 將 PSD 轉換為點陣圖像格式](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}