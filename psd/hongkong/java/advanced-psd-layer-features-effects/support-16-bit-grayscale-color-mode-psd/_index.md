---
date: 2026-09-28
description: 了解如何使用 Aspose.PSD for Java 將 PSD 匯出為 PNG，並將 PSD 色彩模式設定為 16 位元灰階。提供逐步說明與程式碼範例。
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: 匯出 PSD 為 PNG – 16 位元灰階 – Java
og_description: 使用 Aspose.PSD for Java 將 PSD 匯出為 PNG（16 位元灰階）。依循此逐步教學以保留 65,536 種灰階色階。
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: 在 Java 中將 PSD 匯出為 PNG（16 位元灰階） – Aspose.PSD 指南
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: 如何在 Java 中將 PSD 匯出為 PNG 並使用 16 位元灰階色彩模式
url: /zh-hant/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中以 16 位元灰階色彩模式匯出 PSD 為 PNG

## 簡介
將 PSD 匯出為 PNG 同時保留 16 位元灰階色彩模式，可讓您獲得專業相片的色階深度與 PNG 的通用相容性。於本指南中，您將學會如何 **將 PSD 色彩模式設定為 16 位元灰階**，再 **使用 Aspose.PSD for Java 匯出 PSD 為 PNG**。本教學涵蓋從先決條件到除錯的全部內容，讓您能將此工作流程整合至任何基於 Java 的影像管線。

## 快速解答
- **「匯出 PSD 為 PNG」包含什麼步驟？** 載入 PSD，視需要變更色彩模式，然後儲存為 PNG 檔案。  
- **哪個 Aspose 類別負責轉換？** `PsdImage` 用於載入 PSD，`PngOptions` 定義 PNG 輸出設定。  
- **生產環境需要授權嗎？** 需要 – 試用版可用於測試，但商業使用必須購買授權。  
- **PNG 能保留 16 位元深度嗎？** 當然，只要使用 `PngColorType.GrayscaleWithAlpha` 即可。  
- **支援哪些 IDE？** 任何 Java IDE – IntelliJ IDEA、Eclipse、VS Code 或 NetBeans。

## 什麼是匯出 PSD 為 PNG？
匯出 PSD 為 PNG 是將 Adobe Photoshop 文件（PSD）轉換為可攜式網路圖形（PNG）檔案的過程，同時保留影像的像素資料與色彩深度。此轉換常用於在網路上分享高品質的灰階資產，且不會失去色調細節。

## 為什麼要以 16 位元灰階匯出 PSD 為 PNG？
以 PNG 匯出同時保留 16 位元灰階可保存 65 536 種灰階，遠比 8 位元影像提供更豐富的色調層次。PNG 的通用支援確保檔案可在瀏覽器、行動應用程式與桌面編輯器中無損顯示，而 Aspose.PSD 的無損壓縮則保證不會產生雜訊。

## 先決條件
在開始之前，請確保您已準備好以下項目：

1. **Java Development Kit (JDK)** – 從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 安裝最新的 JDK。  
2. **Aspose.PSD for Java library** – 從 [Aspose 下載頁面](https://releases.aspose.com/psd/java/) 下載 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 Visual Studio Code 都可完美運作。  
4. **基本的 Java 知識** – 您應熟悉建立類別、處理例外與操作檔案路徑。  
5. **範例 PSD 檔案** – 可在 Adobe Photoshop 中自行建立，或線上取得免費範本。

## 如何一步一步匯出 PSD 為 PNG

## 如何將 PSD 色彩模式設定為 16 位元灰階？
`PsdImage` 是 Aspose.PSD 用來載入與在記憶體中表示 PSD 檔案的類別。  
`ColorMode` 是一個列舉，定義 PSD 影像的色彩模式。

使用 `PsdImage` 載入 PSD，透過 `ColorMode` 屬性變更其色彩模式，然後儲存修改後的檔案。此操作全程在記憶體中完成，免除中間檔案需求，確保轉換快速且高效。

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

這些匯入讓您能存取操作 PSD 檔案、設定色彩模式以及將結果匯出為 PNG 所需的功能。

## 如何定義來源與輸出目錄？
`File` 是 java.io 的類別，代表檔案系統中的檔案或目錄路徑。

您需要告訴程式從哪裡讀取原始 PSD，以及將轉換後的 PNG 寫入哪裡。使用絕對或相對路徑皆可，但請在不同環境中保持一致，以免發生路徑解析錯誤。

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

將佔位字串替換為您機器上的實際路徑。

## 如何將轉換邏輯封裝成可重用的方法？
`convertPsdToPng` 是自訂方法，封裝了將 PSD 轉換為 PNG 所需的所有步驟與可選設定。

建立專屬方法可讓您在多個檔案或不同設定間重複使用相同的轉換流程。傳入來源路徑、目的資料夾以及可選的壓縮等參數，使工作流程具彈性且易於維護。

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

此方法讓您 **設定 PSD 色彩模式**，再 **匯出 PSD 為 PNG**，全部在同一流程中完成。

## 如何載入 PSD 並套用 16 位元灰階模式？
`PsdImage` 是 Aspose.PSD 用來將 PSD 檔案載入記憶體的類別。  
`ColorMode.GRAYSCALE_16` 是一個列舉值，用於將影像設定為 16 位元灰階。  
`channelBitsCount` 是一個屬性，指定每個通道的位元數。

在轉換方法內，組合完整檔案路徑，實例化 `PsdImage`，並將其 `ColorMode` 改為 `ColorMode.GRAYSCALE_16`。`channelBitsCount` 必須設為 16，才能保留高位元深度，確保影像保有全部色調資訊。

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` 用於追蹤每個匯出檔案所使用的設定。

## 如何在影像上繪製細微邊框（可選步驟）？
`Graphics` 是一個類別，提供在 `PsdImage` 畫布上繪圖的功能。

您可以選擇在影像周圍繪製一個灰色矩形，以便在測試時更清楚看到輸出結果。此步驟示範了如何操作圖層與圖形物件，且矩形會根據影像尺寸動態計算，保持置中。

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

矩形會根據影像尺寸動態計算，保持置中。

## 如何以新色彩模式儲存已修改的 PSD？
`PsdOptions` 是控制 PSD 檔案儲存方式的類別，包括色彩模式與位元深度設定。

在繪圖（或跳過此步驟）之後，對 `PsdImage` 實例呼叫 `save`，傳入保留 16 位元灰階設定的 `PsdOptions` 物件。這確保儲存的 PSD 保持期望的色彩模式且不會遺失資料。

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

## 如何在保留 16 位元深度的情況下將 PSD 轉換為 PNG？
`PngOptions` 是定義 PNG 輸出設定（如色彩類型與壓縮等級）的類別。  
`PngColorType.GrayscaleWithAlpha` 是一個列舉值，可將 16 位元灰階資料與 Alpha 通道一起儲存。

載入剛才儲存的 PSD，使用 `PngColorType.GrayscaleWithAlpha` 設定 `PngOptions`，然後呼叫 `save`。如此即可在 PNG 檔案中保留 16 位元灰階資料，提供無損、高品質的影像，適合後續處理或分發。

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

現在您已成功 **匯出 PSD 為 PNG**，同時保留高品質的 16 位元灰階資料。

## 常見問題與解決方案
| 問題 | 為何會發生 | 解決方式 |
|-------|----------------|-----|
| **「Unsupported color type」例外** | 嘗試以不支援的通道組態儲存 PSD。 | 確保 `channelBitsCount` 與實際位元深度（16）相符，且 `channelsCount` 對於灰階應為 1。 |
| **找不到檔案** | 來源目錄路徑不正確。 | 再次檢查 `sourceDir` 字串，並確認該位置確實存在 PSD 檔案。 |
| **輸出 PNG 顯示全黑** | PNG 儲存時未正確處理 Alpha。 | 如上例使用 `PngColorType.GrayscaleWithAlpha`。 |
| **大型 PSD 記憶體溢位** | 整個檔案一次載入記憶體。 | 透過 `PsdImage.load(inputStream, new LoadOptions())` 開啟串流模式，以有效處理大型檔案。 |

## 常見問答

**Q: 什麼是 16 位元灰階色彩模式？**  
A: 它提供 65 536 種灰階，較標準的 8 位元（256 種）呈現出更豐富的色調細節。

**Q: 我可以將 Aspose.PSD 用於非灰階影像嗎？**  
A: 當然可以！Aspose.PSD 支援 RGB、CMYK、Lab、索引色等多種色彩模式。

**Q: Aspose.PSD 有試用版嗎？**  
A: 有，您可以試用免費的 Aspose.PSD 版。只需前往 [Aspose 下載頁面](https://releases.aspose.com/)。

**Q: 哪裡可以找到更多 Aspose.PSD 範例？**  
A: 請參考官方 [文件](https://reference.aspose.com/psd/java/) 內的深入教學、API 參考與範例專案。

**Q: 如何購買 Aspose.PSD 的授權？**  
A: 您可前往 [Aspose 購買頁面](https://purchase.aspose.com/buy) 取得授權。

**最後更新：** 2026-09-28  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時最新）  
**作者：** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 轉換 PSD 為 PNG 並指定位元深度](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [使用 Aspose.PSD for Java 匯出 PSD 為 PNG 並套用圖層效果](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [使用 Aspose.PSD for Java 儲存 PSD 為 JPEG 並支援 RGB 色彩](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}