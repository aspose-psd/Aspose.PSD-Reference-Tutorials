---
date: 2026-08-17
description: 了解如何使用 Aspose.PSD for Java 在 Java 中裁剪 PSD 檔案——快速、精確地在您的 Java 應用程式中修剪
  Photoshop 文件。
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: 裁剪 PSD 檔案
og_description: 使用 Aspose.PSD for Java 裁剪 PSD 檔案。本指南逐步說明如何高效修剪 Photoshop 檔案，提供免寫程式碼的說明與最佳實踐技巧。
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: 使用 Aspose.PSD 的 Java 裁剪 PSD 檔案 – 快速影像裁剪
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: 使用 Aspose.PSD 的 Java 裁剪 PSD 檔案
url: /zh-hant/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 的 Java 裁剪 PSD 檔案

## 介紹

如果您需要以程式方式裁剪 Photoshop 文件，**crop psd file java** 是從事圖形管線、資產管線或自動化設計工作流程的 Java 開發人員常見的任務。Aspose.PSD for Java 提供了專門的 API，讓您只需幾行程式碼即可定義矩形並擷取所需區域。在本教學中，您將了解為何此函式庫專為高效能裁剪而設計、如何設定開發環境，以及產生 PSD 與 PNG 結果的完整步驟。

## 快速回答
- **哪個函式庫負責在 Java 中裁剪 PSD？** Aspose.PSD for Java。
- **基本裁剪需要多少行程式碼？** 載入影像後只需兩個 API 呼叫。
- **可以將裁剪區域匯出為 PNG 嗎？** 可以，使用內建的 PNG 儲存選項。
- **生產環境是否需要授權？** 試用期結束後需購買商業授權。
- **支援哪些 Java 版本？** 支援 Java 8 及以上版本，包括 Java 11、17 與 21。

## 什麼是 crop psd file java？

crop psd file java 指的是使用 Java 程式碼以程式方式從 Photoshop Document（.psd）中切割出矩形區域的過程。透過 Aspose.PSD，您可以在不啟動 Photoshop 的情況下完成此操作，非常適合伺服器端的影像管線。

## 為什麼使用 Aspose.PSD for Java？

Aspose.PSD 支援 **30+ 輸入與輸出格式**，且可在不將整個文件載入記憶體的情況下處理高達 **500 MB** 的 PSD 檔案，這得益於其串流架構。函式庫會保留圖層、遮色片與色彩描述檔，提供與 Photoshop 原生輸出相符的裁剪結果。這種可量化的效能讓您在一般硬體上執行批次工作時，記憶體使用可預測。

## 前置條件

- **Java 開發環境** – 已安裝並設定 JDK 8 或更新版本。
- **Aspose.PSD for Java** – 下載最新的 JAR 與文件 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)。
- **範例 PSD 檔案** – 將 .psd 檔案放置於專案目錄中，以便程式碼能找到它。

## 如何在 Java 中裁剪 PSD 檔案？

載入來源檔案、定義要保留的矩形、套用裁剪，最後以所需格式儲存結果。整個工作流程僅需五個簡單步驟，每個步驟皆以佔位符示範，您可自行插入實際程式碼。

### 步驟 1：設定文件目錄

將 “Your Document Directory” 替換為包含欲處理 PSD 的絕對或相對路徑。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### 步驟 2：載入 PSD 檔案

`RasterImage` 類別是 Aspose.PSD 用於對 PSD 檔案執行點陣圖操作的入口點。載入檔案會在記憶體中建立可供操作的表示。

```java
String dataDir = "Your Document Directory";
```

### 步驟 3：定義裁剪區域

`Rectangle` 定義了要保留區域的 X、Y 座標以及寬度與高度。此類別屬於標準 Java AWT 套件，Aspose.PSD 會使用它來指定裁剪範圍。

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### 步驟 4：儲存裁剪後的 PSD

套用裁剪後，您可以將結果以 PSD 格式寫回。函式庫僅寫入裁剪後的像素，並保留原始的色彩模式與位元深度。

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### 步驟 5：將裁剪後的影像儲存為 PNG

若需要網頁友好的版本，可將裁剪後的點陣圖匯出為 PNG。Aspose.PSD 提供 PNG 儲存選項，讓您可控制壓縮等級與交錯方式。

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## 常見問題與解決方案

- **矩形座標不正確** – 確保 X/Y 值從 0 開始，代表左上角；負值會拋出 `ArgumentException`。
- **大型檔案記憶體激增** – 使用 `loadOptions.setLoadOnlyVisibleLayers(true)` 選項，可在不需要隱藏圖層時降低記憶體使用。
- **色彩描述檔遺失** – 在裁剪前呼叫 `image.getColorProfile()` 取得原始 ICC 描述檔，裁剪後再重新指派。

## 常見問答

### Q1: 我可以使用 Aspose.PSD for Java 裁剪其他格式的影像嗎？

A1: Aspose.PSD 主要針對 PSD 檔案，但同時支援 BMP、GIF、JPEG、PNG、TIFF 以及其他多種點陣圖格式的輸入與輸出。

### Q2: Aspose.PSD for Java 是否適用於大規模影像處理？

A2: 是的。函式庫的串流架構能在記憶體佔用低於 100 MB 的情況下處理多百頁的 PSD 檔案，十分適合批次作業。

### Q3: 使用 Aspose.PSD for Java 有哪些授權考量？

A3: 生產環境部署必須購買商業授權。相關細節請參閱 [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy)。

### Q4: 我該如何取得 Aspose.PSD for Java 相關問題的支援？

A4: 前往 [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) 提問、分享程式碼片段，並獲得社群與產品工程師的協助。

### Q5: 我可以在購買前先試用 Aspose.PSD for Java 嗎？

A5: 可以，您可下載功能完整的免費試用版 [Aspose.PSD free trial download](https://releases.aspose.com/)。

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## 相關教學

- [在 Aspose.PSD for Java 中以矩形裁剪影像](/psd/java/image-editing/crop-image-by-rectangle/)
- [在 Aspose.PSD for Java 中以位移裁剪影像](/psd/java/image-editing/crop-image-by-shifts/)
- [使用 Aspose.PSD 在 Java 中旋轉影像](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}