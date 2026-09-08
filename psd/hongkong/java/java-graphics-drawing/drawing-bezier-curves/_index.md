---
date: 2026-09-08
description: 了解如何在 Java 中使用 Aspose.PSD for Java 繪製貝塞爾曲線。遵循逐步說明、前置條件以及免編碼範例。
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: 在 Java 中繪製貝塞爾曲線
og_description: 如何在 Java 中使用 Aspose.PSD 繪製貝塞爾曲線。本指南涵蓋前置條件、逐步繪製說明，以及高解析度影像的技巧。
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: 如何在 Java 中使用 Aspose.PSD 函式庫繪製貝塞爾曲線
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: 如何在 Java 中使用 Aspose.PSD 函式庫繪製貝塞爾曲線
url: /zh-hant/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.PSD 庫繪製貝塞爾曲線

## 簡介
如果您需要了解 **如何繪製貝塞爾** 形狀於 Java 桌面或伺服器應用程式中，Aspose.PSD for Java 為您提供乾淨且記憶體效能高的 API。在本教學中，您將看到建立 PSD 畫布、設定繪圖筆、定義控制點，並渲染平滑貝塞爾曲線的完整步驟——全部不需要撰寫任何低階像素操作程式碼。

## 快速答案
- **哪個程式庫負責繪圖？** Aspose.PSD for Java.
- **需要多少行程式碼？** 大約十行簡潔的語句。
- **我可以更改曲線顏色嗎？** 是的，透過調整 `Pen` 的 colour 屬性即可。
- **支援高解析度輸出嗎？** 是的，最高可支援 500 MB 檔案，且不需完整載入記憶體。
- **我需要商業授權嗎？** 免費試用版可用於開發；正式環境則需購買授權。

## 什麼是貝塞爾曲線？
貝塞爾曲線是一條以數學方式定義的平滑線條，由兩個或多個點控制。它廣泛應用於向量圖形、動畫和 UI 設計，以建立優雅且可縮放的形狀。曲線的形狀由起點、終點以及一個或多個影響曲率的控制點決定，設計師可透過簡單參數模型複雜路徑。

## 為什麼使用 Aspose.PSD 繪製貝塞爾曲線？
Aspose.PSD 支援 **30+ image formats**，且可處理 **multi‑hundred‑page PSD files** 而無需將整個文件載入 RAM。程式庫的 `drawBezier()` 方法自動處理抗鋸齒與色彩管理，對於一般 100 × 100 畫布，可在不到一秒的時間內提供像素完美的結果。

## 先決條件
在開始之前，請確保您具備以下先決條件：

1. **Java Development Kit (JDK)** – 安裝並設定任意近期版本（8 或以上）。
2. **Aspose.PSD for Java JAR** – 從 [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) 下載 Aspose.PSD for Java 程式庫，並將其加入專案的 classpath。
3. **Integrated Development Environment (IDE)** – 如 Eclipse、IntelliJ IDEA 或 NetBeans，並已配置 JDK。

## 匯入套件
以下匯入語句會載入用於影像建立與繪圖的 Aspose.PSD 類別。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## 如何在 Java 中繪製貝塞爾曲線？
載入空白的 `PsdImage`，建立 `Graphics` 物件，設定 `Pen`，定義起點、控制點與終點，呼叫 `drawBezier()`，最後儲存影像。此流程只需一次方法呼叫即可產生平滑曲線，且不需手動像素計算。

### 步驟 1：建立影像實例
`PsdImage` 類別是 Aspose.PSD 的頂層物件，代表記憶體中的單一 PSD 檔案。首先，您需要建立 `PsdImage` 類別的實例，以在記憶體中表示 PSD 影像。

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
說明：
- `PsdImage` 以寬度與高度參數實例化（本例為 100 × 100 像素）。

### 步驟 2：初始化圖形上下文
`Graphics` 類別提供在 `PsdImage` 上的繪圖功能。接著，初始化 `Graphics` 類別的實例以對影像執行繪圖操作。

```java
Graphics graphics = new Graphics(image);
```
說明：
- `Graphics` 物件以 `image` 實例初始化，允許執行繪圖操作。

### 步驟 3：清除圖形表面
`clear()` 方法設定圖形表面的背景顏色。使用特定的背景顏色（此處為 `Color.getYellow()`）清除圖形表面。

```java
graphics.clear(Color.getYellow());
```
說明：
- `clear()` 方法設定圖形表面的背景顏色。

### 步驟 4：初始化繪圖筆
`Pen` 物件定義筆畫屬性，如顏色與寬度。設定 `Pen` 物件的顏色與寬度，以決定曲線的繪製方式。

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
說明：
- `Pen` 以黑色和 3 像素寬度初始化。

### 步驟 5：定義貝塞爾曲線參數
控制點決定曲率。為貝塞爾曲線指定控制點與終點。

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
說明：
- `startX`、`startY`：曲線的起始點。  
- `controlX1`、`controlY1`：第一個控制點。  
- `controlX2`、`controlY2`：第二個控制點。  
- `endX`、`endY`：曲線的終止點。

### 步驟 6：繪製貝塞爾曲線
`drawBezier()` 方法使用提供的 `Pen` 與點來繪製曲線。使用 `drawBezier()` 方法，將先前定義的 `Pen` 與控制點套用於影像上以繪製貝塞爾曲線。

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
說明：
- `drawBezier()` 方法使用 `blackPen` 及指定參數繪製曲線。

### 步驟 7：儲存影像
儲存影像會將繪圖寫入磁碟。將繪製好的影像儲存為 BMP 檔案格式。

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## 常見問題與解決方案
- **曲線看起來平直** – 請確認控制點未與起點與終點共線。稍微偏移控制點以產生曲率。  
- **顏色未變更** – 請確保在呼叫 `drawBezier()` 前已修改 `Pen` 的 colour。  
- **大型畫布發生記憶體不足錯誤** – 使用支援串流的 `PsdImage` 建構子，或將繪圖分割成多個圖塊。

## 常見問答

**Q: 我可以在同一張影像中繪製多條貝塞爾曲線嗎？**  
A: 可以，於迴圈中重複呼叫 `drawBezier()`，並為每條曲線更新控制點。

**Q: 如何更改貝塞爾曲線的顏色？**  
A: 在呼叫 `drawBezier()` 前，修改 `Pen` 物件的 colour 屬性（範例中為 `Color.getBlack()`）。

**Q: Aspose.PSD for Java 是否適用於高解析度影像？**  
A: 是的，Aspose.PSD for Java 支援高解析度影像，具有效率的記憶體管理，能處理超過 500 MB 的檔案而無需將整個檔案載入記憶體。

**Q: 我可以將影像匯出為 BMP 以外的格式嗎？**  
A: 可以，Aspose.PSD for Java 支援匯出為 PNG、JPEG、TIFF 以及其他多種點陣圖格式。

**Q: 我在哪裡可以找到更多範例與文件？**  
A: 請前往 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 取得完整指南與程式碼範例。

---

**最後更新:** 2026-09-08  
**測試環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 重新調整影像大小 – 繪製形狀與基本影像操作](/psd/java/basic-image-operations/)
- [使用 Aspose.PSD for Java 在 PSD 中繪製並儲存矩形](/psd/java/basic-image-operations/simple-drawing/)
- [如何使用 Aspose.PSD 在 Java 中變更筆畫顏色](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}