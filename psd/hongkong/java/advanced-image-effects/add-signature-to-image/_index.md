---
date: 2025-12-02
description: 學習如何在畫布上繪製圖像並在 Java 中使用 Aspose.PSD 疊加簽名。遵循此一步一步的 Java 圖像處理教學，並將結果儲存為
  PNG。
language: zh-hant
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: 在畫布上繪製圖像 – 使用 Aspose.PSD for Java 添加簽名
url: /java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在畫布上繪製圖像 – 使用 Aspose.PSD for Java 添加簽名

## 簡介

在圖片上添加手寫或數位簽名是合約、發票或任何需要驗證真偽的文件的常見需求。使用 **Aspose.PSD for Java**，您可以 **draw image on canvas**，將簽名視為另一個覆蓋層。在本 **java image processing tutorial** 中，我們將逐步說明整個工作流程——從載入基礎圖片與簽名檔案、初始化 graphics、繪製覆蓋層，最後 **save image png java** 方式保存。

## 快速解答
- **What does “draw image on canvas” mean?** 它指的是使用 `Graphics` 類將一張圖像渲染到另一張圖像上。  
- **How to add a signature in Java?** 將簽名檔案載入為 `Image`，然後使用 `Graphics.drawImage`。  
- **Which Aspose.PSD version is required?** 任何近期的 24.x 版本皆可；程式碼在最新的函式庫上可正常運作。  
- **Can I overlay multiple images?** 可以——對不同來源重複呼叫 `drawImage`。  
- **Do I need a license?** 試用版可用於開發；正式環境需商業授權。

## “在畫布上繪製圖像” 是什麼？

在 Aspose.PSD 的術語中，於畫布上繪製圖像是指使用 `Graphics` 內容將一個 `Image` 物件繪製到另一個上。此操作是 **overlay images java** 技術的核心，例如添加浮水印、標誌或簽名。

## 為何使用 Aspose.PSD 來覆蓋簽名？

- **Full PSD support** – 支援圖層、遮色片與透明度。  
- **No native OS dependencies** – 純 Java，適合伺服器端處理。  
- **High‑performance rendering** – 為大型檔案與複雜合成優化。  

## 前置條件
- Java Development Kit (JDK) 8 或以上。  
- 已將 Aspose.PSD for Java JAR 加入專案的 classpath。  
- 兩個圖像檔案：基礎圖片（例如 `layers.psd`）與簽名圖形（`sample.psd`）。  

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

> **Pro tip:** 保持兩個圖像使用相同的色彩模式 (RGB)，以免在繪製時出現意外的色彩偏移。

## 步驟 2：初始化 Graphics（initialize graphics java）

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` 物件如同畫筆，讓您 **draw image on canvas**。以主要的 `Image` 初始化後，所有後續的繪圖指令皆作用於該畫布。

## 步驟 3：將簽名加入圖像（how to add signature）

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

在此程式碼片段中，我們透過將簽名定位於右下角來 **overlay images java**。若需其他位置，請調整 `Point` 的數值。

## 常見問題與解決方案

| 症狀 | 原因 | 解決方法 |
|---------|-------|-----|
| 簽名顯示失真 | 畫布與簽名的 DPI 不匹配 | 在繪製前使用 `signature.resize`，或確保兩個檔案使用相同的 DPI。 |
| 輸出檔案過大 | 未使用壓縮直接儲存 | 傳入已設定 `CompressionLevel` 較高的 `PngOptions`。 |
| 未繪製任何內容 | `Graphics` 未釋放 | 繪製完成後呼叫 `graphics.dispose()`（雖非必須，但為良好慣例）。 |

## 結論

透過上述步驟，您已學會 **how to draw image on canvas**，並使用 Aspose.PSD for Java 無縫 **add a signature**。此技術可延伸至浮水印、標誌或任何覆蓋圖形，為您的 Java 應用程式提供強大的 **java image processing** 能力。

## 常見問答

### Q1：我可以在同一張圖像上添加多個簽名嗎？

A1：可以，您只需對不同的簽名圖像重複上述步驟即可。

### Q2：Aspose.PSD 支援其他圖像格式嗎？

A2：支援，Aspose.PSD 支援多種圖像格式，確保圖像處理的彈性。

### Q3：使用 Aspose.PSD for Java 是否需要授權？

A3：是，需要有效的授權才能使用 Aspose.PSD。請前往 [Purchase Aspose.PSD](https://purchase.aspose.com/buy) 了解授權細節。

### Q4：如何取得 Aspose.PSD 的支援？

A4：請造訪 [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) 取得社群支援與討論。

### Q5：購買前我可以先試用 Aspose.PSD for Java 嗎？

A5：可以，您可取得 [free trial](https://releases.aspose.com/) 以在購買前體驗功能。

## 其他常見問題

**Q: 如何變更簽名的不透明度？**  
A: 在呼叫 `drawImage` 前使用 `graphics.setOpacity(float opacity)`。值的範圍為 0.0 （透明）至 1.0 （不透明）。

**Q: 可以旋轉簽名嗎？**  
A: 可以——在繪製前透過 `graphics.rotateTransform(angle)` 套用變換矩陣。

**Q: 能否將簽名繪製到 JPEG 而非 PNG？**  
A: 當然可以。將 `PngOptions` 換成 `JpegOptions`，並指定所需的品質等級。

---

**最後更新：** 2025-12-02  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}