---
date: 2026-09-03
description: 了解如何使用 Aspose.PSD for Java 建立 Java 漸層描邊並自訂 PSD 檔案中的描邊漸層。為開發人員提供的逐步指南。
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: 如何在 Java 中建立漸層描邊圖層
og_description: 使用 Aspose.PSD for Java 在數分鐘內建立 Java 漸層描邊。本教學示範如何在 PSD 檔案中新增與自訂漸層描邊，並提供程式碼範例與最佳實踐。
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: Create gradient stroke java – Aspose.PSD 教學指南
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: Create gradient stroke java – Aspose.PSD 教學指南
url: /zh-hant/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD 在 Java 中建立漸層描邊

## 介紹
如果您需要在不開啟 Photoshop 的情況下 **create gradient stroke java** 效果，您來對地方了。在本教學中，您將學習如何使用 Aspose.PSD for Java——一個純 Java 函式庫，讓您完整程式化控制 PSD 檔案。我們將示範如何載入 PSD、存取圖層的描邊效果、設定漸層填充，最後儲存結果。完成後，您只需幾行程式碼即可為形狀或文字加入專業等級的漸層輪廓。

## 快速解答
- **主要目標是什麼？** 使用 Java 在 PSD 檔案上建立漸層描邊圖層。  
- **哪個函式庫提供 API？** Aspose.PSD for Java（支援 Java 8 +）。  
- **生產環境需要授權嗎？** 需要——必須使用有效或暫時授權。  
- **基本實作需要多長時間？** 簡單描邊大約需要 10‑15 分鐘。  
- **可以自訂漸層類型嗎？** 當然可以——支援線性、徑向與角度式漸層。

## 什麼是漸層描邊圖層？
漸層描邊圖層是一種向量輪廓，其顏色在兩種或多種色調之間平滑過渡。它可套用於形狀、文字或 PSD 檔案內的任何向量遮色片，為設計師提供動態視覺效果，且不會將圖形點陣化。

## 為什麼使用 Aspose.PSD for Java？
Aspose.PSD for Java 提供 **完整的 PSD 支援**，涵蓋超過 100 項功能——包括圖層、遮色片、調整圖層與圖層效果，且可在不將整個文件載入記憶體的情況下處理高達 2 GB 的檔案。此函式庫可在任何支援 Java 的作業系統上執行，無需原生相依性，且每月更新以保持與最新 Photoshop 檔案規格相容。

## 前置條件
1. **Java Development Kit (JDK)** – 從 [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html) 下載並安裝最新的 JDK。  
2. **Aspose.PSD for Java** – 從 [Aspose.PSD download page](https://releases.aspose.com/psd/java/) 下載函式庫。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 NetBeans。  
4. **License** – 若沒有完整商業授權，請取得 [temporary license](https://purchase.aspose.com/temporary-license/)。

## 匯入套件
`import` 陳述式會將必要的類別帶入作用域。  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

現在讓我們把流程拆解成清晰的步驟。

## 步驟 1：載入 PSD 檔案
載入來源檔案是第一步；必須啟用效果資源，以便取得可編輯的描邊資訊。**PsdLoadOptions** 可設定 PSD 檔案的載入方式，讓您啟用或停用特定資源。  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## 步驟 2：存取描邊效果
**StrokeEffect** 代表套用於圖層的輪廓樣式，包括寬度、顏色與漸層填充。  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## 步驟 3：驗證描邊效果屬性
在修改任何內容之前，先讀取現有屬性是良好做法。這能讓您了解目前的設定，避免不小心覆寫重要設定。**GradientFillSettings** 保存描邊效果的漸層填充配置。  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## 步驟 4：修改漸層填充設定
`GradientFill` 定義顏色在描邊上的過渡方式。您可以變更其類型（線性、徑向）、角度與混合模式，然後指派新的顏色與透明度點。  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## 步驟 5：新增與修改顏色與透明度點
漸層由一系列顏色停點與不透明度停點組成。**GradientColorPoint** 定義漸層中的顏色停點，指定其顏色與位置。**GradientTransparencyPoint** 定義漸層中的不透明度停點，指定其不透明度與位置。新增或調整這些點即可塑造描邊的視覺流向。  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## 步驟 6：儲存已修改的 PSD 檔案
完成所有調整後，將更新後的文件寫回磁碟。Aspose.PSD 會自動保留其他所有圖層與資源。  

```text
```java
im.save(exportPath);
```
```

## 步驟 7：驗證修改結果
重新載入已儲存的檔案，並斷言描邊的漸層屬性與您設定的值相符。此驗證步驟對自動化流程至關重要。**Assert** 提供簡易的測試斷言，用於執行期間驗證條件。  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## 常見問題與除錯技巧
- **Missing license error** – 若看到授權例外，請再次確認在任何 API 呼叫之前已正確載入暫時授權檔案。  
- **Gradient not visible** – 請確保目標圖層的 `strokeEnabled` 旗標已設為 `true`，否則在渲染時會忽略此效果。  
- **Performance on large files** – 對於超過 500 MB 的 PSD，建議使用 `PsdImage.load(..., LoadOptions)` 並將 `loadResources = false`，僅啟用您需要的資源，以提升效能。

## 常見問答

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java 是一個純 Java 函式庫，讓開發者能在不需要 Adobe Photoshop 的情況下，建立、編輯、轉換與渲染 Photoshop PSD 檔案。

**Q: Do I need a license to use Aspose.PSD for Java?**  
A: 需要，生產環境必須使用有效授權。您可以取得 [temporary license](https://purchase.aspose.com/temporary-license/) 以進行評估。

**Q: Can I create PSD files from scratch with this library?**  
A: 當然可以。Aspose.PSD 提供 API 讓您從頭建立 PSD 文件、加入圖層、套用效果，並完整程式化儲存檔案。

**Q: Is it possible to apply other effects besides gradient strokes?**  
A: 可以，您同樣可以使用基於效果的 API 套用陰影、發光、斜角等多種圖層效果。

**Q: Where can I find the full reference documentation?**  
A: 完整文件可於 [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/) 取得。

## 結論
現在您已掌握使用 Aspose.PSD 在 PSD 檔案中 **create gradient stroke java** 的完整端對端解決方案。透過載入 PSD、存取描邊效果、設定漸層填充並儲存檔案，您可以自動化原本需要手動在 Photoshop 中完成的複雜圖形工作流程。請嘗試不同的漸層類型、混合模式與不透明度停點，以取得符合您應用需求的精確外觀。

---

**Last Updated:** 2026-09-03  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## 相關教學

- [使用 Aspose.PSD 於 Java 建立漸層填充 PSD – 新增漸層填充圖層](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [在 Aspose.PSD for Java 中建立徑向漸層效果](/psd/java/advanced-image-effects/add-gradient-effects/)
- [使用 Aspose.PSD 於 Java 變更描邊顏色](/psd/java/advanced-image-effects/add-stroke-layer-color/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}