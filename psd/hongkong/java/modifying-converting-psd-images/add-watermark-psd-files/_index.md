---
date: 2026-03-07
description: 學習如何在 PSD 檔案中使用 Aspose.PSD for Java 建立圖像水印 – 快速指南，適用於 PSD 圖像處理與保護您的圖形。
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 在 PSD 檔案中建立圖片浮水印
url: /zh-hant/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 為 PSD 檔案添加水印

## 簡介
水印是一種細緻卻有效的方式，可保護您的圖像並傳達所有權。在本教學中，您將學會如何使用 Aspose.PSD for Java 在 PSD 檔案中 **create image watermark**。無論您是展示作品集的攝影師，還是呈現最新設計的設計師，添加水印對於維護品牌識別都至關重要。現在，端上一杯咖啡，找個舒適的地方，讓我們開始吧！

## 快速回答
- **主要目標是什麼？** 程式化地在 PSD 檔案中建立影像水印。  
- **使用哪個函式庫？** Aspose.PSD for Java。  
- **實作需要多長時間？** 基本水印大約需要 10‑15 分鐘。  
- **主要前置條件是什麼？** Java JDK、Aspose.PSD 函式庫，以及來源 PSD 檔案。  
- **我可以將結果匯出為 PNG 嗎？** 可以 – 使用 `save` 方法搭配 `PngOptions`。

## 什麼是 **create image watermark**？
建立影像水印是指以程式方式在圖像檔上疊加半透明的文字或圖形，將所有權資訊直接嵌入視覺內容中。

## 為什麼在 PSD 影像處理上使用 Aspose.PSD for Java？
Aspose.PSD 提供豐富的 API 供 **psd image processing** 使用，讓您能在不需要 Photoshop 的情況下操作圖層、套用效果並渲染最終圖像。它支援高保真渲染、批次操作，且可在所有主流作業系統上執行。

## 前置條件
在開始編寫程式碼之前，請確保您已具備以下項目：

1. **Java Development Kit (JDK)** – 任意近期版本（8 或以上）。  
2. **Aspose.PSD for Java Library** – 從 [Aspose website](https://releases.aspose.com/psd/java/) 下載。  
3. **IDE** – Eclipse、IntelliJ IDEA，或您偏好的任何編輯器。  
4. **PSD 檔案** – 名為 `layers.psd` 的範例檔案，放置於工作目錄中。  
5. **基本的 Java 知識** – 熟悉類別、物件與檔案 I/O。

## 匯入套件
現在您已完成所有設定，讓我們匯入必要的套件。Java 的 import 可讓您從各種函式庫中取得類別與功能，使程式碼更有效率。以下是您需要的內容：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## 如何 **create image watermark** – 步驟指南

### 步驟 1：設定目錄
首先，我們需要設定 PSD 檔案所在的路徑。這一步相當重要，因為 Java 必須知道在哪裡尋找檔案。

```java
String dataDir = "Your Document Directory";
```

將 `Your Document Directory` 替換為實際包含 `layers.psd` 的資料夾路徑。

### 步驟 2：載入 PSD 檔案
接著，我們會載入 PSD 檔案並將其轉型為 `PsdImage`。此步驟會將檔案轉換為可供操作的格式。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

把它想像成打開一本書，讓您可以在頁面上寫字。

### 步驟 3：建立 Graphics 物件
PSD 檔案載入後，我們需要建立一個 `Graphics` 物件。它讓我們能執行繪圖操作——就像為畫布拿起畫筆一樣。

```java
Graphics graphics = new Graphics(psdImage);
```

### 步驟 4：為水印定義字型
現在是選擇水印外觀的時候。我們將使用 Arial，字型大小為 20。您可以自行更換字型名稱或大小，以符合品牌風格。

```java
Font font = new Font("Arial", 20.0f);
```

### 步驟 5：建立實心筆刷以進行水印繪製
實心筆刷決定水印的顏色與不透明度。我們將 alpha 設為 50（255 為滿值），以取得半透明的灰色。

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

此處，`Color.fromArgb(50, 128, 128, 128)` 會產生 50% 不透明度的灰色——非常適合作為低調簽名。

### 步驟 6：設定文字對齊方式以放置水印
為確保水印正好置於影像中心，我們會設定字串對齊選項。

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### 步驟 7：使用 **java graphics drawstring** 繪製水印
現在進入最精彩的部分。當 graphics context 準備好後，我們會使用 `java graphics drawstring` 將水印文字繪製到影像上。

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

將 `"Some watermark text"` 替換為您希望出現在 PSD 上的實際文字。

### 步驟 8：**Save PSD as PNG** – **export psd png**
水印完成後，我們會 **save psd png**（即將 PSD 匯出為 PNG），讓結果能在任何瀏覽器或影像檢視器中顯示。

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

執行此行程式碼會產生一個包含水印的 PNG 檔案。

## 常見問題與解決方案
- **Watermark not visible?** 請檢查 `Color.fromArgb()` 中的 alpha 值；數值過低會使水印過於透明。  
- **Incorrect dimensions?** 請確保使用 `psdImage.getWidth()` 與 `psdImage.getHeight()` 來設定矩形，讓文字能隨影像尺寸縮放。  
- **License exceptions?** 評估授權可用於測試，但正式上線必須使用正式授權。

## 常見問答

**Q: 我可以自訂水印文字嗎？**  
A: 當然可以！只要在 `drawString` 方法中替換字串為您想要的文字即可。

**Q: 想換其他字型怎麼辦？**  
A: 將 `Font` 的實例化改為任意已安裝的字型，例如 `new Font("Times New Roman", 24.0f)`。

**Q: 有辦法調整不透明度嗎？**  
A: 有的——修改 `Color.fromArgb(alpha, r, g, b)` 的第一個參數。alpha 數值越低，透明度越高。

**Q: 除了 PNG，還能使用其他影像格式嗎？**  
A: 可以。將 `new PngOptions()` 換成 `new JpegOptions()` 或 `new BmpOptions()`，即可 **save psd png** 為其他格式。

**Q: 哪裡可以取得更多協助？**  
A: 如需更深入的問題，請造訪 [Aspose forums](https://forum.aspose.com/c/psd/34) 或參考他們的 [documentation](https://reference.aspose.com/psd/java/)。

## 結論
您現在已學會如何使用 Aspose.PSD for Java 在 PSD 檔案中 **create image watermark**。此技巧不僅能保護您的內容，還能加強品牌在所有視覺資產中的存在感。可自行嘗試不同的字型、顏色與不透明度，以符合您的風格，並記得您可以 **save psd png** 或 **export psd png** 為任何需要的格式。

---

**最後更新：** 2026-03-07  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}