---
date: 2026-03-13
description: 學習如何使用 Aspose.PSD 在 Java 中建立 PSD 縮圖。跟隨我們的逐步指南，快速從 PSD 檔案生成縮圖。
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: 使用 Java 建立 PSD 縮圖 – 從 PSD 產生縮圖
url: /zh-hant/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 建立 PSD 縮圖 Java – 從 PSD 產生縮圖

## 簡介
如果您需要 **create PSD thumbnail Java** 程式碼來從 Photoshop 檔案提取預覽圖像，您來對地方了。無論您是建立數位資產管理器、網站相簿，或是自動化批次處理管線，從 PSD 檔案產生縮圖都能顯著提升效能與使用者體驗。在本教學中，我們將使用 Aspose.PSD for Java 完整示範整個流程，說明如何載入 PSD、定位其內嵌的縮圖資源，並將其另存為獨立的圖像檔案。

## 快速回答
- **哪個函式庫最適合 PSD 縮圖提取？** Aspose.PSD for Java.  
- **實作需要多久？** About 10‑15 minutes for a basic setup.  
- **需要安裝 Photoshop 嗎？** No, Aspose.PSD works independently.  
- **可以將縮圖匯出為哪些影像格式？** Any format supported by Aspose.PSD (e.g., BMP, PNG, JPEG).  
- **生產環境需要授權嗎？** Yes, a commercial license is needed for production use.

## 什麼是 “create PSD thumbnail Java”？
在 Java 中建立 PSD 縮圖是指以程式方式讀取儲存在 Photoshop 文件 (PSD) 內的縮圖預覽，並將其寫出為獨立的圖像檔案。這對於在不載入完整且通常相當龐大的 PSD 內容的情況下，快速產生預覽圖非常有用。

## 為什麼在此任務使用 Aspose.PSD？
- **無需 Photoshop 依賴：** 可在任何具備 JDK 的平台上運行。  
- **完整的 PSD 支援：** 處理所有 PSD 版本與資源，包含縮圖。  
- **簡易 API：** 僅需少量程式碼即可提取並儲存縮圖。  
- **效能最佳化：** 對大型檔案提供高效的記憶體管理。

## 先決條件
在深入縮圖建立的細節之前，先說明您需要哪些準備工作。

### Java 開發環境
- **Java JDK：** 確保您的電腦已安裝 Java Development Kit (JDK)。您可以在[此處](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)下載。  
- **IDE：** 使用如 IntelliJ IDEA、Eclipse 或 NetBeans 等整合開發環境 (IDE) 可讓編寫程式更方便。

### Aspose.PSD 函式庫
- 您需要在專案中加入 Aspose.PSD 函式庫。您可以在[此處](https://releases.aspose.com/psd/java/)下載最新版本。

### Java 基礎知識
- 熟悉 Java 基礎將有助於更有效地閱讀範例程式碼。類別、物件與迴圈等概念會頻繁使用。

## 匯入套件
首先從 Aspose.PSD 函式庫匯入必要的類別。此步驟至關重要，因為它讓您能在程式碼中使用函式庫的功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

完成先決條件後，我們就可以進入主要步驟！從 PSD 檔案建立縮圖只需幾個簡單步驟，我將為您逐一說明。

## 如何建立 PSD 縮圖 Java – 步驟指南

### 步驟 1：設定環境
以下說明如何啟動專案並為產生縮圖做準備。

1. **建立 Java 專案**  
   - 在 IDE 中開啟並建立新的 Java 專案。  
   - 為其命名，例如 `"PsdThumbnailGenerator"`。

2. **加入 Aspose.PSD 函式庫**  
   - 將 Aspose.PSD JAR 檔案加入專案的建置路徑。  
   - 若使用 Maven，請在 `pom.xml` 中加入以下內容：

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### 步驟 2：載入 PSD 檔案
接下來，我們需要載入欲產生縮圖的 PSD 檔案。

1. **指定文件目錄**  
   定義 PSD 檔案所在的目錄。

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **載入 PSD 檔案**  
   使用 `PsdImage` 類別載入您的 PSD 檔案。

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **小技巧：** 將 PSD 檔案放在專用資料夾（例如 `src/main/resources`）以避免路徑問題。

### 步驟 3：遍歷 PSD 資源
現在已載入 PSD 圖像，接下來的步驟是檢查其資源。

1. **取得資源數量**  
   我們將遍歷 PSD 檔案中的所有資源。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **辨識縮圖資源**  
   在迴圈內，檢查資源是否為縮圖。

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### 步驟 4：處理縮圖
一旦辨識出縮圖資源，我們就需要相應地處理它。

1. **取得並檢查縮圖格式**  
   若資源確實為縮圖，則取得它並檢查其格式。

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### 步驟 5：建立並儲存縮圖
這就是魔法發生的地方！我們將從縮圖資料建立新圖像並儲存。

1. **建立新圖像**  
   我們將使用縮圖資源的寬度與高度建立新的位圖圖像。

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **將像素寫入新圖像**  
   將縮圖資料轉移至新建立的圖像。

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **儲存縮圖圖像**  
   最後，將縮圖圖像以唯一名稱儲存至您的文件目錄。

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **常見陷阱：** 忘記關閉 `PsdImage` 物件會導致記憶體洩漏。若使用 Java 7 以上，請將影像處理程式碼包在 try‑with‑resources 區塊中。

## 結論
透過上述步驟，您現在已擁有一套穩固且可重複使用的 **create PSD thumbnail Java** 實作方式，能從任何 Photoshop 檔案提取預覽圖像。此技術可整合至批次處理器、Web 服務或桌面工具，以加速影像目錄建立並提升 UI 響應速度。請使用您自己的 PSD 集合試試看，體驗快速產生輕量級預覽的效果！

## 常見問答
### 什麼是 Aspose.PSD？
Aspose.PSD 是一套 Java 函式庫，讓開發者能以程式方式操作 Photoshop 檔案，簡化 PSD 檔案的處理與管理。

### 我可以免費使用 Aspose.PSD 嗎？
可以，Aspose 提供免費試用版，您可在購買授權前測試此函式庫。

### 我可以將縮圖儲存為哪些格式？
在本範例中，我們將縮圖儲存為 BMP 格式，但 Aspose.PSD 亦支援其他多種格式。

### 使用 Aspose.PSD 是否需要安裝 Photoshop？
不需要，Aspose.PSD 可獨立於 Photoshop 運作。

### 在哪裡可以取得更多 Aspose.PSD 資訊？
您可以參閱 [Aspose.PSD 文件](https://reference.aspose.com/psd/java/) 取得更多細節、教學與資源。

## 常見問題

**Q: 如何從受密碼保護的 PSD 提取縮圖？**  
A: 使用接受密碼參數的 `Image.load` 重載方法載入 PSD。

**Q: 我可以產生 PNG 格式的縮圖而非 BMP 嗎？**  
A: 當然可以。只要在 `save` 方法中更改檔案副檔名，Aspose.PSD 會自動處理轉換。

**Q: 有沒有辦法批次處理多個 PSD 檔案？**  
A: 將程式碼包在迴圈中，遍歷 PSD 檔案目錄，對每個檔案重複相同的提取邏輯。

**Q: 需要哪個版本的 Java？**  
A: Aspose.PSD 支援 Java 8 及以上版本。建議使用最新的 JDK，以獲得更佳效能與安全性。

**Q: 此函式庫能有效處理大型 PSD 檔案嗎？**  
A: 可以，Aspose.PSD 採用延遲載入與最佳化的記憶體管理，能在不耗盡堆積空間的情況下處理大型檔案。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD 24.11 for Java (latest at time of writing)  
**Author:** Aspose