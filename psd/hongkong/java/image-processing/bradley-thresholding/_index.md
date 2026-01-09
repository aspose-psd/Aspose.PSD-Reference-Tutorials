---
date: 2026-01-09
description: 學習如何使用 Aspose.PSD for Java 中的 Bradley 閾值法將 PSD 轉換為 PNG。本指南展示如何選擇最佳閾值並有效地將
  PSD 圖像二值化。
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: 使用 Bradley 閾值法將 PSD 轉換為 PNG（Aspose.PSD Java）
url: /zh-hant/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Bradley 閾值法將 PSD 轉換為 PNG（Aspose.PSD Java）

歡迎閱讀本完整指南，說明如何在 Aspose.PSD for Java 中使用 Bradley 閾值法 **convert PSD to PNG**。在接下來的幾分鐘內，您將了解為何此技術非常適合從 Photoshop 文件產生高對比度、二值化的 PNG 檔案，並獲得實作的逐步說明。

## 快速解答
- **Can I convert PSD to PNG with Aspose.PSD?** 是的 – 載入 PSD，套用 `binarizeBradley`，然後儲存為 PNG。  
- **What does “choose optimal threshold” mean?** 它是決定暗/亮像素分類的敏感度值（0‑1）。  
- **Do I need a license for production use?** 需要商業授權；免費試用版可用於評估。  
- **Which image formats are supported for saving?** PNG、JPEG、BMP 等多種格式，透過 `ImageOptions` 類別提供。  
- **Is the code compatible with Java 8 and later?** 完全相容 – Aspose.PSD Java API 支援 Java 8 以上。

## 什麼是 Bradley 閾值法？
Bradley 閾值法是一種自適應二值化演算法，會為每個像素計算局部平均值，並將像素的強度與該平均值乘以使用者自訂的閾值進行比較。最終產生保留重要細節的乾淨黑白影像。

## 為什麼要使用 Bradley 閾值法將 PSD 轉換為 PNG？
- **Preserve sharp edges** – 適用於 OCR、條碼偵測或任何需要前景與背景明顯分離的工作流程。  
- **Reduce file size** – PNG 為無損格式，但經二值化後通常檔案更小。  
- **Cross‑platform compatibility** – PNG 可在任何平台使用，而 PSD 只限於 Photoshop。

## 前置條件
在開始之前，請確保您已具備：

1. **Java Development Environment** – 已安裝 JDK 8 或更新版本。  
2. **Aspose.PSD Library** – 從 [here](https://releases.aspose.com/psd/java/) 下載最新的 JAR。  
3. **Sample PSD Image** – 任意您想要轉換的 PSD 檔案；也可使用 Aspose 範例中提供的樣本。

## 匯入套件
開始於 Java 專案中匯入必要的類別：

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## 如何使用 Bradley 閾值法將 PSD 轉換為 PNG
以下為完整工作流程，分為清晰的編號步驟。每個步驟包含簡短說明，並附上您需要直接複製貼上的程式碼。

### 步驟 1：載入 PSD 影像
首先，指定來源檔案路徑，並使用 Aspose.PSD 載入。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### 步驟 2：選擇最佳閾值
閾值（範圍 0 – 1）決定二值化的強度。一般起始值為 **0.15**，您可依影像需求調整。

```java
// Define threshold value
double threshold = 0.15;
```

### 步驟 3：二值化 PSD 影像
現在套用 Bradley 演算法。此步驟會根據您選擇的閾值 **binarize PSD image**。

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### 步驟 4：將輸出儲存為 PNG
最後，將處理後的影像以 PNG 格式寫入磁碟。

```java
// Save the output image
image.save(destName, new PngOptions());
```

對所有需要處理的 PSD 檔案重複上述步驟，並依需求微調閾值以取得最佳視覺效果。

## 常見問題與技巧
- **Threshold too low/high:** 若輸出過於雜訊或過度淡化，請逐步調整 `threshold` 值（例如 0.10 – 0.20）。  
- **Memory consumption:** 大型 PSD 檔案可能佔用大量記憶體。建議一次處理單一檔案，或提升 JVM 堆積大小 (`-Xmx`)。  
- **Preview before saving:** 使用 `image.save(\"preview.bmp\", new BmpOptions());` 先檢視二值化結果，再匯出最終 PNG。

## 常見問答

**Q: What is the difference between `binarizeBradley` and other thresholding methods?**  
A: `binarizeBradley` 為每個像素計算局部平均值，較全域閾值法對光線不均的影像更具韌性。

**Q: Can I apply Bradley Thresholding to JPEG or BMP files?**  
A: 是的。使用 `Image.load(...)` 載入任何支援的格式，然後在儲存前呼叫 `binarizeBradley`。

**Q: Is there a way to preview the binarized image before saving?**  
A: 當然可以。使用 Aspose.PSD 的任一影像儲存選項（例如 BMP）寫入暫存預覽檔案。

**Q: Where can I find more support and resources?**  
A: 前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得社群協助，並參考完整的 [documentation](https://reference.aspose.com/psd/java/) 以了解進階情境。

## 結論
您現在已掌握如何透過 **choose an optimal threshold** 與 **binarizing the PSD image**，使用 Bradley 閾值法高效 **convert PSD to PNG**。此方法非常適合需要從複雜 Photoshop 檔案產生乾淨高對比度 PNG 輸出的工作流程。

---

**最後更新：** 2026-01-09  
**測試環境：** Aspose.PSD Java 23.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}