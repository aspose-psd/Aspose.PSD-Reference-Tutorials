---
date: 2026-10-24
description: 了解如何使用 Aspose.PSD for Java 為 PSD 檔案添加圖案覆蓋效果。提供逐步指南、程式碼範例、紋理覆蓋技巧及疑難排解。
keywords:
- how to add pattern overlay
- change pattern overlay color
- psd texture overlay tutorial
- edit psd layer effect
- create custom psd pattern
lastmod: 2026-10-24
linktitle: 添加圖案覆蓋
og_description: 如何使用 Aspose.PSD for Java 為 PSD 檔案添加圖案覆蓋。請依照此逐步教學套用紋理覆蓋、變更顏色，並建立自訂圖案。
og_image_alt: Developer guide showing pattern overlay effect added to a PSD using
  Aspose.PSD for Java
og_title: 如何在 PSD 中使用 Aspose.PSD for Java 添加圖案覆蓋
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to add pattern overlay effects to PSD files using Aspose.PSD
    for Java. Step‑by‑step guide with code examples, texture overlay tips, and troubleshooting.
  headline: How to add pattern overlay in PSD with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to add pattern overlay effects to PSD files using Aspose.PSD
    for Java. Step‑by‑step guide with code examples, texture overlay tips, and troubleshooting.
  name: How to add pattern overlay in PSD with Aspose.PSD for Java
  steps:
  - name: Load the PSD image
    text: Load the source PSD file while enabling the loading of effect resources.
      LoadOptions configures how a PSD file is read, and `setLoadEffectsResource(true)`
      ensures effect resources are loaded. > **Pro tip:** Keep `loadOptions.setLoadEffectsResource(true)`;
      otherwise the pattern overlay effect won’t b
  - name: Extract existing pattern overlay information
    text: '`PatternOverlayEffect` represents the pattern overlay layer effect and
      provides access to its settings. Retrieve the `PatternOverlayEffect` from the
      target layer (here we assume it’s the second layer, index 1). If your PSD uses
      a different layer order, adjust the index accordingly.'
  - name: Modify pattern overlay settings
    text: Now you can change color, opacity, blend mode, and offsets. These changes
      directly affect how the pattern is rendered on the layer. > **Why it matters:**
      Changing the blend mode to `Difference` creates a striking visual contrast,
      useful for highlighting texture details.
  - name: Edit the underlying pattern data
    text: '`PatternFillSettings` holds the bitmap that is tiled as the pattern. Replace
      the original pattern bitmap with a custom one. The example below builds a tiny
      4 × 2 pattern using a few basic colors. > **Common pitfall:** Forgetting to
      update the `PatternId` will leave the old pattern attached, causing '
  - name: Save the edited image
    text: Persist the changes to a new file. We also update the pattern name and ID
      in the settings before saving.
  - name: Verify the changes
    text: Reload the saved file and confirm that the overlay reflects the new settings.
      You can add unit‑test‑style assertions here (e.g., checking `patternOverlayEffect.getOpacity()`
      equals `193`) to automate verification.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java works independently, but you can combine it with libraries
      like ImageIO or TwelveMonkeys for additional format support.
    question: Can I use Aspose.PSD for Java with other Java image processing libraries?
  - answer: Refer to the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for a complete API reference.
    question: Where can I find detailed documentation for Aspose.PSD for Java?
  - answer: Yes, you can download a free trial from the [Aspose.PSD download page](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      help or purchase a support plan for direct assistance.
    question: How can I get support for Aspose.PSD for Java?
  - answer: Yes, a temporary license is available through the [Aspose temporary license
      page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- pattern overlay
- Aspose.PSD
- Java image processing
- PSD effects
title: 如何在 PSD 中使用 Aspose.PSD for Java 添加圖案覆蓋
url: /zh-hant/java/advanced-image-effects/add-pattern-overlay/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 PSD 中使用 Aspose.PSD for Java 添加圖樣覆蓋

如果您需要在 Java 應用程式中 **添加圖樣覆蓋** 到 Photoshop (PSD) 檔案，Aspose.PSD for Java 可讓此工作變得簡單。在本教學中，您將學習如何載入 PSD、編輯其圖樣覆蓋設定，並儲存結果——全部使用清晰、可投入生產的程式碼。完成後，您將了解圖樣覆蓋在品牌化、紋理製作及動態影像產生方面的實用性。

## 快速解答
- **我可以達成什麼？** 在任何 PSD 圖層上添加或修改圖樣覆蓋效果。  
- **需要的函式庫？** Aspose.PSD for Java（最新版本）。  
- **先決條件？** JDK 8 以上、Aspose.PSD JAR，以及範例 PSD 檔案。  
- **典型實作時間？** 基本覆蓋大約需要 10–15 分鐘。  
- **程式碼可以重複使用嗎？** 可以——相同方法適用於任何含有圖樣資源的 PSD。  

## 什麼是圖樣覆蓋 PSD？

圖樣覆蓋 PSD 是一種圖層效果，會將小型點陣圖（圖樣）平鋪於選取的圖層上。它常用於紋理、品牌印章或裝飾背景。**您可以程式化地變更圖樣的顏色、偏移、混合模式，甚至取代底層點陣圖。**  

## 為何使用 Aspose.PSD for Java 添加圖樣覆蓋？

您可以在不安裝 Photoshop 的情況下添加圖樣覆蓋，保持 100 % 圖層完整性，且可在 Windows、Linux 或 macOS 上執行。Aspose.PSD 支援 **超過 50 種輸入與輸出格式**，且能在不將整個檔案載入記憶體的情況下處理數百頁文件，十分適合伺服器端自動化。

## 先決條件

在開始之前，請確保您已具備以下項目：

- 已安裝 Java Development Kit (JDK) 8 或更新版本。  
- 已將 Aspose.PSD for Java 函式庫加入專案的 classpath。您可從 [Aspose.PSD 官方網站](https://releases.aspose.com/psd/java/) 下載。  
- 一個範例 PSD 檔案（例如 `PatternOverlay.psd`），其其中一個圖層已包含圖樣覆蓋效果。

## 匯入套件

`com.aspose.psd` 命名空間包含您所需的所有類別。  

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

## 步驟說明

### 步驟 1：載入 PSD 圖像

載入來源 PSD 檔案，同時啟用效果資源的載入。LoadOptions 可設定 PSD 檔案的讀取方式，`setLoadEffectsResource(true)` 可確保載入效果資源。  

```java
// Load the PSD image
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

> **專業提示：** 保持 `loadOptions.setLoadEffectsResource(true)`；否則圖樣覆蓋效果將無法存取。

### 步驟 2：擷取現有圖樣覆蓋資訊

`PatternOverlayEffect` 代表圖樣覆蓋圖層效果，並提供其設定的存取。從目標圖層取得 `PatternOverlayEffect`（此處假設為第二層，索引為 1）。  

```java
// Extract information about the pattern overlay
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

如果您的 PSD 使用不同的圖層順序，請相應調整索引。

### 步驟 3：修改圖樣覆蓋設定

現在您可以變更顏色、不透明度、混合模式與偏移。這些變更會直接影響圖樣在圖層上的呈現方式。  

```java
// Modify pattern overlay settings
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

> **為何重要：** 將混合模式改為 `Difference` 可產生顯著的視覺對比，適合突顯紋理細節。

### 步驟 4：編輯底層圖樣資料

`PatternFillSettings` 保存作為圖樣平鋪的點陣圖。將原始圖樣點陣圖替換為自訂圖樣。以下範例使用幾種基本顏色建立一個 4 × 2 的小圖樣。  

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

> **常見陷阱：** 忘記更新 `PatternId` 會使舊圖樣仍被附加，導致視覺變更被忽略。

### 步驟 5：儲存編輯後的影像

將變更持久化至新檔案。儲存前，我們亦會在設定中更新圖樣名稱與 ID。  

```java
// Save the edited image
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

### 步驟 6：驗證變更

重新載入已儲存的檔案，確認覆蓋效果已套用新設定。  

```java
// Verify the changes in the edited file
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Add assertions to ensure the changes have been applied successfully
```

您可以在此加入單元測試式斷言（例如檢查 `patternOverlayEffect.getOpacity()` 是否等於 `193`）以自動化驗證。

## 如何使用 Aspose.PSD 套用紋理覆蓋

將較大的點陣圖載入 `PatternFillSettings` 物件，並在圖層上平鋪。調整 `horizontalOffset` 與 `verticalOffset` 以控制重複間距，讓您完整掌握紋理的放置。透過微調這些偏移，可建立無縫紋理，避免可見接縫，並使圖樣與其他設計元素精確對齊。

## 如何變更圖樣覆蓋顏色

變更覆蓋顏色只需呼叫 `settings.setColor(...)`。`setColor` 方法會為覆蓋指定新的 `Color`，在圖樣渲染時使用。**步驟 3** 的範例示範將顏色切換為綠色。您可以使用任何 `Color` 常數或自行建立 ARGB 值。

## 如何建立自訂 PSD 圖樣

**步驟 4** 中的迴圈示範如何以程式方式建立自訂圖樣。透過將您的 ARGB 值填入 `int[]` 陣列並定義矩形大小，即可產生任意可重複的圖樣——非常適合即時打造品牌專屬的紋理。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|-------|--------|-----|
| **圖樣未變更** | `PatternId` 未更新或圖層索引錯誤 | 確保您修改正確的 `PattResource` 並呼叫 `settings.setPatternId(...)`。 |
| **顏色顛倒** | 混合模式不小心設定為 `Difference` | 選擇符合設計意圖的混合模式（例如 `Normal`、`Overlay`）。 |
| **匯出的 PSD 失去圖層** | 使用過時的 Aspose.PSD 版本 | 升級至最新的 Aspose.PSD for Java 版本。 |
| `NullPointerException` 發生於 `getEffects()[0]` | 圖層未套用任何效果 | 在轉型前確認圖層確實包含 `PatternOverlayEffect`。 |

## 常見問答

**Q: 我可以將 Aspose.PSD for Java 與其他 Java 影像處理函式庫一起使用嗎？**  
A: Aspose.PSD for Java 可獨立運作，但您可以結合 ImageIO 或 TwelveMonkeys 等函式庫以支援額外格式。

**Q: 我可以在哪裡找到 Aspose.PSD for Java 的詳細文件？**  
A: 請參考 [Aspose.PSD for Java 文件](https://reference.aspose.com/psd/java/) 以取得完整的 API 參考。

**Q: 是否提供 Aspose.PSD for Java 的免費試用？**  
A: 有，您可從 [Aspose.PSD 下載頁面](https://releases.aspose.com/) 下載免費試用版。

**Q: 我該如何取得 Aspose.PSD for Java 的支援？**  
A: 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 尋求社群協助，或購買支援方案以獲得直接協助。

**Q: 我可以取得 Aspose.PSD for Java 的臨時授權嗎？**  
A: 可以，臨時授權可於 [Aspose 臨時授權頁面](https://purchase.aspose.com/temporary-license/) 取得。

---

**最後更新：** 2026-10-24  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose

## 相關教學

- [圖樣覆蓋 PSD：使用 Aspose.PSD for Java 添加效果](/psd/java/advanced-image-effects/add-pattern-effects/)
- [在 Java 中使用 Aspose.PSD 套用顏色覆蓋並設定不透明度](/psd/java/image-editing/color-overlay-effect/)
- [如何添加填色：使用 Java 為 PSD 檔案新增顏色填充圖層](/psd/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}