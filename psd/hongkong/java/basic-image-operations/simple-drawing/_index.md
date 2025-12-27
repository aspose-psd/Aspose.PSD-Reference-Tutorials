---
date: 2025-12-27
description: 學習如何在 PSD 檔案中使用 Aspose.PSD for Java 繪製紅色矩形及其他形狀。本分步指南涵蓋建立文件、添加圖層以及使用程式碼範例進行繪圖。
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 繪製紅色矩形
url: /zh-hant/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 繪製紅色矩形

## 介紹

歡迎閱讀本步驟指南，了解如何使用 Aspose.PSD for Java **繪製紅色矩形**！本教學將帶您建立新的 PSD 文件、加入圖層，並以自訂顏色繪製圖形。無論是自動化圖形資產或建構設計工具的後端，本指南都提供了必要的基礎構件。

## 快速回答
- **建立 PSD 檔的主要類別是什麼？** `PsdImage`
- **哪個方法可清除圖層的背景顏色？** `Graphics.clear(Color)`
- **如何繪製紅色矩形？** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **開發階段需要授權嗎？** 測試可使用免費試用版；正式上線需購買授權。
- **可以使用相同的 API 操作既有 PSD 檔嗎？** 可以，Aspose.PSD 完全支援 PSD 編輯。

## 什麼是於 PSD 檔中繪製紅色矩形？
於 PSD 檔中繪製紅色矩形是指使用 `Graphics` 物件，在指定的圖層上以紅色填滿或描邊的方式繪製矩形形狀。此操作常用於標示區域、建立佔位符或以程式方式加入簡易圖形。

## 為什麼選擇 Aspose.PSD for Java 來操作 PSD 檔？
Aspose.PSD 提供純 Java API，讓您在不安裝 Photoshop 的情況下讀取、編輯與寫入 Photoshop PSD 檔。它支援圖層管理、顏色操作與向量繪圖，非常適合伺服器端影像處理、自動化資產管線與自訂圖形產生。

## 前置條件

- 已在機器上安裝 Java Development Kit (JDK)。  
- Aspose.PSD for Java 套件。可從 [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) 下載。

## 匯入套件

開始之前，將所需的類別匯入您的 Java 專案：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 步驟 1：建立新文件

先建立一個具有指定畫布大小的全新 PSD 文件。此文件將容納我們稍後要繪製的圖層。

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## 步驟 2：新增圖層

接著，新增一個覆蓋整個圖像寬高的空白圖層。圖層是分離繪圖操作的關鍵。

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## 步驟 3：繪製圖形

我們將使用 `Graphics` 類別操作圖層的像素資料。以下提供三個範例，說明如何清除背景並以不同顏色繪製矩形。

### 清除圖層顏色（將背景設為黃色）

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 繪製紅色矩形（主要示範）

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### 繪製藍色矩形（額外範例）

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## 步驟 4：儲存變更

最後，將修改後的 PSD 圖像寫入磁碟。檔案將包含新圖層與繪製的圖形。

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## 常見問題與解決方案

- **圖層繪製後未顯示：** 請確保在建立 `Graphics` 物件之前已將圖層加入圖像。
- **顏色顯示不正確：** 請確認使用 `Color.getRed()`（或其他靜態方法），而非超出範圍的自訂 RGB 值。
- **檔案未儲存：** 請確認 `outputDir` 路徑已存在且程式具有寫入權限。

## 常見問答

### Q1：可以使用 Aspose.PSD for Java 操作既有的 PSD 檔嗎？

A1：可以，Aspose.PSD for Java 提供完整功能來編輯與操作既有的 PSD 檔。

### Q2：在哪裡可以取得 Aspose.PSD for Java 的支援？

A2：您可前往 [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) 取得相關支援。

### Q3：Aspose.PSD for Java 有免費試用版嗎？

A3：有，請點擊 [here](https://releases.aspose.com/) 下載免費試用版。

### Q4：如何購買 Aspose.PSD for Java 的授權？

A4：請前往 [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) 購買授權。

### Q5：是否提供臨時授權？

A5：有，您可從 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 其他常見問答

**Q：除了矩形，還能繪製其他形狀嗎？**  
A：可以，`Graphics` 類別同樣支援繪製橢圓、直線與自訂路徑。

**Q：Aspose.PSD 支援在繪製的圖形中使用透明度嗎？**  
A：當然支援，您可以使用帶有 ARGB 顏色的 `SolidBrush` 來加入透明度。

**Q：可以編輯圖層的不透明度嗎？**  
A：可以，每個 `Layer` 物件都有 `setOpacity` 方法，接受 0 到 255 的值。

**Q：如何載入既有的 PSD 檔而不是建立新檔？**  
A：在操作圖層前使用 `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` 載入檔案。

## 結論

您現在已掌握如何使用 Aspose.PSD for Java **繪製紅色矩形** 以及其他基本圖形。透過建立文件、加入圖層、清除背景，並以 `Graphics` API 繪圖，您可以自動化許多圖形設計工作。接下來可嘗試不同的筆刷、圖層效果與檔案格式，進一步擴展應用。

---

**最後更新：** 2025-12-27  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}