---
date: 2025-12-08
description: 了解如何在 Java 中使用 Aspose.PSD 按特定角度旋轉圖像。本指南涵蓋 Java 圖像旋轉、特定角度旋轉圖像、背景處理等內容。
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 以特定角度旋轉圖片
url: /zh-hant/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 以特定角度旋轉圖像

## Introduction

如果您需要在 Java 應用程式中以程式方式 **如何旋轉圖像**，Aspose.PSD for Java 提供乾淨且高效能的 API，負責繁重的工作。無論您是在建構照片編輯器、產生縮圖，或是為 Web 服務準備資產，將圖像以精確角度旋轉都是常見需求。在本教學中，我們將從載入 PSD 檔案到儲存旋轉後的結果，完整示範整個流程，並強調快取與背景處理等最佳實踐。

> **快速解答**  
> - **哪個函式庫最適合在 Java 中旋轉圖像？** Aspose.PSD for Java.  
> - **我可以以任意角度旋轉嗎？** 可以，`rotate` 方法接受 `float` 型別的角度（正值或負值）。  
> - **開發時需要授權嗎？** 免費試用可用於測試；正式環境需購買授權。  
> - **支援哪些圖像格式？** PSD、JPEG、PNG、TIFF、GIF、BMP 等多種格式。  
> - **如何設定空白區域的背景顏色？** 將 `Color` 例項傳遞給 `rotate` 方法。

## What is Image Rotation in Java?

什麼是 Java 中的圖像旋轉？

圖像旋轉是指將像素矩陣繞著一個樞紐點（通常是中心）以指定角度旋轉。在 Java 中，您可以使用 `Graphics2D` 手動實作，但 Aspose.PSD 抽象化了數學運算，處理不同的色深，且在處理 PSD 檔案時保留圖層資訊。

## Why Use Aspose.PSD for Rotating Images?

為什麼使用 Aspose.PSD 來旋轉圖像？

- **精確度：** 可以任意小數度數旋轉，且不會失真。  
- **效能：** 內建快取 (`image.cacheData()`) 可加速大型檔案。  
- **背景控制：** 可指定背景顏色以填補旋轉後產生的空白。  
- **格式彈性：** 載入 PSD，輸出 JPEG、PNG 或任何支援的格式。

## Prerequisites

先決條件

1. **Java Development Kit (JDK 8 或更新版本)** – 可運作的 Java IDE 或命令列環境。  
2. **Aspose.PSD for Java** – 從 [Aspose.PSD Java page](https://reference.aspose.com/psd/java/) 下載最新的 JAR。  
3. **範例 PSD 檔案** – 例如 `sample.psd`，放置於程式碼可參照的資料夾中。

## Import Packages

匯入套件

首先，匯入我們需要的類別。無論您選擇的旋轉角度為何，這些匯入皆保持不變。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

逐步指南

### Step 1: Define Your Document Directory

步驟 1：定義文件目錄

設定保存來源 PSD 檔案以及寫入輸出結果的資料夾。

```java
String dataDir = "Your Document Directory";
```

> **專業提示：** 使用絕對路徑或 `System.getProperty("user.dir")` 以避免相對路徑帶來的意外。

### Step 2: Specify Source and Destination File Paths

步驟 2：指定來源與目的檔案路徑

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

您可以將 `destName` 改為任何支援的副檔名（`.png`、`.tiff` 等），以符合輸出需求。

### Step 3: Load the Image

步驟 3：載入圖像

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` 會自動偵測檔案格式，並回傳具體的 `RasterImage` 以進行點陣圖操作。

### Step 4: Cache Image Data (Optional but Recommended)

步驟 4：快取圖像資料（可選但建議）

```java
if (!image.isCached())
{
    image.cacheData();
}
```

快取會將圖像像素存於記憶體中，提升後續轉換的速度——對於大型 PSD 檔案特別有用。

### Step 5: Rotate the Image

步驟 5：旋轉圖像

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – 以度數（float）表示的旋轉角度。變更此值即可旋轉任意角度，例如 `-45f` 代表逆時針。  
- **true** – 在擴展畫布以容納旋轉後圖像時，保持原始長寬比。  
- **Color.getRed()** – 用於填補旋轉後產生的空白角落的背景顏色。可依需求改為 `Color.getWhite()` 或其他自訂顏色。

### Step 6: Save the Result

步驟 6：儲存結果

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` 讓您控制品質、壓縮以及其他 JPEG 專屬設定。若需無損輸出，可改用 `PngOptions`。

## Common Issues and Solutions

常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|-------|-------|-----|
| **旋轉後出現空白角落** | 未提供背景顏色 | 將 `Color`（例如 `Color.getWhite()`）傳遞給 `rotate`。 |
| **大型 PSD 產生記憶體不足錯誤** | 圖像未快取 | 在處理前呼叫 `image.cacheData()`。 |
| **角度方向不正確** | 正負角度混淆 | 使用負值進行順時針旋轉（或依座標系統相反）。 |
| **變更未儲存** | 忘記呼叫 `save` | 確認在旋轉後執行 `image.save(...)`。 |

## Frequently Asked Questions

常見問答

**Q: 我可以使用 Aspose.PSD for Java 旋轉具有透明度的圖像嗎？**  
A: 可以。此函式庫會保留 alpha 通道；若希望角落保持透明，請勿指定不透明的背景顏色。

**Q: 支援旋轉的圖像檔案格式有任何限制嗎？**  
A: 沒有。Aspose.PSD 支援 PSD、JPEG、PNG、TIFF、GIF、BMP、JPEG2000、WMF、EMF 等多種格式。

**Q: 我可以使用負角度旋轉圖像嗎？**  
A: 當然可以。將負的 float 傳遞給 `rotate`（例如 `-30f`）即可順時針旋轉。

**Q: Aspose.PSD 在旋轉時提供即時圖像預覽嗎？**  
A: 此 API 僅為伺服器端。若需即時預覽，請將旋轉後的位圖整合至 UI 框架（Swing、JavaFX）並刷新畫面。

**Q: 有 Aspose.PSD 的社群論壇可以尋求協助嗎？**  
A: 有，請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 提問與分享經驗。

## Conclusion

結論

現在您已了解如何使用 Aspose.PSD for Java 以特定角度 **旋轉圖像** 檔案。透過快取、背景顏色控制與彈性的輸出選項，您可以將精確的旋轉功能整合至任何基於 Java 的圖像工作流程中。

---

**最後更新：** 2025-12-08  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}