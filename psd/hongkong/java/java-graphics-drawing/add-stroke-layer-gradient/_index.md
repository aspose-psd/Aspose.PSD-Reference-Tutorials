---
date: 2026-01-14
description: 學習如何使用 Aspose.PSD for Java 在 PSD 檔案中建立漸層描邊圖層並自訂描邊漸層，透過此一步一步的教學。
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中創建漸層描邊圖層
url: /zh-hant/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中建立漸層描邊圖層

## 介紹
有沒有想過要在 PSD 檔案中 **建立漸層描邊圖層**，卻又想用 Java 來完成？您來對地方了！今天我們將深入探討 Aspose.PSD for Java——這個功能強大的函式庫，讓您輕鬆操作 PSD 檔案。無論您是圖形程式設計新手，或是想微調既有設計，本指南都會一步一步帶您加入並自訂描邊漸層。

## 快速回答
- **主要目標是什麼？** 在 PSD 檔案上建立漸層描邊圖層。  
- **需要哪個函式庫？** Aspose.PSD for Java。  
- **需要授權嗎？** 需要，有效（或暫時）授權才能在正式環境使用。  
- **支援哪個 Java 版本？** Java 8 或以上。  
- **實作大約需要多久？** 基本的漸層描邊大約 10‑15 分鐘即可完成。

## 什麼是漸層描邊圖層？
漸層描邊圖層是圍繞形狀或文字的向量輪廓，顏色會在不同色彩之間平滑過渡。使用 Aspose.PSD，您可以以程式方式定義顏色、透明度、角度以及類型（線性、徑向等）的描邊。

## 為什麼使用 Aspose.PSD for Java？
- **完整 PSD 支援** – 讀取、編輯、寫入 PSD 檔案，無需 Photoshop。  
- **豐富的效果 API** – 取得描邊、陰影、發光等多種圖層效果。  
- **跨平台** – 在任何支援 Java 的作業系統上皆可執行。  
- **無原生相依** – 純 Java 實作，易於整合至 CI 流程。

## 前置條件
1. **Java Development Kit (JDK)** – 從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-downloads.html) 下載並安裝最新的 JDK。  
2. **Aspose.PSD for Java** – 從 [Aspose.PSD 下載頁面](https://releases.aspose.com/psd/java/) 取得函式庫。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 NetBeans。  
4. **授權** – 若沒有正式授權，請取得 [暫時授權](https://purchase.aspose.com/temporary-license/)。

## 匯入套件
首先，匯入我們在載入 PSD、存取效果以及設定漸層填色時需要的類別。

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

現在讓我們把整個流程拆解成清晰的步驟。

## 步驟 1：載入 PSD 檔案
載入來源 PSD，並啟用效果資源，使描邊效果可用。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## 步驟 2：存取描邊效果
假設要修改的描邊位於第三個圖層（索引 2），我們取得它的 `StrokeEffect`。

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## 步驟 3：驗證描邊效果屬性
在進行變更前，我們先確認現有設定，以確保知道要更新哪些項目。

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

## 步驟 4：修改漸層填色設定
在此步驟中，我們變更顏色、透明度、混合模式等屬性，以達到預期的外觀。

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

## 步驟 5：新增與修改顏色與透明度點
加入新的顏色與透明度點，並調整既有的點，以塑造漸層效果。

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

## 步驟 6：儲存已修改的 PSD 檔案
完成所有調整後，將更新後的檔案寫回磁碟。

```java
im.save(exportPath);
```

## 步驟 7：驗證修改結果
載入剛儲存的檔案，並斷言每個屬性都已正確套用變更。

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
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## 結論
現在您已掌握如何使用 Aspose.PSD for Java 在 PSD 檔案中 **建立漸層描邊圖層**。只要載入 PSD、存取描邊效果、調整漸層填色設定，最後儲存結果，即可在不開啟 Photoshop 的情況下，程式化產生專業等級的圖形。

## 常見問題
### 什麼是 Aspose.PSD for Java？
Aspose.PSD for Java 是一套讓開發者在 Java 應用程式中處理 PSD 檔案的函式庫，提供建立、操作與轉換 PSD 檔案的功能。

### 使用 Aspose.PSD for Java 是否需要授權？
是的，使用 Aspose.PSD for Java 必須擁有有效授權。您可以取得 [暫時授權](https://purchase.aspose.com/temporary-license/) 以進行評估。

### 我可以用 Aspose.PSD for Java 從頭建立 PSD 檔案嗎？
當然可以！Aspose.PSD for Java 提供完整的 API，讓您以程式方式建立與操作 PSD 檔案。

### 是否可以使用 Aspose.PSD for Java 套用其他效果？
可以，您可以使用 Aspose.PSD for Java 套用陰影、發光等各種效果。

### 哪裡可以找到 Aspose.PSD for Java 的文件說明？
您可以在此處取得文件說明 [here](https://reference.aspose.com/psd/java/)。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-01-14  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose