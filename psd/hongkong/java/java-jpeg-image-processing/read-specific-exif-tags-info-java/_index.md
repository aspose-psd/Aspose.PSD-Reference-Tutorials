---
date: 2026-10-08
description: 了解如何使用 Aspose.PSD for Java (asp) 於 Java 中讀取 EXIF 標籤，透過我們的逐步教學提升您的影像處理能力。
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: 在 Java 中讀取特定 EXIF 標籤資訊
og_description: Java 開發人員可使用 Aspose.PSD 快速提取影像中繼資料的 EXIF 標籤。本指南將帶領您載入 PSD、定位縮圖資源，並列印關鍵
  EXIF 欄位，如 WhiteBalance 與 ISO speed。
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: 如何在 Java 中使用 Aspose.PSD 讀取 EXIF 標籤
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: 如何在 Java 中使用 Aspose.PSD 讀取 EXIF 標籤
url: /zh-hant/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中使用 Aspose (asp) 讀取特定 EXIF 標籤資訊

## 介紹
如果您需要 **在 Java 中讀取 EXIF 標籤**，Aspose.PSD (asp) 提供一個乾淨、純 Java 的 API，無需 Photoshop 即可運作。在本教學中，您將學習如何從 PSD 圖像中提取 EXIF 資料，僅選取您關心的標籤，並將其列印到主控台。我們將涵蓋從設定開發環境到提取諸如 WhiteBalance、ISO 速度與焦距等中繼資料的全部步驟。讓我們開始吧！

## 快速解答
- **哪個函式庫可以在 Java 中讀取 PSD 的 EXIF 資料？** Aspose.PSD (asp)  
- **可以提取哪些標籤？** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, and more.  
- **生產環境是否需要授權？** Yes, a commercial license is required; a free trial is available.  
- **我可以將它用於其他影像格式嗎？** The same API supports PNG, JPEG, TIFF via Java image metadata extraction.  
- **實作大約需要多久？** About 10‑15 minutes for a basic read‑only scenario.

## 什麼是 asp (Aspose.PSD for Java)？
Aspose.PSD for Java 是一個純 Java 函式庫，讓開發人員無需安裝 Photoshop 即可處理 Adobe Photoshop 檔案（PSD、PSB）。它提供對圖層、資源與中繼資料（包括 EXIF 標籤）的程式化存取，使其成為 **java image metadata extraction** 任務的理想選擇。

## 為何使用 Aspose.PSD (asp) 進行 EXIF 抽取？
您只需兩個方法呼叫即可在 Java 中抽取 EXIF 標籤，且該函式庫可處理高達 2 GB 的檔案而不必將整個文件載入記憶體。它支援 **30 多種影像格式**，並保留精確的相機設定，讓您在 Windows、Linux 與 macOS 環境中獲得確定性的結果。

## 前置條件
在深入程式碼之前，您需要先準備以下項目：

1. **Java Development Kit (JDK)：** 確保您的機器已安裝 JDK。您可以從 [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
2. **Aspose.PSD for Java：** 從 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) 下載函式庫。  
3. **Integrated Development Environment (IDE)：** 如 IntelliJ IDEA、Eclipse 或 NetBeans 等 IDE 可提升編寫程式的便利性。  
4. **PSD 檔案：** 含有 EXIF 資料的 PSD 檔案。您可以使用本教學提供的範例或任何其他帶有 EXIF 標籤的 PSD 檔案。

## 匯入套件
匯入所需的 Aspose.PSD 類別，例如 Image、PsdImage、ThumbnailResource 與 JpegExifData，以便操作 PSD 檔案。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 步驟 1：載入 PSD 圖像
`Image.load()` loads a file and returns an Image object representing the image data.  
`PsdImage` is the Aspose.PSD class that provides PSD‑specific functionality.  
The `Image.load()` method loads any supported image file into memory, returning a generic `Image` object that you can cast to a PSD‑specific type.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

在此步驟中，我們使用 `Image.load()` 方法載入 PSD 檔案。`PsdImage` 類別用於表示 PSD 圖像，並將載入的圖像轉型為此類別，以存取 PSD 專屬功能。

## 步驟 2：遍歷圖像資源
`PsdImage.getResources()` returns a collection of embedded resources such as thumbnails and EXIF data.  
The `PsdImage.getResources()` call returns a collection of all embedded resources. By iterating over this collection you can locate thumbnail resources that contain EXIF metadata.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

我們使用 `for` 迴圈遍歷圖像資源。目標是找出屬於 `ThumbnailResource` 或 `Thumbnail4Resource` 的資源，因為這些類型保存了 EXIF 資料。

## 步驟 3：抽取 EXIF 資料
`ThumbnailResource.getJpegOptions()` provides access to JPEG options including EXIF metadata.  
`JpegExifData` holds individual EXIF tag values.  
The `ThumbnailResource.getJpegOptions()` method provides access to a `JpegExifData` object, which holds individual EXIF tags such as WhiteBalance, ISOSpeed, and FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

我們使用 `if` 陳述式檢查資源是否為 `ThumbnailResource` 的實例。如果是，則將其轉型並取得其 `JpegOptions` 以存取 `ExifData`。最後，我們列印出包括 WhiteBalance、Pixel Dimensions、ISOSpeed 與 FocalLength 等多個 EXIF 標籤。

## 常見問題與技巧
- **Null EXIF data：** 某些 PSD 檔案可能不包含帶有 EXIF 資訊的縮圖資源。存取標籤值前務必先檢查是否為 `null`。  
- **File path errors：** 使用絕對路徑或確保工作目錄指向包含 PSD 檔案的資料夾。  
- **License restrictions：** 免費試用版限制可處理的頁數；升級為完整授權即可無限制使用。

## 常見問答

### 什麼是 EXIF 資料？
EXIF（Exchangeable Image File Format）資料是嵌入於影像檔案中的中繼資料，包含相機設定、日期時間與影像尺寸等資訊。

### 我可以使用 Aspose.PSD 編輯 EXIF 資料嗎？
可以，Aspose.PSD 允許您讀取與修改 EXIF 資料。您可以更新標籤並將變更儲存回影像檔案。

### Aspose.PSD for Java 是免費的嗎？
Aspose.PSD 提供可從 [Aspose.PSD official releases page](https://releases.aspose.com/) 下載的免費試用版。若需完整功能，必須購買授權。

### Aspose.PSD 支援哪些其他格式？
Aspose.PSD 支援多種 Adobe Photoshop 格式，包括 PSD、PSB 等，亦提供將這些格式轉換為 PNG、JPEG、TIFF 等的選項。

### 如何取得 Aspose.PSD 的支援？
您可以透過 Aspose.PSD [forum](https://forum.aspose.com/c/psd/34) 取得支援。

### 這如何協助 **java image metadata extraction**？
透過使用 `JpegExifData` 物件，您可以程式化地抽取任何所需的 EXIF 標籤，為跨影像格式的更廣泛中繼資料抽取任務奠定堅實基礎。

---

**最後更新:** 2026-10-08  
**測試環境:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**作者:** Aspose

## 相關教學

- [讀取與修改 Jpeg Exif 標籤 Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Java Jpeg 圖像處理](/psd/java/java-jpeg-image-processing/)
- [如何使用 Aspose.PSD for Java 以特定角度旋轉圖像](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}