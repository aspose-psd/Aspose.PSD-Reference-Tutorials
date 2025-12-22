---
date: 2025-12-19
description: 探索使用 Aspose.PSD for Java 進行 Java 圖像處理，學習如何在執行時加入特效。本教學將一步一步示範如何為圖像加入特效。
linktitle: Add Effects at Runtime
second_title: Aspose.PSD Java API
title: Java 圖像處理 - 使用 Aspose.PSD for Java 在執行時加入效果
url: /zh-hant/java/advanced-techniques/add-effects-runtime/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在執行時使用 Aspose.PSD for Java 添加效果

## 簡介

在 Java 開發的世界裡，**java image manipulation** 是常見需求，特別是當你想以動態視覺樣式豐富圖形時。使用 Aspose.PSD for Java——一個功能強大且多功能的 Java 函式庫，你可以輕鬆地 **在執行時加入效果** 以提升圖像。於本教學中，我們將逐步說明每個步驟，解釋 *為何* 每一步重要，並提供實用技巧，讓你能立即在自己的專案中套用效果。

## 快速答覆
- **哪個函式庫可協助 java image manipulation？** Aspose.PSD for Java。  
- **我可以在執行時加入效果嗎？** 可以——使用 layer‑effects API 來套用顏色覆蓋、陰影等。  
- **開發時需要授權嗎？** 測試時可使用臨時授權；正式上線需購買完整授權。  
- **需要哪個版本的 JDK？** 任意較新的 JDK（8 以上）。  
- **在哪裡可以下載免費試用版？** 從 Aspose.PSD 下載頁面（前置條件中有連結）。

## 什麼是 java image manipulation？
Java image manipulation 指的是使用 Java 函式庫以程式方式建立、編輯或增強點陣圖。常見任務包括調整大小、過濾、圖層合成以及套用視覺效果——這正是 Aspose.PSD 為 Photoshop 風格的 PSD 檔案所提供的功能。

## 為何使用 Aspose.PSD 進行 java image manipulation？
- **完整的 PSD 支援** – 保留圖層、遮色片與調整資料。  
- **不需本機 Photoshop** – 完全在 Java 中運作。  
- **執行時彈性** – 隨時加入、修改或移除效果。  
- **跨平台** – 可在任何支援 JDK 的作業系統上執行。

## 前置條件

在深入本教學之前，請確保已具備以下前置條件：

1. Java Development Kit (JDK)：確保系統已安裝 Java。可從 [here](https://www.oracle.com/java/technologies/javase-downloads.html) 下載最新 JDK。  
2. Aspose.PSD for Java 函式庫：需要取得 Aspose.PSD for Java 函式庫。若尚未下載，請從 [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) 取得。  
3. 文件目錄：建立一個存放文件的目錄，並記住其路徑。在範例中，該目錄稱為 `Your Document Directory`。

## 匯入套件

在 Java 專案中，匯入必要的套件以使用 Aspose.PSD for Java 的功能。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 步驟 1：載入 PSD 圖像

首先載入欲套用效果的 PSD 圖像。請確保設定正確的檔案路徑。

```java
String sourceFileName = "Your Document Directory/ThreeRegularLayers.psd";
String exportPath = "Your Document Directory/ThreeRegularLayersChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## 步驟 2：加入顏色覆蓋效果

在此步驟中，我們將為 PSD 圖像的特定圖層加入顏色覆蓋效果。此示範 **如何以程式方式加入效果**。

```java
ColorOverlayEffect effect = im.getLayers()[1].getBlendingOptions().addColorOverlay();
effect.setColor(Color.getGreen());
effect.setOpacity((byte)128);
effect.setBlendMode(BlendMode.Normal);
```

## 步驟 3：儲存已修改的圖像

最後，將套用效果後的已修改圖像儲存為新檔案。

```java
im.save(exportPath);
```

恭喜！您已成功使用 Aspose.PSD for Java 在執行時加入效果，這是現代 java image manipulation 的關鍵技術。

## 常見問題與解決方案

| Issue | Cause | Fix |
|-------|-------|-----|
| **Effect not visible** | 未設定 `loadOptions.setLoadEffectsResource(true)` | 請確保在載入 PSD 前設定此旗標。 |
| **Opacity looks wrong** | 使用了大於 127 的有號 `byte` | 如範例所示轉型為 `(byte)128`，或使用無號 int 並除以 255。 |
| **Layer index out of bounds** | 圖層編號錯誤 | 使用 `im.getLayers().length` 確認圖層順序，或在 Photoshop 中檢查 PSD。 |

## 常見問答

**Q: 我可以對單一圖層套用多個效果嗎？**  
A: 可以，您可以在同一圖層的混合選項上串接呼叫，例如 `addDropShadow()`、`addInnerGlow()` 等。

**Q: Aspose.PSD 是否相容多種影像格式？**  
A: 是，Aspose.PSD 支援 PSD、BMP、JPEG、PNG、TIFF 等多種格式，讓您在操作後可在格式間轉換。

**Q: 我要如何取得 Aspose.PSD for Java 的臨時授權？**  
A: 您可從 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 若有任何 Aspose.PSD 相關問題或疑問，我該向哪裡尋求協助？**  
A: 前往 Aspose.PSD [support forum](https://forum.aspose.com/c/psd/34) 取得協助並與社群互動。

**Q: 是否有 Aspose.PSD for Java 的免費試用版？**  
A: 有，您可在 [here](https://releases.aspose.com/) 下載免費試用版。

## 結論

Aspose.PSD for Java 簡化了 **java image manipulation**，提供您一套強大的工具組，讓您在不離開 Java 生態系的情況下加入動態視覺效果。透過本指南，您現在已掌握 **如何在執行時加入效果**（如顏色覆蓋），從而為網頁、桌面或行動應用程式創造更豐富、更具吸引力的圖形。

---  

**最後更新：** 2025-12-19  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}