---
date: 2026-01-01
description: 探索如何在 Java 中使用 Aspose.PSD for Java 裁剪圖像。遵循我們的逐步指南載入 PSD 檔案、裁剪圖像矩形，並將
  PSD 轉換為 JPEG。
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: Crop Image Java：使用 Aspose.PSD 以矩形裁剪圖像
url: /zh-hant/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 裁剪影像 Java：使用 Aspose.PSD 以矩形裁剪影像

## 簡介

操作圖形是 **java image processing** 的日常工作，而 Aspose.PSD for Java 為您提供乾淨且高效能的 API 來處理 PSD 檔案。在本教學中，您將學習如何使用矩形 **裁剪影像**、載入 PSD 檔案，最後將結果轉換為 JPEG——只需幾行 Java 程式碼。

## 快速解答
- **「crop image java」是什麼意思？** 它指的是使用 Java 程式碼將影像裁剪至指定的矩形。  
- **哪個函式庫負責此操作？** Aspose.PSD for Java 提供所需的類別。  
- **測試是否需要授權？** 提供免費試用版；正式環境需購買授權。  
- **我可以將裁剪後的 PSD 轉換為 JPEG 嗎？** 可以——儲存時使用 `JpegOptions`。  
- **實作大約需要多久？** 基本情境通常在 10 分鐘以內。

## 什麼是於 Java 中以矩形裁剪影像？

以矩形裁剪影像是指選取特定區域（由 X、Y、寬度與高度定義），並捨棄該區域之外的所有內容。當您需要聚焦於較大 PSD 文件中的特定區域時，這項操作相當常見。

## 為什麼要使用 Aspose.PSD 來執行此任務？

- **無外部相依性** – 可在純 Java 環境下運作。  
- **支援 PSD、PNG、JPEG 及其他多種格式** – 您可以即時 **將 PSD 轉換為 JPEG**。  
- **高保真度渲染** – 在裁剪過程中保留圖層資訊與色彩描述檔。  

## 先決條件

- 已安裝 Java Development Kit（JDK）。  
- Aspose.PSD for Java 程式庫 – 從 [website](https://releases.aspose.com/psd/java/) 下載。

## 匯入套件

確保在 Java 專案中加入必要的套件，以利用 Aspose.PSD for Java 的功能。請在 Java 檔案的開頭加入以下 import 陳述式：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

現在，我們將此流程分解為多個步驟，指導您如何使用 Aspose.PSD for Java 以矩形裁剪影像。

## 步驟 1：設定文件目錄

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為實際放置 PSD 檔案的路徑。

## 步驟 2：指定來源與目標檔案

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

定義來源 PSD 檔案與目標 JPEG 檔案的路徑。

## 步驟 3：載入並快取影像

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

此處我們將 **PSD 檔案載入** 為 `RasterImage` 實例，並快取其資料以提升效能。

## 步驟 4：建立並定義裁剪矩形

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

建立 `Rectangle` 類別的實例，設定裁剪所需的尺寸。各參數分別代表 **X**、**Y**、**寬度** 與 **高度**。

## 步驟 5：裁剪並儲存影像

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

使用指定的矩形執行裁剪操作，並透過 `JpegOptions` 儲存結果，以 **將 PSD 轉換為 JPEG**。

視需求重複上述步驟，並依實際需求調整參數。

## 常見問題與技巧

- **矩形超出影像範圍** – 確保矩形座標位於來源影像的尺寸內。  
- **記憶體使用** – 完成後呼叫 `rasterImage.dispose()` 釋放本機資源。  
- **品質控制** – 您可以設定 `JpegOptions.setQuality(int)` 以控制輸出 JPEG 的壓縮等級。

## 結論

在本教學中，我們示範了如何使用 Aspose.PSD for Java 以矩形 **crop image java**。依循這些步驟，您即可輕鬆將強大的影像處理功能——載入 PSD 檔案、裁剪特定區域，並將結果轉換為 JPEG——整合至任何 Java 應用程式中。

## 常見問答

### Q1：我可以將 Aspose.PSD for Java 與其他 Java 框架一起使用嗎？

A1：可以，Aspose.PSD for Java 可與各種 Java 框架整合，為您的開發專案提供彈性。

### Q2：是否提供 Aspose.PSD for Java 的免費試用？

A2：可以，您可在此處取得免費試用版 [here](https://releases.aspose.com/).

### Q3：我可以在哪裡取得額外的支援或協助？

A3：請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得社群支援與討論。

### Q4：如何取得 Aspose.PSD for Java 的臨時授權？

A4：您可在此處取得臨時授權 [here](https://purchase.aspose.com/temporary-license/).

### Q5：Aspose.PSD for Java 支援哪些影像格式的裁剪？

A5：Aspose.PSD for Java 支援多種影像格式，包括 PSD、PNG、JPEG 等。

---

**最後更新：** 2026-01-01  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}