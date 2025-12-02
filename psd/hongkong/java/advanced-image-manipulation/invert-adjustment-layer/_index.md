---
date: 2025-12-02
description: 學習如何使用影像處理 Java 函式庫 Aspose.PSD 以套用多個調整圖層，包括反相調整圖層，實現無縫的 PSD 操作。
language: zh-hant
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 影像處理 Java 函式庫：使用 Aspose.PSD 反轉圖層
url: /java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for Java 中使用反相調整圖層

## 介紹

如果您在尋找功能強大的 **image processing java library**，Aspose.PSD for Java 是市面上最具彈性的選擇之一。在本教學中，我們將示範如何在 PSD 檔案中加入 **Invert Adjustment Layer**，此技巧可與其他調整圖層結合，產生複雜的視覺效果。無論您是開發批次處理工具或單張圖片編輯器，本指南都提供清晰、一步一步的操作流程，讓您快速完成任務。

## 快速回答
- **Invert Adjustment Layer 會做什麼？** 它會反轉所選區域的所有顏色值，產生負片效果。  
- **哪個函式庫提供此功能？** Aspose.PSD，一個領先的 **image processing java library**。  
- **可以與其他調整圖層堆疊使用嗎？** 可以 – 您可以 **apply multiple adjustment layers**，例如 Brightness/Contrast、Hue/Saturation 等。  
- **開發時需要授權嗎？** 提供免費試用版；正式上線時需購買授權。  
- **實作大約需要多久？** 基本案例通常在 10 分鐘以內完成。

## 什麼是 Invert Adjustment Layer？

Invert Adjustment Layer 是一種非破壞性的編輯，會翻轉其影響範圍內每個像素的 RGB 值。因為它位於圖層堆疊之上，您可以隨時切換可見性或重新排列順序，而不會永久改變原始影像資料。

## 為什麼選擇 Aspose.PSD 作為您的 Image Processing Java Library？

- **完整的 PSD 支援** – 無需安裝 Photoshop，即可讀取、編輯與寫入 Photoshop 檔案。  
- **跨平台** – 可在任何 Java 執行環境 (Java 6+ ) 上運行。  
- **豐富的調整功能** – 內建多種常見編輯方法，讓您能在單一工作流程中 **apply multiple adjustment layers**。  
- **效能最佳化** – 能有效處理大型檔案，對批次處理尤為重要。

## 前置條件

在開始之前，請確保您已具備以下項目：

1. **Aspose.PSD Library** – 從官方網站[此處](https://releases.aspose.com/psd/java/)下載。  
2. **Java 開發環境** – 已安裝並設定 JDK 6.0 或更新版本。  

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

將來源檔案載入為 `PsdImage` 物件。此物件在記憶體中代表整個 PSD 文件。

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## 步驟 3：加入 Invert Adjustment Layer

呼叫內建方法，在目前的圖層堆疊最上方插入 Invert Adjustment Layer。之後您可以再加入其他圖層（例如 Brightness、Hue），以 **apply multiple adjustment layers**。

```java
im.addInvertAdjustmentLayer();
```

## 步驟 4：儲存輸出

將修改後的 PSD 寫入磁碟。儲存的檔案已包含 Invert Adjustment Layer，且可在 Photoshop 或任何支援 PSD 的檢視器中開啟。

```java
im.save(outputPath);
```

### 剛剛發生了什麼？

- PSD 已載入記憶體。  
- 在最上層加入了 Invert Adjustment Layer。  
- 影像已儲存，保留了非破壞性的編輯。

您已成功使用 Aspose.PSD 這個 **image processing java library** 來操作 PSD 檔案。

## 常見問題與技巧

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | 檔案路徑錯誤或檔案遺失 | 確認 `dataDir` 與檔名；測試時使用絕對路徑 |
| **Layer order not as expected** | 在既有圖層之後加入圖層會改變堆疊順序 | 在加入其他調整之前先呼叫 `im.addInvertAdjustmentLayer()`，或透過 `im.getLayers()` 重新排序圖層 |
| **Performance slowdown on large PSDs** | 將極大檔案一次載入記憶體 | 考慮分段處理頁面或增大 JVM 堆疊大小 (`-Xmx2g`) |

## 常見問答

**Q: Aspose.PSD 是否相容所有 Java 版本？**  
A: Aspose.PSD 支援 Java 6.0 及之後的版本。

**Q: 我可以在一次操作中套用多個調整圖層嗎？**  
A: 可以，您可以堆疊多個調整圖層——如 Invert、Brightness、Hue/Saturation——以達成複雜效果。

**Q: 哪裡可以找到 Aspose.PSD 的其他文件？**  
A: 請參考文件[此處](https://reference.aspose.com/psd/java/)取得完整指南與 API 參考。

**Q: 有提供免費試用版嗎？**  
A: 有，您可以在[此處](https://releases.aspose.com/)探索免費試用。

**Q: 如何取得 Aspose.PSD 的臨時授權？**  
A: 您可在[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

---

**最後更新：** 2025-12-02  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}