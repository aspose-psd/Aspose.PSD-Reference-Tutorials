---
date: 2026-03-31
description: 學習如何使用 Aspose.PSD for Java 將 PSD 儲存為 PNG。此 PSD 通道混合器教學示範如何將 PSD 轉換為 PNG、修改
  RGB 與 CMYK 圖層，以及批次處理 PSD 檔案。
linktitle: Export Channel Mixer Adjustment Layer in PSD - Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中使用通道混合器調整圖層將 PSD 儲存為 PNG
url: /zh-hant/java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Channel Mixer 調整圖層將 PSD 儲存為 PNG

## 介紹

如果您需要在保留 Channel Mixer 圖層所做調整的同時 **將 PSD 儲存為 PNG**，您來對地方了。在本步驟式 **psd channel mixer 教學** 中，我們將示範如何載入 PSD 檔案、調整 RGB 與 CMYK Channel Mixer 調整圖層，最後匯出為 PNG。您也會看到相同的做法如何擴展至 **批次處理 PSD 檔案** 以應對大型專案。

## 快速解答
- **「將 PSD 儲存為 PNG」是什麼意思？** 它會將 Photoshop 文件轉換為無損的 PNG，並保留透明度。  
- **哪個函式庫負責轉換？** Aspose.PSD for Java 提供對調整圖層的完整支援。  
- **我可以同時處理 RGB 與 CMYK 檔案嗎？** 可以 – API 包含 `RgbChannelMixerLayer` 與 `CmykChannelMixerLayer` 類別。  
- **正式環境需要授權嗎？** 需要授權版本；測試時可使用臨時授權。  
- **可以批次處理嗎？** 當然可以 – 您可以遍歷資料夾，對每個 PSD 套用相同步驟。

## 什麼是 Channel Mixer 調整圖層？

Channel Mixer 調整圖層允許您重新混合紅、綠、藍（或青、品紅、黃、黑）通道的貢獻，以達到精確的色彩平衡。與一般圖層不同，它是非破壞性的，意味著原始像素資料保持不變。

## 為什麼使用 Aspose.PSD 來 **將 PSD 轉換為 PNG**？

- **完整圖層保真度** – 轉換過程中會保留所有調整圖層。  
- **不需 Photoshop** – 可在任何伺服器或 CI 流程上執行程式碼。  
- **同時支援 RGB 與 CMYK** – 適合列印就緒的工作流程。  

## 前置條件

1. **Aspose.PSD for Java** – 從 [download page](https://releases.aspose.com/psd/java/) 下載。  
2. **Java Development Kit (JDK) 8+** – 確認 `java` 已加入 PATH。  
3. **IDE** – IntelliJ IDEA、Eclipse 或您偏好的任何編輯器。  
4. **範例 PSD 檔案** – 含有 Channel Mixer 調整圖層的檔案（包括 RGB 與 CMYK 變體）。  

## 匯入套件

首先，匯入我們需要的類別。這會為處理 PSD 檔案與 PNG 匯出選項建立環境。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 如何 **將 PSD 儲存為 PNG** – RGB 範例

### 步驟 1：載入包含 RGB Channel Mixer 圖層的 PSD 檔案

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";

PsdImage im = (PsdImage) Image.load(sourceFileName);
```

我們指向保存 PSD 的資料夾（`dataDir`），並將檔案載入 `PsdImage` 物件，從而完整存取其圖層。

### 步驟 2：修改 RGB Channel Mixer 圖層

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof RgbChannelMixerLayer) {
        RgbChannelMixerLayer rgbLayer = (RgbChannelMixerLayer) im.getLayers()[i];
        rgbLayer.getRedChannel().setBlue((short) 100);
        rgbLayer.getBlueChannel().setGreen((short) -100);
        rgbLayer.getGreenChannel().setConstant((short) 50);
    }
}
```

我們遍歷所有圖層，找到 `RgbChannelMixerLayer`，並調整其通道數值。此範例將紅色通道中的藍色貢獻提升，降低藍色通道中的綠色，並對綠色通道加入固定偏移。

### 步驟 3：儲存已修改的 PSD（仍為 PSD）

```java
String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
im.save(psdPathAfterChange);
```

儲存檔案會保留調整圖層，讓您日後如有需要可在 Photoshop 中重新開啟。

### 步驟 4：將影像匯出為 PNG（即 **將 PSD 儲存為 PNG** 步驟）

```java
String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

我們建立 `PngOptions` 實例，將顏色類型設定為 `TruecolorWithAlpha` 以保留透明度，然後匯出影像。

## 如何 **將 PSD 儲存為 PNG** – CMYK 範例

### 步驟 5：載入包含 CMYK Channel Mixer 圖層的 PSD 檔案

```java
sourceFileName = dataDir + "ChannelMixerAdjustmentLayerCmyk.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

載入流程相同；只是不同行使用 CMYK 色彩模型的檔案。

### 步驟 6：修改 CMYK Channel Mixer 圖層

```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof CmykChannelMixerLayer) {
        CmykChannelMixerLayer cmykLayer = (CmykChannelMixerLayer) img.getLayers()[i];
        cmykLayer.getCyanChannel().setBlack((short) 20);
        cmykLayer.getMagentaChannel().setYellow((short) 50);
        cmykLayer.getYellowChannel().setCyan((short) -25);
        cmykLayer.getBlackChannel().setYellow((short) 25);
    }
}
```

在此我們調整 CMYK 通道：將黑色加入青色、微調品紅的黃色成分等。這展示了 API 在列印導向檔案上的彈性。

### 步驟 7：儲存已修改的 CMYK PSD

```java
psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
img.save(psdPathAfterChange);
```

同樣，我們保留帶有新調整的 PSD 版本。

### 步驟 8：將 CMYK 影像匯出為 PNG

```java
pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
img.save(pngExportPath, options);
```

即使來源為 CMYK，PNG 匯出仍會自動轉換為基於 RGB 的 PNG，並保留透明度。

## 常見問題與解決方案

| 問題 | 為何發生 | 解決方法 |
|------|----------|----------|
| PNG 顯示顏色錯誤 | CMYK → RGB 轉換未使用正確的色彩配置檔 | 確認來源 PSD 已嵌入 ICC 配置檔；Aspose.PSD 於匯出時會遵循該配置檔。 |
| 找不到調整圖層 | 圖層類型不符（例如是「色階平衡」圖層） | 在轉型前先確認圖層類別 (`RgbChannelMixerLayer` 或 `CmykChannelMixerLayer`)。 |
| 執行時出現授權例外 | 未使用有效授權使用函式庫 | 在開發期間從 [temporary license](https://purchase.aspose.com/temporary-license/) 頁面套用臨時授權。 |

## 常見問答

**Q: 我可以在 Java 中使用 Aspose.PSD 處理其他影像格式嗎？**  
A: 可以，函式庫支援 PNG、JPEG、BMP、TIFF 等多種格式，除了 PSD 之外。

**Q: 如何處理其他調整圖層，例如曲線或色階？**  
A: 每種調整都有對應的類別（例如 `CurvesAdjustmentLayer`），您可以像處理通道混合器範例一樣操作它們。

**Q: 有沒有方法可以 **批次將 PSD 檔案** 轉換為 PNG？**  
A: 當然可以。將上述步驟包在 `for‑each` 迴圈中，遍歷目錄內的檔案，套用相同的修改與匯出邏輯。

**Q: 轉換時如何保留最高影像品質的最佳實踐是什麼？**  
A: 使用 `PngOptions` 並設定 `TruecolorWithAlpha`，避免降採樣。同時保留原始 PSD，以便日後需要無損編輯時使用。

**Q: 正式環境是否需要付費授權？**  
A: 需要。臨時授權可用於評估，但商業部署必須購買正式授權。

**最後更新：** 2026-03-31  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}