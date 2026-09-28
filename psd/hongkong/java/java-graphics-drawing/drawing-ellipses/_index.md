---
date: 2026-09-28
description: 了解如何在 Java 中使用 Aspose.PSD 繪製橢圓，這是領先的 Java 圖像處理教學，教您建立橢圓及其他形狀。
keywords:
- how to draw ellipse
- draw shapes java
- java image processing tutorial
- create ellipse image
- draw ellipses java
lastmod: 2026-09-28
linktitle: 在 Java 中繪製橢圓
og_description: 了解如何在 Java 中使用 Aspose.PSD 繪製橢圓，這是頂級的 Java 圖像處理教學，可讓您高效建立橢圓、繪製形狀，並產生點陣圖影像。
og_image_alt: Guide showing how to draw an ellipse in Java with Aspose.PSD
og_title: 如何在 Java 中使用 Aspose.PSD 庫繪製橢圓
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to draw ellipse in Java using Aspose.PSD, the leading Java
    image processing tutorial for creating ellipses and other shapes.
  headline: How to draw ellipse in Java using Aspose.PSD library
  type: TechArticle
- questions:
  - answer: Aspose.PSD offers a fully functional trial that lets you evaluate all
      features before purchasing a license.
    question: Can I use Aspose.PSD for free?
  - answer: Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides, API references, and sample projects.
    question: Where can I find more examples and documentation?
  - answer: Temporary licenses are available through the Aspose portal at [Aspose.PSD
      Temporary License](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  - answer: It supports BMP, PNG, JPEG, TIFF, GIF, and native PSD among others.
    question: What image formats can Aspose.PSD export to?
  - answer: Yes, the library is designed for high‑throughput server environments and
      includes features such as multi‑threaded processing and memory‑efficient streaming.
    question: Is Aspose.PSD suitable for enterprise‑level workloads?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw ellipse
- Aspose.PSD
- Java graphics
- image processing
title: 如何在 Java 中使用 Aspose.PSD 庫繪製橢圓
url: /zh-hant/java/java-graphics-drawing/drawing-ellipses/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.PSD 庫繪製橢圓

## 介紹
在本教學中，您將學習 **如何在 Java 中使用 Aspose.PSD 庫繪製橢圓**。Aspose.PSD for Java 是一個強大的 API，讓您無需 Adobe Photoshop 即可建立、編輯與匯出 PSD 檔案。繪製橢圓等形狀是任何 Java 影像處理專案的核心技能，本指南將一步步帶您完成從專案設定到儲存最終位圖的全部過程。

## 快速回答
- **哪個庫最適合在 Java 中繪製橢圓？** Aspose.PSD for Java。  
- **需要多少行程式碼？** 大約十行，加上一些設定語句。  
- **開發是否需要授權？** 免費試用可用於測試；正式上線需購買商業授權。  
- **可以輸出為 BMP、PNG 或 JPEG 嗎？** 可以，Aspose.PSD 支援 BMP、PNG、JPEG 以及 PSD。  
- **此 API 是否相容於 Java 8 及以上版本？** 完全支援 Java 8‑21。

## Aspose.PSD for Java 是什麼？
Aspose.PSD for Java 是一個純 Java 庫，可程式化地建立、操作與轉換 Photoshop PSD 檔案。它支援超過 100 種影像格式，且能在不將整個文件載入記憶體的情況下處理高達 2 GB 的檔案。

## 為何使用 Aspose.PSD 繪製橢圓？
Aspose.PSD 提供高效能，能在數秒內處理多頁文件，並支援超過 100 種輸入與輸出格式，如 BMP、PNG、JPEG 與 PSD。它完全在 Java 中運行，無需本機 Photoshop，因而非常適合 CI/CD 流程與雲端服務。

## 前置條件
- 具備基本的 Java 程式設計知識。  
- 已安裝 JDK 8 或更新版本。  
- 使用 IntelliJ IDEA 或 Eclipse 等 IDE。  
- Aspose.PSD for Java 程式庫。可從 [Aspose.PSD for Java 下載頁面](https://releases.aspose.com/psd/java/) 下載。

## 匯入套件
首先，從 Aspose.PSD 命名空間匯入所需的類別。

## 如何在 Java 中繪製橢圓？
載入 Aspose.PSD 程式庫，建立空白的 PsdImage 畫布，取得 Graphics 物件，必要時清除背景，接著使用 Pen 物件搭配所需的顏色與樣式在 Rectangle 範圍內繪製橢圓。最後，以 BMP、PNG 或 JPEG 格式儲存影像。此流程通常不超過 15 行程式碼。

## 步驟 1：設定 Java 專案
在開始編寫程式碼之前，請確保專案已將 Aspose.PSD JAR 作為 Maven/Gradle 依賴項或加入至 classpath。

## 步驟 2：建立 PsdImage 實例
PsdImage 代表一個記憶體中的 Photoshop 文件，並提供繪圖畫布。

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

## 步驟 3：初始化 Graphics 物件
Graphics 提供繪圖方法，可在影像表面上繪製形狀。

```java
Image image = new PsdImage(100, 100);
```

## 步驟 4：清除 Graphics 表面
可選擇以背景顏色清除畫布，以確保繪圖區域乾淨。

```java
Graphics graphics = new Graphics(image);
```

## 步驟 5：繪製虛線橢圓
Pen 定義繪製形狀時輪廓的顏色與樣式。

```java
graphics.clear(Color.getYellow());
```

## 步驟 6：繪製實線橢圓
使用實心藍色筆刷的 Pen 為第二個橢圓建立實線輪廓。

```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```

## 步驟 7：儲存影像
BmpOptions 指定儲存影像的 BMP 格式設定。

```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```

```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## 常見問題與解決方案
- **影像顯示為空白：** 確認在繪製前已使用可見顏色呼叫 `graphics.clear()`。  
- **橢圓變形：** 請確認 `Rectangle` 的尺寸與影像的長寬比相符。  
- **大型檔案記憶體不足錯誤：** 使用 `PsdImage` 的串流 API 逐段處理檔案，而非一次載入整個文件。

## 常見問答

**Q: 我可以免費使用 Aspose.PSD 嗎？**  
A: Aspose.PSD 提供功能完整的試用版，讓您在購買授權前評估所有功能。

**Q: 我在哪裡可以找到更多範例與文件？**  
A: 請前往 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) 取得完整指南、API 參考與範例專案。

**Q: 我如何取得測試用的臨時授權？**  
A: 可於 Aspose 入口網站取得臨時授權，網址為 [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/)。

**Q: Aspose.PSD 能匯出哪些影像格式？**  
A: 支援 BMP、PNG、JPEG、TIFF、GIF 以及原生 PSD 等多種格式。

**Q: Aspose.PSD 適用於企業級工作負載嗎？**  
A: 是的，該程式庫針對高吞吐量的伺服器環境設計，具備多執行緒處理與記憶體效能優化的串流功能。

## 結論
現在您已擁有使用 Aspose.PSD 在 Java 中 **繪製橢圓** 的完整端對端範例。透過建立 `PsdImage`、使用 `Graphics` API，並設定 `Pen` 物件，即可繪製虛線與實線橢圓，並以支援的點陣圖格式儲存結果。將這些步驟整合至您的應用程式，即可產生動態圖形、縮圖或自訂 UI 元件，而無需依賴外部圖形編輯器。

---

**最後更新：** 2026-09-28  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose

## 相關教學

- [在 PSD 中使用 Aspose.PSD for Java 繪製並儲存矩形](/psd/java/basic-image-operations/simple-drawing/)
- [使用 Aspose.PSD for Java 重新調整影像大小 – 繪製形狀與基本影像操作](/psd/java/basic-image-operations/)
- [為影像添加簽名 – 使用 Aspose.PSD for Java 在畫布上繪製影像](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}