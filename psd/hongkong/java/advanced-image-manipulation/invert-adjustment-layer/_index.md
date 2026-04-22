---
date: 2026-04-22
description: 學習如何使用影像處理 Java 函式庫 Aspose.PSD 來套用多個調整圖層，包括反相調整圖層，以實現無縫的 PSD 操作。
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: 反相調整圖層
second_title: Aspose.PSD Java API
title: 影像處理 Java 程式庫：使用 Aspose.PSD 反轉圖層
url: /zh-hant/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for Java 中的反相調整圖層

## 介紹

如果您正在尋找功能強大的 image processing java library，Aspose.PSD for Java 是市場上最通用的選項之一。在本教學中，我們將逐步說明如何在 PSD 檔案中加入 **Invert Adjustment Layer**，此技術可與其他調整圖層結合，實現複雜的視覺效果。無論您是在構建批次處理工具、伺服器端影像服務，或是單張影像編輯器，本指南都提供清晰、一步步的流程，讓您快速且可靠地完成任務。

## 快速解答
- **Invert Adjustment Layer 做什麼？** 它會反轉所選區域的所有顏色值，產生負片影像效果（即它 **converts PSD to negative**）。  
- **哪個函式庫提供此功能？** Aspose.PSD，一個領先的 **image processing java library**。  
- **我可以與其他調整圖層堆疊使用嗎？** 可以 – 您可以 **apply multiple adjustment layers**，例如亮度/對比、色相/飽和度等。  
- **開發時需要授權嗎？** 提供免費試用版；正式上線需購買授權。  
- **實作需要多長時間？** 基本使用情境通常在 10 分鐘以內完成。

## 什麼是 Invert Adjustment Layer？

Invert Adjustment Layer 是一種非破壞性編輯，會翻轉其影響範圍內每個像素的 RGB 值。由於它位於圖層堆疊之上，您可以隨時切換可見性或重新排序，而不會永久改變原始影像資料。這是 **invert colors PSD** 檔案或製作攝影負片的最簡單方式。

## 為什麼選擇 Aspose.PSD 作為您的 Image Processing Java Library？

- **Full PSD support** – 讀取、編輯與寫入 Photoshop 檔案，無需安裝 Photoshop。  
- **Cross‑platform** – 可在任何 Java 執行環境（Java 6+）上運行。  
- **Rich adjustment features** – 內建多種常見編輯方法，讓您在單一工作流程中輕鬆 **apply multiple adjustment layers**。  
- **Performance‑optimized** – 高效處理大型檔案，對於 **batch process psd images** 極為重要。  

## 前置條件

在開始之前，請確保您具備以下項目：

1. **Aspose.PSD Library** – 從官方網站[此處](https://releases.aspose.com/psd/java/)下載。  
2. **Java Development Environment** – 已安裝並設定 JDK 6.0 或更新版本。  

現在，讓我們深入程式碼。

## 匯入套件

先匯入必要的類別。這些匯入讓您可以使用核心影像處理 API 以及 PSD 專屬功能。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## 步驟 1：設定文件目錄

定義包含來源 PSD 檔案的資料夾，以及輸出檔案的儲存位置。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：載入 PSD 檔案

將來源檔案載入至 `PsdImage` 物件。此物件在記憶體中代表整個 PSD 文件。

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## 步驟 3：新增 Invert Adjustment Layer

呼叫內建方法，在目前的圖層堆疊上方插入 Invert Adjustment Layer。之後您可以再加入其他圖層（例如亮度、色相）以 **apply multiple adjustment layers**。

```java
im.addInvertAdjustmentLayer();
```

## 步驟 4：儲存輸出

將修改後的 PSD 持久化至磁碟。儲存的檔案現在包含 Invert Adjustment Layer，且可於 Photoshop 或任何相容的檢視器開啟。

```java
im.save(outputPath);
```

### 剛剛發生了什麼？

- PSD 已載入至記憶體。  
- 已將 Invert Adjustment Layer 加入為最上層圖層。  
- 影像已儲存，保留了非破壞性編輯。

您現在已成功使用 Aspose.PSD，一個 **image processing java library**，來操作 PSD 檔案。

## 使用反相調整批次處理 PSD 圖像

如果需要對數十或數百個檔案套用相同的反相效果，您可以將上述程式碼放入簡單的迴圈，遍歷 PSD 目錄。由於函式庫 **performance‑optimized**，即使處理大型批次亦相當快速，且可在同一迴圈中結合其他調整（例如亮度、色相）。

## 將 PSD 轉換為負片影像

Invert Adjustment Layer 本質上就是 **convert PSD to negative** 的操作。將此圖層置於最上層，即可在不永久改變原始像素資料的前提下，取得完整的負片效果。之後您亦可移除或停用該圖層，恢復原始外觀。

## 常見問題與技巧

| 問題 | 原因 | 解決方案 |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | 檔案路徑不正確或檔案遺失 | 核對 `dataDir` 與檔名；測試時使用絕對路徑 |
| **Layer order not as expected** | 在現有圖層之後加入圖層會改變堆疊順序 | 在加入其他調整前先使用 `im.addInvertAdjustmentLayer()`，或透過 `im.getLayers()` 重新排序圖層 |
| **Performance slowdown on large PSDs** | 將非常大的檔案一次載入記憶體 | 考慮分批處理頁面或增加 JVM 堆疊大小（`-Xmx2g`） |

## 常見問答

**Q: Aspose.PSD 是否相容所有 Java 版本？**  
A: Aspose.PSD 支援 Java 6.0 及以上版本。

**Q: 我可以在單一次操作中套用多個調整圖層嗎？**  
A: 可以，您可以堆疊多個調整圖層——如 Invert、Brightness、Hue/Saturation——以實現複雜效果。

**Q: 我可以在哪裡找到 Aspose.PSD 的其他文件？**  
A: 請參考文件[此處](https://reference.aspose.com/psd/java/)以取得完整指南與 API 參考。

**Q: Aspose.PSD 有提供免費試用嗎？**  
A: 有，您可以在[此處](https://releases.aspose.com/)探索免費試用版。

**Q: 我該如何取得 Aspose.PSD 的臨時授權？**  
A: 您可在[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

**最後更新:** 2026-04-22  
**測試環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}