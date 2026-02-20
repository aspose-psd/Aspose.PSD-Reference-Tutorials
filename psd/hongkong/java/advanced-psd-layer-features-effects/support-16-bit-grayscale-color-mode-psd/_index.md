---
date: 2026-02-20
description: 學習如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG，並將 PSD 色彩模式設定為 16 位元灰階。提供逐步說明與程式碼範例。
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中將 PSD 轉換為 16 位元灰階色彩模式的 PNG
url: /zh-hant/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

}}

All preserved.

Now produce final content with translations.

Make sure to keep code block placeholders unchanged.

Let's construct final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 將 PSD 轉換為 PNG（16 位元灰階色彩模式）

## 介紹
當你踏入平面設計與影像處理的世界時，了解 **如何將 PSD 轉換為 PNG** 就像擁有一把祕密武器。使用 16‑bit 灰階模式能帶來驚人的深度與色調豐富度，讓你的影像脫穎而出。在本教學中，我們將示範如何 **設定 PSD 色彩模式** 為 16‑bit 灰階，然後使用 Aspose.PSD for Java **將 PSD 匯出為 PNG**。準備好提升你的影像工作流程了嗎？讓我們開始吧。

## 快速解答
- **「convert PSD to PNG」是什麼意思？** 載入 PSD，視需要變更其色彩模式，然後儲存為 PNG 檔案。  
- **哪個 Aspose 類別負責轉換？** 用 `PsdImage` 載入，`PngOptions` 儲存。  
- **需要特別授權嗎？** 測試可使用試用版，正式環境需購買授權。  
- **能在 PNG 中保留 16 位元深度嗎？** 可以，使用 `PngColorType.GrayscaleWithAlpha`。  
- **支援哪些 IDE？** 任意 Java IDE，例如 IntelliJ IDEA、Eclipse、VS Code 等。

## 為什麼要將 PSD 轉換為 16 位元灰階 PNG？
* **保留色調細節：** 16 位元灰階可儲存 65,536 種灰階，比 8 位元的 256 種多得多。  
* **廣泛相容性：** PNG 在瀏覽器、行動應用程式與桌面工具上都有廣泛支援，同時保留高品質資料。  
* **無損工作流程：** 使用 Aspose.PSD 轉換可避免不必要的壓縮雜訊，適合存檔或後續處理。

## 前置條件
在開始之前，先確保已完成以下設定，以獲得最佳教學體驗。你需要：

1. **Java Development Kit (JDK)** – 確保已安裝最新版本。可從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java Library** – 這是操作 PSD 檔案的引擎。可從 [Aspose 下載頁面](https://releases.aspose.com/psd/java/) 取得。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 Visual Studio Code 都可使用。  
4. **基本的 Java 知識** – 熟悉 Java 語法會讓步驟更順暢。  
5. **範例 PSD 檔案** – 可自行在 Adobe Photoshop 中建立，或線上下載免費範例。

準備好了嗎？太好了！讓我們匯入必要的套件並開始編寫程式碼。

## 匯入套件
要開始動手，先在 Java 檔案中加入所需的 Aspose.PSD 匯入語句：

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

這些匯入讓你可以使用操作 PSD 檔案、設定色彩模式以及將結果匯出為 PNG 的功能。

## 步驟 1：定義目錄
首先，設定來源與輸出資料夾。這告訴程式從哪裡讀取原始 PSD，並將轉換後的檔案寫入哪裡。

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

將佔位字串替換為你機器上的實際路徑。

## 步驟 2：建立處理影像的 Method
我們將把轉換邏輯封裝在可重複使用的方法中。它會接受所有可能需要調整的參數，例如色彩模式、位元深度與壓縮方式。

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

此方法讓你 **設定 PSD 色彩模式**，然後 **將 PSD 匯出為 PNG**，一次完成。

## 步驟 3：定義檔案路徑並載入 PSD
在方法內部，組合完整的檔案路徑並載入原始的 16‑bit 灰階 PSD：

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` 用來記錄每個匯出檔案所使用的設定。

## 步驟 4：處理圖層或完整影像
現在我們可以在特定圖層或整張影像上繪圖。此範例會加上一條細微的灰色邊框，使結果更易辨識。

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
繪製完成後，我們會以你指定的色彩模式與位元深度儲存 PSD。這正是 **設定 PSD 色彩模式** 後轉換的核心步驟。

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
最後，我們載入剛剛儲存的 PSD，並匯出為 PNG。透過使用 `PngColorType.GrayscaleWithAlpha`，即可在 PNG 檔案中保留 16‑bit 深度。

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

現在你已成功 **將 PSD 轉換為 PNG**，同時保留高品質的 16‑bit 灰階資料。

## 常見問題與解決方案
| 問題 | 為何發生 | 解決方法 |
|------|----------|----------|
| **「Unsupported color type」例外** | 嘗試以不支援的通道配置儲存 PSD。 | 確保 `channelBitsCount` 與實際位元深度（16）相符，且 `channelsCount` 為灰階（1）正確值。 |
| **找不到檔案** | 來源目錄路徑不正確。 | 再次確認 `sourceDir` 字串，並確保 PSD 檔案存在。 |
| **輸出 PNG 為全黑** | PNG 儲存時未處理 Alpha 通道。 | 如上所示使用 `PngColorType.GrayscaleWithAlpha`。 |

## 常見問答

**Q: 什麼是 16 位元灰階色彩模式？**  
A: 它提供 65,536 種灰階，遠比標準的 8‑bit（256 種）呈現更多色調細節。

**Q: 可以將 Aspose.PSD 用於非灰階影像嗎？**  
A: 當然可以！Aspose.PSD 支援 RGB、CMYK、Lab 等多種色彩模式。

**Q: 有 Aspose.PSD 的試用版嗎？**  
A: 有，你可以試用免費的 Aspose.PSD 版。只要前往 [Aspose 下載頁面](https://releases.aspose.com/) 即可。

**Q: 哪裡可以找到更多 Aspose.PSD 的使用範例？**  
A: 可參考 [文件說明](https://reference.aspose.com/psd/java/) 取得更深入的範例與教學。

**Q: 如何購買 Aspose.PSD 的授權？**  
A: 前往 [Aspose 購買頁面](https://purchase.aspose.com/buy) 即可購買授權。

---

**最後更新：** 2026-02-20  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}