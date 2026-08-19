---
date: 2026-04-05
description: 學習如何修改 Gradient Overlay Java，以使用 Aspose.PSD for Java 編輯 PSD 檔案中的 Gradient
  Overlay 效果，並以程式方式新增 Gradient Overlay PSD 圖層。
keywords:
- modify gradient overlay java
- add gradient overlay psd
- Aspose.PSD Java
- PSD layer effects
- gradient overlay effect
linktitle: 使用 Java 修改 PSD 中的漸層覆蓋效果
second_title: Aspose.PSD Java API
title: 修改漸層疊加 Java – 使用 Java 修改 PSD 中的漸層疊加效果
url: /zh-hant/java/psd-layer-management-effects/modify-gradient-overlay-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 修改 Gradient Overlay Java – 使用 Java 修改 PSD 中的 Gradient Overlay 效果

## 介紹

在本教學中，您將學習如何 **modify gradient overlay java** 以使用 Aspose.PSD for Java 更改 Photoshop (PSD) 檔案中的 Gradient Overlay 效果。無論您是自動化重複的設計工作，或是構建自訂的影像處理流程，掌握此技巧即可在不開啟 Photoshop 的情況下為作品增添專業感。

## 快速解答
- **我需要哪個函式庫？** Aspose.PSD for Java (download **[here](https://releases.aspose.com/psd/java/)**)。  
- **需要哪個 Java 版本？** JDK 1.8 or later.  
- **我可以在任何圖層上添加 gradient overlay 嗎？** Yes – just target the desired layer index.  
- **生產環境是否需要授權？** Yes, a commercial license is needed for non‑evaluation use.  
- **實作大約需要多久？** Roughly 10‑15 minutes for a basic setup.

## 什麼是 “modify gradient overlay java”？

在 Java 中修改 gradient overlay 意味著以程式方式調整位於 PSD 圖層之上的視覺漸層。這讓您可以在不使用 Photoshop 手動編輯的情況下變更顏色、不透明度、混合模式、角度與比例。

## 為什麼使用 Aspose.PSD 來添加 gradient overlay PSD 圖層？

- **自動化：** 在批次作業中處理數十個 PSD 檔案。  
- **精確度：** 為不透明度、角度和顏色點設定精確的數值。  
- **跨平台：** 在 Windows、Linux 或 macOS 上執行相同程式碼。  
- **不需要 Photoshop：** 適用於伺服器端渲染或 CI 流程。

## 前置條件

- Aspose.PSD for Java 函式庫 – 從上方連結下載。  
- 已安裝 Java Development Kit (JDK) 1.8+。  
- IDE，例如 IntelliJ IDEA 或 Eclipse。  
- 包含至少一個欲編輯圖層的範例 PSD 檔案。  
- 具備 Java 語法的基本認識。

確認清單後，我們即可深入程式碼。

## 匯入套件

首先，匯入可讓我們存取 PSD 處理、圖層效果與漸層設定的類別。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layereffects.ILayerEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 如何 modify gradient overlay java – 步驟 1：載入 PSD 檔案

使用 `PsdLoadOptions` 載入檔案可確保保留任何現有的效果。

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "psdnet256.psd";

// Enable support for existing layer effects
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);

// Load the PSD file
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath, psdLoadOptions);
```

## 如何 add gradient overlay PSD – 步驟 2：定位目標圖層

識別您想編輯的圖層。在本範例中，我們使用第二個圖層 (`[1]`)。

```java
BlendingOptions layerBlendOptions = psdImage.getLayers()[1].getBlendingOptions();
```

## 步驟 3：搜尋現有的 Gradient Overlay 效果

我們會取得現有的效果，若不存在則建立新的效果。

```java
GradientOverlayEffect gradientOverlayEffect = null;
for (ILayerEffect effect : layerBlendOptions.getEffects()) {
    if (effect instanceof GradientOverlayEffect) {
        gradientOverlayEffect = (GradientOverlayEffect) effect;
        break;
    }
}

if (gradientOverlayEffect == null) {
    // Create a new GradientOverlayEffect if it doesn't exist
    gradientOverlayEffect = layerBlendOptions.addGradientOverlay();
}
```

## 步驟 4：修改 Gradient Overlay 效果

### 設定不透明度與混合模式

```java
gradientOverlayEffect.setOpacity((byte) 200);
gradientOverlayEffect.setBlendMode(BlendMode.Hue);
```

### 自訂漸層顏色與設定

```java
GradientFillSettings settings = gradientOverlayEffect.getSettings();
settings.setColorPoints(new IGradientColorPoint[]{
        new GradientColorPoint(Color.getGreenYellow(), 0, 50),
        new GradientColorPoint(Color.getBlueViolet(), 4096, 50),
});
settings.setAngle(80);
settings.setScale(150);
settings.setGradientType(GradientType.Linear);
settings.getTransparencyPoints()[0].setOpacity(100);
settings.getTransparencyPoints()[1].setOpacity(100);
```

## 步驟 5：儲存已修改的 PSD 檔案

最後，將變更寫入新檔案並清理資源。

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "psdnet256.psd_output.psd";

psdImage.save(outPsdFilePath);
psdImage.dispose();
```

## 常見問題與解決方案

- **儲存後效果未顯示：** 請確認圖層索引正確，且混合模式未設定為會隱藏漸層的模式（例如 `Normal` 且不透明度為 0 %）。  
- **顏色點顛倒：** `GradientColorPoint` 物件的順序決定起點到終點；若漸層方向與預期相反，請交換順序。  
- **載入時例外：** 確認已呼叫 `psdLoadOptions.setLoadEffectsResource(true)`；否則可能忽略現有效果，導致 `null` 參考。

## 常見問答

### 我可以在單一圖層上套用多個 gradient overlay 嗎？

是的，您可以透過向圖層的混合選項新增 `GradientOverlayEffect` 實例，為單一圖層套用多個 gradient overlay。

### 可以從圖層移除 gradient overlay 效果嗎？

當然可以！只要從圖層的混合選項中刪除對應的效果，即可移除已存在的 gradient overlay。

### 使用 Aspose.PSD for Java 我還能套用哪些其他效果？

Aspose.PSD for Java 可套用多種效果，如投影、內發光、外發光等。您可以依需求自訂每項效果。

### 我要如何還原對 PSD 檔案的變更？

如果尚未儲存檔案，您只需重新載入原始 PSD 檔案。若已儲存，則需從備份還原或以程式方式撤銷變更。

## 常見問題

**Q: 這適用於包含 smart objects 的 PSD 檔案嗎？**  
A: 是的，但 smart objects 會被視為一般圖層；gradient overlay 會影響其點陣化的表示。

**Q: 我可以串接多個具有不同混合模式的 gradient overlay 嗎？**  
A: 當然可以。每個 `GradientOverlayEffect` 都可以擁有自己的混合模式，從而實現複雜的視覺組合。

**Q: 有辦法在修改前讀取目前的 gradient 設定嗎？**  
A: 有。使用 `gradientOverlayEffect.getSettings()` 取得現有的 `GradientFillSettings`，並檢查其屬性。

**Q: 修改後的 PSD 仍能與 Photoshop 相容嗎？**  
A: 儲存的檔案遵循 PSD 規範，Photoshop 能順利開啟，並保留新加入或編輯的 gradient overlay。

**Q: 開發版是否需要商業授權？**  
A: 測試時免費評估授權即可，但正式部署需購買授權。

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}