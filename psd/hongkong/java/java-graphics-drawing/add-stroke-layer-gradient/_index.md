---
title: 如何在 Java 中加入描邊圖層漸變
linktitle: 如何在 Java 中加入描邊圖層漸變
second_title: Aspose.PSD Java API
description: 透過這個全面的逐步教學，了解如何使用 Aspose.PSD for Java 在 PSD 檔案中新增和自訂筆觸圖層漸層。
weight: 10
url: /zh-hant/java/java-graphics-drawing/add-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中加入描邊圖層漸變

## 介紹
有沒有想過如何使用 Java 為影像添加描邊圖層漸層？嗯，您來對地方了！今天，我們將深入了解 Aspose.PSD for Java 的世界，這是一個功能強大的程式庫，可幫助您輕鬆操作 PSD 檔案。無論您是初學者還是經驗豐富的開發人員，本逐步指南都將引導您完成為 PSD 檔案添加描邊圖層漸層的過程。因此，請係好安全帶，準備好提高您的圖形編輯技能！
## 先決條件
在我們開始之前，您需要做好一些準備。確保您具備以下條件：
1.  Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK。您可以從以下位置下載：[甲骨文網站](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library：您可以從[Aspose.PSD下載頁面](https://releases.aspose.com/psd/java/).
3. 整合開發環境 (IDE)：任何 IDE（例如 IntelliJ IDEA、Eclipse 或 NetBeans）都可以使用。
4. 有效許可證：您可以獲得[臨時執照](https://purchase.aspose.com/temporary-license/)如果你沒有完整的。
## 導入包
首先，讓我們導入必要的套件。這些將使我們能夠使用操作 PSD 檔案所需的類別和方法。
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
現在，讓我們將範例分解為多個步驟以便更好地理解。
## 第 1 步：載入 PSD 文件
首先，我們需要載入要修改的PSD檔。我們將使用`PsdLoadOptions`指定我們要載入效果資源。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## 步驟 2： 存取描邊效果
接下來，我們需要存取我們感興趣的圖層的描邊效果。
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## 步驟 3：驗證描邊效果屬性
在進行任何更改之前，我們先驗證描邊效果的屬性，以確保我們修改的是正確的設定。
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
## 步驟 4：修改漸層填滿設置
現在，是時候根據我們的要求修改漸層填充設定了。我們將更改顏色、不透明度、混合模式和其他屬性。
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
## 第 5 步：新增和修改顏色和透明度點
讓我們添加新的顏色和透明度點並修改現有的以實現所需的漸變效果。
```java
//新增色點
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
//更改前一點的位置
fillSettings.getColorPoints()[1].setLocation(1899);
//增加新的透明點
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
//更改先前透明點的位置
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## 步驟6：儲存修改後的PSD文件
進行所有必要的修改後，我們需要儲存 PSD 檔案。
```java
im.save(exportPath);
```
## 第 7 步：驗證修改
最後，讓我們載入已儲存的 PSD 檔案並驗證我們的變更是否已正確應用。
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
//檢查色點
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
//檢查透明度點
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
現在你就擁有了！現在您知道如何使用 Aspose.PSD for Java 在 PSD 檔案中新增和操作筆畫圖層漸層。本教學介紹了載入 PSD 檔案、存取和修改描邊效果以及儲存變更。借助這些技能，您可以創建具有視覺吸引力的漸變並自訂 PSD 檔案以滿足您的需求。
## 常見問題解答
### 什麼是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一個函式庫，可讓開發人員在 Java 應用程式中使用 PSD 文件，提供建立、操作和轉換 PSD 檔案的功能。
### 我需要許可證才能使用 Aspose.PSD for Java 嗎？
是的，您需要有效的授權才能使用 Aspose.PSD for Java。你可以獲得一個[臨時執照](https://purchase.aspose.com/temporary-license/)出於評估目的。
### 我可以使用 Aspose.PSD for Java 從頭開始建立 PSD 檔案嗎？
絕對地！ Aspose.PSD for Java 提供了全面的 API 來以程式設計方式建立和操作 PSD 檔案。
### 是否可以使用 Aspose.PSD for Java 應用其他效果？
是的，您可以使用 Aspose.PSD for Java 應用各種效果，例如陰影、發光等。
### 在哪裡可以找到 Aspose.PSD for Java 的文檔？
你可以找到文檔[這裡](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
