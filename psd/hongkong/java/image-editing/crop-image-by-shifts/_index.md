---
date: 2026-07-03
description: 了解如何使用 Aspose.PSD for Java 於 Java 裁切影像。本 step‑by‑step 影像裁切教學涵蓋 loading
  PSD files、setting shift values 以及 saving the result。
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: 依位移裁切影像
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD 的 Java 依位移裁切影像
url: /zh-hant/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 以位移裁剪 Java 圖像（使用 Aspose.PSD）

## 介紹

在 Java 圖像處理中，**crop image java** 是準備圖形、縮圖或 UI 資產的常見需求。Aspose.PSD for Java 透過提供一個簡單的 `crop` 方法，使此工作變得直觀，且可作用於任何支援的點陣格式。在本教學中，您將學習如何載入 PSD 檔案、定義左、右、上、下的位移值、套用裁剪，並儲存結果——全部不需自行撰寫像素操作程式碼。

## 快速解答
- **什麼程式庫負責裁剪？** Aspose.PSD for Java 提供內建的 `crop` 方法。  
- **我需要授權嗎？** 臨時授權可用於評估；正式環境需購買完整授權。  
- **支援的格式？** 超過 30 種點陣格式，包括 PSD、JPEG、PNG、BMP 與 TIFF。  
- **最大檔案大小？** 可處理高達 2 GB 的檔案，且不會一次將整張圖像載入記憶體。  
- **需要多少行程式碼？** 只需五個邏輯步驟——載入、快取、定義位移、裁剪與儲存。

## 什麼是 crop image java？
`crop image java` 指在 Java 應用程式中修剪點陣圖的操作。使用 Aspose.PSD 時，該操作由 `crop` 方法執行，該方法接受圖像四邊的位移值，並回傳新的圖像實例。

## 為何使用 Aspose.PSD 進行圖像裁剪？
Aspose.PSD 支援 **30+** 種圖像格式，且能在使用低於 150 MB 記憶體的情況下處理多百頁的 PSD 檔案，這歸功於其延遲載入架構。此程式庫亦保證像素級精確的結果，保留圖層、遮罩與色彩配置檔——這是許多通用圖像程式庫無法保證的。

## 前置條件

### Java 開發工具包 (JDK)

確保您的系統已安裝最新版本的 JDK。您可從 [此處](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。

### Aspose.PSD for Java 程式庫

首先，您需要取得 Aspose.PSD for Java 程式庫。前往 [下載頁面](https://releases.aspose.com/psd/java/) 下載最新版本。

### 整合開發環境 (IDE)

選擇您喜愛的 Java IDE，例如 Eclipse 或 IntelliJ，以獲得順暢的編程體驗。

## 如何裁剪 crop image java？

載入來源檔案、為每一側定義像素位移，然後呼叫 `crop` 方法——整個工作流程僅需五行簡潔程式碼。`crop` 操作會產生只包含您指定區域的新圖像，原始檔案保持不變。

### 步驟 1：載入圖像

`Image` 是 Aspose.PSD 中所有圖像類型的基礎類別。  
`RasterImage` 代表點陣圖，並提供裁剪功能。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 步驟 2：快取圖像資料

`cacheData()` 會將圖像資料載入記憶體，以加快處理速度。  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### 步驟 3：定義位移值

以像素為單位指定圖像四側（左、上、右、下）的位移值。  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### 步驟 4：套用裁剪

`crop(left, right, top, bottom)` 會依照每側指定的像素位移值裁剪圖像。  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### 步驟 5：儲存結果

`JpegOptions` 定義 JPEG 編碼設定，例如品質與色彩配置檔。  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

恭喜！您已成功使用 Aspose.PSD for Java 裁剪圖像。

## 常見問題與解決方案

- **圖像未變化：** 請確認位移值為正且未超過原始尺寸。  
- **大型檔案發生 OutOfMemoryError：** 如步驟 2 所示啟用快取；這會讓 Aspose.PSD 使用暫存檔而非將整張圖像保留在記憶體中。  
- **裁剪後顏色偏移：** 若需精確的顏色保真度，請在儲存時呼叫 `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` 以保留色彩配置檔。

## 常見問答

**Q: Aspose.PSD 是否相容所有圖像格式？**  
A: 是的，Aspose.PSD 支援超過 30 種點陣格式，包括 PSD、JPEG、PNG、BMP、TIFF 與 GIF，確保廣泛相容性。

**Q: 我可以對同一圖像執行多次裁剪嗎？**  
A: 當然可以。每次呼叫 `crop` 後都會得到新的圖像物件，您可以依需求再次裁剪。

**Q: 有 Aspose.PSD 的社群論壇嗎？**  
A: 有，您可在 [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) 獲得支援並與社群互動。

**Q: 如何取得 Aspose.PSD 的臨時授權？**  
A: 前往 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 有示範專案展示 Aspose.PSD 功能嗎？**  
A: 請參閱 [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/) 的文件與範例。

---

**最後更新：** 2026-07-03  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## 相關教學

- [使用矩形裁剪圖像（Aspose.PSD for Java）](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - 使用 Aspose.PSD for Java 展開與裁剪圖像](/psd/java/image-editing/expand-and-crop-images/)
- [Resize Image Java - 在 Aspose.PSD for Java 中使用 Resize Type 列舉](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}