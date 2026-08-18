---
date: 2026-03-21
description: 學習如何使用 Aspose.PSD for Java 轉換 PSD 為 PNG 以及裁剪 PSD 檔案。本指南展示在 Java 應用程式中的逐步圖像處理。
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: 如何在裁剪的同時使用 Aspose.PSD for Java 將 PSD 轉換為 PNG
url: /zh-hant/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在使用 Aspose.PSD for Java 時將 psd 轉換為 png 並裁剪

## 簡介
在充滿變化的 Java 開發領域，精通高效的影像處理至關重要。在本教學中，您將學會 **如何將 psd 轉換為 png**，並在同一工作流程中使用功能強大的 Aspose.PSD for Java 函式庫進行裁剪。透過本步驟指南，您將能為 PNG 匯出加入精確的裁剪，讓 Java 應用程式自信地處理 PSD 資產。

## 快速解答
- **此程式碼的功能是什麼？** 載入 PSD，裁剪矩形，並儲存為 PNG。  
- **需要哪個函式庫？** Aspose.PSD for Java（最新版本）。  
- **是否需要授權？** 是，商業授權在正式環境中是必須的。  
- **我可以自訂裁剪區域嗎？** 當然可以——您可以設定所需的 X、Y、寬度與高度。  
- **此方法對大型檔案是否快速？** 是，Aspose.PSD 已針對高效能處理進行最佳化。

## 什麼是 convert psd to png？
將 PSD 轉換為 PNG 意指把具層次的 Photoshop 文件展平成無損的 PNG 圖像。此格式非常適合網頁傳遞、縮圖，或任何需要光柵圖像且不保留原始圖層的情境。

## 為什麼在轉換為 PNG 前要裁剪 PSD？
裁剪可讓您只擷取設計中需要的部分，減少檔案大小並聚焦於相關的視覺內容。這在產生縮圖、UI 資產或為響應式版面配置準備圖像時特別有用。

## 先決條件
在開始本教學之前，請確保您已具備以下條件：
- 具備 Java 程式設計的基本知識。  
- 系統已安裝 Java Development Kit（JDK）。  
- 已下載 Aspose.PSD for Java 函式庫並加入專案。  
- 一個用於實驗的範例 PSD 檔案。

## 匯入套件
在您的 Java 專案中，務必匯入使用 Aspose.PSD 功能所需的套件：
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定專案
先建立一個 Java 專案，並將 Aspose.PSD for Java 函式庫加入專案的 classpath。這樣即可取得所有影像處理相關的類別。

## 步驟 2：載入 PSD 圖像
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*此處我們將來源 PSD 檔案載入至 `RasterImage` 物件，該物件提供基於光柵的操作，例如裁剪。*

## 步驟 3：定義裁剪區域
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*`Rectangle` 定義您想保留的區域。調整 `x`、`y`、`width` 與 `height` 的值以符合您的設計需求。此步驟直接回應「定義裁剪區域」的關鍵字。*

## 步驟 4：裁剪 PSD 圖像
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*呼叫 `crop` 會在記憶體中修改圖像，捨棄指定矩形之外的所有內容。*

## 步驟 5：設定 PNG 匯出選項
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` 讓您控制 PNG 的特定設定，如壓縮等級、顏色類型等。*

## 步驟 6：將裁剪後的圖像儲存為 PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*`save` 方法執行 **convert psd to png** 的操作，同時保留您先前定義的裁剪。*

## 常見問題與技巧
- **矩形尺寸不正確：** 確保寬度與高度不超過原始圖像大小，否則會拋出例外。  
- **大型 PSD 的記憶體使用：** 儲存後釋放 `RasterImage` 物件（`image.dispose()`）以釋放原生資源。  
- **未設定授權：** 若未使用有效授權執行程式，輸出 PNG 會出現浮水印。

## 常見問答
### 我可以使用 Aspose.PSD for Java 裁剪不規則形狀的 PSD 檔案嗎？
可以，Aspose.PSD for Java 允許您自訂裁剪區域，從而將圖像裁剪成各種形狀。

### Aspose.PSD for Java 適合大規模圖像處理任務嗎？
絕對適合！Aspose.PSD 專為高效處理大型圖像而設計，適用於需要大量圖像處理的專案。

### 使用 Aspose.PSD for Java 是否需要授權？
是，商業使用必須擁有有效授權。您可從 [Aspose Purchase](https://purchase.aspose.com/buy) 取得。

### 如何取得 Aspose.PSD for Java 的協助或回報問題？
請前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 尋求協助、分享使用經驗，並回報您遇到的問題。

### 購買前我可以先試用 Aspose.PSD for Java 嗎？
當然可以！您可透過此處的免費試用 [here](https://releases.aspose.com/) 了解函式庫功能。

**最後更新：** 2026-03-21  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}