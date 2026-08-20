---
date: 2026-05-19
description: 了解如何在 Java 中使用 Aspose.PSD 以特定角度旋轉圖像。本指南涵蓋 rotate image java、rotate image
  specific angle、background handling 等內容。
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: 如何以特定角度旋轉圖像
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 以特定角度旋轉圖像
url: /zh-hant/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在特定角度旋轉圖像（使用 Aspose.PSD for Java）

如果您需要在 Java 應用程式中以程式方式 **how to rotate image**，Aspose.PSD for Java 提供乾淨且高效能的 API，負責繁重的計算工作。無論您是在建構相片編輯器、產生縮圖，或是為 Web 服務準備資產，精確角度的圖像旋轉都是常見需求。本教學將完整示範從載入 PSD 檔案到儲存旋轉後結果的全流程，同時強調快取與背景處理等最佳實踐。

## 快速解答
- **什麼程式庫最適合在 Java 中旋轉圖像？** Aspose.PSD for Java 提供最可靠的旋轉引擎。  
- **我可以以任意角度旋轉嗎？** 可以，`rotate` 方法接受 `float` 型別的角度，正值或負值皆可。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線需購買商業授權。  
- **支援哪些圖像格式？** PSD、JPEG、PNG、TIFF、GIF、BMP、JPEG2000、WMF、EMF，以及超過 30 種其他格式。  
- **如何為空白區域設定背景顏色？** 在 `rotate` 方法中傳入 `Color` 例項。

## 如何在特定角度使用 Aspose.PSD for Java 旋轉圖像？

載入來源檔案，呼叫 `image.rotate(angle, true, backgroundColor)`，然後儲存——只需三個簡潔步驟，即可為您處理所有繁雜的數學運算。Aspose.PSD 會保留圖層、色彩配置檔與 Alpha 通道，同時擴展畫布以避免裁切，即使是 12.5° 這類分數角度，輸出也能如預期般精確。此方法適用於從幾 KB 到數百頁的 PSD 檔案，且不會耗盡記憶體。

## 什麼是 Java 中的圖像旋轉？

圖像旋轉是一種幾何變換，將像素矩陣繞著樞紐點（通常是圖像中心）依指定角度旋轉。使用純 Java 時，您需要操作 `Graphics2D` 物件、計算三角函數偏移，並手動處理背景。Aspose.PSD 抽象化了這些複雜度，自動處理色深、圖層遮罩與不同檔案格式。

## 為什麼使用 Aspose.PSD 來旋轉圖像？

Aspose.PSD 支援 **30+ 輸入與輸出格式**，且能在一般伺服器級 CPU 上於 **5 秒內處理 500 頁 PSD 檔案**。內建快取 (`image.cacheData()`) 可將大型資產的記憶體使用量降低最高 60%，`rotate` 方法允許您指定背景顏色，必要時保留透明角落。這些量化的優勢使其成為高吞吐量圖像管線的業界標準選擇。

## 前置條件

在開始之前，請確保您已具備：

1. **Java Development Kit (JDK 8 或更新版本)** – 任何 IDE 或命令列環境皆可。  
2. **Aspose.PSD for Java** – 從 [Aspose.PSD Java 頁面](https://reference.aspose.com/psd/java/) 下載最新的 JAR。  
3. **範例 PSD 檔案** – 例如 `sample.psd`，放置於程式碼可參考的資料夾中。

## 匯入套件

`RasterImage` 類別與相關工具是旋轉工作流程的核心。

`RasterImage` 類別是 Aspose.PSD 用於點陣圖像操作的主要物件。它提供載入、轉換與儲存點陣圖像的方法，同時保留中繼資料。

## 步驟說明

### 步驟 1：定義文件目錄

設定保存來源 PSD 與輸出結果的資料夾。使用絕對路徑或 `System.getProperty("user.dir")` 可避免相對路徑的意外情況。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 步驟 2：指定來源與目標檔案路徑

提供輸入 PSD 的完整檔名以及期望的輸出格式（例如 PNG、JPEG、TIFF）。變更 `destName` 的副檔名會自動選擇相應的編碼器。

```java
String dataDir = "Your Document Directory";
```

### 步驟 3：載入圖像

`Image.load` 方法會偵測檔案格式，並回傳可供點陣操作的具體 `RasterImage` 實例。

`Image` 類別是一個工廠，從磁碟讀取檔案並建立適合進一步處理的記憶體表示。它支援對所有 30+ 支援類型的自動格式偵測。

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### 步驟 4：快取圖像資料（可選但建議）

呼叫 `image.cacheData()` 會將像素資料存入記憶體，顯著加速後續的轉換，尤其是對於大型 PSD 檔案，否則會觸發重複的磁碟 I/O。

`cacheData()` 方法強制圖像完整載入至 RAM，減少在密集運算期間的延遲載入開銷。

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### 步驟 5：旋轉圖像

以三個參數呼叫 `rotate`：旋轉角度（float）、是否展開畫布的旗標，以及新露出角落的背景顏色。

`rotate` 方法會圍繞圖像中心旋轉，必要時放大畫布以容納旋轉後的邊界。背景 `Color` 會填滿所有空白區域，避免出現透明或黑色角落。

- **20f** – 以度數表示的旋轉角度（float）。可更改此值以設定任意角度，例如 `-45f` 代表順時針旋轉。  
- **true** – 在擴展畫布時保持原始寬高比。  
- **Color.getRed()** – 填充空白角落的背景顏色；可依需求替換為 `Color.getWhite()` 或其他自訂顏色。

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### 步驟 6：儲存結果

選擇編碼器（JPEG、PNG 等），然後呼叫 `save`。`JpegOptions` 讓您調整品質，`PngOptions` 則提供無損輸出。

`save` 方法使用指定的選項物件將轉換後的圖像寫入磁碟，確保壓縮等級與色深依需求被保留。

```java
image.rotate(20f, true, Color.getRed());
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|-------|-----|
| **旋轉後出現空白角落** | 未提供背景顏色 | 傳入 `Color`（例如 `Color.getWhite()`）至 `rotate`。 |
| **大型 PSD 記憶體不足錯誤** | 圖像未快取 | 在處理前呼叫 `image.cacheData()`。 |
| **角度方向不正確** | 正負角度混淆 | 使用負值進行順時針旋轉（或依座標系統相反）。 |
| **變更未儲存** | 忘記呼叫 `save` | 確保在旋轉後執行 `image.save(...)`。 |

## 常見問答

**Q: 可以使用 Aspose.PSD for Java 旋轉帶透明度的圖像嗎？**  
A: 可以。此函式庫會保留 Alpha 通道；若不提供不透明的背景顏色，角落會保持透明。

**Q: 支援旋轉的圖像檔案格式有任何限制嗎？**  
A: 沒有。Aspose.PSD 支援 PSD、JPEG、PNG、TIFF、GIF、BMP、JPEG2000、WMF、EMF，以及超過 30 種其他格式。

**Q: 可以使用負角度旋轉圖像嗎？**  
A: 當然可以。傳入負的 float（例如 `-30f`）即可實現順時針旋轉。

**Q: Aspose.PSD 在旋轉時提供即時圖像預覽嗎？**  
A: 此 API 僅為伺服器端使用。若需即時預覽，可在 Swing、JavaFX 等 UI 框架中渲染旋轉後的位圖並刷新畫面。

**Q: 有 Aspose.PSD 的社群論壇可以求助嗎？**  
A: 有，請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 提問或分享使用經驗。

**最後更新：** 2026-05-19  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## 相關教學

- [在 Aspose.PSD for Java 中使用雙三次重採樣器的高品質圖像縮放](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Java 圖像縮放 - 在 Aspose.PSD for Java 中使用 Resize Type 列舉](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [使用 Aspose.PSD 的 Java 模糊圖像 – 添加模糊效果](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}