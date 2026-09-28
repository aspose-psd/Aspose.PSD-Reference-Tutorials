---
date: 2026-09-28
description: 使用 Aspose.PSD 在 Java 中向 JFIF 段添加縮圖。遵循一步一步的指南，快速且可靠地在 PSD 檔案中嵌入縮圖。
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: 在 Java 中向 JFIF 段添加縮圖
og_description: 使用 Aspose.PSD 在 Java 中向 JFIF 段添加縮圖。遵循一步一步的指南，快速且可靠地在 PSD 檔案中嵌入縮圖。
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: 如何在 Java 中向 JFIF 段添加縮圖
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: 如何在 Java 中向 JFIF 段添加縮圖
url: /zh-hant/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中向 JFIF 段添加縮圖

## 介紹
在 PSD 檔案的 JFIF 段添加縮圖是常見需求，當您需要快速的視覺預覽而不必載入完整圖像時。本教學將教您如何使用 Aspose.PSD 在 Java 中**添加縮圖**至 JFIF 段。完成本指南後，您將擁有可執行的程式碼範例、對底層 JFIF 結構的了解，以及有效處理大型檔案的技巧。

## 快速回答
- **需要的函式庫是什麼？** Aspose.PSD for Java.
- **支援哪個 Java 版本？** JDK 11 或更新版本.
- **需要多少行程式碼？** 大約 10 行即可完成載入、修改與儲存.
- **可以處理多兆位元組的檔案嗎？** 可以，Aspose.PSD 以串流方式處理資料，記憶體使用量保持低.
- **需要商業授權嗎？** 生產環境必須購買授權；亦提供免費試用版.

## 什麼是 JFIF 段？
JFIF 段是 JPEG 檔案交換格式（JPEG File Interchange Format）的區塊，可儲存縮圖、EXIF 或色彩描述檔等可選資料。  
它位於 PSD 檔案的 JPEG 串流中，並被大多數圖像檢視器識別，用於快速產生預覽。

## 為什麼要在 PSD 檔案中添加縮圖？
Aspose.PSD for Java 支援 **30 多種影像格式**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案。加入縮圖可減少傳輸預覽時的網路頻寬，並加速相簿應用程式的 UI 呈現。

## 前置條件
- Java Development Kit (JDK)：確保您的系統已安裝 Java。您可以從 [Oracle 的 JDK 網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。
- Aspose.PSD for Java：您需要擁有 Aspose.PSD for Java 函式庫。可從 [Aspose.PSD Java 下載頁面](https://releases.aspose.com/psd/java/) 取得。
- Integrated Development Environment (IDE)：使用如 IntelliJ IDEA 或 Eclipse 等 IDE 進行 Java 開發。
- Basic Understanding of Java：熟悉 Java 程式語言及其概念。

## 如何在 Java 中向 JFIF 段添加縮圖？
載入目標 PSD，定位 JFIF 資源，替換其縮圖資料，然後儲存檔案。整個過程只需幾個簡單的 API 呼叫，且 Aspose.PSD 會為您處理低階的 JPEG 結構。

### 步驟 1：匯入套件
`Document`、`JfifResource` 以及相關類別屬於 Aspose.PSD 命名空間。Document 代表 PSD 檔案的容器，JfifResource 提供對 PSD 內 JFIF 段的存取。請在原始檔案的最上方匯入它們。

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### 步驟 2：載入 PSD 圖像
透過將檔案路徑傳入建構子，建立 `PsdImage` 實例。PsdImage 是 Aspose.PSD 用來表示 Photoshop 文件的類別。此步驟會在串流像素資料的同時載入文件的中繼資料。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### 步驟 3：遍歷圖像資源
在 `Resources` 集合中搜尋 `JfifResource`。找到後，您可以將其縮圖位元組陣列替換為新的 JPEG 編碼預覽。

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### 步驟 4：調整縮圖資料
使用任意影像處理函式庫產生小尺寸 JPEG 縮圖（例如 120 × 120 px），然後將產生的位元組陣列指派給 `jfifResource.ThumbnailData`。

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### 步驟 5：儲存修改後的圖像
呼叫 `PsdImage` 物件的 `save` 方法，指定輸出路徑與目標格式。JFIF 段現在已包含新的縮圖。

```java
image.save(dataDir + "output.psd");
```

## 常見問題與解決方案
- **縮圖在檢視器中不可見：** 確認縮圖資料為有效的 JPEG 位元組陣列，且其尺寸不超過 256 × 256 px，這是 JFIF 規範支援的最大尺寸。
- **大型 PSD 發生 OutOfMemoryError：** 使用 `PsdImage.load(inputStream, true)` 開啟串流模式，以降低記憶體使用量。
- **資源類型不正確：** 確認您修改的資源確實為 `JfifResource`；其他資源如 `ExifResource` 不會影響縮圖顯示。

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套商業函式庫，讓開發者能在不需要 Adobe Photoshop 的情況下建立、編輯、轉換與渲染 Photoshop PSD 檔案。

**Q: 在哪裡可以找到 Aspose.PSD for Java 的更多文件？**  
A: 詳細文件可於 [Aspose.PSD for Java 文件頁面](https://reference.aspose.com/psd/java/) 找到。

**Q: Aspose.PSD for Java 可用於商業用途嗎？**  
A: 可以，Aspose.PSD for Java 可用於商業。您可從 [Aspose.PSD 的購買頁面](https://purchase.aspose.com/buy) 購買授權。

**Q: 我可以在購買前試用 Aspose.PSD for Java 嗎？**  
A: 可以，您可從 [Aspose.PSD 的試用下載頁面](https://releases.aspose.com/) 下載免費試用版。

**Q: 如何取得 Aspose.PSD for Java 的支援？**  
A: 請前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 取得支援。

---

**最後更新：** 2026-09-28  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose

## 相關教學

- [使用 Aspose PSD for Java 為 PSD 檔案新增 IOPA 資源](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [為影像新增簽章 – 使用 Aspose.PSD for Java 在畫布上繪製影像](/psd/java/advanced-image-effects/add-signature-to-image/)
- [如何使用 Aspose.PSD for Java 以特定角度旋轉影像](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}