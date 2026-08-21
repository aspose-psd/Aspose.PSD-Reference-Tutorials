---
date: 2026-06-23
description: 了解如何在 Java 中使用 Aspose.PSD 將 PSD 轉換為 PNG 並按比例調整圖像大小。本分步教學涵蓋圖像快取、調整大小以及儲存為
  PNG。
keywords:
- convert psd to png
- save psd as png
- how to cache image
- resize image without distortion
- proportional image scaling
linktitle: 將 PSD 轉換為 PNG 並按比例調整大小
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  headline: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for
    Java
  type: TechArticle
- description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  name: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – Java 8 or later installed.'
    text: '**Java Development Kit (JDK)** – Java 8 or later installed.'
  - name: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
  - name: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
    text: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
  type: HowTo
- questions:
  - answer: Aspose.PSD supports PSD, PNG, JPEG, BMP, GIF, and many more. See the full
      list in the [documentation](https://reference.aspose.com/psd/java/). For the
      full API reference, see the guide **here**.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Purchase a commercial license on the [Aspose store](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Absolutely – request a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Are temporary licenses available for testing?
  - answer: The [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) is a great place
      to ask questions and share solutions.
    question: Where can I find community support?
  - answer: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).
    question: How do I access the full API reference?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並按比例調整大小
url: /zh-hant/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並按比例調整大小

## 簡介

## 快速回答
- **Aspose.PSD 能將 PSD 轉換為 PNG 嗎？** 是 – 只需載入 PSD 並使用 `PngOptions` 儲存。
- **此函式庫支援按比例調整大小嗎？** 當然；使用 `resizeWidthProportionally` 和 `resizeHeightProportionally`。
- **我需要先快取影像嗎？** 快取（`image.cacheData()`）可提升大型 PSD 檔案的效能。
- **需要哪個 Java 版本？** 完全支援 Java 8 或更新版本。
- **生產環境是否需要授權？** 是，商業授權可移除評估水印。

## 什麼是「將 PSD 轉換為 PNG」以及為何重要？

**convert PSD to PNG** 指的是將分層的 Photoshop 文件轉換為單層、無損的 PNG 檔案，保留透明度與視覺忠實度。此轉換讓您在不需要 Photoshop 的情況下分享設計，產生適合網路使用的資產與縮圖，並將龐大的 PSD 檔案從客戶端瀏覽器中卸載，同時保持 UI 元件與品牌所需的品質。

## 為何在 Java 中按比例調整影像大小？

將影像 **不失真** 地調整大小可保持原始寬高比例，讓圖形在任何螢幕尺寸上都能保持預期的外觀。Aspose.PSD 的比例縮放方法會自動計算缺少的維度，省去手動計算，避免圖像被拉伸或壓扁的風險。

## 為何這對開發人員很重要

對開發人員而言，按比例調整大小與 PSD 轉 PNG 轉換可減少記憶體使用量並提升載入速度，確保應用程式能有效處理大型圖形。提前縮放影像可使 UI 呈現於各裝置保持一致，且不需在建置伺服器上安裝 Photoshop，簡化部署並降低營運成本。

- **減少 PSD 檔案大小** – 在轉換前縮小大型 PSD，可降低記憶體使用並加速後續處理。  
- **一致的 UI 呈現** – 按比例調整大小可確保圖示與圖形在各裝置上保持視覺平衡。  
- **無需 Photoshop 依賴** – 可在伺服器或 CI 流程中執行這些操作，無需安裝 Photoshop。  

## 先決條件

在深入程式碼之前，請確保您已具備以下條件：

1. **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。  
2. **Aspose.PSD for Java** – 從官方網站[此處](https://releases.aspose.com/psd/java/)下載最新的 JAR。  
3. 一個範例 PSD 檔案（`sample.psd`），放置於可從專案引用的目錄中。  

## 匯入套件

`PsdImage` 類別是 Aspose.PSD 的核心物件，代表記憶體中的 PSD 檔案。匯入必要的命名空間以進行載入、快取、調整大小與 PNG 匯出。

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：載入 PSD 影像

**直接回答：** 使用 `new PsdImage("sample.psd")` 載入來源檔案；然後呼叫 `image.cacheData()` 以預先載入影像資料，避免後續操作時重複讀取磁碟。

`cacheData()` 會將整個 PSD 載入記憶體，使後續處理更快。`cacheData()` 方法將整個文件讀入記憶體，對大型檔案的後續處理提供更快速度。首先，載入來源 PSD 檔案。若檔案較大，快取影像資料可減少在執行後續操作時的記憶體波動。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## 步驟 2：按比例調整影像大小（Java）

**直接回答：** 呼叫 `image.resizeWidthProportionally(targetWidth)`（或 `resizeHeightProportionally`）以縮小影像，同時自動保留原始長寬比。

`resizeWidthProportionally(int targetWidth)` 會縮放影像寬度，並自動計算相應的高度以保留原始長寬比。現在決定新的尺寸。在此範例中，我們將影像縮小至原始大小的 **一半**，同時保留長寬比。您可以根據需要調整目標寬度或高度。

`resizeWidthProportionally` 方法根據原始比例計算相應的高度，因而影像 **不失真** 地被調整大小。兩種方法皆可使用——Aspose.PSD 會為您處理另一個維度。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **專業提示：** 使用 `resizeWidthProportionally` *或* `resizeHeightProportionally`——函式庫會自動計算另一個維度以保持影像比例。

## 步驟 3：將調整大小的影像儲存為 PNG

**直接回答：** 建立 `PngOptions` 實例，指派給影像，然後呼叫 `image.save("output.png", pngOptions)` 以 PNG 格式寫入調整大小的檔案。

`PngOptions` 指定 PNG 匯出的設定，例如壓縮等級與色彩深度。最後，將調整大小的影像匯出為 PNG 格式。此步驟完成 **convert PSD to PNG** 工作流程。

程式執行後，您會得到一個 PNG 檔案，其大小為原始 PSD 的一半，且具備相同的視覺品質且不失真。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

程式執行後，您會得到一個 PNG 檔案，其大小為原始 PSD 的一半，且具備相同的視覺品質且不失真。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|-------|-------|-----|
| **OutOfMemoryError** | 大型 PSD 未快取 | 在調整大小前呼叫 `image.cacheData()` |
| **Blank PNG output** | 檔案路徑不正確 | 確認 `dataDir` 及寫入權限 |
| **Aspect ratio looks off** | 手動同時設定寬度與高度 | 使用 Aspose.PSD 提供的比例方法 |

## 減少 PSD 檔案大小的技巧

- **在載入檔案前裁剪不必要的圖層**。  
- **按比例調整大小**，如上所示，以提前縮小尺寸。  
- **以適當的位元深度儲存為 PNG**，避免多餘資料。  

## 常見問答

**Q: Aspose.PSD 是否相容所有影像格式？**  
A: Aspose.PSD 支援 PSD、PNG、JPEG、BMP、GIF 等等。完整清單請參閱[文件](https://reference.aspose.com/psd/java/)。完整 API 參考請見 **此處** 的指南。

**Q: 我可以在商業專案中使用 Aspose.PSD 嗎？**  
A: 可以。請於 [Aspose 商店](https://purchase.aspose.com/buy) 購買商業授權。

**Q: 是否提供測試用的臨時授權？**  
A: 當然可以 – 請於[此處](https://purchase.aspose.com/temporary-license/)申請臨時授權以作評估。

**Q: 我可以在哪裡找到社群支援？**  
A: [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 是提問與分享解決方案的好地方。

**Q: 如何取得完整的 API 參考文件？**  
A: 詳細的 API 文件可於[此處](https://reference.aspose.com/psd/java/)取得。

## 結論

您現在已了解如何使用 Aspose.PSD for Java **將 PSD 轉換為 PNG**、**按比例調整影像大小**，以及有效地處理快取。將這些步驟整合到您的應用程式中，即可提供快速且高品質的影像處理，而無需依賴本機 Photoshop 安裝。此 **aspose psd java** 方法是任何 **java image processing tutorial** 的可靠組成部分，協助您在保持視覺忠實度的同時控制 PSD 檔案大小。

---

**最後更新：** 2026-06-23  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.PSD 進行簡單縮放 – Java 影像操作函式庫](/psd/java/basic-image-operations/simple-resizing/)
- [Java 影像縮放 – 在 Aspose.PSD for Java 中使用 Resize Type 列舉](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [使用雙三次重採樣器在 Aspose.PSD for Java 中進行高品質影像縮放](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}