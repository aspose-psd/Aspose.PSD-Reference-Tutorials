---
title: 如何在 Java 中加入描邊圖層圖案
linktitle: 如何在 Java 中加入描邊圖層圖案
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 將描邊圖層圖案新增至 PSD 檔案。請按照此逐步指南輕鬆增強您的影像。
weight: 11
url: /zh-hant/java/java-graphics-drawing/add-stroke-layer-pattern/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中加入描邊圖層圖案

## 介紹
在 Java 中為影像添加描邊圖層圖案可能聽起來是一項艱鉅的任務，但使用 Aspose.PSD for Java，這比您想像的要容易。無論您是設計圖形還是使用照片編輯應用程序，本指南都將逐步引導您完成整個過程。準備好開始了嗎？讓我們深入了解吧！
## 先決條件
在開始之前，您需要一些東西：
- Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK。
-  Aspose.PSD for Java：從以下位置下載庫[這裡](https://releases.aspose.com/psd/java/)並將其包含在您的項目中。
- IDE：使用您最喜歡的整合開發環境 (IDE)，例如 IntelliJ IDEA 或 Eclipse。
## 導入包
首先，您需要將必要的套件匯入到您的 Java 專案中。這些軟體套件對於使用 Aspose.PSD 至關重要。
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
## 第 1 步：載入 PSD 文件
新增描邊圖層圖案的第一步是載入要編輯的 PSD 檔案。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
透過載入 PSD 文件，您現在可以存取和操作其圖層和效果。
## 步驟2：準備新的模式數據
接下來，您需要準備將應用於筆劃圖層的新圖案資料。
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
此圖案資料將用於建立新的筆劃效果。
## 步驟 3： 存取描邊效果
要修改描邊效果，您需要存取特定圖層及其混合選項。
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
這可確保您使用正確的圖層和效果。
## 第四步：修改描邊效果
現在，讓我們用新的圖案資料來修改筆劃效果。
### 更新描邊效果屬性
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### 更新模式資源
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
此程式碼片段使用新的模式資料更新模式資源。
## 第 5 步：應用新模式
最後，將新圖案套用到描邊效果並儲存變更。
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
這可確保正確套用新模式並儲存變更後的檔案。
## 第 6 步：驗證更改
為了確保一切正常，請再次載入檔案並驗證變更。
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
此步驟驗證圖案資料是否已正確應用於筆畫效果。
## 結論
現在你就擁有了！您已使用 Aspose.PSD for Java 成功將描邊圖層圖案新增至 PSD 檔案。透過執行以下步驟，您可以輕鬆自訂和增強影像。快樂編碼！
## 常見問題解答
### 什麼是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一個函式庫，可讓開發人員以程式設計方式建立、編輯和轉換 PSD（Photoshop 文件）檔案。
### 我可以在商業專案中使用 Aspose.PSD for Java 嗎？
是的，您可以在商業項目中使用它。您可以從以下位置購買許可證[這裡](https://purchase.aspose.com/buy).
### Aspose.PSD for Java 是否有免費試用版？
是的，您可以從以下位置下載免費試用版[這裡](https://releases.aspose.com/).
### 如何獲得 Aspose.PSD for Java 支援？
您可以從 Aspose 社群論壇獲得支持[這裡](https://forum.aspose.com/c/psd/34).
### Aspose.PSD for Java 有哪些系統需求？
您需要安裝 JDK 和 IDE 來進行開發。該庫支援多種作業系統，包括 Windows、Linux 和 macOS。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
