---
date: 2026-03-13
description: 學習如何使用 Aspose.PSD for Java 為 PSD 檔案新增色相飽和度圖層。本指南亦示範如何批次處理 PSD 檔案以及以程式方式建立色相調整圖層。
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Add Hue Saturation Layer to PSD with Aspose.PSD for Java
url: /zh-hant/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 中加入色相飽和度圖層

## 介紹
在平面設計領域，顏色的操作扮演關鍵角色——特別是調整色相、飽和度與亮度，能大幅改變圖像的氛圍與品質。使用 Photoshop（PSD 檔案）中的調整圖層是一種有效的做法。如果你想透過 Java 程式化 **add hue saturation layer**，Aspose.PSD 函式庫可以協助你！本教學將逐步說明如何在 PSD 檔案中加入 Hue Saturation Adjustment Layer，提升工作流程的生產力與效率。

## 快速解答
- **什麼程式庫可以在 Java 中新增色相飽和度圖層？** Aspose.PSD for Java。  
- **需要安裝 Photoshop 嗎？** 不需要，該函式庫可獨立於 Photoshop 使用。  
- **可以批次處理 PSD 檔案嗎？** 可以——自動化步驟後即可一次套用於多個檔案。  
- **需要哪個版本的 Java？** JDK 8 或更新版本。  
- **商業使用是否需要授權？** 需要，試用期結束後必須購買商業授權。

## 什麼是「add hue saturation layer」操作？
**add hue saturation layer** 操作會建立一個非破壞性的調整圖層，讓你在不改變原始像素資料的情況下調整色相、飽和度與亮度值。這非常適合在整個構圖或特定色彩範圍內進行細緻的顏色微調。

## 為什麼選擇 Aspose.PSD for Java？
- **無需 Photoshop 依賴** – 可在任何支援 Java 的平台上執行。  
- **完整 PSD 相容性** – 保留所有圖層資訊、遮色片與效果。  
- **支援批次處理** – 可遍歷資料夾，對數十個檔案套用相同調整。  
- **效能導向** – 為大型文件與伺服器端自動化進行最佳化。

## 前置條件
在開始撰寫程式碼之前，請先確保以下項目已備妥：

1. **Java Development Kit (JDK)：** 請確認已在電腦上安裝 JDK 8 以上版本。可從 [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
2. **Aspose.PSD for Java Library：** 需要取得 Aspose.PSD 函式庫，可在此 [download here](https://releases.aspose.com/psd/java/) 取得。  
3. **IDE：** 建議使用 IntelliJ IDEA 或 Eclipse 等適合的整合開發環境 (IDE) 進行 Java 開發。  
4. **基礎 Java 知識：** 具備 Java 程式基礎較佳，但不必擔心，我們會逐行說明。

現在前置條件已就緒，讓我們進入有趣的程式編寫階段吧！

## 匯入套件
要開始使用 Aspose.PSD 函式庫，第一步是匯入必要的類別。以下示範在 Java 檔案中如何完成：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

請確保已將相應的函式庫加入專案，讓這些匯入能順利運作。

## 步驟 1：設定文件目錄
每個專案都需要一個起始點，我們的也不例外。請指定存放 PSD 檔案的目錄，這對正確載入與儲存圖像至關重要。

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## 步驟 2：載入現有的 PSD 檔案
要操作既有的 PSD 檔案，首先必須將其載入程式中。以下為示範程式碼：

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

在此程式碼中，將 `"HueSaturationAdjustmentLayer.psd"` 替換為你想編輯的現有 PSD 檔案名稱。

## 步驟 3：編輯色相/飽和度圖層
接下來，我們會遍歷已載入 PSD 圖像的圖層，尋找並編輯任何現有的 Hue/Saturation 圖層。此步驟涉及修改色相、飽和度與亮度值。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

在此範例中：  
- 我們將色相調整為 **-25**、飽和度調整為 **-12**，亮度調整為 **+67**。  
- `getRange(2)` 方法允許依需求微調特定色彩範圍。

## 步驟 4：儲存已修改的 PSD 檔案
完成調整後，下一步是將檔案儲存。這是確保所做變更不會遺失的關鍵步驟。

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## 步驟 5：新增一個色相/飽和度圖層
如果需要 **create hue adjustment layer**，可以在另一個 PSD 檔案中加入全新的 Hue/Saturation 調整圖層。使用相同的載入方式，改為呼叫 `addHueSaturationAdjustmentLayer()` 方法。

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## 步驟 6：為新圖層設定色相/飽和度值
建立新圖層後，請像先前一樣套用所需的色相、飽和度與亮度設定。

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## 步驟 7：儲存更新後的 PSD 檔案
最後，將加入 Hue/Saturation 圖層的 PSD 檔案儲存，以便檢視變更結果。

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

恭喜！你已成功使用 Aspose.PSD for Java 操作 PSD 檔案。現在可以嘗試不同的圖像與更深入的調整，為你的平面設計專案注入新生命。

## 如何批次處理帶有色相調整的 PSD 檔案
由於上述程式碼完全可腳本化，你可以將整個流程包在迴圈中，遍歷資料夾內的每一個 `.psd` 檔案。這樣即可 **batch process psd files**，一次執行相同的色相、飽和度與亮度微調，特別適合大規模品牌更新。

## 常見問題與解決方案
- **載入檔案時出現 NullPointerException：** 請確認 `dataDir` 以正確的檔案分隔符 (`/` 或 `\`) 結尾，且檔名正確。  
- **調整值超出範圍：** 色相、飽和度與亮度的允許值為 -255 至 255，請將數值限制在此範圍內。  
- **找不到圖層：** 若 PSD 中沒有 Hue/Saturation 圖層，`instanceof` 檢查會跳過該區塊。可先使用 `addHueSaturationAdjustmentLayer()` 建立圖層。

## 常見問答

**Q: 什麼是 Hue Saturation Adjustment Layer？**  
A: 它允許在不永久改變原始像素的情況下，調整圖像的顏色屬性。

**Q: 使用 Aspose.PSD 是否需要安裝 Photoshop？**  
A: 不需要，Aspose.PSD 為獨立函式庫，可獨立於 Photoshop 運作。

**Q: 可以使用 Aspose.PSD 進行批次處理嗎？**  
A: 可以，您可以自動化並批次處理多個 PSD 檔案。

**Q: Aspose.PSD 是免費的嗎？**  
A: Aspose.PSD 提供免費試用，但長期使用需購買授權。您可在此查看價格 [here](https://purchase.aspose.com/buy)。

## 結論
以程式方式處理圖形可開啟無限可能。使用 Aspose.PSD for Java 來 **add hue saturation layer** 以及 **create hue adjustment layer**，提供彈性與效率，能簡化你的設計工作流程。無論是為專案增強照片，或是製作驚豔的視覺內容，精通這些工具都能大幅提升產出品質。

歡迎深入探索 Aspose.PSD 的更多功能，參考 [documentation](https://reference.aspose.com/psd/java/) 或考慮取得 [temporary license](https://purchase.aspose.com/temporary-license/) 以測試函式庫的完整威力。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---