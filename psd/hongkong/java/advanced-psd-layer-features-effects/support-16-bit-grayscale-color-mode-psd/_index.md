---
date: 2025-12-17
description: 學習如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG，同時將 PSD 色彩模式設定為 16 位元灰階。逐步指南，附有程式碼範例。
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中將 PSD 轉換為 16 位元灰階色彩模式的 PNG
url: /zh-hant/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 轉換為 PNG（使用 16 位元灰階色彩模式）於 Java

## 簡介
當您踏入平面設計與影像處理的領域時，了解如何 **將 PSD 轉換為 PNG** 就像掌握了一把祕密武器。特別是使用 16‑bit 灰階模式，能為影像帶來驚人的深度與細節，讓畫面更加突出。在本教學中，我們將示範如何 **設定 PSD 色彩模式** 為 16‑bit 灰階，然後使用 Aspose.PSD for Java **將 PSD 匯出為 PNG**。準備好提升您的影像工作流程了嗎？讓我們開始吧。

## 快速答覆
- **「將 PSD 轉換為 PNG」包含哪些步驟？** 載入 PSD、（可選）變更色彩模式，最後儲存為 PNG 檔案。  
- **哪個 Aspose 類別負責轉換？** `PsdImage` 用於載入，`PngOptions` 用於儲存。  
- **需要特別授權嗎？** 試用版可用於測試；正式環境需購買授權。  
- **能在 PNG 中保留 16‑bit 深度嗎？** 可以，使用 `PngColorType.GrayscaleWithAlpha`。  
- **支援哪些 IDE？** 任何 Java IDE – IntelliJ IDEA、Eclipse、VS Code 等皆可。

## 先決條件
在開始之前，請確保已完成以下設定，以便順利完成本教學。您需要：

1. **Java Development Kit (JDK)** – 請確保已安裝最新版本，可從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java Library** – 這是操作 PSD 檔案的核心引擎，請從 [Aspose 下載頁面](https://releases.aspose.com/psd/java/) 取得。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 Visual Studio Code 都可。  
4. **基本的 Java 知識** – 熟悉 Java 語法會讓步驟更順暢。  
5. **範例 PSD 檔案** – 可自行在 Adobe Photoshop 中建立，或線上下載免費範本。

準備好了嗎？太好了！讓我們匯入必要的套件並開始編寫程式碼。

## 匯入套件
首先，將所需的 Aspose.PSD 套件加入您的 Java 檔案：

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

這些匯入讓您可以存取操作 PSD、設定色彩模式以及匯出 PNG 所需的功能。

## 步驟 1：定義目錄
先設定來源與輸出資料夾，讓程式知道從哪裡讀取原始 PSD、以及把轉換後的檔案寫到哪裡。

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

請將佔位字串替換為您電腦上實際的路徑。

## 步驟 2：建立處理影像的 Method
我們將轉換邏輯封裝在可重複使用的方法中。此方法接受您可能想調整的參數，例如色彩模式、位元深度與壓縮方式。

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

此方法讓您 **設定 PSD 色彩模式** 後，再 **將 PSD 匯出為 PNG**，流程一次完成。

## 步驟 3：定義檔案路徑並載入 PSD
在方法內組合完整的檔案路徑，並載入原始的 16‑bit 灰階 PSD：

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` 用來記錄每次匯出檔案所使用的設定，方便辨識。

## 步驟 4：處理圖層或完整影像
接下來，我們會在特定圖層或整張影像上繪製。本例中，我們加上一條細微的灰色邊框，以提升結果的可見度。

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

矩形會動態計算，確保無論影像大小如何，都能保持置中。

## 步驟 5：儲存已修改的 PSD 檔案
繪製完畢後，我們依照您指定的色彩模式與位元深度儲存 PSD。這正是 **設定 PSD 色彩模式** 後進行轉換的核心步驟。

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## 步驟 6：將 PSD 轉換為 PNG
最後，載入剛剛儲存的 PSD，並以 PNG 格式匯出。使用 `PngColorType.GrayscaleWithAlpha` 可在 PNG 中保留 16‑bit 深度。

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

現在您已成功 **將 PSD 轉換為 PNG**，同時保留了高品質的 16‑bit 灰階資料。

## 常見問題與解決方案
| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| **「Unsupported color type」例外** | 嘗試以不支援的通道組合儲存 PSD。 | 確認 `channelBitsCount` 與實際位元深度（16）相符，且 `channelsCount` 為灰階所需的 1。 |
| **找不到檔案** | 來源目錄路徑錯誤。 | 再次檢查 `sourceDir` 字串，並確認 PSD 檔案確實存在。 |
| **輸出 PNG 為全黑** | PNG 儲存時未正確處理 Alpha 通道。 | 如上例使用 `PngColorType.GrayscaleWithAlpha`。 |

## 常見問答

**Q：什麼是 16‑bit 灰階色彩模式？**  
A：它提供 65 536 種灰階階調，較標準的 8‑bit（256 階調）呈現出更豐富的色調細節。

**Q：我可以在非灰階影像上使用 Aspose.PSD 嗎？**  
A：當然可以！Aspose.PSD 支援 RGB、CMYK、Lab 等多種色彩模式。

**Q：Aspose.PSD 有試用版嗎？**  
A：有，您可以免費試用 Aspose.PSD。只要前往 [Aspose 下載頁面](https://releases.aspose.com/) 即可。

**Q：哪裡可以找到更多 Aspose.PSD 的範例？**  
A：請參考 [文件說明](https://reference.aspose.com/psd/java/)，裡面有更深入的範例與教學。

**Q：如何購買 Aspose.PSD 的授權？**  
A：請前往 [Aspose 購買頁面](https://purchase.aspose.com/buy) 取得授權。

---

**最後更新日期：** 2025-12-17  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}