---
date: 2026-04-08
description: 學習如何使用 Aspose.PSD for Java 以及 Aspose 臨時授權，將 PSD 匯出為 PNG 並建立新的 PSD 圖層。本分步教學涵蓋
  PSD 圖像操作及設定圖層位置。
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: 新增普通圖層至 PSD
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 匯出 PSD 為 PNG 並新增一般圖層 – Aspose 臨時授權
url: /zh-hant/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 匯出為 PNG 並使用 Aspose.PSD for Java 新增常規圖層

## 簡介

在本 **aspose psd tutorial** 中，您將學習如何 **export PSD to PNG** 同時在同一檔案內 **creating a new regular layer**，並 **using an aspose temporary license** 進行開發。無論您是需要產生適合網頁的縮圖、為設計流程準備資產，或只是想實驗 **psd image manipulation**，Aspose.PSD for Java 都能提供完整的程式化控制。我們將逐步說明每個步驟——從載入來源檔案到同時儲存更新後的 PSD 以及 PNG 副本——讓您立即開始操作 PSD 圖層。

## 快速解答
- **我可以一次呼叫就 export PSD to PNG 嗎？** 是的，加入圖層後，您可以使用 `PngOptions` 呼叫 `save`。
- **我需要開發用的授權嗎？** 臨時授權可用於測試；正式環境則需要完整授權。
- **支援哪個 Java 版本？** Aspose.PSD 可在 Java 8 及以上版本運行。
- **圖層定位是以像素為單位嗎？** 是的，您可使用 **set layer position** 方法以像素設定 left、top、right、bottom 座標。
- **PNG 會保留圖層透明度嗎？** PNG 會包含所有可見圖層合併後的結果。

## 為何使用 aspose 臨時授權？

使用 **aspose temporary license** 可讓您在不受功能限制的情況下評估 Aspose.PSD 的完整功能。它會移除評估水印，解鎖所有 API——包括 **create new psd layer** 物件的功能，並讓您在類似正式環境中測試程式碼，之後再購買永久授權。

## 先決條件

在開始之前，請確保您已具備以下條件：

- **Java 開發環境** – 已安裝 JDK 8 以上及建置工具（Maven/Gradle）。
- **Aspose.PSD for Java** – 從官方網站[此處](https://releases.aspose.com/psd/java/)下載最新 JAR。
- **範例 PSD 檔案** – 本教學將使用 `OneLayer.psd`。

## 匯入套件

在您的 Java 類別中加入必要的匯入。這些類別提供 **psd image manipulation** 與圖層處理的核心功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 什麼是「set layer position」以及為何重要？

當您新增圖層時，需要定義它在畫布上的位置。`setLeft`、`setTop`、`setRight` 與 `setBottom` 方法會以像素座標 **set layer position**。正確的定位可確保圖形精確對齊，這對於合成 UI 資產或製作列印就緒檔案等工作至關重要。

## 逐步指南

### 步驟 1：載入 PSD 檔案

首先，載入您要修改的現有 PSD。這會產生可供操作的 `PsdImage` 物件。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### 步驟 2：準備像素資料與矩形區域

我們將建立兩個像素緩衝區 (`int[]`) 並定義新圖層要繪製的矩形區域。這是 **creating a new psd layer** 的基礎。

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### 步驟 3：初始化圖層資料

以預設的 ARGB 值填滿像素緩衝區。數值 `-10000000` 代表半透明的深色調。

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### 步驟 4：新增常規圖層（操作 PSD 圖層）

現在，我們 **add regular layers** 到 PSD 圖像，並使用 left、top、right、bottom 屬性 **set layer position**。此示範說明如何以程式方式 **manipulate PSD layers**。

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### 步驟 5：匯出 PSD 為 PNG 並儲存更新後的 PSD

圖層就緒後，儲存修改後的文件。首先，我們將結果匯出為 PNG（**export psd to png** 步驟），接著將新增圖層的 PSD 持久化。

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **專業提示：** 若僅需 PNG，您可省略 PSD 的 `save` 呼叫，直接使用 `PngOptions` 呼叫 `save`。

## 常見問題與疑難排解

| 症狀 | 可能原因 | 解決方案 |
|------|----------|----------|
| PNG 顯示空白 | 圖層不可見或完全透明 | 請確保設定非透明的像素值，或呼叫 `layer.setVisible(true)`。 |
| `ArrayIndexOutOfBoundsException` | 矩形大小與像素陣列長度不匹配 | 請確認 `rect.width * rect.height == dataArray.length`。 |
| 執行時發生 LicenseException | 未載入有效授權 | 在呼叫任何 API 方法前，先載入臨時或永久授權。 |

## 常見問答

**Q: Aspose.PSD 是否相容於 Java 8？**  
A: 是，Aspose.PSD 支援 Java 8 及更高版本。

**Q: 我可以對新增的圖層套用變換（旋轉、縮放）嗎？**  
A: 當然可以！`Layer` 類別提供 `rotate`、`scale`、`translate` 等方法，以完整控制變換。

**Q: 我可以在哪裡找到更多 Aspose.PSD 文件？**  
A: 詳細的 API 文件可於[此處](https://reference.aspose.com/psd/java/)取得。

**Q: 我如何取得 Aspose.PSD 的臨時授權？**  
A: 前往臨時授權頁面[此處](https://purchase.aspose.com/temporary-license/)。

**Q: 有 Aspose.PSD 的社群論壇可供支援嗎？**  
A: 有，請在 Aspose 論壇[此處](https://forum.aspose.com/c/psd/34)加入討論。

## 結論

您現在已學會如何使用 Aspose.PSD for Java **export PSD to PNG** 並 **adding new regular layers**，同時了解 **aspose temporary license** 如何讓您無限制地試用此工作流程。本教學展示了核心的 **psd image manipulation** 功能：載入檔案、建立圖層、填充像素資料，以及匯出最終合成。歡迎嘗試不同的矩形尺寸、像素顏色或圖層效果，以符合您專案的需求。

---

**最後更新：** 2026-04-08  
**測試版本：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}