---
title: 如何在 Java 中添加描边图层渐变
linktitle: 如何在 Java 中添加描边图层渐变
second_title: Aspose.PSD Java API
description: 通过这个全面的分步教程，了解如何使用 Aspose.PSD for Java 在 PSD 文件中添加和自定义笔划图层渐变。
type: docs
weight: 10
url: /zh/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## 介绍
有没有想过如何使用 Java 向图像添加描边图层渐变？嗯，您来对地方了！今天，我们将深入了解 Aspose.PSD for Java 的世界，这是一个功能强大的库，可帮助您轻松操作 PSD 文件。无论您是初学者还是经验丰富的开发人员，本分步指南都将引导您完成向 PSD 文件添加描边图层渐变的过程。因此，系好安全带，准备好提高您的图形编辑技能！
## 先决条件
在我们开始之前，您需要做好一些准备工作。确保您具备以下条件：
1.  Java 开发工具包 (JDK)：确保您的系统上安装了 JDK。您可以从以下位置下载：[甲骨文网站](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library：您可以从[Aspose.PSD下载页面](https://releases.aspose.com/psd/java/).
3. 集成开发环境 (IDE)：任何 IDE（例如 IntelliJ IDEA、Eclipse 或 NetBeans）都可以使用。
4. 有效许可证：您可以获得[临时执照](https://purchase.aspose.com/temporary-license/)如果你没有完整的。
## 导入包
首先，让我们导入必要的包。这些将使我们能够使用操作 PSD 文件所需的类和方法。
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
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
现在，让我们将示例分解为多个步骤以便更好地理解。
## 第 1 步：加载 PSD 文件
首先，我们需要加载要修改的PSD文件。我们将使用`PsdLoadOptions`指定我们要加载效果资源。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## 第 2 步：访问描边效果
接下来，我们需要访问我们感兴趣的图层的描边效果。这里，我们假设它是 PSD 文件中的第三层（索引 2）。
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## 步骤 3：验证描边效果属性
在进行任何更改之前，我们先验证一下描边效果的属性，以确保我们修改的是正确的设置。
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
## 步骤 4：修改渐变填充设置
现在，是时候根据我们的要求修改渐变填充设置了。我们将更改颜色、不透明度、混合模式和其他属性。
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
## 第 5 步：添加和修改颜色和透明度点
让我们添加新的颜色和透明度点并修改现有的以实现所需的渐变效果。
```java
//添加新色点
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
//更改前一点的位置
fillSettings.getColorPoints()[1].setLocation(1899);
//添加新的透明点
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
//更改先前透明点的位置
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## 第6步：保存修改后的PSD文件
进行所有必要的修改后，我们需要保存 PSD 文件。
```java
im.save(exportPath);
```
## 第 7 步：验证修改
最后，让我们加载保存的 PSD 文件并验证我们的更改是否已正确应用。
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
//检查色点
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
//检查透明度点
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
## 结论
现在你就得到了它！您现在知道如何使用 Aspose.PSD for Java 在 PSD 文件中添加和操作笔划图层渐变。本教程介绍了加载 PSD 文件、访问和修改描边效果以及保存更改。借助这些技能，您可以创建具有视觉吸引力的渐变并自定义 PSD 文件以满足您的需求。
## 常见问题解答
### 什么是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一个库，允许开发人员在 Java 应用程序中使用 PSD 文件，提供创建、操作和转换 PSD 文件的功能。
### 我需要许可证才能使用 Aspose.PSD for Java 吗？
是的，您需要有效的许可证才能使用 Aspose.PSD for Java。你可以获得一个[临时执照](https://purchase.aspose.com/temporary-license/)出于评估目的。
### 我可以使用 Aspose.PSD for Java 从头开始创建 PSD 文件吗？
绝对地！ Aspose.PSD for Java 提供了全面的 API 来以编程方式创建和操作 PSD 文件。
### 是否可以使用 Aspose.PSD for Java 应用其他效果？
是的，您可以使用 Aspose.PSD for Java 应用各种效果，如阴影、发光等。
### 在哪里可以找到 Aspose.PSD for Java 的文档？
你可以找到文档[这里](https://reference.aspose.com/psd/java/).