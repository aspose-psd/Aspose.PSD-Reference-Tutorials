---
date: 2025-11-29
description: 學習如何使用 Aspose.PSD for Java 添加圖案效果並自訂 PSD 圖案覆蓋層。請跟隨我們的逐步指南，提升您的影像。
language: zh-hant
linktitle: Add Pattern
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中加入圖案效果
url: /java/advanced-image-effects/add-pattern-effects/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中添加圖案效果

## 簡介

在本教學中，您將會學會 **如何添加圖案** 效果到 PSD 檔案，使用 Aspose.PSD for Java。無論您是建立圖形密集的 Web 服務或是桌面設計工具，客製化圖案覆蓋都能為您的影像增添額外的視覺衝擊。我們將逐步說明——從載入 PSD、調整圖案資料到最終儲存結果——讓您能在自己的專案中自信地運用這些技巧。

## 快速答覆
- **主要的程式庫是什麼？** Aspose.PSD for Java  
- **哪個方法可加入圖案覆蓋？** `PatternOverlayEffect` 搭配 `PatternFillSettings`  
- **測試時需要授權嗎？** 提供免費試用版；正式環境需購買授權  
- **實作大約需要多久？** 基本覆蓋約 10–15 分鐘即可完成  
- **可以與其他 Java 圖像程式庫一起使用嗎？** 可以，若需要可將 Aspose.PSD 與其他程式庫串接  

## 什麼是圖案覆蓋？

圖案覆蓋是一種填色樣式，會在圖層上重複小位圖（即 *圖案*）以覆蓋整個區域。以 Photoshop 的說法，它是可套用於圖層的效果之一，用來提供質感、品牌標誌或裝飾圖樣。Aspose.PSD 透過 `PatternOverlayEffect` 類別提供此功能，讓您能完整程式化控制顏色、不透明度、混合模式以及圖案的實際像素資料。

## 為什麼要自訂 PSD 圖案覆蓋？

- **品牌一致性：** 用品牌專屬設計取代通用圖案。  
- **動態圖形：** 為遊戲或 UI 主題即時產生獨特紋理。  
- **自動化：** 批次處理數百個檔案，免除手動 Photoshop 操作。  

## 先決條件

在開始之前，請確保您已具備：

- 已安裝 Java Development Kit (JDK)。  
- 已將 Aspose.PSD for Java 程式庫加入專案（可從 [Aspose.PSD 網站](https://releases.aspose.com/psd/java/) 下載）。  

## 匯入套件

在 Java 類別的最上方加入必要的匯入：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

> **專業提示：** 請保持匯入的有序；未使用的匯入會產生編譯警告。

## 如何添加圖案效果 – 步驟指南

### 步驟 1：載入影像

首先，載入您想要修改的 PSD 檔案。我們會啟用 `loadEffectsResource`，讓現有的效果可供編輯。

```java
// Load the PSD image
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

> **注意：** 請將 `YourImagePath` 與 `YourExportPath` 替換為您機器上的實際目錄。

### 步驟 2：擷取圖案覆蓋資訊

接著，從第二層（索引 1）取得現有的 `PatternOverlayEffect`。這樣即可取得可供修改的設定物件。

```java
// Extract information about the pattern overlay
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### 步驟 3：修改圖案覆蓋設定

現在我們開始客製化覆蓋——變更顏色、不透明度、混合模式與偏移量。這正是 **自訂 PSD 圖案覆蓋** 以符合設計需求的地方。

```java
// Modify pattern overlay settings
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

### 步驟 4：編輯圖案資料

此步驟會取代構成圖案的實際位圖。我們會為圖案 ID 產生新的 GUID，賦予易讀名稱，並定義一個簡易的 4×2 像素矩陣。

```java
// Edit the pattern data
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

> **警告：** 圖案矩陣的尺寸必須與您在 `Rectangle` 中指定的尺寸相符。尺寸不匹配會導致 PSD 損毀。

### 步驟 5：儲存編輯後的影像

完成設定與圖案資料的更新後，將變更寫入新檔案。

```java
// Save the edited image
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

### 步驟 6：驗證變更

最後，重新載入已儲存的檔案，以確保覆蓋正確套用。您可以加入斷言或目視檢查來驗證結果。

```java
// Verify the changes in the edited file
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Add assertions to ensure the changes have been applied successfully
```

> **提示：** 使用單元測試框架（例如 JUnit）可自動化大量批次處理的驗證工作。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|------|------|----------|
| 圖案未顯示 | 不透明度設定為 0 或混合模式隱藏了圖案 | 調整 `setOpacity`（0‑255）並嘗試不同的 `BlendMode` |
| 儲存的檔案損毀 | 圖案矩形尺寸不正確 | 確認 `Rectangle` 與像素陣列長度相符 |
| 取得效果時拋出 `ClassCastException` | 該圖層未包含 `PatternOverlayEffect` | 檢查圖層索引，並確認該圖層確實有圖案覆蓋 |

## 常見問答

**Q: 可以將 Aspose.PSD for Java 與其他 Java 圖像處理程式庫一起使用嗎？**  
A: Aspose.PSD for Java 可獨立運作，但您仍可與 ImageIO、TwelveMonkeys 等程式庫結合，以支援其他格式。

**Q: 在哪裡可以找到 Aspose.PSD for Java 的詳細文件？**  
A: 請參考 [Aspose.PSD for Java 文件](https://reference.aspose.com/psd/java/) 以取得完整的 API 說明。

**Q: Aspose.PSD for Java 有提供免費試用嗎？**  
A: 有，您可在此取得免費試用版 [here](https://releases.aspose.com/)。

**Q: 如何取得 Aspose.PSD for Java 的支援？**  
A: 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 取得社群協助，或購買支援方案以獲得優先協助。

**Q: 可以取得 Aspose.PSD for Java 的臨時授權嗎？**  
A: 可以，臨時授權可在此取得 [here](https://purchase.aspose.com/temporary-license/)。

## 結論

恭喜！您已掌握 **如何添加圖案** 效果與 **自訂 PSD 圖案覆蓋** 的技巧，使用 Aspose.PSD for Java。透過本教學的步驟，您可以以程式方式豐富影像、自動化重複的設計工作，並將高階圖形工作流程整合至任何 Java 應用程式中。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-11-29  
**測試環境：** Aspose.PSD for Java 24.11 (latest at time of writing)  
**作者：** Aspose