---
date: 2026-10-08
description: 了解如何使用 Aspose.PSD for Java 從 JFIF 圖像提取縮圖。逐步指南、程式碼片段以及給 Java 開發人員的最佳實踐。
keywords:
- how to extract thumbnail
- how to read jfif
- java extract image metadata
lastmod: 2026-10-08
linktitle: 在 Java 中從 JFIF 提取縮圖
og_description: 如何使用 Aspose.PSD for Java 從 JFIF 圖像提取縮圖。請參考此詳細教學，以有效讀取 JFIF 檔案並取得圖像中繼資料。
og_image_alt: Screenshot of Java code extracting a thumbnail from a JFIF image with
  Aspose.PSD
og_title: 如何在 Java 中從 JFIF 提取縮圖 – Aspose.PSD 指南
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to extract thumbnail from JFIF images using Aspose.PSD for
    Java. Step‑by‑step guide, code snippets, and best practices for Java developers.
  headline: How to extract thumbnail from JFIF in Java
  type: TechArticle
- description: Learn how to extract thumbnail from JFIF images using Aspose.PSD for
    Java. Step‑by‑step guide, code snippets, and best practices for Java developers.
  name: How to extract thumbnail from JFIF in Java
  steps:
  - name: load the PSD image
    text: First, create a `PsdImage` object that represents the source file. This
      object gives you access to all embedded resources, including thumbnails. Replace
      `"Your Document Directory"` with the actual path to your JFIF/PSD file.
  - name: iterate over image resources
    text: Next, loop through the image’s resources collection to find the thumbnail
      entry. The thumbnail is stored as a `JfifResource` object. This loop checks
      each resource in the PSD image to find the thumbnail resource.
  - name: extract JFIF data
    text: When the thumbnail resource is found, cast it to `JfifResource` and read
      its raw JFIF byte array. You can then write the bytes to a file or process them
      in memory. If the JFIF data is present, you can extract and utilize it for your
      application.
  - name: extract EXIF data (optional)
    text: If you also need metadata such as camera model or capture date, the same
      `JfifResource` exposes an `ExifData` object. Pull the desired tags and use them
      as needed. This step allows you to retrieve and work with EXIF information associated
      with the thumbnail.
  - name: save the thumbnail (optional)
    text: Finally, write the extracted JFIF bytes to a `.jpg` file so you can view
      the thumbnail directly. Saving the thumbnail makes it easy to verify the extraction
      result.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to read, edit,
      and export PSD, JPEG, JFIF, and many other image formats programmatically.
    question: What is Aspose.PSD for Java?
  - answer: You can download Aspose.PSD for Java from the **Aspose.PSD for Java download
      page**([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)).
    question: How can I download Aspose.PSD for Java?
  - answer: Yes, you can get a free trial from the **Aspose free trial page**([https://releases.aspose.com/](https://releases.aspose.com/)).
    question: Is a free trial available?
  - answer: You can find the documentation on the **Aspose.PSD Java API reference**([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)).
    question: Where is the official documentation?
  - answer: You can get support from the Aspose.PSD community forum **Aspose PSD forum**([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).
    question: How do I obtain support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract thumbnail
- Aspose.PSD
- Java image processing
title: 如何在 Java 中從 JFIF 提取縮圖
url: /zh-hant/java/java-jpeg-image-processing/extract-thumbnail-from-jfif-java/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中從 JFIF 提取縮圖

## 介紹
在本教學中，您將學習 **提取縮圖** 從 JFIF 圖像使用 Aspose.PSD for Java。縮圖提取是當您需要快速預覽大型圖像集合、產生相簿，或在多媒體應用程式中嵌入低解析度預覽時的常見需求。完成本指南後，您將能夠讀取 JFIF 檔案、定位其縮圖資源，並僅透過幾行 Java 程式碼取得嵌入的圖像資料。

## 快速解答
- **需要的函式庫是什麼？** Aspose.PSD for Java.
- **目標的主要格式是什麼？** JFIF (JPEG File Interchange Format) thumbnails.
- **開發時需要授權嗎？** 開發時可使用免費試用版；正式上線則需商業授權。
- **需要多少行程式碼？** 大約 10‑15 行程式碼，分為四個步驟。
- **我也可以讀取 EXIF 中繼資料嗎？** 是的，同一縮圖資源可提供 EXIF 資料。

## 什麼是提取縮圖？
**提取縮圖** 指的是以程式方式取得儲存在 JFIF 或 PSD 檔案內的小型預覽圖像。此預覽圖通常為 100 × 100 px 或更小，用於在不載入完整解析度圖像的情況下快速視覺辨識。

## 為什麼使用 Aspose.PSD for Java？
Aspose.PSD 支援 **30 多種影像格式**（包括 PSD、PSB、BMP、JPEG、PNG 以及 JFIF），且可在不將整張圖像載入記憶體的情況下處理高達 **2 GB** 的檔案。此函式庫能處理複雜的中繼資料結構，如 EXIF 與 IPTC，並在 Windows、macOS 與 Linux JVM 上提供一致的 API。

## 前置條件
- 基本的 Java 程式設計知識。
- 已在電腦上安裝 JDK（Java Development Kit）。
- Aspose.PSD for Java 函式庫。您可從 **Aspose.PSD for Java 下載頁面**([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)) 下載。
- 已設定好的整合開發環境（IDE），如 IntelliJ IDEA 或 Eclipse。

## 如何在 Java 中從 JFIF 圖像提取縮圖？
載入 JFIF 檔案、定位縮圖資源，並取得其二進位資料——整個過程僅需四個簡潔步驟。以下程式碼片段示範每個步驟；您只需將佔位路徑替換為自己的圖像檔案位置即可。

### 步驟 1：載入 PSD 圖像
首先，建立一個代表來源檔案的 `PsdImage` 物件。此物件可讓您存取所有嵌入的資源，包括縮圖。

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.jpeg.JFIFData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```  
將 `"Your Document Directory"` 替換為 JFIF/PSD 檔案的實際路徑。

### 步驟 2：遍歷圖像資源
接著，遍歷圖像的資源集合以尋找縮圖項目。縮圖以 `JfifResource` 物件儲存。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "example.psd");
```  
此迴圈檢查 PSD 圖像中的每個資源，以尋找縮圖資源。

### 步驟 3：提取 JFIF 資料
當找到縮圖資源後，將其轉型為 `JfifResource`，並讀取其原始 JFIF 位元組陣列。之後您可以將位元組寫入檔案或在記憶體中處理。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Further processing steps go here.
    }
}
```  
如果存在 JFIF 資料，您即可提取並在應用程式中使用。

### 步驟 4：提取 EXIF 資料（可選）
如果您還需要相機型號或拍攝日期等中繼資料，同一個 `JfifResource` 會提供 `ExifData` 物件。擷取所需的標籤並依需求使用。

```java
ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
JfifData jfif = thumbnail.getJpegOptions().getJfif();
if (jfif != null) {
    // Extract JFIF data and process.
}
```  
此步驟讓您取得並處理與縮圖相關的 EXIF 資訊。

### 步驟 5：儲存縮圖（可選）
最後，將提取的 JFIF 位元組寫入 `.jpg` 檔案，以便直接檢視縮圖。

```java
JpegExifData exif = thumbnail.getJpegOptions().getExifData();
if (exif != null) {
    // Extract EXIF data and process.
}
```  
儲存縮圖可讓您輕鬆驗證提取結果。

## 常見問題與故障排除
- **Null thumbnail resource** – 某些 JFIF 檔案未包含嵌入的縮圖。請確認來源圖像有預覽，或改用其他檔案。
- **Unsupported image size** – 極大的檔案可能超出預設記憶體限制。如遇 `OutOfMemoryError`，請使用 `-Xmx2g` 增加 JVM 堆積大小。
- **Incorrect file path** – 請確保路徑使用正斜線 (`/`) 或在 Windows 上使用雙反斜線 (`\\`)。

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一個函式庫，讓開發人員能以程式方式讀取、編輯與匯出 PSD、JPEG、JFIF 以及許多其他影像格式。

**Q: 如何下載 Aspose.PSD for Java？**  
A: 您可從 **Aspose.PSD for Java 下載頁面**([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)) 下載 Aspose.PSD for Java。

**Q: 是否提供免費試用？**  
A: 是的，您可從 **Aspose 免費試用頁面**([https://releases.aspose.com/](https://releases.aspose.com/)) 取得免費試用。

**Q: 官方文件在哪裡？**  
A: 您可在 **Aspose.PSD Java API 參考文件**([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) 中找到相關文件。

**Q: 如何取得 Aspose.PSD 的支援？**  
A: 您可從 Aspose.PSD 社群論壇 **Aspose PSD 論壇**([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) 獲得支援。

**Q: 我可以提取縮圖以外的其他中繼資料嗎？**  
A: 可以，同一個 `JfifResource` 可存取 EXIF、IPTC 與 XMP 中繼資料。

**Q: 此函式庫能在所有主要作業系統上運作嗎？**  
A: 此函式庫為純 Java，能在 Windows、macOS 與 Linux 上執行，且不需原生相依性。

---

**Last Updated:** 2026-10-08  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## 相關教學

- [Java JPEG 圖像處理](/psd/java/java-jpeg-image-processing/)
- [使用 Aspose.PSD for Java 重新調整圖像 – 繪製形狀與基本圖像操作](/psd/java/basic-image-operations/)
- [如何使用 Aspose.PSD 執行簡易縮放 – Java 圖像操作函式庫](/psd/java/basic-image-operations/simple-resizing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}