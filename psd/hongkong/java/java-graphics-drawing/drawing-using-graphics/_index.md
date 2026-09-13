---
date: 2026-09-13
description: 了解如何在 Java 中使用 Aspose.PSD 繪製橢圓及其他形狀。本分步 Java Graphics 教學示範 gradient fills、
  polygon fills 與 image export。
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: 在 Java 中使用 Graphics 繪圖
og_description: 了解如何在 Java 中使用 Aspose.PSD 繪製橢圓。本 Java Graphics 教學涵蓋形狀繪製、 gradient
  fills、 polygon filling 與 exporting images。
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: 如何在 Java 中使用 Aspose.PSD 的 Graphics 功能繪製橢圓
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: 如何在 Java 中使用 Aspose.PSD 的 Graphics 功能繪製橢圓
url: /zh-hant/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.PSD 的圖形繪製橢圓

## 介紹
在本 Java 圖形教學中，您將學習如何使用 Aspose.PSD for Java 以程式方式 **繪製橢圓** 物件及其他形狀。無論是需要產生動態縮圖、建立自訂 UI 元件，或是自動化設計工作流程，掌握橢圓繪製與漸層填充都能讓您精確控制視覺效果。以下步驟將帶您完成圖形初始化、設定筆與刷子，並將結果匯出為常見影像格式。

## 快速回答
- **需要的函式庫是什麼？** Aspose.PSD for Java（從官方網站下載）。  
- **本教學聚焦於哪種形狀？** 繪製橢圓並填充多邊形。  
- **可以匯出除 BMP 之外的格式嗎？** 可以 – 支援 PNG、JPEG、TIFF 等多種格式。  
- **開發時需要授權嗎？** 測試時可使用免費臨時授權；正式環境需要完整授權。  
- **API 適用於大型影像嗎？** Aspose.PSD 可處理高達 500 MB 的檔案，且不會將整個位圖載入記憶體。

## 如何在 Java 中繪製橢圓？
載入具有指定寬度與高度的 `PsdImage`，建立 `Graphics` 物件，設定 `Pen`，然後以限定矩形呼叫 `drawEllipse`。整個操作僅需少數方法呼叫，於現代硬體上對於 800×600 的影像可在一秒內完成。

## 什麼是 Aspose.PSD for Java？
Aspose.PSD for Java 是一套 **純 Java 函式庫，提供 50 多種影像格式轉換與完整的 PSD 編輯功能**，無需 Adobe Photoshop。它能渲染、修改與匯出多層檔案，同時保持低記憶體使用率，適合伺服器端圖形產生。

## 為什麼使用 Aspose.PSD 繪製形狀？
Aspose.PSD 提供高效能、廣泛的格式支援與精確的渲染，讓它成為伺服器端圖形產生與複雜形狀繪製的理想選擇。

- **效能：** 可處理高達 500 MB 的影像，堆疊使用量低於 150 MB（約比競爭對手低 30 %）。  
- **格式支援：** 超過 50 種輸入與輸出格式，包括 BMP、PNG、JPEG、TIFF 與 PSD。  
- **精確度：** 次像素渲染確保在高 DPI 顯示器上呈現清晰的橢圓與平滑的漸層。

## 前置條件
- 具備 Java 程式設計的基礎知識。  
- 已安裝 Java Development Kit（JDK）。  
- 使用 IntelliJ IDEA 或 Eclipse 等 IDE。  
- Aspose.PSD for Java 函式庫。可從 [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) 下載。

## 匯入套件
要開始使用，請匯入必要的 Aspose.PSD 類別與標準 Java 工具。以下類別提供繪圖基元與顏色處理：
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## 步驟 1：建立影像物件
`PsdImage` 代表一個記憶體中的點陣畫布，可在其上繪圖並以各種格式儲存。
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## 步驟 2：初始化 graphics 物件
`Graphics` 是與 `PsdImage` 連結的繪圖表面，支援向量操作如繪製形狀。
```java
Graphics graphics = new Graphics(image);
```

## 步驟 3：清除影像表面
`clear` 以單一背景色填滿整個畫布。
```java
graphics.clear(Color.getWhite());
```

## 步驟 4：建立並設定 Pen 物件
`Pen` 定義繪製輪廓時的顏色、寬度與樣式。
```java
Pen pen = new Pen(Color.getBlue());
```

## 步驟 5：繪製形狀
`drawEllipse` 依目前的 Pen 在指定的矩形內繪製橢圓。
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## 步驟 6：使用 Brush 填充
`LinearGradientBrush` 建立在定義區域內由兩種顏色過渡的漸層填充。
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## 步驟 7：儲存已修改的影像
`save` 將 `PsdImage` 以選擇的格式（如 BMP 或 PNG）寫入磁碟。
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## 常見陷阱與疑難排解
- **Graphics 發生 NullPointerException：** 確保在建立 `Graphics` 物件前已完整實例化 `PsdImage`。  
- **顏色不正確：** 當預設調色盤不符合需求時，使用 `Color.fromArgb` 指定精確的 ARGB 值。  
- **大型影像效能下降：** 啟用 `PsdImageOptions` 並設定 `compression = CompressionType.Rle` 以減少記憶體開銷。

## 常見問答

**Q: Aspose.PSD 能處理複雜的影像操作嗎？**  
A: 能，除了形狀繪製外，還支援圖層合併、通道調整、文字渲染與進階遮罩等功能。

**Q: Aspose.PSD 適用於高效能應用程式嗎？**  
A: 絕對可以；此函式庫已針對速度進行最佳化，能在一般伺服器上於 2 秒內處理 10 MP 影像。

**Q: 我可以在哪裡找到更多範例與文件？**  
A: 前往 [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) 取得完整指南與 API 參考文件。

**Q: Aspose.PSD 支援多種影像格式匯出嗎？**  
A: 能，您可以匯出為 BMP、PNG、JPEG、TIFF、GIF、PSD 等多種格式。

**Q: 若遇到問題，我該如何取得支援或協助？**  
A: 可在 [support forum](https://forum.aspose.com/c/psd/34) 向 Aspose.PSD 社群求助，或考慮取得 [temporary license](https://purchase.aspose.com/temporary-license/) 以獲得優先協助。

---

**最後更新：** 2026-09-13  
**測試環境：** Aspose.PSD for Java 24.10  
**作者：** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 重新調整影像大小 – 繪製形狀與基本影像操作](/psd/java/basic-image-operations/)
- [使用 Aspose.PSD for Java 在 PSD 中繪製並儲存矩形](/psd/java/basic-image-operations/simple-drawing/)
- [在影像上添加簽名 – 使用 Aspose.PSD for Java 在畫布上繪製影像](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}