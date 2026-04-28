---
date: 2026-04-28
description: 學習如何使用 Aspose.PSD for Java 在畫布上繪製圖像，為圖像添加簽名。本 Java 圖像處理教學示範如何將圖像另存為 PNG
  並疊加圖形。
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: 在圖片上添加簽名
second_title: Aspose.PSD Java API
title: 在圖片上添加簽名 – 使用 Aspose.PSD for Java 在畫布上繪製圖片
url: /zh-hant/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在圖像上添加簽名 – 使用 Aspose.PSD for Java 在畫布上繪製圖像

## 簡介

在合約、發票或任何需要驗證真偽的文件中，加入手寫或數位的 **add signature to image** 是常見需求。在本教學中，您將看到 Aspose.PSD for Java 如何讓您 **draw image on canvas**，並將簽名視為另一個覆蓋層。我們將逐步說明載入基礎圖片、載入簽名檔案、初始化圖形上下文、繪製覆蓋層，最後 **save image as PNG**。完成後，您將擁有一個可重複使用的模式，適用於任何 **java image processing** 情境，無論是簽名、浮水印或標誌。

## 快速答案

- **What does “draw image on canvas” mean?** 它指的是使用 `Graphics` 類別將一個圖像渲染到另一個圖像上。  
- **How to add a signature in Java?** 將簽名檔案載入為 `Image`，並使用 `Graphics.drawImage`。  
- **Which Aspose.PSD version is required?** 任何近期的 24.x 版本皆可；程式碼可在最新的函式庫上運作。  
- **Can I overlay multiple images?** 可以——對不同來源重複呼叫 `drawImage`。  
- **Do I need a license?** 試用版可用於開發；正式環境需要商業授權。  

## 什麼是「Draw Image on Canvas」？

在 Aspose.PSD 的術語中，在畫布上繪製圖像是指使用 `Graphics` 上下文將一個 `Image` 物件繪製到另一個上。此操作是 **overlay images java** 技術的核心，例如添加浮水印、標誌或簽名。

## 為什麼使用 Aspose.PSD 來疊加簽名？

- **Full PSD support** – 完整的 PSD 支援 – 可處理圖層、遮色片與透明度。  
- **No native OS dependencies** – 無原生作業系統相依性 – 純 Java，適合伺服器端處理。  
- **High‑performance rendering** – 高效能渲染 – 為大型檔案與複雜合成進行最佳化。  

## 先決條件

- Java Development Kit (JDK) 8 或更高版本。  
- 已將 Aspose.PSD for Java JAR 加入專案的 classpath。  
- 兩個圖像檔案：基礎圖片（例如 `layers.psd`）以及簽名圖形（`sample.psd`）。  

## 匯入套件

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：載入主要與次要圖像

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** 保持兩個圖像使用相同的色彩模式 (RGB)，以避免繪製時出現意外的色彩偏移。

## 步驟 2：初始化圖形 (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` 物件就像畫筆，讓您 **draw image on canvas**。以主要的 `Image` 初始化它，會將所有後續的繪圖指令綁定到該畫布上。

## 步驟 3：將簽名加入圖像 (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

在此程式碼片段中，我們透過將簽名定位於右下角來 **overlay images java**。如果需要不同的位置，請調整 `Point` 的數值。

## 常見問題與解決方案

| 症狀 | 原因 | 解決方法 |
|---------|-------|-----|
| 簽名顯示失真 | 畫布與簽名的 DPI 不匹配 | 在繪製前使用 `signature.resize`，或確保兩個檔案使用相同的 DPI。 |
| 輸出檔案過大 | 未使用壓縮儲存 | 傳入已設定 `CompressionLevel` 為較高值的 `PngOptions`。 |
| 未繪製任何內容 | Graphics 未釋放 | 在繪製後呼叫 `graphics.dispose()`（可選，但建議這樣做）。 |

## 實務使用的額外提示

- **Multiple signatures:** 使用不同的 `Image` 物件和座標重複呼叫 `graphics.drawImage`。  
- **Opacity control:** 在繪製前使用 `graphics.setOpacity(float opacity)` 以使簽名半透明。  
- **Rotating the signature:** 若需要斜角簽名，請使用 `graphics.rotateTransform(angle)`。  
- **Saving to other formats:** 將 `PngOptions` 替換為 `JpegOptions` 或 `BmpOptions` 以輸出 JPEG、BMP 等格式。  

## 常見問答

### Q1: 我可以在圖像中添加多個簽名嗎？

A1: 可以，您可以透過對不同的簽名圖像重複步驟來添加多個簽名。

### Q2: Aspose.PSD 支援其他圖像格式嗎？

A2: 是的，Aspose.PSD 支援多種圖像格式，確保圖像處理的彈性。

### Q3: 使用 Aspose.PSD for Java 是否需要授權？

A3: 是的，使用 Aspose.PSD 需要有效的授權。請前往 [Purchase Aspose.PSD](https://purchase.aspose.com/buy) 了解授權細節。

### Q4: 我該如何取得 Aspose.PSD 的支援？

A4: 請前往 [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) 取得社群支援與討論。

### Q5: 我可以在購買前試用 Aspose.PSD for Java 嗎？

A5: 可以，您可以取得 [free trial](https://releases.aspose.com/) 以在購買前體驗功能。

**其他常見問答**

**Q: 如何變更簽名的不透明度？**  
A: 在呼叫 `drawImage` 前使用 `graphics.setOpacity(float opacity)`。值的範圍為 0.0 （透明）到 1.0 （不透明）。

**Q: 可以旋轉簽名嗎？**  
A: 可以——在繪製前透過 `graphics.rotateTransform(angle)` 套用變換矩陣。

**Q: 我可以將簽名繪製到 JPEG 而非 PNG 嗎？**  
A: 當然可以。將 `PngOptions` 替換為 `JpegOptions`，並指定所需的品質等級。

## 結論

透過上述步驟，您已學會使用 Aspose.PSD for Java **how to add signature to image**，即 **drawing an image on canvas**。相同的模式亦可延伸至浮水印、標誌或任何覆蓋圖形，為您的 Java 應用程式提供強大的 **java image processing** 功能。

---

**最後更新：** 2026-04-28  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}