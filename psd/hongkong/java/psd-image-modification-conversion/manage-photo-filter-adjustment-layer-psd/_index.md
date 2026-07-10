---
date: 2026-03-28
description: 學習如何使用 Aspose.PSD for Java 建立相片濾鏡圖層並新增調整圖層 PSD 檔案。遵循本指南，即可輕鬆編輯與添加濾鏡。
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: 如何使用 Java 在 PSD 中建立相片濾鏡圖層
url: /zh-hant/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 管理 PSD 中的照片濾鏡調整圖層 - Java

## 簡介
如果您是一位希望在 PSD 檔案中 **建立 photo filter layer** 物件的 Java 開發者，您已經來對地方了。在本教學中，我們將示範如何使用 Aspose.PSD for Java 來編輯既有的 Photo Filter Adjustment Layers，以及新增圖層。完成後，您將清楚知道如何 **建立 photo filter layer**、調整其屬性，甚至以程式方式 **add adjustment layer PSD** 檔案，提升您的平面設計工作流程效率。

## 快速解答
- **哪個函式庫在 Java 中處理 PSD 圖層？** Aspose.PSD for Java  
- **我可以編輯既有的 Photo Filter 圖層嗎？** 可以 – 載入 PSD，定位 `PhotoFilterLayer`，然後修改其屬性。  
- **如何新增一個濾鏡圖層？** 在 `PsdImage` 實例上使用 `addPhotoFilterLayer(Color)`。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。  
- **支援哪個 Java 版本？** JDK 8 以上（建議使用 JDK 11）。

## 什麼是照片濾鏡調整圖層？
照片濾鏡調整圖層是一種非破壞性的效果，會以選定的顏色為整張影像著色，類似於套用相機濾鏡。它存在於獨立的圖層上，讓您可以調整顏色、密度與亮度，而不會改變原始像素。

## 為什麼使用 Aspose.PSD 來建立照片濾鏡圖層？
- **完整控制** PSD 結構，無需 Adobe Photoshop。  
- **跨平台** Java API 可在 Windows、Linux 與 macOS 上執行。  
- **無 COM interop** – 純 Java，適合伺服器端處理。  
- **支援 PSD 1‑8 版**，保留圖層效果與遮色片。

## 先決條件
### 必要軟件
1. **Java Development Kit (JDK)**：確保機器上已安裝相容的 JDK 版本，可從 [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java**：操作 PSD 檔案需要 Aspose.PSD 函式庫，可從 [Aspose releases page](https://releases.aspose.com/psd/java/) 下載。別忘了參考 [Aspose documentation](https://reference.aspose.com/psd/java/) 取得更多資訊。  
3. **IDE（整合開發環境）**：使用 IntelliJ IDEA 或 Eclipse 等 IDE 可讓開發更順暢。

### 了解基礎
熟悉 Java 程式設計並對 PSD 檔案的運作原理有基本認識會很有幫助。若您是第一次在 Java 中使用函式庫，建議先熟悉匯入與使用框架的方式。

## 匯入套件
要開始使用，我們需要從 Aspose.PSD 函式庫匯入必要的類別。以下是您在 Java 檔案開頭需要貼上的簡單匯入語句：
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
只要把它貼到 Java 檔案的最上方，即可開始操作 PSD 影像！

## 編輯現有的照片濾鏡圖層
### 步驟 1：設定資料目錄
首先，您需要定義存放 PSD 檔案的目錄。將 `"Your Document Directory"` 替換為實際路徑，讓檔案組織更有條理：
```java
String dataDir = "Your Document Directory";
```

### 步驟 2：載入 PSD 檔案
接著，載入您想編輯的 PSD 檔案。請確認 `PhotoFilterAdjustmentLayer.psd` 已存在於上述目錄中：
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### 步驟 3：初始化影像物件
利用 Aspose 內建功能，我們將影像載入專案：
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 步驟 4：遍歷圖層
接下來，我們會檢查 PSD 檔案中的所有圖層，目標是找到 `PhotoFilterLayer`：
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### 步驟 5：自訂照片濾鏡圖層
這裡就是魔法發生的地方！您可以修改 `Color` 與 `Density`。例如，我們可以將顏色設為鮮豔的紅色，並調整密度：
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### 步驟 6：儲存編輯後的 PSD 檔案
最後，將變更儲存為新的 PSD 檔案：
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
您已成功編輯 PSD 檔案中的 Photo Filter Adjustment Layer。

## 新增照片濾鏡圖層
### 步驟 1：設定目錄路徑
同前，我們先定義資料目錄：
```java
String dataDir = "Your Document Directory";
```

### 步驟 2：載入來源檔案
本例中，我們載入另一個 PSD 檔案，準備 **add adjustment layer PSD**：
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### 步驟 3：再次初始化影像物件
必須建立新的 `PsdImage` 實例，於是載入檔案：
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 步驟 4：新增照片濾鏡圖層
現在，我們可以以自訂顏色新增 Photo Filter 圖層。操作方式如下：
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### 步驟 5：儲存新 PSD 檔案
再次將變更儲存。以下程式碼即完成此步驟：
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
您已成功在 PSD 檔案中加入新的照片濾鏡圖層。

## 常見問題與解決方案
- **載入影像時出現 `ClassCastException`** – 請確認載入的檔案確實為 PSD；其他格式需使用不同的類別。  
- **顏色值顯示不正確** – 請使用 `Color.fromArgb(alpha, red, green, blue)`，每個組件的取值範圍為 0‑255。  
- **找不到圖層** – 請驗證來源 PSD 確實包含 `PhotoFilterLayer`。可使用 `im.getLayers().length` 進行除錯。

## 常見問答
### 什麼是 Aspose.PSD？
Aspose.PSD 是一套 .NET 與 Java 函式庫，用於建立、編輯與轉換 PSD 檔案。

### 我可以免費試用 Aspose.PSD 嗎？
可以，Aspose 提供免費試用版。請前往 [here](https://releases.aspose.com/) 下載。

### 哪裡可以找到文件？
完整文件可於 [Aspose's reference page](https://reference.aspose.com/psd/java/) 取得。

### 如何購買 Aspose.PSD？
您可透過 [this link](https://purchase.aspose.com/buy) 購買軟體。

### 是否提供 Aspose.PSD 的支援？
當然！您可在 Aspose 支援論壇 [here](https://forum.aspose.com/c/psd/34) 取得協助。

**最後更新：** 2026-03-28  
**測試環境：** Aspose.PSD for Java 24.11（截至 2026 年的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}