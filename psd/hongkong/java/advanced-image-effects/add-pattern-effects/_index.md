---
date: 2026-04-12
description: 學習如何使用 Aspose.PSD for Java 為 PSD 檔案新增圖樣覆蓋效果。逐步指南，附程式碼範例與疑難排解技巧。
keywords:
- pattern overlay psd
- apply texture overlay
- change pattern overlay color
- add pattern overlay
- create custom psd pattern
linktitle: 新增圖樣覆蓋
second_title: Aspose.PSD Java API
title: 圖案覆蓋 PSD：使用 Aspose.PSD for Java 添加效果
url: /zh-hant/java/advanced-image-effects/add-pattern-overlay/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 圖案疊加 PSD：使用 Aspose.PSD for Java 添加效果

如果您需要從 Java 應用程式 **add pattern overlay** 到 Photoshop (PSD) 檔案，Aspose.PSD for Java 可讓此任務變得簡單直觀。在本教學中，我們將示範如何載入 PSD、編輯其圖案疊加設定，並儲存結果——全部使用清晰、可投入生產的程式碼。完成後，您將了解圖案疊加在品牌化、紋理建立以及動態影像產生方面的實用性。

## 快速解答
- **我可以達成什麼？** 在任何 PSD 圖層上新增或修改圖案疊加效果。  
- **需要的函式庫？** Aspose.PSD for Java（最新版本）。  
- **先決條件？** JDK 8+、Aspose.PSD JAR，以及範例 PSD 檔案。  
- **典型實作時間？** 基本疊加大約需要 10–15 分鐘。  
- **我可以重複使用此程式碼嗎？** 是——相同方法適用於任何具備圖案資源的 PSD。  

## 什麼是圖案疊加 PSD？

圖案疊加 PSD 是一種圖層效果，會將小位圖（圖案）平鋪於選取的圖層上。它常用於紋理、品牌印章或裝飾背景。使用 Aspose.PSD，您可以以程式方式變更圖案的顏色、偏移、混合模式，甚至取代底層圖案資料。

## 為何使用 Aspose.PSD for Java 來添加圖案疊加？

- **完整 PSD 相容性：** 保留所有 Photoshop 功能，且不會遺失圖層資訊。  
- **不需本機 Photoshop：** 可在任何伺服器或 CI 環境中運行。  
- **豐富 API：** 直接存取混合模式、不透明度與圖案資源。  
- **跨平台：** 在 Windows、Linux 與 macOS 上以相同程式碼基礎執行。  

## 先決條件

在開始之前，請確保您已具備以下項目：

- 已在機器上安裝 Java Development Kit (JDK)。  
- 已將 Aspose.PSD for Java 函式庫加入專案的 classpath。您可從 [Aspose.PSD website](https://releases.aspose.com/psd/java/) 下載。  
- 一個範例 PSD 檔案（例如 `PatternOverlay.psd`），其其中一個圖層已包含圖案疊加效果。  

## 匯入套件

在您的 Java 類別中，匯入必要的 Aspose.PSD 命名空間：

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

## 步驟指南

### 步驟 1：載入 PSD 圖像

首先，載入來源 PSD 檔案，同時啟用載入效果資源：

```java
// Load the PSD image
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

> **專業提示：** 保持 `loadOptions.setLoadEffectsResource(true)`；否則圖案疊加效果將無法存取。

### 步驟 2：擷取現有圖案疊加資訊

從目標圖層取得 `PatternOverlayEffect`（此處假設為第二層，索引為 1）：

```java
// Extract information about the pattern overlay
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

如果您的 PSD 使用不同的圖層順序，請相應調整索引。

### 步驟 3：修改圖案疊加設定

現在您可以變更顏色、不透明度、混合模式與偏移。這些變更會直接影響圖案在圖層上的呈現方式：

```java
// Modify pattern overlay settings
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

> **為何重要：** 將混合模式改為 `Difference` 會產生顯著的視覺對比，適合突顯紋理細節。

### 步驟 4：編輯底層圖案資料

將原始圖案位圖取代為自訂圖案。以下範例使用幾種基本顏色建立一個 4×2 的小圖案：

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

> **常見陷阱：** 若忘記更新 `PatternId`，舊圖案仍會被保留，導致視覺變更被忽略。

### 步驟 5：儲存編輯後的影像

將變更持久化至新檔案。我們亦在儲存前於設定中更新圖案名稱與 ID：

```java
// Save the edited image
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

### 步驟 6：驗證變更

重新載入已儲存的檔案，確認疊加效果已套用新設定：

```java
// Verify the changes in the edited file
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Add assertions to ensure the changes have been applied successfully
```

您可以在此加入單元測試式斷言（例如，檢查 `patternOverlayEffect.getOpacity()` 是否等於 `193`）以自動化驗證。

## 如何使用 Aspose.PSD 套用紋理疊加

如果您的目標是 **apply texture overlay** 而非單純圖案，您可以使用相同的 `PatternFillSettings` 物件，但提供較大的位圖作為紋理。依需求調整 `horizontalOffset` 與 `verticalOffset` 以平鋪紋理。

## 如何變更圖案疊加顏色

變更疊加顏色只需呼叫 `settings.setColor(...)`。**步驟 3** 的範例示範了將顏色切換為綠色。您可以使用任何 `Color` 常數或自行建立 ARGB 值來實驗。

## 如何建立自訂 PSD 圖案

**步驟 4** 中的迴圈示範了如何以程式方式建立自訂圖案。透過將您的 ARGB 值填入 `int[]` 陣列並定義矩形尺寸，即可產生任意可重複的圖案——非常適合即時打造品牌專屬的紋理。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **Pattern does not change** | `PatternId` not updated or wrong layer index | Ensure you modify the correct `PattResource` and call `settings.setPatternId(...)`. |
| **Colors appear inverted** | Blend mode set to `Difference` unintentionally | Choose a blend mode that matches your design intent (e.g., `Normal`, `Overlay`). |
| **Exported PSD loses layers** | Using an outdated Aspose.PSD version | Upgrade to the latest Aspose.PSD for Java release. |
| **`NullPointerException` on `getEffects()[0]`** | Layer has no effects applied | Verify the layer actually contains a `PatternOverlayEffect` before casting. |

## 常見問答

**Q: 我可以將 Aspose.PSD for Java 與其他 Java 影像處理函式庫一起使用嗎？**  
A: Aspose.PSD for Java 可獨立運作，但您可以與 ImageIO 或 TwelveMonkeys 等函式庫結合，以支援額外格式。

**Q: 我可以在哪裡找到 Aspose.PSD for Java 的詳細文件？**  
A: 請參考 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 以取得完整 API 參考。

**Q: 是否提供 Aspose.PSD for Java 的免費試用？**  
A: 有，您可從 [Aspose.PSD download page](https://releases.aspose.com/) 下載免費試用版。

**Q: 我該如何取得 Aspose.PSD for Java 的支援？**  
A: 前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 獲取社群協助，或購買支援方案以取得直接協助。

**Q: 我可以取得 Aspose.PSD for Java 的臨時授權嗎？**  
A: 有，您可透過 [Aspose temporary license page](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 結論

您現在已學會如何使用 Aspose.PSD for Java **add pattern overlay** PSD 檔案的效果。透過操作混合模式、不透明度、偏移與底層圖案位圖，您可以直接從 Java 程式碼產生動態紋理與品牌元素。歡迎嘗試不同的顏色、圖案與混合模式，以符合專案的視覺風格。

---

**最後更新：** 2026-04-12  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}