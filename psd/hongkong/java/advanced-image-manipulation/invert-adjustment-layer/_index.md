---
date: 2026-11-04
description: 了解如何使用 Aspose.PSD for Java 套用反相調整圖層、批次處理 PSD 圖像，並建立負片 PSD 檔案。
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: 反相調整圖層
og_description: 如何使用 Aspose.PSD for Java 新增反相調整圖層、批次處理 PSD 圖像，並建立負片 PSD。請參考逐步指南。
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: 如何在 Java 中使用 Aspose.PSD 新增反相調整圖層
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: 如何在 Java 中使用 Aspose.PSD 新增反相調整圖層
url: /zh-hant/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.PSD 新增反相調整圖層

## 介紹

如果您正在尋找一個強大的 **image processing java library**，Aspose.PSD for Java 是市場上最通用的選擇之一。在本教學中，您將看到 **how to use Aspose** 如何將 **Invert Adjustment Layer** 插入 PSD 檔案，並與其他調整圖層堆疊，甚至可對數十個檔案執行此操作。無論您是構建批次處理工具、伺服器端影像服務，或是單張影像編輯器，以下步驟都能在數分鐘內將來源 PSD 轉換為可完全編輯的負片影像。

## 快速解答
- **What does the Invert Adjustment Layer do?** 它會翻轉選取區域內的每個 RGB 值，將影像變成相片底片。  
- **Which library provides this feature?** Aspose.PSD，一個領先的 **image processing java library**。  
- **Can I stack it with other adjustments?** 可以 – 您可以 **apply multiple adjustment layers** 如亮度/對比、色相/飽和度等。  
- **Do I need a license for development?** 提供免費試用版；正式使用需購買授權。  
- **How long does the implementation take?** 基本案例通常在 10 分鐘內完成。

## 什麼是 Invert Adjustment Layer？

Invert Adjustment Layer 是一種非破壞性編輯，會反轉其影響的每個像素的顏色值。由於它位於圖層堆疊之上，您可以隨時切換可見性或重新排序，而不會永久改變原始影像資料。這是建立 **negative image PSD** 檔案或實現經典底片效果的最快方法。

## 為何使用 Aspose.PSD 作為您的 image processing java library？

Aspose.PSD 支援 **200+ PSD features**，可在不需要 Photoshop 的情況下讀寫 Photoshop 檔案，且在處理多頁文件時使用的堆積記憶體低於 500 MB。它可在任何 Java 執行環境 (Java 6+ ) 上執行，讓您在 Windows、Linux 或 macOS 伺服器上進行 **batch process psd images**。

## 前置條件

1. **Aspose.PSD for Java** – 從官方網站下載最新的 JAR [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)。  
2. **Java Development Kit** – 已安裝 JDK 6.0 或更新版本，並在 `PATH` 中設定。

現在您可以開始撰寫程式碼。

## 匯入套件

`PsdImage` 類別代表記憶體中的整個 Photoshop 文件，而調整圖層類別位於 `com.aspose.psd.layers.adjustments` 套件中。

`PsdImage` 是 Aspose.PSD 的頂層物件，封裝 PSD 檔案的結構與像素資料。匯入相應的命名空間後，即可載入、編輯與儲存 PSD 檔案。

## 步驟 1：設定文件目錄

定義包含來源 PSD 檔案的資料夾以及輸出檔案的儲存位置。使用絕對路徑可避免工作目錄變更時產生 `NullPointerException`。

## 步驟 2：載入 PSD 檔案

將來源檔案載入至 `PsdImage` 物件。此物件在記憶體中保留完整的圖層層級，支援非破壞性編輯。

`PsdImage` 類別提供靜態的 `load` 方法，讀取檔案標頭、驗證格式，並建立可供操作的記憶體表示。

## 步驟 3：新增 Invert Adjustment Layer

呼叫內建方法在目前的圖層堆疊最上方插入 Invert Adjustment Layer。之後您可以再加入其他圖層（例如亮度、色相）以 **apply multiple adjustment layers**。

`addInvertAdjustmentLayer()` 會將 Invert Adjustment Layer 新增至 PSD 的圖層集合中。

## 步驟 4：儲存輸出

將修改後的 PSD 持久化至磁碟。

`save()` 會將 PSD 檔案（包括所有圖層與中繼資料）寫入指定路徑。

儲存使用相同的 `save` 方法，寫入完整文件、所有調整圖層、遮色片與中繼資料至指定格式。

### 發生了什麼？

PSD 檔案已載入至 `PsdImage` 物件，建立了 `InvertAdjustmentLayer` 並將其作為最上層圖層加入，最後文件已儲存。此流程在保留原始影像資料的同時，加入了可隨時切換或重新排序的非破壞性反相效果。

您已成功使用 Aspose.PSD，一個 **image processing java library**，來操作 PSD 檔案。

## 如何使用 invert adjustment 進行 PSD 圖像批次處理？

在 `for` 迴圈中載入每個檔案，套用相同步驟，並對每次迭代呼叫 `save`。由於 Aspose.PSD 以串流方式處理檔案，您可以在記憶體使用量低於 300 MB 的情況下處理 **hundreds of PSDs**，只需重複使用同一個 `PsdImage` 實例。

## 如何將 PSD 轉換為負片影像？

將 Invert Adjustment Layer 加為最上層項目並儲存文件——此操作等同於 **convert PSD to negative**。之後可停用或刪除該圖層，以在不重新載入來源檔案的情況下恢復原始外觀。

## 常見問題與技巧

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | 檔案路徑不正確或檔案遺失 | 驗證 `dataDir` 與檔名；測試時使用絕對路徑 |
| **Layer order not as expected** | 在現有圖層之後新增圖層會改變堆疊順序 | 在其他調整之前插入 invert 圖層，或使用 `psdImage.getLayers().move()` 重新排序 |
| **Performance slowdown on large PSDs** | 將非常大的檔案載入記憶體 | 增加 JVM 堆積大小 (`-Xmx2g`) 或使用 `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` 以分段處理檔案 |

## 常見問答

**Q: Is Aspose.PSD compatible with all Java versions?**  
A: 是的，支援 Java 6.0 及以上版本，包括 Java 8、11 與 17。

**Q: Can I apply multiple adjustment layers in a single operation?**  
A: 當然可以。新增 invert 圖層後，您可以呼叫 `addBrightnessAdjustmentLayer()`、`addHueSaturationAdjustmentLayer()` 等方法，以堆疊多種效果。

**Q: Where can I find the full API reference?**  
A: 完整文件可於 [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/) 取得。

**Q: Is there a free trial for Aspose.PSD?**  
A: 有，您可以下載試用版 [Aspose.PSD trial download](https://releases.aspose.com/)。

**Q: How do I obtain a temporary license for testing?**  
A: 請申請臨時授權 [temporary license request page](https://purchase.aspose.com/temporary-license/)。

---

**最後更新：** 2026-11-04  
**測試版本：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## 相關教學

- [在 Java 中使用 Aspose.PSD 為 PSD 檔案新增等級調整圖層](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [如何在 PSD 中新增調整圖層 – 通道混合器 (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [如何編輯 PSD - 使用 Java 新增曲線調整圖層](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}