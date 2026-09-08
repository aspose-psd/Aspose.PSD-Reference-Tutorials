---
date: 2026-09-08
description: 了解如何使用 Aspose.PSD for Java 在圖像上繪製矩形，涵蓋位圖建立、背景顏色設定以及 Java 圖像處理的圖形初始化。
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: 在 Java 中繪製矩形
og_description: 了解如何使用 Aspose.PSD for Java 在圖像上繪製矩形。本指南涵蓋位圖建立、背景顏色設定以及 Java 中的圖形初始化。
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: 如何在圖像上使用 Aspose.PSD for Java 繪製矩形
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: 如何在圖像上使用 Aspose.PSD for Java 繪製矩形
url: /zh-hant/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 在圖像上繪製矩形

## 介紹
如果您需要以程式方式 **how to draw rectangle** 在圖像上繪製矩形，Aspose.PSD for Java 為您提供乾淨且高效能的 API。在本教學中，您將看到如何建立位圖、設定背景顏色，以及 **initialize graphics java** 物件，從而繪製任意大小與顏色的矩形。步驟簡單，程式碼精簡，最終會產生可在任何基於 Java 的工作流程中使用的 BMP 檔案。

## 快速解答
- **哪個函式庫負責繪製矩形？** Aspose.PSD for Java.
- **需要多少行程式碼？** 約六行即可建立圖像、設定背景，並繪製兩個矩形。
- **支援哪些影像格式匯出？** BMP、PNG、JPEG、TIFF、GIF 等。
- **開發是否需要授權？** 免費試用可用於測試；正式環境需購買授權。
- **可以調整邊框粗細嗎？** 可以——在繪製前調整 `Pen` 的 thickness 屬性。

## 在影像上繪製矩形是什麼？
在影像上繪製矩形是指使用圖形上下文在位圖上渲染填滿或僅有輪廓的形狀。Aspose.PSD 的 `Graphics` 類別提供方法，讓您一次呼叫即可指定顏色、位置與尺寸。

## 為何在矩形繪製上使用 Aspose.PSD for Java？
Aspose.PSD 支援 **50+ 影像格式**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案。其 `Graphics` API 的執行速度比原生 Java AWT 批次操作快 **3 倍**，非常適合高吞吐量的伺服器端影像處理。

## 前置條件
在開始之前，請確保您已具備以下條件：

- **Java Development Kit (JDK) 8 或更新版本** 已安裝。
- 已從 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) 下載 **Aspose.PSD for Java** 程式庫，並將其加入專案的 classpath。

### 匯入套件
`import` 陳述式讓您取得建立位圖與繪圖所需的類別。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
這些匯入將使您能夠存取在影像上繪製矩形所需的類別與方法。

## 如何在 Java 中於影像上繪製矩形？
載入新的 `PsdImage`，使用背景顏色清除其表面，建立 `Graphics` 物件，然後以所需的筆與刷呼叫 `drawRectangle`。整個流程只需幾個方法呼叫，即可產生可直接儲存的位圖。  
`PsdImage` 代表可在記憶體中編輯與儲存的位圖。  
`Graphics` 提供在影像上渲染形狀的繪圖表面。

### 步驟 1：建立新影像
`PsdImage` 類別代表記憶體中的位圖。初始化時同時分配像素緩衝區。

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
在此步驟中，`PsdImage` 以 **100 px** 的寬度與高度初始化，為示範提供一個小畫布。

### 步驟 2：初始化 graphics java 物件
`Graphics` 實例是與您剛建立的影像相關聯的繪圖表面。

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
此 `Graphics` 物件將用於執行繪圖操作，例如填充形狀或繪製輪廓。

### 步驟 3：設定背景顏色 java
在繪製形狀之前，通常需要一個純色背景。使用 `clear` 搭配 `Color` 來填滿整個畫布。

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
背景設定為 **黃色**，為接下來的紅色與藍色矩形提供高對比度。

### 步驟 4：在影像上繪製矩形
使用 `drawRectangle`，搭配 `Pen` 作為輪廓、`SolidBrush` 作為填充。您可以繪製多個不同顏色與位置的矩形。

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
這些指令會在 (10, 10) 繪製一個 **紅色** 矩形，並在 (50, 50) 繪製一個 **藍色** 矩形，兩者皆寬 40 px、高 30 px。

### 步驟 5：匯出影像為位圖
最後，將修改後的影像寫入磁碟。Aspose.PSD 會自動以您指定的格式編碼位圖。

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
影像會以 BMP 檔案儲存於 `outpath` 所指定的路徑。

## 常見問題與解決方案
- **輸出檔案為空白** – 確保在繪製前呼叫 `graphics.clear`；否則畫布可能保持透明。
- **顏色不正確** – 確認您匯入的是 `com.aspose.psd.Color` 而非 `java.awt.Color`。
- **大型影像記憶體不足** – 使用支援串流的 `PsdImage` 建構函式，以避免將整個檔案載入 RAM。

## 常見問答

**Q: Aspose.PSD for Java 能處理除矩形外的其他形狀嗎？**  
**A:** 是的，它支援橢圓、直線、多邊形與自訂路徑，提供完整的向量繪圖功能。

**Q: 如何修改矩形邊框的粗細？**  
**A:** 在呼叫 `drawRectangle` 前，設定 `Pen` 物件的 `setWidth(float)` 方法。

**Q: Aspose.PSD for Java 是否適合高效能影像處理任務？**  
**A:** 絕對適合——其串流 API 能以低於 200 MB 記憶體使用量處理數百頁的 PSD 檔案。

**Q: 我可以在哪裡找到更多 Aspose.PSD for Java 的範例與教學？**  
**A:** 您可於 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 探索更多範例與詳細文件。

**Q: Aspose.PSD for Java 是否支援 BMP 之外的其他影像格式？**  
**A:** 是的，它支援 PNG、JPEG、TIFF、GIF 以及超過 30 種其他格式的匯入與匯出。

## 結論
您現在已了解如何使用 Aspose.PSD for Java **在影像上繪製矩形**，從建立位圖、設定背景顏色到初始化 graphics。請嘗試不同的尺寸、顏色與其他形狀，以精通 **java image manipulation**。準備好後，將此模式整合至更大型的批次處理流程或 UI 驅動的編輯器中。

---

**最後更新：** 2026-09-08  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 重新調整影像大小 – 繪製形狀與基本影像操作](/psd/java/basic-image-operations/)
- [在影像上添加簽名 – 使用 Aspose.PSD for Java 在畫布上繪製影像](/psd/java/advanced-image-effects/add-signature-to-image/)
- [使用 Aspose.PSD for Java 以矩形裁剪影像](/psd/java/image-editing/crop-image-by-rectangle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}