---
date: 2026-04-03
description: 學習如何使用 Aspose.PSD for Java 將 PSD 儲存為帶有描邊效果和顏色填充的 PNG。本分步指南快速展示如何將 PSD
  匯出為 PNG。
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: 將 PSD 另存為 PNG 並套用描邊效果 – Java
second_title: Aspose.PSD Java API
title: 將 PSD 另存為 PNG 並套用描邊效果 – Java
url: /zh-hant/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 儲存為 PNG 並套用描邊效果與顏色填充 – Java

## 簡介

在本指南中，您將學習如何使用 Aspose.PSD for Java 在套用描邊效果與顏色填充的同時 **將 PSD 儲存為 PNG**。無論您是資深開發者或剛入門，此步驟式教學都能讓您輕鬆完成任務。我們將從環境設定講起，直到匯出最終影像，讓您能快速在自己的專案中 **將 PSD 匯出為 PNG**。

## 快速解答
- **此教學的目的為何？** 它示範如何在套用可自訂的描邊效果後，將 PSD 檔案儲存為 PNG。  
- **使用哪個函式庫？** Aspose.PSD for Java。  
- **需要授權嗎？** 免費試用可用於測試；正式環境需購買授權。  
- **可以更改描邊顏色嗎？** 可以——您可以透過 `ColorFillSettings` 設定任意顏色。  
- **是否支援批次處理？** 當然可以——將程式碼包在迴圈中即可處理多個 PSD 檔案。

## 什麼是「將 PSD 儲存為 PNG」？
將 PSD 儲存為 PNG 意味著將 Photoshop 原生的分層檔案轉換為平面、適合網路使用的影像格式，同時保留視覺品質。當您需要在網站、行動應用程式或任何不直接支援 PSD 檔案的平台上顯示 PSD 內容時，這非常有用。

## 為什麼要套用描邊效果與顏色填充？
描邊會在圖層內容周圍添加清晰的輪廓，使圖形在複雜背景下更為突出。將其與自訂填充顏色結合，可讓您為影像加上品牌色、突顯 UI 元素，或製作引人注目的縮圖，而無需離開 Photoshop。

## 先決條件

1. **Java Development Kit (JDK) 8+** – 確保 `java` 已加入 PATH。  
2. **Aspose.PSD for Java** – 從[網站](https://releases.aspose.com/psd/java/)下載。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
4. **範例 PSD** – 已包含描邊效果的檔案（或在 Photoshop 中自行加入）。  
5. **基本的 Java 知識** – 您只需撰寫少量程式碼，並無高階需求。

一旦準備就緒，我們即可開始編寫程式碼。

## 匯入套件

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

這些匯入語句提供了載入 PSD、修改描邊以及儲存 PSD 與 PNG 輸出的所有必要類別。

## 如何將 PSD 儲存為 PNG 並套用描邊效果

### 步驟 1：載入 PSD 檔案

首先，指向存放來源 PSD 的資料夾。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為您機器上的實際路徑。

現在載入檔案，同時保留任何現有的效果資源：

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 步驟 2：設定描邊顏色（並可選擇自訂寬度）

以下迴圈會遍歷每個圖層，取得第一個 `StrokeEffect`，並更改其填充顏色。如果需要 **自訂描邊寬度**，也可以在 `StrokeEffect` 物件上調整 `setWidth` 或 `setPosition`。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> 小技巧：`Color.getDeepPink()` 只是一個範例。若要自訂 RGB 值，請使用 `new Color(r, g, b)`。

### 步驟 3：儲存已修改的 PSD（可選）

如果您想保留已更新描邊的 PSD 版本，可使用以下方式儲存：

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### 步驟 4：將影像匯出為 PNG（核心「將 PSD 儲存為 PNG」步驟）

最後，將編輯過的 PSD 轉換為可供網路使用的 PNG 檔案：

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

此 PNG 會保留先前設定的深粉紅描邊，且 `TruecolorWithAlpha` 選項確保透明度得以保留。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|------|------|----------|
| **`ArrayIndexOutOfBoundsException`** | 圖層沒有任何效果，或第一個效果不是 `StrokeEffect`。 | 確認圖層確實包含描邊，或遍歷 `getEffects()` 以尋找正確的類型。 |
| **顏色未變更** | 您可能編輯的是設定的副本，而非原始設定。 | 確保直接從 `effect.getFillSettings()` 轉型為 `ColorFillSettings`。 |
| **PNG 顯示空白** | PSD 在載入時未對圖層進行光柵化。 | 在完成所有修改後呼叫 `im.save(..., new PngOptions())`；避免在變更前先儲存原始的 `im`。 |

## 常見問與答

**Q: 我可以使用 Aspose.PSD for Java 為單一圖層套用多個效果嗎？**  
A: 可以，您可以存取圖層的混合選項，並依需求加入任意數量的效果，包括陰影、發光與描邊等。

**Q: 能否自動化處理一批 PSD 檔案？**  
A: 當然可以。將載入、套用效果與儲存的邏輯包在 `for‑each` 迴圈中，遍歷目錄中的檔案即可。

**Q: 如何還原對 PSD 檔案所做的變更？**  
A: 在儲存任何修改之前重新載入原始檔案；Aspose.PSD 並未提供撤銷堆疊功能。

**Q: 我可以自訂描邊寬度與位置嗎？**  
A: 可以。使用 `effect.setWidth(float)` 與 `effect.setPosition(StrokeEffect.Position)` 來控制厚度與位置（內側、外側或居中）。

**Q: Aspose.PSD for Java 函式庫可以免費使用嗎？**  
A: 提供免費試用版供評估。完整功能需購買授權。詳情請參閱 [購買選項](https://purchase.aspose.com/buy)。

---

**最後更新：** 2026-04-03  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}