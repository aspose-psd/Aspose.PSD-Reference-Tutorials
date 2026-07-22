---
date: 2026-07-22
description: 了解如何使用 Aspose.PSD 在 Java 中將 PSD 另存為 PNG、保留 PNG 透明度，並旋轉 PSD 圖層。提供逐步指南、免寫程式碼說明與故障排除技巧。
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: 使用 Aspose.PSD 在 Java 中將 PSD 另存為 PNG 並旋轉圖層
og_description: 使用 Aspose.PSD for Java 將 PSD 另存為 PNG。保留透明度、旋轉圖層，僅需幾行程式碼即可匯出 PNG，適用於自動化工作流程。
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: 使用 Aspose.PSD 在 Java 中將 PSD 另存為 PNG 並旋轉圖層
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: 使用 Aspose.PSD 在 Java 中將 PSD 另存為 PNG 並旋轉圖層
url: /zh-hant/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## 相關教學

- [Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [How to compress PNG files using Aspose.PSD for Java](/psd/java/optimizing-png-files/compress-png-files/)
- [How to Rotate Image in Java with Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# 在 Java 中使用 Aspose.PSD 將 PSD 另存為 PNG 並旋轉圖層

## 簡介
如果您需要 **將 PSD 另存為 PNG** 同時旋轉圖層，本指南適合您。無論您是在構建批次處理工具、需要即時圖像處理的 Web 服務，或只是想自動化設計工作流程，程式化操作都能節省時間並消除對 Adobe Photoshop 的依賴。在本教學中，我們將示範如何 **旋轉 PSD 圖層** 並使用 Aspose.PSD for Java 將結果匯出為 PNG。讓我們捲起袖子，讓您的設計工作流程順暢運作！

## 快速解答
- **可以使用哪個函式庫？** Aspose.PSD for Java  
- **能否一次完成旋轉與將 PSD 另存為 PNG？** 可以 – 先旋轉 PSD 再另存為 PNG  
- **需要授權嗎？** 免費試用可用於測試；正式環境需購買授權  
- **支援哪個 Java 版本？** Java 8 及以上  
- **PNG 輸出會保留透明度嗎？** 會，設定 `PngColorType.TruecolorWithAlpha` 即可

## 什麼是「將 PSD 轉換為 PNG」？
將 Photoshop 文件（PSD）轉換為 PNG 圖像，會將視覺內容——包括圖層、遮色片與 Alpha 通道——提取到一種廣泛支援的點陣格式，並保留透明度。這使得 PNG 成為網頁圖形、縮圖以及後續圖像處理的理想選擇。產生的 PNG 可直接用於網頁、行動應用程式，或由其他圖像函式庫進一步處理。

## 為什麼使用 Aspose.PSD for Java 來將 PSD 另存為 PNG 並旋轉 PSD 圖層？
Aspose.PSD 讓您 **將 PSD 另存為 PNG** 並旋轉圖層，無需安裝 Photoshop。它支援 **超過 50 種輸入與輸出格式**，在使用不到 200 MB 記憶體的情況下處理多頁 PSD 檔，且可在 Windows、Linux 與 macOS 上執行。API 僅需少量方法呼叫，即可提供高保真度的結果，內建圖層效果、遮色片與 Alpha 通道的處理。

## 先決條件
在開始撰寫程式碼之前，請確保您已具備以下項目：

- **Java Development Kit (JDK)** – 從 [Oracle 官方網站](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
- **整合開發環境 (IDE)** – IntelliJ IDEA、Eclipse 或 NetBeans 都可以。  
- **Aspose.PSD for Java 函式庫** – 從 [發行頁面](https://releases.aspose.com/psd/java/) 取得最新 JAR。  
- **基本的 Java 知識** – 熟悉類別、物件與例外處理。

## 逐步指南

### 步驟 1：設定 Java 專案
在 IDE 中建立新 Java 專案，並將 Aspose.PSD JAR 加入專案的建置路徑。

### 步驟 2：匯入必要類別
`PsdImage` 是代表 Photoshop 文件的核心類別。`PngOptions` 控制 PNG 的特定設定，`RotateFlipType` 定義旋轉與翻轉操作。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

這些匯入讓您可以存取圖像載入、旋轉以及 PNG 專屬的選項。

### 步驟 3：定義檔案路徑
指定來源 PSD 的位置以及輸出檔案的寫入路徑。測試時使用絕對路徑可避免「找不到檔案」的錯誤。

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **專業提示：** 在較大的專案中，將路徑寫入設定檔以便維護。

### 步驟 4：載入 PSD 檔案
`PsdImage` 會將整個 Photoshop 文件（包括所有圖層、遮色片與效果）載入為可操作的物件。

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

此時 `im` 代表完整的 PSD，已可進行後續轉換。

### 步驟 5：旋轉圖像（如何旋轉 PSD）
`RotateFlipType` 列舉了所有支援的旋轉與翻轉方式。此範例將圖像旋轉 270° 並同時在兩個軸翻轉，會交換寬高並鏡像圖像。

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

您也可以嘗試其他值，例如 `Rotate90FlipNone` 或 `Rotate180FlipX`。

### 步驟 6：將旋轉後的圖像另存為 PNG（save PSD as PNG）
設定 `PngOptions` 以保留透明度（`PngColorType.TruecolorWithAlpha`），然後呼叫 `save`。PNG 會保留圖層的透明資訊，確保在 Web 或行動應用中順利使用。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

產生的 PNG 保留 Alpha 通道，適合合成或進一步處理。

### 步驟 7：另存修改後的 PSD（可選）
如果您也需要一個已套用旋轉的 PSD 檔案，可將修改後的 `PsdImage` 再寫回磁碟。

```java
im.save(psdPath);
```

現在您同時擁有 PNG 預覽與更新後的 PSD 檔案。

## 常見問題與解決方案
- **找不到檔案：** 確認 `dataDir` 以路徑分隔符（`/` 或 `\`）結尾。  
- **大型 PSD 記憶體不足（OutOfMemoryError）：** 增加 JVM 堆積大小（`-Xmx2g`）。  
- **透明度遺失：** 必須設定 `PngColorType.TruecolorWithAlpha`，否則 PNG 會失去 Alpha。  
- **翻轉 PSD 圖像行為異常：** 再次檢查所選的 `RotateFlipType` 常數，有些常數會同時執行旋轉與翻轉。

## 常見問答

**Q: 能否只旋轉 PSD 中的特定圖層？**  
A: 可以，在遍歷 `im.getLayers()` 後呼叫 `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`。

**Q: Aspose.PSD for Java 有性能限制嗎？**  
A: 函式庫對大多數檔案都能有效處理，但極大型 PSD（>500 MB）可能需要額外記憶體或串流選項。

**Q: Aspose.PSD 可以免費使用嗎？**  
A: 提供免費試用，但正式環境需購買授權。請參考 [temporary license](https://purchase.aspose.com/temporary-license/) 進行測試。

**Q: 哪裡可以找到詳細文件？**  
A: 完整文件位於 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)。

**Q: 若使用 Aspose.PSD 時遇到問題該怎麼辦？**  
A: 可透過 [Aspose Support Forum](https://forum.aspose.com/c/psd/34) 取得協助。

**Q: 轉換 PSD 為 PNG 時會保留圖層效果嗎？**  
A: 會，使用 `PngColorType.TruecolorWithAlpha` 時，大多數視覺效果會被光柵化至 PNG。

**Q: 能否批次處理多個 PSD 檔案？**  
A: 當然可以，將程式碼包在遍歷 PSD 目錄的迴圈中即可。

**Q: 可以設定 PNG 壓縮等級嗎？**  
A: `PngOptions` 提供 `setCompressionLevel(int)` 方法，可微調輸出大小。

**Q: 是否需要關閉圖像物件？**  
A: `PsdImage` 實作 `Closeable`；請使用 try‑with‑resources 或在 `finally` 區塊呼叫 `im.close()`。

**Q: 旋轉後的 PNG 會保留原始尺寸嗎？**  
A: 旋轉 90° 或 270° 會交換寬高，PNG 會自動反映新的方向。

## 結論
透過 Aspose.PSD for Java，您可以 **將 PSD 另存為 PNG**、**保留 PNG 透明度**，以及 **旋轉 PSD 圖層**，僅需幾行程式碼。此方法免除 Photoshop 的需求，加速自動化工作流程，並讓您完整掌控圖像輸出。立即在您的專案中試試，體驗時間上的巨大節省！

---

**最後更新：** 2026-07-22  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}