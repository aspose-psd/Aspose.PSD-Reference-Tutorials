---
date: 2026-06-13
description: 了解如何使用 Aspose.PSD for Java 在 PSD 檔案中繪製矩形。本指南提供逐步程式碼示例、圖層添加、伺服器端影像處理及形狀繪製。
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: 執行簡單繪圖
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 在 PSD 中繪製矩形
url: /zh-hant/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 PSD 中使用 Aspose.PSD for Java 繪製矩形

## 簡介

在本教學中，您將學習如何使用純 Java 的 Aspose.PSD 函式庫在 Photoshop PSD 檔案中 **繪製矩形** 形狀。無論您是構建伺服器端資產流水線、自動產生縮圖，或是為現有設計加入動態圖形，以下步驟都能提供完整、可投入生產的解決方案。我們將說明如何建立新的 PSD 文件、加入圖層、清除背景，最後繪製紅色與藍色矩形——全部不需啟動 Photoshop。

## 快速答覆
- **建立 PSD 檔案的主要類別是什麼？** `PsdImage`
- **哪個方法可清除圖層的背景顏色？** `Graphics.clear(Color)`
- **如何繪製紅色矩形？** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **開發時需要授權嗎？** 免費試用版可用於測試；正式環境需購買授權。
- **我可以使用相同的 API 操作現有的 PSD 檔案嗎？** 是，Aspose.PSD 支援完整的 PSD 編輯。

## 在 PSD 檔案中繪製紅色矩形是什麼？

繪製紅色矩形是指使用 `Graphics` 物件在 PSD 圖像的特定圖層上繪製以紅色填充或描邊的矩形形狀。此操作常用於標示區域、建立佔位圖，或以程式方式加入簡單圖形。

## 為何使用 Aspose.PSD for Java 來操作 PSD 檔案？

Aspose.PSD for Java 支援 **超過 50 種輸入與輸出格式**，可在不將整個檔案載入記憶體的情況下處理上百頁的 PSD 檔，且可在任何支援 Java 8 以上的平台上執行。其伺服器端影像處理引擎免除 Photoshop 的需求，降低授權成本，並能在一般虛擬機上每小時處理高達 **10 GB** 的影像資料，實現自動化工作流程。

## 前置條件

- 已在機器上安裝 Java Development Kit (JDK) 8 或更新版本。  
- Aspose.PSD for Java 函式庫。您可從 [Aspose.PSD for Java 文件](https://reference.aspose.com/psd/java/) 下載。

## 匯入套件

`import` 陳述式將所需的類別匯入作用域，讓您能操作 PSD 圖像、圖層、顏色與圖形。

- `PsdImage` 類別是 Aspose.PSD 的頂層物件，代表記憶體中的單一 PSD 檔案。  
- `Graphics` 提供繪圖基元，如直線、矩形與橢圓。  
- `Color` 與 `Pen` 讓您指定筆劃顏色與粗細。  
- `Layer` 類別代表 PSD 文件中的單一圖層。  
- `Rectangle` 類別定義用於繪圖操作的矩形區域之位置與大小。  
- `SolidBrush` 類別以純色填滿形狀。

## 建立 PSD 文件的第一步是什麼？

您可透過提供畫布寬度與高度（像素）來實例化 `PsdImage`，此舉會建立空的 PSD 檔案結構。設定好任何初始圖層或背景後，呼叫 `save` 方法並傳入檔案路徑，即可將文件寫入磁碟。這樣即可為後續的編輯操作做好準備。

## 步驟 1：建立新文件

首先，建立一個具有所需畫布尺寸的全新 PSD 文件。此文件將容納我們即將繪製的圖層。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 如何在 PSD 圖像中新增空白圖層？

首先，建立一個與父層 `PsdImage` 具有相同寬度與高度的 `Layer` 實例。接著使用 `add` 方法將此圖層加入影像的 `Layers` 集合。圖層加入影像後，取得其 `Graphics` 物件以執行繪圖操作；若未完成此步驟，繪圖將不會顯示。

## 步驟 2：新增圖層

接著，新增一個覆蓋影像全寬全高的空白圖層。圖層對於分離繪圖操作至關重要。

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## 清除圖層背景顏色的目的為何？

使用特定 `Color` 呼叫 `Graphics.clear` 會將整個圖層填滿該顏色，實質上重設所有像素資料。這可確保先前的內容被移除，圖層從已知的背景開始，避免在之後於 Photoshop 開啟或編輯 PSD 時出現意外的透明度或顏色混合。

## 步驟 3：繪製圖形

我們將使用 `Graphics` 類別來操作圖層的像素資料。以下提供三個範例，說明如何清除背景並以不同顏色繪製矩形。

### 清除圖層顏色（將背景設為黃色）

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### 繪製紅色矩形（主要焦點）

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 繪製藍色矩形（額外範例）

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## 如何將編輯後的 PSD 檔案儲存至磁碟？

在 `PsdImage` 物件上使用 `save` 方法，傳入完整檔案路徑，並可選擇指定欲輸出的影像格式（預設為 PSD）。此操作會將所有圖層、遮色片與繪圖指令寫入單一符合 Photoshop 規範的 PSD 檔，使其在開啟時不會出現警告。

## 步驟 4：儲存變更

最後，將已修改的 PSD 影像寫入磁碟。檔案將包含新圖層與繪製的形狀。

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## 常見問題與解決方案

- **繪製後圖層未顯示：** 請確保在建立 `Graphics` 物件之前已將圖層加入影像。繪圖表面必須附加於有效的圖層上。  
- **顏色顯示不正確：** 請確認使用 `Color.getRed()`（或 `Color.getBlue()`），而非建立超出 0‑255 範圍的自訂 RGB 值。  
- **檔案未儲存：** 請確認 `outputDir` 路徑存在且應用程式具備寫入權限。在 Linux 上，可能需要調整資料夾所有權或使用 `Files.createDirectories`。  
- **大型檔案效能下降：** 使用 `PsdImage` 的 `setLoadOptions` 僅載入必要的通道，降低超過 200 MB PSD 的記憶體使用量。

## 常見問與答

**Q1: 我可以使用 Aspose.PSD for Java 來操作既有的 PSD 檔案嗎？**  
A1: 可以，Aspose.PSD for Java 提供廣泛功能，可編輯與操作既有 PSD 檔案，包括圖層重新排序、遮色片調整與向量繪圖。

**Q2: 我可以在哪裡取得 Aspose.PSD for Java 的支援？**  
A2: 您可前往 [Aspose.PSD for Java 論壇](https://forum.aspose.com/c/psd/34) 獲得社群協助與官方回應。

**Q3: 是否提供 Aspose.PSD for Java 的免費試用？**  
A3: 有，您可在 [此處](https://releases.aspose.com/) 取得免費試用版。試用版包含全部功能，但會在儲存的檔案上加上浮水印。

**Q4: 我要如何購買 Aspose.PSD for Java 的授權？**  
A4: 您可於 [Aspose.PSD 購買頁面](https://purchase.aspose.com/buy) 購買授權。授權方案包括永久授權、訂閱制與站點授權。

**Q5: 是否提供 Aspose.PSD for Java 的臨時授權？**  
A5: 有，您可從 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 其他常見問與答

**Q: 我可以繪製除矩形外的其他形狀嗎？**  
A: 可以，`Graphics` 類別亦支援繪製橢圓、直線，以及透過 `drawPath` 方法的自訂路徑。

**Q: Aspose.PSD 是否支援繪製形狀的透明度？**  
A: 當然支援；您可使用帶有 ARGB 顏色的 `SolidBrush` 來加入 alpha 透明度，實現半透明覆蓋層。

**Q: 是否可以編輯圖層的透明度？**  
A: 可以，每個 `Layer` 物件都有 `setOpacity` 方法，可接受 0 至 255 的數值，讓您細緻控制圖層透明度。

**Q: 我要如何載入既有的 PSD 檔案而不是建立新檔案？**  
A: 在操作圖層之前，使用 `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` 載入檔案。載入的影像會保留所有原始圖層與遮色片。

## 結論

您現在已掌握使用 Aspose.PSD for Java **繪製矩形** 形狀與操作 PSD 檔案中圖層的技巧。透過建立文件、加入圖層、清除背景，並使用 `Graphics` API 繪圖，您可以在伺服器端自動化無數平面設計任務。可嘗試不同的筆、刷子與圖層效果，將此基礎延伸為完整功能的影像產生流程。

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [How to Draw Shapes Java – Basic Image Operations](/psd/java/basic-image-operations/)
- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Last Updated:** 2026-06-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose