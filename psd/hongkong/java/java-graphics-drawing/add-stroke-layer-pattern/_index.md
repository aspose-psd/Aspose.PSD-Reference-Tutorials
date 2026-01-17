---
date: 2026-01-17
description: 學習如何使用 Aspose.PSD for Java 添加筆劃圖樣。跟隨此一步一步的指南，快速提升您的 PSD 圖像。
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中使用 Aspose.PSD 添加筆劃樣式
url: /zh-hant/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD 中使用 Java 添加筆劃圖案

## 介紹
如果您需要 **在 Photoshop 檔案中添加筆劃圖案（Java）**，Aspose.PSD for Java 讓這個過程變得相當簡單。無論您是在開發圖形設計工具、自動化批次編輯，或只是想試驗圖層效果，本教學都會一步步帶您完成——從載入 PSD 到驗證新圖案。讓我們一起快速提升影像效果吧。

## 快速答覆
- **需要哪個函式庫？** Aspose.PSD for Java  
- **支援哪個 Java 版本？** JDK 8 或更新版本  
- **測試需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買授權  
- **實作大約需要多久？** 基本圖案筆劃約 10‑15 分鐘即可完成  
- **可以在多個圖層重複使用圖案嗎？** 可以，只要將相同的 `PattResource` 指派給其他圖層即可  

## 什麼是 add stroke pattern java？
在 Java 中添加筆劃圖案是指將自訂的填充（通常是重複的點陣圖）套用到圖層的筆劃效果。此技巧可讓您直接在 PSD 檔案內建立風格化的輪廓──例如虛線、磚牆紋理或自訂圖形邊框──而不必開啟 Photoshop。

## 為什麼使用 Aspose.PSD 來 add stroke pattern java？
- **完整的 PSD 相容性** – 所有圖層效果、資源與混合模式皆會被完整保留。  
- **不需本機 Photoshop** – 只要有 JDK 的作業系統皆可執行。  
- **程式化控制** – 可自動化批次處理或整合至伺服器端服務。  
- **功能豐富的 API** – 透過單一流暢介面即可存取全域資源、圖案填充與混合模式。  

## 前置條件
- **Java Development Kit (JDK)** – 請確保已安裝 JDK 8 或更新版本。  
- **Aspose.PSD for Java** – 從 [此處](https://releases.aspose.com/psd/java/) 下載函式庫，並將 JAR 加入專案的 classpath。  
- **IDE** – IntelliJ IDEA、Eclipse，或您慣用的任何編輯器。  

## 匯入套件
首先，匯入處理 PSD、顏色、矩形與筆劃效果所需的類別。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## 步驟 1：載入 PSD 檔案
載入來源 PSD，以便操作其圖層與資源。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## 步驟 2：準備新圖案資料
建立一個 4 × 4 像素的簡易圖案，作為筆劃使用。

```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```

## 步驟 3：取得筆劃效果
在目標圖層（本例為第四層）上找到筆劃效果。

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## 步驟 4：修改筆劃效果
### 更新筆劃效果屬性
調整不透明度與混合模式，以觀察新圖案的視覺效果。

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### 更新圖案資源
以剛建立的圖案取代現有的全域圖案資源。

```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```

## 步驟 5：套用新圖案
將更新後的圖案資源綁定至筆劃效果，並儲存 PSD。

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## 步驟 6：驗證變更
重新載入檔案，確認新圖案、不透明度與混合模式已正確套用。

```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```

## 常見問題與解決方案
| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 圖案未顯示 | `PatternId` 參考錯誤 | 確認 `PattResource` 上設定的 `PatternId` 與 `PatternFillSettings` 中使用的相同。 |
| 筆劃儲存後消失 | 不透明度設為 0 或效果被隱藏 | 確認 `setOpacity` 的值介於 0‑255 之間，且 `isVisible()` 回傳 `true`。 |
| 顏色異常 | 混合模式不符 | 使用符合設計需求的 `BlendMode.Color`（或其他模式）。 |

## 常見問答
### 什麼是 Aspose.PSD for Java？
Aspose.PSD for Java 是一套讓開發者能以程式方式建立、編輯與轉換 PSD（Photoshop Document）檔案的函式庫。

### 可以在商業專案中使用 Aspose.PSD for Java 嗎？
可以，您可於商業專案中使用。請從 [此處](https://purchase.aspose.com/buy) 購買授權。

### 有提供免費試用版嗎？
有，您可從 [此處](https://releases.aspose.com/) 下載免費試用版。

### 如何取得 Aspose.PSD for Java 的支援？
您可以在 Aspose 社群論壇取得支援，連結在 [此處](https://forum.aspose.com/c/psd/34)。

### Aspose.PSD for Java 的系統需求是什麼？
您需要安裝 JDK 與開發用的 IDE。此函式庫支援多種作業系統，包括 Windows、Linux 與 macOS。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新日期：** 2026-01-17  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose