---
title: 如何在 Java 中添加描边图层图案
linktitle: 如何在 Java 中添加描边图层图案
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 将描边图层图案添加到 PSD 文件。按照此分步指南轻松增强您的图像。
type: docs
weight: 11
url: /zh/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## 介绍
在 Java 中向图像添加描边图层图案可能听起来是一项艰巨的任务，但使用 Aspose.PSD for Java，这比您想象的要容易。无论您是设计图形还是使用照片编辑应用程序，本指南都将逐步引导您完成整个过程。准备好开始了吗？让我们深入了解吧！
## 先决条件
在开始之前，您需要一些东西：
- Java 开发工具包 (JDK)：确保您的系统上安装了 JDK。
-  Aspose.PSD for Java：从以下位置下载库[这里](https://releases.aspose.com/psd/java/)并将其包含在您的项目中。
- IDE：使用您最喜欢的集成开发环境 (IDE)，例如 IntelliJ IDEA 或 Eclipse。
## 导入包
首先，您需要将必要的包导入到您的 Java 项目中。这些软件包对于使用 Aspose.PSD 至关重要。
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## 第 1 步：加载 PSD 文件
添加描边图层图案的第一步是加载要编辑的 PSD 文件。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
通过加载 PSD 文件，您现在可以访问和操作其图层和效果。
## 第2步：准备新的模式数据
接下来，您需要准备将应用于笔划图层的新图案数据。
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
该图案数据将用于创建新的笔画效果。
## 第 3 步：访问描边效果
要修改描边效果，您需要访问特定图层及其混合选项。
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
这可确保您使用正确的图层和效果。
## 第四步：修改描边效果
现在，让我们用新的图案数据修改笔划效果。
### 更新描边效果属性
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### 更新模式资源
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
此代码片段使用新的模式数据更新模式资源。
## 第 5 步：应用新模式
最后，将新图案应用到描边效果并保存更改。
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
这可确保正确应用新模式并保存更改后的文件。
## 第 6 步：验证更改
为了确保一切正常，请再次加载文件并验证更改。
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
此步骤验证图案数据是否已正确应用于笔画效果。
## 结论
现在你就得到了它！您已使用 Aspose.PSD for Java 成功将描边图层图案添加到 PSD 文件中。通过执行以下步骤，您可以轻松自定义和增强图像。快乐编码！
## 常见问题解答
### 什么是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一个库，允许开发人员以编程方式创建、编辑和转换 PSD（Photoshop 文档）文件。
### 我可以在商业项目中使用 Aspose.PSD for Java 吗？
是的，您可以在商业项目中使用它。您可以从以下位置购买许可证[这里](https://purchase.aspose.com/buy).
### Aspose.PSD for Java 是否有免费试用版？
是的，您可以从以下位置下载免费试用版[这里](https://releases.aspose.com/).
### 如何获得 Aspose.PSD for Java 支持？
您可以从 Aspose 社区论坛获得支持[这里](https://forum.aspose.com/c/psd/34).
### Aspose.PSD for Java 有哪些系统要求？
您需要安装 JDK 和 IDE 来进行开发。该库支持多种操作系统，包括 Windows、Linux 和 macOS。