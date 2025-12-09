---
date: 2025-12-08
description: 學習如何在 Java 中使用 Aspose.PSD 將 PSD 轉換為 PNG 並按比例調整圖像大小。此一步一步的教學涵蓋圖像快取、調整大小以及儲存為
  PNG。
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並按比例調整大小
url: /zh-hant/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並按比例調整大小

## 介紹

如果您需要在保持原始長寬比的情況下 **將 PSD 轉換為 PNG**，您已經來到正確的地方。在本教學中，我們將完整示範一個 **Aspose.PSD 教學**，說明如何在 Java 中 **按比例調整影像** 檔案、快取影像以提升效能，最後將結果儲存為 PNG。完成後，您即可將此工作流程整合到任何基於 Java 的影像處理管線中。

## 快速解答
- **Aspose.PSD 能將 PSD 轉換為 PNG 嗎？** 是 – 只需載入 PSD 並使用 `PngOptions` 儲存。
- **此函式庫支援按比例調整大小嗎？** 當然；使用 `resizeWidthProportionally` 與 `resizeHeightProportionally`。
- **我需要先快取影像嗎？** 快取（`image.cacheData()`）可提升大型 PSD 檔案的效能。
- **需要哪個 Java 版本？** 完全支援 Java 8 或更新版本。
- **生產環境需要授權嗎？** 需要，商業授權可移除評估水印。

## 什麼是「將 PSD 轉換為 PNG」以及為何重要？

將 Photoshop 文件（PSD）轉換為可攜式網路圖形（PNG）檔案，可讓您以輕量、適合網路的格式分享分層設計。PNG 保留透明度且具無損品質，十分適合 UI 資產、縮圖或任何對影像保真度有要求的情境。

## 為何在 Java 中按比例調整影像大小？

**按比例調整影像** 可避免失真，確保圖形在不同螢幕上看起來自然。`Aspose.PSD` API 提供專門的比例縮放方法，會自動計算相符的高度或寬度，讓您免於手動計算錯誤。

## 前置條件

在開始撰寫程式碼之前，請確保您已具備：

1. **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。
2. **Aspose.PSD for Java** – 從官方網站[此處](https://releases.aspose.com/psd/java/)下載最新 JAR。
3. 一個範例 PSD 檔案（`sample.psd`），放置於可於專案中參考的目錄下。

## 匯入套件

將必要的匯入加入您的 Java 類別。這些類別讓您能存取影像載入、快取、調整大小以及 PNG 輸出選項。

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：載入 PSD 影像

首先載入來源 PSD 檔案。若檔案較大，快取影像資料可減少記憶體使用，提升後續操作的效能。

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

接下來決定新尺寸。在此範例中，我們將影像縮小至原始大小的 **一半**，同時保留長寬比。您可以依需求調整目標寬度或高度。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **小技巧：** 使用 `resizeWidthProportionally` *或* `resizeHeightProportionally` — 函式庫會自動計算另一個維度以保持影像比例。

## 步驟 3：將調整大小的影像儲存為 PNG

最後，將調整大小的影像匯出為 PNG 格式。此步驟完成 **將 PSD 轉換為 PNG** 的工作流程。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

執行程式後，您會在指定位置找到一個 PNG 檔案，其大小為原始 PSD 的一半，且具相同的視覺品質，沒有任何失真。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|-------|-----|
| **OutOfMemoryError** | 大型 PSD 未快取 | 在調整大小前呼叫 `image.cacheData()` |
| **Blank PNG output** | 檔案路徑不正確 | 確認 `dataDir` 及寫入權限 |
| **Aspect ratio looks off** | 手動同時設定寬度與高度 | 使用 Aspose.PSD 提供的比例方法 |

## 常見問答

**Q: Aspose.PSD 是否相容所有影像格式？**  
A: Aspose.PSD 支援 PSD、PNG、JPEG、BMP、GIF 等多種格式。完整清單請參閱[文件說明](https://reference.aspose.com/psd/java/)。

**Q: 我可以在商業專案中使用 Aspose.PSD 嗎？**  
A: 可以。請於[Aspose 商店](https://purchase.aspose.com/buy)購買商業授權。

**Q: 是否提供測試用的臨時授權？**  
A: 當然 – 請於[此處](https://purchase.aspose.com/temporary-license/)申請臨時授權以供評估。

**Q: 我可以在哪裡取得社群支援？**  
A: 可前往[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)提問與分享解決方案。

**Q: 如何取得完整的 API 參考文件？**  
A: 完整的 API 文件可於[此處](https://reference.aspose.com/psd/java/)取得。

## 結論

您現在已掌握 **將 PSD 轉換為 PNG**、按比例調整影像大小，以及使用 Aspose.PSD for Java 高效快取的完整流程。將這些步驟整合到您的應用程式中，即可在不依賴本機 Photoshop 安裝的情況下，提供快速且高品質的影像處理。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-08  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose