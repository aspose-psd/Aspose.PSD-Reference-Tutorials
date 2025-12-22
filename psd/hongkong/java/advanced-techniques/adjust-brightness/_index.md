---
date: 2025-12-19
description: 學習如何使用 Aspose.PSD for Java 調整圖像的亮度。本 Java 圖像處理教學提供逐步指引。
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 調整圖像亮度
url: /zh-hant/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 調整影像亮度

## 介紹

如果你想 **了解如何在 Java 程式碼中直接調整圖片的亮度**，你來對地方了。亮度微調是平面設計師、攝影師以及任何建立影像處理流程的人常見的工作。在本 **java 影像操作教學** 中，我們將完整示範工作流程——載入 PSD/TIFF、套用亮度偏移，並儲存結果——使用 Aspose.PSD for Java 函式庫。

## 快速答覆
- **哪個函式庫負責亮度調整？** Aspose.PSD for Java  
- **哪個方法變更亮度？** `RasterImage.adjustBrightness()`  
- **可以同時處理 PSD 與 TIFF 檔案嗎？** 可以，API 同時支援兩種格式。  
- **正式環境需要授權嗎？** 非評估用途需購買商業授權。  
- **實作大約需要多久？** 基本調整通常在 10 分鐘以內完成。

## 什麼是影像亮度調整？

影像亮度調整會改變影像中每個像素的整體明亮度。提升亮度會讓暗部變亮，降低亮度則會使整張圖片變暗。此操作常用於校正曝光不足的照片、為列印做資產準備，或在應用程式中製作視覺效果。

## 為什麼選擇 Aspose.PSD for Java？

- **完整格式支援** – PSD、TIFF、JPEG、PNG 等多種格式。  
- **無外部原生相依** – 純 Java 實作，易於整合。  
- **高效能快取** – 點陣資料可快取，以加速重複操作。  
- **豐富 API** – 提供顏色校正、圖層、遮色片及其他進階編輯方法。

## 前置條件

在開始教學之前，請確保已具備以下前置條件：

- Aspose.PSD for Java 函式庫：從 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 下載並安裝函式庫。

## 匯入套件

首先，將必要的套件匯入你的 Java 專案。以下範例使用的匯入語句如下：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

現在，讓我們把調整影像亮度的流程拆解成簡單的步驟：

## 使用 Aspose.PSD 調整亮度的方法

### 步驟 1：載入影像

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

在此步驟中，我們載入目標影像，並將其轉型為 `RasterImage` 以便後續處理。

### 步驟 2：調整亮度

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

此處使用 `adjustBrightness` 方法修改影像的亮度。範例中將亮度降低 50 單位，你可以依需求自行調整此數值。

### 步驟 3：設定 TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

為儲存調整後的影像設定 `TiffOptions`。請依實際需求調整 `bitsPerSample` 與 `photometric` 屬性。

### 步驟 4：儲存結果影像

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

最後，使用先前設定好的 `TiffOptions` 將修改後的影像寫入檔案。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **`ClassCastException` 在轉型 Image 時發生** | 檔案不是點陣圖（例如向量 PSD）。 | 檢查來源檔案格式，或在轉型前使用 `image instanceof RasterImage` 進行判斷。 |
| **亮度變更沒有作用** | 調整前未先快取影像資料。 | 如步驟 1 所示，呼叫 `rasterImage.cacheData()`。 |
| **儲存的檔案顯示損毀** | `TiffOptions` 設定不正確。 | 確認 `bitsPerSample` 與來源影像深度相符（通常為每通道 8 位元）。 |

## 常見問答

### Q1：我可以在 PSD 以外的其他影像格式調整亮度嗎？

A1：可以，Aspose.PSD for Java 支援 JPEG、PNG、TIFF 等多種影像格式。

### Q2：在影像調整過程中發生錯誤，我該如何處理？

A2：可以使用 try‑catch 區塊捕捉例外，進行錯誤處理。

### Q3：亮度調整的範圍有沒有上限？

A3：調整範圍取決於影像內容與格式，但 Aspose.PSD 提供彈性讓你自行客製化。

### Q4：我可以在商業專案中使用 Aspose.PSD for Java 嗎？

A4：可以，Aspose.PSD for Java 為商業授權函式庫，可從 [here](https://purchase.aspose.com/buy) 取得授權。

### Q5：有提供免費試用版嗎？

A5：有，請從 [here](https://releases.aspose.com/) 下載免費試用版。

### Q6：`adjustBrightness` 方法會影響圖層的可見性嗎？

A6：此方法作用於點陣化的合成影像，圖層的可見性會在點陣化過程中被考慮。

### Q7：我可以串接多個調整（例如對比度、飽和度）一起使用嗎？

A7：當然可以。調整完亮度後，你可以在同一個 `RasterImage` 實例上呼叫 `adjustContrast`、`adjustSaturation` 等方法。

---

**最後更新日期：** 2025-12-19  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}