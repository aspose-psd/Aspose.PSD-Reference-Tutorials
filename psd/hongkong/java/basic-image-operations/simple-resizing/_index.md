---
date: 2026-06-13
description: 了解如何使用 Java 圖像處理函式庫調整圖像大小。跟隨我們的逐步指南，使用 Aspose.PSD for Java 進行高效的圖像處理。
keywords:
- java image manipulation library
- how to resize image java
- change image dimensions java
linktitle: 執行簡易調整大小
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  headline: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  type: TechArticle
- description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  name: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  steps:
  - name: Set Your Document Directory
    text: Define the folder that contains the source PSD file. Replace the placeholder
      with your actual path.
  - name: Specify Source and Destination Paths
    text: Create full file names for the input PSD and the output JPEG.
  - name: Load the Image
    text: '`Image.load(path)` reads an image file from the given path and returns
      an `Image` instance. Load the PSD into an `Image` object.'
  - name: Resize the Image
    text: '`image.resize(width, height)` changes the image dimensions to the specified
      pixel size. Resize to the desired dimensions (e.g., 300 × 300 pixels).'
  - name: Save the Resized Image
    text: '`image.save(path, options)` writes the image to the specified file using
      the given format options. Export the resized bitmap as a JPEG file. > **Pro
      tip:** Experiment with different width/height values or maintain the aspect
      ratio by calculating one dimension from the other.'
  type: HowTo
- questions:
  - answer: Absolutely. The `resize(width, height)` method lets you define any pixel
      size you need.
    question: Can I resize images to specific dimensions using Aspose.PSD for Java?
  - answer: Yes. Besides PSD, the library supports JPEG, PNG, BMP, TIFF, and many
      more.
    question: Is Aspose.PSD for Java compatible with different image formats?
  - answer: Refer to the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for a full API reference.
    question: Where can I find additional documentation for Aspose.PSD for Java?
  - answer: Certainly! Download the [free trial version](https://releases.aspose.com/)
      to explore all features.
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to ask
      questions and share experiences with the community.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD 進行簡易調整大小 – Java 圖像處理函式庫
url: /zh-hant/java/basic-image-operations/simple-resizing/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 進行簡易調整大小 – Java 圖像處理函式庫

## 介紹

如果您是一位尋找可靠的 **java image manipulation library** 的 Java 開發人員，您來對地方了。在本教學中，我們將示範如何使用 Aspose.PSD for Java 來 **how to resize image java** 專案——這是一個強大的函式庫，使圖像處理快速且簡單。完成本指南後，您將擁有一個清晰、可直接投入生產環境的範例，能夠嵌入任何 Java 應用程式中。

## 快速回答
- **使用的函式庫是什麼？** Aspose.PSD for Java，領先的 java image manipulation library。  
- **我可以調整任何 PSD 的大小嗎？** 是的——此函式庫支援 PSD、JPEG、PNG 等多種格式。  
- **如何指定尺寸？** 呼叫 `image.resize(width, height)` 並傳入所需的像素尺寸。  
- **我需要授權嗎？** 免費試用可用於開發；正式環境需要授權。  
- **需要哪個 Java 版本？** Java 8 或以上。

## 什麼是 Java 圖像處理函式庫？

一個 **java image manipulation library** 是一組 Java API，讓您能以程式方式編輯點陣圖——包括調整大小、裁切、格式轉換與圖層處理——而無需外部工具。Aspose.PSD 為 PSD 及其他多種格式提供這些功能，並向開發人員公開乾淨的物件導向 API。

## 為何使用 Aspose.PSD 進行簡易調整大小？

Aspose.PSD 提供 **performance‑optimized** 演算法，能在一般伺服器上於一秒內處理超過 500 層的檔案，且完全以 Java 執行——不需要原生 DLL 或外部二進位檔。此函式庫支援 **30+ image formats**（包括 PSD、JPEG、PNG、TIFF、BMP、GIF），且可處理超過 200 MB 的檔案而不需將整個文件載入記憶體，這使其非常適合高吞吐量的伺服器端工作流程。

## 前置條件

在開始之前，請確保您已具備以下項目：

1. **Java Development Kit (JDK)** – 從 [Java website](https://www.oracle.com/java/) 下載最新版本。  
2. **Aspose.PSD for Java** – 從 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) 取得函式庫。  

具備上述項目可確保調整大小範例的順利設定。

## 匯入套件

`Image` 類別及相關匯出選項是載入與儲存檔案所必需的。

`Image` 是代表可載入、編輯與儲存之圖像的主要類別。

`JpegOptions` 指定以 JPEG 格式儲存圖像的設定。

這些匯入讓您能使用核心的 `Image` 類別與 JPEG 匯出選項。

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.JpegOptions;
```

## 步驟指南

### 步驟 1：設定文件目錄

定義包含來源 PSD 檔案的資料夾。將佔位符替換為實際路徑。

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：指定來源與目標路徑

為輸入的 PSD 與輸出的 JPEG 建立完整檔名。

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "SimpleResizing_out.jpg";
```

### 步驟 3：載入圖像

`Image.load(path)` 從給定路徑讀取圖像檔案，並回傳 `Image` 實例。

將 PSD 載入 `Image` 物件中。

```java
Image image = Image.load(sourceFile);
```

### 步驟 4：調整圖像大小

`image.resize(width, height)` 會將圖像尺寸變更為指定的像素大小。

將圖像調整至所需尺寸（例如 300 × 300 像素）。

```java
image.resize(300, 300);
```

### 步驟 5：儲存調整後的圖像

`image.save(path, options)` 依指定的格式選項將圖像寫入指定檔案。

將調整大小的位圖匯出為 JPEG 檔案。

```java
image.save(destName, new JpegOptions());
```

> **小技巧：** 嘗試不同的寬度/高度值，或透過根據另一維度計算來維持長寬比。

## 如何在 Java 中變更圖像尺寸？

在 `Image` 實例上使用 `resize(width, height)` 方法，傳入所需的精確像素值。例如，`image.resize(800, 600)` 會產生 800 × 600 像素的輸出，同時保留色彩深度與中繼資料。如果想保留原始長寬比，請在呼叫 `resize` 前根據原始寬高比計算第二個維度。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **`OutOfMemoryError`** | 非常大的 PSD 檔案可能會超過 JVM 堆積大小。 | 增加 JVM 堆積大小 (`-Xmx2g`) 或分段處理圖像。 |
| **Unsupported format** | 嘗試在未提供適當選項的情況下載入非 PSD 檔案。 | 使用適當的 `Image.load` 重載，或先將檔案轉換。 |
| **Distorted output** | 長寬比不正確。 | 根據原始長寬比計算高度，或使用 `image.resizeProportionally`。 |

## 常見問答

**Q: 我可以使用 Aspose.PSD for Java 將圖像調整至特定尺寸嗎？**  
A: 當然可以。`resize(width, height)` 方法讓您可以定義任何所需的像素尺寸。

**Q: Aspose.PSD for Java 是否相容於不同的圖像格式？**  
A: 是的。除了 PSD，該函式庫還支援 JPEG、PNG、BMP、TIFF 等多種格式。

**Q: 我可以在哪裡找到 Aspose.PSD for Java 的其他文件？**  
A: 請參考 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 以取得完整的 API 參考文件。

**Q: 我可以在購買前試用 Aspose.PSD for Java 嗎？**  
A: 當然！下載 [free trial version](https://releases.aspose.com/) 以探索所有功能。

**Q: 我該如何取得 Aspose.PSD for Java 的支援？**  
A: 前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 提問並與社群分享使用經驗。

## 結論

在本教學中，我們示範了像 Aspose.PSD 這樣的 **java image manipulation library** 如何讓 **how to resize image java** 任務變得輕鬆。遵循上述簡潔步驟，即可將圖像調整大小整合至任何 Java 應用程式，確保快速且可靠的結果，且無需外部工具。

---

**最後更新：** 2026-06-13  
**測試環境：** Aspose.PSD for Java 24.12 (latest)  
**作者：** Aspose

## 相關教學

- [在 Aspose.PSD for Java 中使用 Resize Type 列舉的 Java 圖像調整大小](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [在 Aspose.PSD for Java 中使用雙三次重採樣器的高品質圖像縮放](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並比例調整大小](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}