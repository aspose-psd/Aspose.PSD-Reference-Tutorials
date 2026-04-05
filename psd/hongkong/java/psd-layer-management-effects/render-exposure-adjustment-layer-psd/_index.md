---
date: 2026-04-05
description: 學習如何使用 Aspose.PSD for Java 在 PSD 檔案中渲染曝光調整圖層。提供逐步指南與程式碼範例，說明如何修改與新增曝光圖層。
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: 在 PSD 檔案中渲染曝光調整圖層 - Java
second_title: Aspose.PSD Java API
title: 在 PSD 檔案中渲染曝光調整圖層 - Java
url: /zh-hant/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 檔案中渲染曝光調整圖層 - Java

## 介紹

您是否正在處理 Photoshop PSD 檔案，且需要以程式方式 **渲染曝光調整圖層**？無論是微調現有圖層或是新增圖層，Aspose.PSD for Java 都提供了一套強大且直觀的解決方案。在本指南中，我們將示範如何使用 Aspose.PSD for Java 來渲染與修改 PSD 檔案中的曝光調整圖層。完成本教學後，您將能在既有圖層中調整曝光設定，並向 PSD 檔案中加入新的曝光調整圖層。讓我們立即開始吧！

## 快速答覆
- **需要哪個函式庫？** Aspose.PSD for Java
- **可以編輯既有的曝光圖層嗎？** 可以，您可以變更曝光、偏移與 gamma 校正。
- **如何新增曝光調整圖層？** 在 `PsdImage` 實例上使用 `addExposureAdjustmentLayer()`。
- **支援 PNG 匯出嗎？** 完全支援 – 使用 `PngOptions` 將結果儲存為 PNG。
- **正式環境需要授權嗎？** 生產環境必須使用商業授權；亦提供免費試用版。

## 什麼是渲染曝光調整圖層？

曝光調整圖層是一種非破壞性的 Photoshop 圖層，會 **變更底層影像的亮度、偏移與 gamma**。渲染此圖層即是套用這些設定，使視覺結果呈現調整後的樣子，之後您可以將其匯出為 PNG 等格式。

## 為什麼使用 Aspose.PSD for Java 來渲染曝光調整圖層？

- **完整控制** – 在不開啟 Photoshop 的情況下操作圖層屬性。
- **批次處理** – 可自動對大量檔案執行調整。
- **跨平台** – 只要有 JDK，即可在任何系統上執行。
- **保留 PSD 結構** – 圖層仍保持可編輯，方便日後再修改。

## 前置需求

1. **Java Development Kit (JDK)** – 至少 JDK 8。
2. **Aspose.PSD for Java** – 從 [here](https://releases.aspose.com/psd/java/) 下載。
3. **基本的 Java 知識** – 您應熟悉標準的 Java 語法。
4. **IDE 或文字編輯器** – 如 IntelliJ IDEA、Eclipse、VS Code，或任何您慣用的編輯器。

## 匯入套件

首先，匯入所需的 Aspose.PSD 類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 如何渲染曝光調整圖層 – 步驟說明

### 步驟 1：載入 PSD 檔案

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

將 `"Your Document Directory"` 替換為存放 **您的 PSD 檔案** 的資料夾路徑。`Image.load()` 方法會回傳一個 `PsdImage` 物件，讓您完整存取文件的圖層。

### 步驟 2：編輯既有的曝光調整圖層

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

此 **迴圈** 會遍歷每一個圖層，尋找 `ExposureLayer`，並更新其三個關鍵參數。這就是 **渲染曝光調整圖層** 並套用自訂值的核心程式碼。

### 步驟 3：儲存已修改的 PSD 檔案

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

修改後的 PSD 仍保留所有原始圖層，但曝光調整已反映新設定。

### 步驟 4：將結果匯出為 PNG

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

使用 `PngOptions` 搭配 `TruecolorWithAlpha` 可確保匯出的 PNG 保留完整的色深與 PSD 中的任何 **透明度**。

### 步驟 5：新增曝光調整圖層

若需在既有文件中 **新增曝光調整圖層**，請使用以下程式碼：

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

`addExposureAdjustmentLayer` 方法會建立一個全新的調整圖層，並設定指定的曝光、偏移與 gamma 值，之後您可以像之前一樣渲染並匯出。

## 常見問題與技巧

- **找不到圖層** – 請確認 PSD 確實包含 `ExposureLayer`。如範例所示使用 `instanceof ExposureLayer` 可避免 `ClassCastException`。
- **檔案路徑錯誤** – 請使用絕對路徑，或確保 `dataDir` 以檔案分隔符 (`/` 或 `\`) 結尾。
- **授權例外** – 未載入有效授權時，輸出會加上浮水印。請在程式碼開頭註冊授權 (`License license = new License(); license.setLicense("Aspose.PSD.lic");`)。

## 常見問答

### 什麼是 Aspose.PSD for Java？

Aspose.PSD for Java 是一套可讓您以 Java 程式語言建立、編輯與轉換 PSD 檔案的函式庫，提供完整的 Photoshop 文件操作功能。

### 我可以使用 Aspose.PSD for Java 操作其他類型的圖層嗎？

可以，Aspose.PSD for Java 支援多種圖層類型，包括文字圖層、調整圖層與影像圖層，讓您對 PSD 檔案進行廣泛的操作。

### 如何開始使用 Aspose.PSD for Java？

您可以從 [website](https://releases.aspose.com/psd/java/) 下載函式庫，並參考 [documentation](https://reference.aspose.com/psd/java/) 取得詳細教學與範例。

### 是否提供 Aspose.PSD for Java 的免費試用？

有的，您可以在此處下載免費試用版 [here](https://releases.aspose.com/)。

### 如何取得 Aspose.PSD for Java 的技術支援？

您可前往 [Aspose support forum](https://forum.aspose.com/c/psd/34) 提問，社群成員會協助您解決問題。

**其他問題**

**Q: 我可以批次處理多個 PSD 檔案嗎？**  
A: 當然可以。將載入、編輯與儲存的程式碼包在迴圈中，對檔案路徑清單逐一執行。

**Q: 新增曝光圖層時，函式庫會保留圖層層級結構嗎？**  
A: 會的。新圖層會被加入至現有圖層之上，保持原有的層級結構。

**Q: 除了 PNG，還能匯出哪些影像格式？**  
A: Aspose.PSD 支援 JPEG、BMP、TIFF 等多種格式，皆可透過對應的 `*Options` 類別設定。

---

**最後更新：** 2026-04-05  
**測試環境：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}