---
date: 2026-08-28
description: 使用 Aspose.PSD 在 Java 中為圖層添加圖案。請按照此逐步指南套用描邊圖層效果、配置圖案資源，並高效儲存您的 PSD 檔案。
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: 如何在 Java 中為描邊圖層添加圖案
og_description: 使用 Aspose.PSD 在 Java 中為圖層添加圖案。請遵循此簡明指南套用描邊圖層效果、配置圖案資源，並高效儲存您的 PSD
  檔案。
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: 在 Java 中為圖層添加圖案 – Aspose.PSD 教程
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: 如何在 Java 中為圖層添加圖案
url: /zh-hant/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中為圖層添加圖案

## 介紹
在 Java 中為圖層添加圖案是一個常見需求，當您需要使用自訂描邊效果豐富 Photoshop PSD 檔案時。使用 Aspose.PSD for Java，這項工作變得簡單，即使您是新手也沒問題。在本教學中，您將學習如何載入 PSD、建立圖案資源、將其附加到描邊效果，並儲存結果——全部以清晰的逐步說明呈現。

## 快速回答
- **需要的函式庫是什麼？** Aspose.PSD for Java.  
- **實作需要多長時間？** 基本圖案大約需要 10‑15 分鐘。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **支援哪個 Java 版本？** JDK 8 或更新版本。  
- **可以在 Web 服務中使用嗎？** 是的，API 與平台無關，可在任何 Java 環境中使用。  

## 為圖層添加圖案是什麼？
為圖層添加圖案是指將平鋪的點陣圖指派給描邊或填色效果，使圖形在形狀輪廓上重複。此技術廣泛用於裝飾邊框、紋理與品牌覆蓋層，讓設計師能在不手動繪製每個元素的情況下，建立一致的視覺主題。

## 為什麼要使用 Aspose.PSD 來完成此任務？
Aspose.PSD 支援 **30 多種影像格式**，且可在不將整個文件載入記憶體的情況下操作最高 **2 GB** 的 PSD 檔案，於一般伺服器硬體上提供快速效能。其流暢的 API 讓您以程式方式處理圖層效果，省去在自動化流程中使用 Photoshop 的需求。

## 前置條件
在開始之前，請確保您已具備以下條件：
- 已安裝 Java Development Kit (JDK) 8 或更新版本。
- Aspose.PSD for Java – 從 **Aspose.PSD for Java 下載頁面**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) 下載，並將 JAR 加入專案的 classpath。
- 一個如 IntelliJ IDEA 或 Eclipse 的 IDE，用於編輯與執行範例程式碼。
- 一個包含您想要修改之形狀圖層的範例 PSD 檔案。

## 匯入套件
首先，匯入提供 PSD 物件、資源與效果存取的命名空間。

```
// No actual code block is added to preserve original placeholders.
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
```

## 如何在 Java 中為圖層添加圖案？

載入目標 PSD，建立圖案資源，將其附加到目標圖層的描邊效果，最後儲存檔案。此端對端流程僅需幾行程式碼，即可適用於任何包含向量形狀圖層的標準 PSD。

### 步驟 1：載入 PSD 檔案
載入文件後，您即可存取其圖層層級結構與效果集合。  
`PsdLoadOptions` 用於設定 PSD 的讀取方式，而 `PsdImage` 代表記憶體中的已載入檔案。

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

透過載入 PSD 檔案，您現在可以存取並操作其圖層與效果。

### 步驟 2：準備新圖案資料
建立一個 `PatternResource`，用於保存您想要作為描邊圖案平鋪的點陣圖。`PatternResource` 為 PSD 的全域資源，儲存可重複的點陣圖圖案。`Rectangle` 定義圖案的邊界，`UUID` 提供唯一識別碼。

```
// Placeholder for original code.
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
```

此圖案資料將用於建立新的描邊效果。

### 步驟 3：存取描邊效果
找出已具備描邊的形狀圖層，然後取得其 `StrokeEffect` 物件。`StrokeEffect` 代表套用於形狀圖層的描邊圖層效果。

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

此步驟確保您正操作正確的圖層與效果。

### 步驟 4：修改描邊效果
現在更新描邊的屬性，以參照新的圖案資源。

#### 更新描邊效果屬性
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### 更新圖案資源
`PattResource` 為 PSD 的全域圖層資源，儲存圖案資料。

```
// Placeholder for original code.
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
```

這些程式碼片段會將現有圖案替換為您提供的圖案。

### 步驟 5：套用新圖案
`PatternFillSettings` 保存基於圖案的描邊效果的填充設定。將變更提交至圖層，並將更新後的 PSD 寫回磁碟。

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

此步驟確保新圖案正確套用，且檔案已儲存變更。

### 步驟 6：驗證變更
重新載入檔案，檢查描邊以確認圖案如預期顯示。

```
// Placeholder for original code.
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
```

此步驟驗證圖案資料已正確套用至描邊效果。

## 常見問題與故障排除
- **圖案未顯示：** 確保圖案影像的 DPI 與 PSD 的解析度相符，且描邊的 `Enabled` 標誌設定為 `true`。  
- **大型 PSD 檔案導致 OutOfMemoryError：** 使用 `PsdImage.load(..., LoadOptions)` 並以 `LoadOptions.setLoadAllLayers(false)` 於需要時載入圖層。  
- **選取了錯誤的圖層：** 在存取其效果前，先確認圖層索引或名稱；您可以列舉 `psdImage.getLayers()` 以列出可用圖層。  

## 常見問答

**Q: Aspose.PSD for Java 是什麼？**  
A: Aspose.PSD for Java 是一個讓開發人員能以程式方式建立、編輯與轉換 PSD（Photoshop Document）檔案的函式庫。

**Q: 我可以在商業專案中使用 Aspose.PSD for Java 嗎？**  
A: 可以，您可在商業專案中使用。您可以從 **Aspose 授權購買頁面**([Aspose purchase page](https://purchase.aspose.com/buy)) 購買授權。

**Q: 是否提供 Aspose.PSD for Java 的免費試用版？**  
A: 有，您可從 **Aspose 下載頁面**([Aspose releases page](https://releases.aspose.com/)) 下載免費試用版。

**Q: 我該如何取得 Aspose.PSD for Java 的支援？**  
A: 您可從 Aspose 社群論壇 **此處**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)) 獲得支援。

**Q: Aspose.PSD for Java 的系統需求是什麼？**  
A: 您需要安裝 JDK 以及開發用的 IDE。此函式庫支援 Windows、Linux 與 macOS。

## 結論
您現在已學會如何使用 Aspose.PSD 在 Java 中為圖層添加圖案。依循上述步驟，您即可以程式方式為 PSD 檔案加入自訂描邊圖案，自動化品牌工作流程，並將圖形處理整合至任何基於 Java 的應用程式。探索其他 Aspose.PSD 功能，如圖層合併、顏色調整，以及匯出為 PNG 或 JPEG，以進一步擴充您的影像處理工具箱。

---

**最後更新：** 2026-08-28  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose

## 相關教學

- [渲染圖案填充圖層 PSD 檔案](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [圖案覆蓋 PSD：使用 Aspose.PSD for Java 添加效果](/psd/java/advanced-image-effects/add-pattern-effects/)
- [如何在 Java 中使用 Aspose.PSD 更改描邊顏色](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}