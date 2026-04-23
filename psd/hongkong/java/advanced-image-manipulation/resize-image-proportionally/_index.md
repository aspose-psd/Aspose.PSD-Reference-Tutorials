---
date: 2026-02-09
description: 學習如何使用 Aspose.PSD 在 Java 中將 PSD 轉換為 PNG 並按比例調整圖像大小。此一步一步的教學涵蓋圖像緩存、調整大小以及儲存為
  PNG。
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並按比例調整大小
url: /zh-hant/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並按比例調整大小

## 介紹

如果您需要在保持原始長寬比的情況下 **將 PSD 轉換為 PNG**，您已來到正確的地方。在本 **Aspose.PSD Java** 教學中，我們將完整示範一個 **Java 圖像處理教學**，說明 **如何調整圖像大小** 的比例、如何快取圖像以提升效能，最後將結果儲存為 PNG。完成後，您即可將此工作流程整合至任何基於 Java 的圖像處理管線中。

## 快速解答
- **Aspose.PSD 能將 PSD 轉換為 PNG 嗎？** 是 – 只需載入 PSD 並使用 `PngOptions` 儲存。  
- **此函式庫支援比例縮放嗎？** 當然可以；使用 `resizeWidthProportionally` 與 `resizeHeightProportionally`。  
- **需要先快取圖像嗎？** 快取 (`image.cacheData()`) 能提升大型 PSD 檔案的效能。  
- **需要哪個 Java 版本？** 完全支援 Java 8 或更新版本。  
- **生產環境需要授權嗎？** 需要，商業授權會移除評估水印。

## 什麼是「將 PSD 轉換為 PNG」以及為何重要？

將 Photoshop 文件 (PSD) 轉換為可攜式網路圖形 (PNG) 檔案，可讓您以輕量、適合網路的格式分享分層設計。PNG 保留透明度且採用無損壓縮，十分適合 UI 資產、縮圖或任何對圖像品質有要求的情境。

## 為何在 Java 中按比例調整圖像大小？

**如何調整圖像大小** 而不扭曲長寬比，可確保圖形在不同螢幕上呈現自然。`Aspose.PSD` API 提供專門的 **按比例調整圖像大小** 方法，會自動計算相符的高度或寬度，避免手動計算錯誤。

## 為何這對開發者很重要

- **減少 PSD 檔案大小** – 在轉換前先縮小大型 PSD，可降低記憶體使用量並加速後續處理。  
- **一致的 UI 呈現** – 比例縮放保證圖示與圖形在各裝置上維持視覺平衡。  
- **無需 Photoshop** – 您可在伺服器或 CI 管線上執行這些操作，無需安裝 Photoshop。

## 前置條件

在開始撰寫程式碼前，請確保您已具備：

1. **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。  
2. **Aspose.PSD for Java** – 從官方網站[此處](https://releases.aspose.com/psd/java/)下載最新 JAR。  
3. 一個範例 PSD 檔案 (`sample.psd`)，放置於可從專案引用的目錄中。

## 匯入套件

在您的 Java 類別中加入必要的匯入。這些類別讓您能存取圖像載入、快取、縮放以及 PNG 輸出選項。

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：載入 PSD 圖像

首先載入來源 PSD 檔案。若檔案較大，快取圖像資料可減少在執行後續操作時的記憶體波動。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## 步驟 2：按比例縮放圖像（Java）

接著決定新的尺寸。在此範例中，我們將圖像縮小為原始大小的 **一半**，同時保留長寬比。您可依需求調整目標寬度或高度。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **專業提示：** 使用 `resizeWidthProportionally` *或* `resizeHeightProportionally` — 函式庫會自動計算另一個維度，以保持圖像比例。

## 步驟 3：將縮放後的圖像儲存為 PNG

最後，將縮放後的圖像匯出為 PNG 格式。此步驟完成 **將 PSD 轉換為 PNG** 的工作流程。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

程式執行後，您會得到一個 PNG 檔案，其大小為原始 PSD 的一半，且保持相同的視覺品質，沒有任何失真。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **OutOfMemoryError** | 大型 PSD 未快取 | 在縮放前呼叫 `image.cacheData()` |
| **Blank PNG output** | 檔案路徑不正確 | 核對 `dataDir` 以及寫入權限 |
| **Aspect ratio looks off** | 手動同時設定寬度與高度 | 使用 Aspose.PSD 提供的比例方法 |

## 減少 PSD 檔案大小的技巧

- **裁剪不必要的圖層** 後再載入檔案。  
- **按比例縮放** 如上所示，以提前縮小尺寸。  
- **以適當的位元深度儲存為 PNG**，避免產生過多資料。

## 常見問答

**Q: Aspose.PSD 是否相容所有圖像格式？**  
A: Aspose.PSD 支援 PSD、PNG、JPEG、BMP、GIF 等多種格式。完整列表請參閱[文件說明](https://reference.aspose.com/psd/java/)。

**Q: 我可以在商業專案中使用 Aspose.PSD 嗎？**  
A: 可以。請於[Aspose 商店](https://purchase.aspose.com/buy)購買商業授權。

**Q: 有提供測試用的臨時授權嗎？**  
A: 當然有 – 可於[此處](https://purchase.aspose.com/temporary-license/)申請臨時授權以供評估使用。

**Q: 我可以在哪裡取得社群支援？**  
A: 前往[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)提問或分享解決方案。

**Q: 如何取得完整的 API 參考文件？**  
A: 詳細的 API 文件可在[此處](https://reference.aspose.com/psd/java/)取得。

## 結論

您現在已了解如何 **將 PSD 轉換為 PNG**、**按比例調整圖像大小**，以及如何使用 Aspose.PSD for Java 高效快取圖像。將這些步驟整合至您的應用程式，即可在不依賴本機 Photoshop 安裝的情況下，提供快速且高品質的圖像處理。此 **aspose psd java** 方法是任何 **Java 圖像處理教學** 的可靠組成部分，能協助您在控制 PSD 檔案大小的同時，保持視覺忠實度。

---

**最後更新:** 2026-02-09  
**測試環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
