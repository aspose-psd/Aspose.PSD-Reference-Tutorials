---
date: 2026-08-01
description: 了解如何使用 Aspose.PSD for Java 進行 Java 影像模糊、套用 Gaussian blur 濾鏡，並在簡單步驟中將
  PSD 轉換為 GIF。
keywords:
- blur image java
- apply gaussian blur
- convert psd to gif
- aspose psd conversion
lastmod: 2026-08-01
linktitle: 模糊影像
og_description: 使用 Aspose.PSD 快速進行 Java 影像模糊。了解如何套用 Gaussian blur、添加模糊效果，並在簡潔的 Java
  教學中將 PSD 轉換為 GIF。
og_image_alt: Guide showing Java code to blur an image and convert PSD to GIF using
  Aspose.PSD
og_title: Java 影像模糊 – 使用 Aspose.PSD 添加 Gaussian Blur 效果
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to blur image java using Aspose.PSD for Java, apply gaussian
    blur filter and convert PSD to GIF in a few simple steps.
  headline: Blur Image Java with Aspose.PSD – Add Blur Effect
  type: TechArticle
- description: Learn how to blur image java using Aspose.PSD for Java, apply gaussian
    blur filter and convert PSD to GIF in a few simple steps.
  name: Blur Image Java with Aspose.PSD – Add Blur Effect
  steps:
  - name: Define File Paths
    text: Set the source PSD file and the destination GIF file. Using absolute or
      correctly resolved relative paths prevents “File not found” errors.
  - name: Load the Image
    text: The `Image` class represents any image format that Aspose.PSD can read.
      Loading a PSD returns a concrete subclass that gives you access to layers and
      raster data.
  - name: Convert to RasterImage
    text: '`RasterImage` is the raster‑based representation required by most filters,
      including Gaussian blur. Casting the loaded image ensures the blur algorithm
      works on pixel data rather than vector information.'
  - name: Apply Blur Filter
    text: '`GaussianBlurFilter` applies a Gaussian kernel with a configurable radius.
      In this example we use a radius of 15 pixels on both the X and Y axes, which
      yields a smooth, natural‑looking blur.'
  - name: Save the Result
    text: '`GifOptions` tells Aspose.PSD to encode the final raster image as a GIF.
      The library handles color quantisation automatically, so the output file size
      stays small without manual tweaking. By following these five steps, you have
      successfully **blurred an image** using Aspose.PSD for Java and saved th'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library can blur images in Java?
  - answer: Gaussian blur filter.
    question: Which filter creates a smooth blur?
  - answer: Yes – use `GifOptions`.
    question: Can I output to GIF after blurring?
  - answer: A free trial works for testing; a license is required for production.
    question: Do I need a license for development?
  - answer: About 10‑15 minutes for a basic blur.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- blur image java
- Aspose.PSD
- Java image processing
- gaussian blur
- PSD to GIF
title: 使用 Aspose.PSD 的 Java 影像模糊 – 添加模糊效果
url: /zh-hant/java/advanced-techniques/blur-image/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 的 Blur Image Java – 添加模糊效果

## 介紹

如果您需要快速且可靠地 **blur image java** 程式，Aspose.PSD for Java 為您提供簡單的 API，能在任何 PSD 檔案上加入模糊效果。本 **java image processing tutorial** 將一步步說明如何 **apply gaussian blur**、如何 **convert psd to gif**，以及為何在 Java 應用程式中可能需要使用背景模糊。說明採用淺顯語言，即使您是影像處理函式庫的新手也能跟上。您亦可於 [here](https://releases.aspose.com/) 探索其他 Aspose 函式庫。

## 快速解答
- **什麼函式庫可以在 Java 中模糊影像？** Aspose.PSD for Java.  
- **哪種濾鏡能產生平滑的模糊？** Gaussian blur filter.  
- **模糊後可以輸出為 GIF 嗎？** Yes – use `GifOptions`.  
- **開發時需要授權嗎？** 免費試用可用於測試；正式環境需購買授權。  
- **實作需要多長時間？** 基本模糊大約需要 10‑15 分鐘。

## 「blur image java」是什麼？

在 Java 中對影像進行模糊，指的是套用卷積運算，以相鄰像素的平均值來柔化細節，通常使用 Gaussian kernel。此操作會降低高頻資訊，產生平滑、失焦的外觀。它常用於背景效果、隱私遮蔽或藝術風格，且可套用於 PSD 檔案中的任何點陣圖層。

## 為什麼要使用 Aspose.PSD 來完成此任務？

Aspose.PSD 提供即用且高效能的 Gaussian blur 實作，可作用於 PSD 檔案內的任何點陣圖層。此函式庫支援 **120+ 影像格式**，可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的 PSD 檔案，且可在支援 Java 8+ 的任何作業系統上執行。它亦提供一鍵轉換為 GIF、PNG、JPEG 及其他多種格式，免除額外影像函式庫的需求。

## 前置條件

- 已安裝 Java Development Kit (JDK)。  
- Aspose.PSD for Java 函式庫。您可於 [here](https://releases.aspose.com/psd/java/) 下載。  
- 具備基本的 Java 語法知識。

## 匯入套件

`com.aspose.psd` 套件提供載入、編輯與儲存 Photoshop 文件的核心類別。請在開始編寫程式碼前匯入所需的類別。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussianBlurFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## 步驟說明

### 步驟 1：定義檔案路徑  
設定來源 PSD 檔案與目標 GIF 檔案。使用絕對路徑或正確解析的相對路徑可避免「File not found」錯誤。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "BlurAnImage_out.gif";
```

### 步驟 2：載入影像  
`Image` 類別代表 Aspose.PSD 能讀取的任何影像格式。載入 PSD 時會回傳具體的子類別，讓您存取圖層與點陣資料。

```java
// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

### 步驟 3：轉換為 RasterImage  
`RasterImage` 是大多數濾鏡（包括 Gaussian blur）所需的點陣表示。將載入的影像轉型為 `RasterImage` 可確保模糊演算法作用於像素資料，而非向量資訊。

```java
// Convert the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
```

### 步驟 4：套用模糊濾鏡  
`GaussianBlurFilter` 會以可設定半徑的 Gaussian kernel 進行模糊。在本範例中，我們在 X 與 Y 軸皆使用 15 像素的半徑，產生平滑、自然的模糊效果。

```java
// Pass Bounds[rectangle] of the image and GaussianBlurFilterOptions instance to the Filter method
rasterImage.filter(rasterImage.getBounds(), new GaussianBlurFilterOptions(15, 15));
```

### 步驟 5：儲存結果  
`GifOptions` 告訴 Aspose.PSD 將最終的點陣圖編碼為 GIF。函式庫會自動處理顏色量化，因而使輸出檔案大小保持較小，無需手動調整。

```java
// Save the results in GIF format
rasterImage.save(destName, new GifOptions());
```

依照上述五個步驟，您已成功使用 Aspose.PSD for Java **模糊影像**，並將結果儲存為 GIF。

## 為何此議題重要

影像模糊不僅是美觀的調整；它能提升 UI 可讀性、保護敏感資料，並製作專業等級的景深效果。使用 Aspose.PSD 套用 Gaussian blur，於一般 3.0 GHz CPU 上對 1920×1080 影像的處理時間少於 200 ms，適合於桌面或 Web 應用程式的即時預覽情境。

## 常見使用情境

1. **User‑interface overlays** – 在顯示模態對話框時，套用細微的模糊以暗化背景。  
2. **Privacy protection** – 在分享前遮蔽影像中的人臉或車牌。  
3. **Artistic filters** – 結合多次模糊以營造夢幻效果。

## 常見問題與技巧

- **Incorrect file path** – 確認 `dataDir` 以符合作業系統的分隔符號 (`/` 或 `\`) 結尾。  
- **Unsupported image format** – 模糊濾鏡僅支援點陣圖；向量圖層必須先轉為點陣圖。  
- **Performance** – 較大的影像可能需要更長時間；若對速度有嚴格要求，可在套用濾鏡前先調整影像大小。  
- **Memory consumption** – 處理完畢後，若在迴圈中處理大量影像，請呼叫 `System.gc()` 或關閉串流以釋放記憶體。

## 常見問答

### Q1: Aspose.PSD for Java 是否適合初學者？
**A:** 絕對適合！Aspose.PSD 附有完整文件與直觀 API，能指引各層次開發者。

### Q2: 我可以將 Aspose.PSD 用於商業專案嗎？
**A:** 可以。請前往 [here](https://purchase.aspose.com/buy) 了解授權方案。

### Q3: 有提供免費試用嗎？
**A:** 有，您可於 [here](https://releases.aspose.com/) 取得免費試用。

### Q4: 我該從哪裡取得 Aspose.PSD for Java 的支援？
**A:** 請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得支援相關問題的協助。

### Q5: 我要如何取得 Aspose.PSD 的臨時授權？
**A:** 您可於 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 結論

Aspose.PSD for Java 讓 **blur image java** 任務變得輕鬆。無論您需要 **apply gaussian blur**、**add blur effect**，或 **convert PSD to GIF**，此函式庫皆能處理繁重工作。可嘗試不同的模糊半徑、結合多種濾鏡，並探索 **blur background java** 如何提升您的應用程式。

---

**最後更新：** 2026-08-01  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose

## 相關教學

- [將 PSD 轉為 GIF - 使用 Aspose.PSD for Java 套用高斯與 Wiener 濾鏡於彩色影像](/psd/java/image-processing/apply-gaussian-wiener-filters-color-image/)
- [逐步濾鏡 - 使用 Aspose.PSD for Java 套用 Motion Wiener 濾鏡](/psd/java/image-processing/apply-motion-wiener-filters/)
- [如何在 Aspose.PSD for Java 中套用漸層效果](/psd/java/advanced-image-effects/add-gradient-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}