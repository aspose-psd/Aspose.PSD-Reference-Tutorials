---
date: 2026-03-07
description: 學習如何在 PSD 檔案中使用 Aspose.PSD for Java 新增「色階調整」圖層來調整色階，快速掌握色調微調技巧。
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: 如何調整色階 – 在 PSD 中新增色階調整圖層
url: /zh-hant/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 中新增等級調整圖層

## 介紹
如果你想了解 **如何調整等級** 在你的 Photoshop 文件中，等級調整圖層是完美的工具。它讓你在不永久改變原始像素的情況下微調陰影、中間調和高光。在本教學中，我們將示範如何使用 Aspose.PSD for Java 為 PSD 檔案新增等級調整圖層，讓你只需幾個步驟即可實現專業級的色調控制。

## 快速回答
- **等級調整圖層的作用是什麼？** 它以非破壞性的方式修改影像的色調範圍。  
- **使用哪個函式庫？** Aspose.PSD for Java。  
- **需要授權嗎？** 開發時可使用免費試用版；正式上線需購買授權。  
- **實作需要多久？** 基本調整大約需要 10‑15 分鐘。  
- **可以調整多個通道嗎？** 可以，您可以為每個顏色通道分別設定輸入/輸出等級。

## 什麼是等級調整圖層？
等級調整圖層讓你透過調整輸入陰影、中間調與高光以及輸出等級來校正影像的色調平衡。因為它存在於獨立的圖層上，你可以切換其可見性或刪除它，而不會影響底層的藝術作品。

## 為什麼要使用 Aspose.PSD 新增等級調整圖層？
- **自動化：** 將等級調整整合到批次處理流程中。  
- **跨平台：** 在任何支援 Java 的作業系統上皆可執行。  
- **精確度：** 以程式方式存取每個通道的設定，取得精確結果。  

## 前置條件
1. Java Development Kit (JDK)。如果尚未安裝，請從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載或使用 OpenJDK。  
2. Aspose.PSD for Java 函式庫 – 從此 [download link](https://releases.aspose.com/psd/java/) 取得最新的 JAR。  
3. 具備 Java 程式設計的基本知識。  
4. 使用 IntelliJ IDEA、Eclipse 或 NetBeans 等 IDE，並將 Aspose.PSD JAR 加入專案的 classpath。

## 匯入套件
在開始撰寫程式碼之前，我們需要從 Aspose.PSD 函式庫匯入必要的套件。以下示範如何操作：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
這些匯入讓我們能存取載入 PSD 檔案、操作等級調整圖層以及調整單一通道設定的類別。

## 如何在 PSD 檔案中調整等級
以下是一個逐步指南，示範如何以程式方式 **調整等級**。

### 步驟 1：設定檔案路徑
設定來源 PSD 檔案與編輯後檔案的儲存路徑。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
將 `"Your Document Directory"` 替換為您機器上的實際資料夾路徑。

### 步驟 2：載入 PSD 檔案
從來源檔案建立 `PsdImage` 實例。
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
現在您可以完整存取 PSD 內的所有圖層。

### 步驟 3：遍歷圖層
尋找要修改的等級調整圖層。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
`instanceof LevelsLayer` 檢查確保我們只處理等級調整圖層。

### 步驟 4：調整等級通道設定
調整所選通道的輸入與輸出值。
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **輸入中間調等級：** 調整中間調範圍。  
- **輸入陰影等級：** 使陰影變暗或變亮。  
- **輸入高光等級：** 控制最亮的部分。  
- **輸出陰影/高光等級：** 定義最終輸出範圍。

隨意嘗試不同的數值，觀察對影像的影響。

### 步驟 5：儲存修改後的 PSD 檔案
將變更儲存為新檔案。
```java
im.save(psdPathAfterChange);
```
您會在 `psdPathAfterChange` 指定的位置找到更新後的 PSD。

## 常見問題與解決方案
- **檔案未找到：** 確認 `dataDir` 指向正確的資料夾，且來源 PSD 檔案確實存在。  
- **ClassCastException：** 確保載入的檔案確實為 PSD；其他格式需使用不同的類別。  
- **授權錯誤：** 在正式建置時使用有效的 Aspose.PSD 授權；開發階段可使用試用版。

## 結論
現在您已了解 **如何調整等級**，透過在 PSD 檔案中新增與設定等級調整圖層，使用 Aspose.PSD for Java。此技巧讓您在保持工作流程全自動化的同時，精確控制色調平衡。持續嘗試不同的通道數值，並探索批次處理，以將相同調整套用至多張影像。

## 常見問答

**Q: 什麼是等級調整圖層？**  
A: 它是一個非破壞性的圖層，讓您可以修改影像的色調範圍（陰影、中間調、高光）。

**Q: 可以在未購買授權的情況下使用 Aspose.PSD 嗎？**  
A: 可以，您可以使用免費試用版評估函式庫，但商業部署需購買授權。

**Q: 在哪裡可以找到 Aspose.PSD 的文件？**  
A: 您可以在 [here](https://reference.aspose.com/psd/java/) 找到文件。

**Q: Aspose 產品有社群支援嗎？**  
A: 當然！您可以在 [Aspose forum](https://forum.aspose.com/c/psd/34) 提問並取得協助。

**Q: 如何取得 Aspose.PSD 的臨時授權？**  
A: 您可以在 [here](https://purchase.aspose.com/temporary-license/) 申請臨時授權。

---

**最後更新：** 2026-03-07  
**測試環境：** Aspose.PSD 最新版 (Java)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}