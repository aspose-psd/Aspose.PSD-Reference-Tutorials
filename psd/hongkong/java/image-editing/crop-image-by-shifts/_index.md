---
date: 2026-01-01
description: 掌握 Java 圖像處理，學習如何使用 Aspose.PSD for Java 裁剪圖像。全面的教學，實現無縫圖像操作。
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: Java 圖像處理 – 使用 Aspose.PSD 以位移方式裁剪圖像
url: /zh-hant/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像處理 – 以位移裁剪圖像 (Aspose.PSD)

## 介紹

如果你正在從事 **java image processing**，很快就會發現精確裁剪是任何圖形工作流程的基礎構件。無論是要裁剪邊框、移除不需要的背景，或是為網路傳遞準備資產，了解 **how to crop image** 的程式寫法都能節省大量手動時間。在本教學中，我們將示範如何透過指定每一側的位移值來裁剪點陣圖，使用功能強大的 **Aspose.PSD for Java** 函式庫。完成後，你將能自信地 **use the crop method**，甚至 **optimize image cropping** 以提升效能。

## 快速解答
- **What library handles java image processing?** Aspose.PSD for Java  
- **Which method crops a raster image?** `RasterImage.crop(left, right, top, bottom)`  
- **Do I need to cache data first?** Yes – caching improves speed for large PSD files  
- **Can I set custom cropping margins?** Absolutely – specify left, right, top, and bottom shifts  
- **What output formats are supported?** JPEG, PNG, BMP, and many more via `ImageOptions`

## 什麼是 java 圖像處理？
Java 圖像處理指的是使用基於 Java 的 API 來操作點陣圖與向量圖形。常見任務包括調整尺寸、套用濾鏡、格式轉換，以及 **image cropping margins** 的調整——這些都可以在伺服器端或桌面應用程式中自動化執行。

## 為何在 java 圖像處理中使用 Aspose.PSD？
Aspose.PSD 提供純 Java 解決方案，能完整解析 Photoshop 相容的 PSD 檔案、圖層、通道與遮色片。它不需要本機函式庫、跨平台運作，且提供直觀的 **crop raster image** API，能輕鬆整合至現有的 Java 專案。

## 前置條件

- **Java Development Kit (JDK)** – 從 [here](https://www.oracle.com/java/technologies/javase-downloads.html) 下載最新版本。  
- **Aspose.PSD for Java Library** – 從 [download page](https://releases.aspose.com/psd/java/) 取得最新發行版。  
- **Integrated Development Environment (IDE)** – Eclipse、IntelliJ IDEA，或任何你慣用的編輯器。

## 匯入套件

在你的 Java 專案中，匯入必要的類別以開始裁剪流程：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步驟指南

### 步驟 1：載入圖像 (how to crop image)

首先，將來源 PSD 檔案載入為 `RasterImage` 實例。這樣即可直接存取像素層級的資料。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### 步驟 2：快取圖像資料 (optimize image cropping)

將圖像資料快取至記憶體，可減少 I/O 開銷，特別是在執行多次裁剪等操作時。

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### 步驟 3：定義裁剪邊距 (image cropping margins)

指定每一側要裁減多少像素。依需求調整這些值，以符合目標的 **image cropping margins**。

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### 步驟 4：套用裁剪 (use crop method)

呼叫 `crop` 方法並傳入位移值。此 **crop raster image** 操作會直接修改底層點陣圖。

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### 步驟 5：儲存結果 (how to crop image to a new format)

最後，將裁剪後的圖像寫入磁碟。本例使用 JPEG 格式，但任何 Aspose.PSD 支援的格式皆可使用。

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

恭喜！你已成功使用 Aspose.PSD for Java **cropped an image by shifts**，這是任何 **java image processing** 工具箱中的核心技能。

## 常見問題與解決方案

| Issue | Solution |
|-------|----------|
| **`OutOfMemoryError` on large PSD files** | 確保在第 2 步呼叫 `cacheData()`，並考慮增大 JVM 堆積大小（`-Xmx`）。 |
| **Unexpected transparent borders** | 檢查你的位移值是否正確反映所需的邊距；負值會導致擴展而非裁減。 |
| **Saving in the wrong format** | 使用適當的 `ImageOptions` 子類別（例如 `PngOptions`）來呼叫 `save`。 |

## 常見問答

**Q: Is Aspose.PSD compatible with all image formats?**  
A: 是的，Aspose.PSD 支援廣泛的點陣與向量格式，確保在各種專案中的彈性運用。

**Q: Can I apply multiple cropping operations to the same image?**  
A: 當然可以。你可以多次呼叫 `crop`，每次都會基於圖像當前的狀態執行。

**Q: Is there a community forum for Aspose.PSD support?**  
A: 有，您可以在 [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) 取得支援並與社群互動。

**Q: How can I obtain a temporary license for Aspose.PSD?**  
A: 請前往 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: Are there any sample projects showcasing Aspose.PSD functionalities?**  
A: 請參考 [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/) 中的說明與範例。

## 結論

本指南說明了如何透過指定位移值來 **crop raster image**，這項技巧對於精細的 **java image processing** 至關重要。現在，你已具備將裁剪整合至更大工作流程的堅實基礎，無論是為網站準備資產、產生縮圖，或是清理掃描文件，都能得心應手。

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}