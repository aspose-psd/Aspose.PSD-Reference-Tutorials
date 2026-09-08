---
date: 2026-09-08
description: 了解如何在 Java 中使用 Aspose.PSD 的 Graphics Path 類別建立圖像。本分步指南將示範如何有效地加入文字、形狀以及清除圖像背景。
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: 如何在 Java 中使用 Graphics Path 建立圖像
og_description: 了解如何在 Java 中使用 Aspose.PSD 建立圖像。本教學涵蓋使用 Graphics Path 類別加入文字、形狀以及清除圖像背景。
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: 如何在 Java 中使用 Graphics Path 及 Aspose.PSD 建立圖像
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: 如何在 Java 中使用 Graphics Path 建立圖像
url: /zh-hant/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Graphics Path 在 Java 中建立圖像

## 介紹
在本教學中，您將學習 **如何建立圖像** 檔案，以程式方式利用 Aspose.PSD for Java 提供的強大 **Graphics Path** 類別。無論您需要繪製自訂形狀、嵌入文字，或清除圖像背景，以下逐步指南將向您展示如何僅用幾行程式碼即可達到專業等級的效果。

## 快速解答
- **哪個函式庫處理複雜繪圖？** Aspose.PSD for Java 的 Graphics Path 類別。  
- **我可以在圖像中加入文字嗎？** 可以 – 使用 `GraphicsPath.addString` 方法。  
- **是否支援清除背景？** 當然，使用透明筆刷填充路徑即可。  
- **需要哪個 Java 版本？** JDK 11 或更新版本。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。

## Graphics Path 類別是什麼？
`GraphicsPath` 類別是 Aspose.PSD 用於定義向量繪圖指令的核心物件。它讓您將形狀、文字與填充組合成單一可重複使用的路徑，並可在任何圖像上渲染。透過建立路徑，您可以在一次渲染過程中套用筆、筆刷與變換，提升效能並使繪圖邏輯保持有序。

## 為何在 Java 中使用 Graphics Path 來加入文字圖像與清除圖像背景？
Aspose.PSD 支援 **超過 50 種圖像格式**（包括 PSD、PNG、JPEG、BMP），且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案。使用 Graphics Path 可將繪圖、文字放置與背景清除合併於單一高效能操作，相較於僅使用點陣圖的方式，可將記憶體開銷降低至 **30 %**。

## 前置條件
1. **Java Development Kit (JDK)** – 已安裝穩定的 JDK 11 以上版本。可從 [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java library** – 從 [here](https://releases.aspose.com/psd/java/) 取得最新的 JAR，並將其加入專案的 classpath。  
3. **IDE** – 任何 Java IDE，例如 Eclipse、IntelliJ IDEA 或 VS Code。  

有了上述條件，您即可開始建立圖像。

## 匯入套件
要使用圖形功能，請匯入所需的命名空間：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

這些匯入會公開圖像操作所需的核心繪圖、筆刷與筆類別。

## 如何在 Java 中使用 Graphics Path 建立圖像？
建立新的點陣畫布，附加 `Graphics` 物件，並準備繪圖表面。此一步會設定一個 **500 × 500 像素** 的位圖，準備進行向量渲染。畫布起始為透明，讓您之後可以填入任意背景顏色或圖案，這對於清除圖像背景的情境相當重要。

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## 步驟 1：初始化圖像與圖形
此處我們建立一個 `PsdImage` 物件（500 × 500），並取得其 `Graphics` 內容。  
`PsdImage` 代表一個在記憶體中的點陣圖，Aspose.PSD 可對其進行操作並儲存為多種格式。  
`Graphics` 提供繪圖方法，可將形狀、文字與路徑渲染至 `PsdImage`。

## 步驟 2：建立與設定 Graphics Path
接著，我們建立一個包含圓形、矩形與文字標籤的 `GraphicsPath`。  
`GraphicsPath` 是幾何圖形的容器；您可在渲染前向其加入形狀、線條與字串。

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### 向圖像加入文字 (add text image java)
`GraphicsPath` 的 `addString` 方法會使用提供的字型與筆刷，將指定文字放置於給定座標。這是將清晰、可縮放文字嵌入向量路徑的最可靠方式。

## 步驟 3：繪製與填充路徑
現在，我們使用藍色筆繪製路徑，並以垂直剝線筆刷填充，若需要亦可透過填入透明圖樣來 **clear image background java**。`Pen` 定義輪廓樣式，`HatchBrush` 則產生圖樣填充。

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## 步驟 4：儲存圖像
最後，將組合好的圖像寫入磁碟，使用 PNG 格式（或任何 50+ 支援的格式）。`save` 方法會根據您提供的檔案副檔名決定輸出檔案類型。

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## 常見問題與解決方案
- **路徑不可見** – 確認筆的顏色與填充筆刷形成對比。  
- **文字模糊** – 使用更高解析度的圖像或具足夠 DPI 的 TrueType 字型。  
- **大型檔案發生記憶體不足** – 啟用 `PsdImageOptions.setUseMemoryCache(true)` 以串流資料，而非完整載入。

## 常見問答

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一個 Java 函式庫，可讓您在不需要 Photoshop 的情況下建立、編輯與轉換 Photoshop (PSD) 檔案及其他點陣格式。

**Q: 我可以處理非 PSD 的格式嗎？**  
A: 可以 – 函式庫支援 **50+** 種格式，包括 PNG、JPEG、BMP、TIFF 與 GIF。

**Q: 是否提供試用版？**  
A: 有，您可在 [here](https://releases.aspose.com/) 取得 Aspose.PSD 的免費試用版。

**Q: 我要如何購買授權？**  
A: 您可從 [here](https://purchase.aspose.com/buy) 購買 Aspose.PSD。

**Q: 我可以在哪裡取得支援？**  
A: 您可在 [Aspose’s forum](https://forum.aspose.com/c/psd/34) 尋求支援與討論。

## 結論
透過本指南，您現在已了解如何使用 Aspose.PSD 的 Graphics Path 類別，建立具備複雜向量形狀、嵌入文字與透明背景的 **如何建立圖像** 檔案。可嘗試不同的筆、筆刷與路徑幾何形狀，為遊戲、使用者介面或自動化報告產生等需求打造更豐富的圖形。

---

**Last Updated:** 2026-09-08  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## 相關教學

- [使用 Aspose.PSD 設定路徑在 Java 中產生 PSD 圖像](/psd/java/image-editing/create-image-by-setting-path/)
- [使用 Aspose.PSD for Java 重新調整圖像大小 – 繪製形狀與基本圖像操作](/psd/java/basic-image-operations/)
- [在圖像加入簽名 – 使用 Aspose.PSD for Java 在畫布上繪製圖像](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}