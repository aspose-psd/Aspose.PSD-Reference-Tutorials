---
date: 2026-02-12
description: 學習如何使用 Aspose.PSD for Java 來調整圖像大小。提供包含 Resize Type 列舉的逐步說明，並附上將 PSD
  轉換為 JPEG 的技巧。
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
title: Java 圖像調整大小 - 在 Aspose.PSD for Java 中使用 Resize Type 列舉
url: /zh-hant/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 調整圖像大小 Java：在 Aspose.PSD for Java 中使用 Resize Type 列舉

## 介紹

在 Java 應用程式中調整圖像大小是常見需求，使用 Aspose.PSD 後 **resize image java** 操作變得輕鬆。在本教學中，您將學習如何使用功能強大的 Resize Type 列舉 **resize image java**，同時了解在調整大小後如何 **convert psd to jpeg**。無論您是開發桌面工具或伺服器端服務，這些步驟都能協助您可靠地處理圖像尺寸，並實現高品質的圖像調整。

## 快速回答
- **什麼程式庫處理 resize image java？** Aspose.PSD for Java。  
- **哪種 resize type 提供最佳品質？** `ResizeType.LanczosResample`。  
- **我可以在調整大小後將 PSD 轉換為 JPEG 嗎？** 是 – 只需使用 `JpegOptions` 保存。  
- **生產環境是否需要授權？** 需要有效的 Aspose.PSD 授權才能在生產環境使用。  
- **此方法適用於大量批次嗎？** 絕對可以；API 已針對效能進行最佳化。

## 什麼是 Resize Image Java？

「resize image java」指的是使用 Java 程式碼以程式方式變更圖像的像素尺寸。Aspose.PSD 提供簡潔的 API，抽象低階像素操作，讓您專注於業務邏輯，而非圖像處理細節。

## 為什麼使用 Resize Type 列舉？

Resize Type 列舉讓您能細緻控制重取樣演算法，平衡速度與品質。對於大多數應用程式而言，`LanczosResample` 提供了不錯的折衷，能在不造成過大效能負擔的情況下產生銳利的結果。選擇合適的 resize type 是實現高品質圖像調整的關鍵。

## 前置條件

在開始本教學之前，請確保已具備以下條件：

1. **Java 開發環境** – 已安裝並配置 JDK 8+。  
2. **Aspose.PSD Library** – 從 [website](https://releases.aspose.com/psd/java/) 下載並安裝 Aspose.PSD 程式庫。  
3. **Sample PSD File** – 準備好用於實驗的 PSD 範例檔案。您可以使用本教學的 [sample.psd](Your Document Directory/sample.psd) 檔案。

## 匯入套件

首先，將必要的套件匯入您的 Java 專案：

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步驟 1：載入圖像

使用 `RasterImage` 類別載入現有圖像。以下程式碼示例說明如何執行：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## 步驟 2：調整圖像大小

現在，使用 Resize Type 列舉調整已載入的圖像。在此範例中，我們使用 Lanczos Resample 方法，這是在 **how to resize image** 時取得高品質的理想選擇：

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 步驟 3：儲存調整後的圖像

調整完成後，使用指定的尺寸與選擇的 resize type 儲存圖像。此處同時示範如何 **convert psd to jpeg**，將結果保存為 JPEG 檔案：

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

您已完成一次完整的 **resize image java** 工作流程，產生高品質的圖像調整結果與可直接使用的 JPEG 輸出。

## 常見問題與解決方案

- **圖像調整後變模糊** – 嘗試使用其他 `ResizeType`（例如 `Bicubic` 或 `NearestNeighbour`）以找出最適合您圖像的視覺效果。  
- **大型 PSD 檔案發生 OutOfMemoryError** – 將圖像分成較小的區塊處理，或增加 JVM 堆積大小（`-Xmx` 參數）。

## 常見問答

### Q1：Aspose.PSD for Java 是否適用於小型與大型專案？

A1：絕對適用！Aspose.PSD for Java 設計能因應各種規模的專案，提供可擴充性與效能。

### Q2：我可以使用除 Lanczos Resample 之外的其他 resize type 嗎？

A2：可以，Aspose.PSD for Java 提供多種 resize type，例如 Nearest Neighbour、Bicubic 等。請參考文件取得完整清單。

### Q3：在哪裡可以找到 Aspose.PSD for Java 的其他支援？

A3：如有任何問題或需要協助，請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)。

### Q4：是否有 Aspose.PSD for Java 的免費試用版？

A4：有，您可以在此取得免費試用版 [here](https://releases.aspose.com/)。

### Q5：如何取得 Aspose.PSD for Java 的臨時授權？

A5：欲取得臨時授權，請前往 [this link](https://purchase.aspose.com/temporary-license/)。

## 常見問題

**Q：如何在不調整大小的情況下以程式方式將 PSD 檔案轉換為 JPEG？**  
A：使用 `Image.load` 載入 PSD，然後呼叫 `image.save("output.jpg", new JpegOptions());`。

**Q：在調整大小時是否能保留原始 DPI？**  
A：可以，在儲存前於 `Image` 物件設定 `Resolution` 屬性。

**Q：我可以串接多次調整大小操作嗎？**  
A：雖然可以多次呼叫 `resize`，但計算最終尺寸一次性調整會更有效率。

## 其他問答

**Q：Resize Type 列舉會影響處理速度嗎？**  
A：會的，較簡單的演算法如 `NearestNeighbour` 速度較快但品質較低，而 `LanczosResample` 雖稍慢卻能提供更高品質。

**Q：我可以在多執行緒環境中調整圖像大小嗎？**  
A：Aspose.PSD API 在唯讀操作下是執行緒安全的。若要同時調整大小，請為每個執行緒建立獨立的 `Image` 實例。

**Q：在調整大小時如何處理帶有 Alpha 通道的圖像？**  
A：程式庫預設會保留 Alpha 透明度。如需將圖像平面化，請在儲存前設定背景顏色。

**最後更新：** 2026-02-12  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}