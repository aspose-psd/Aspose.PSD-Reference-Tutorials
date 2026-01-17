---
date: 2026-01-17
description: 了解如何使用 Aspose.PSD for Java 添加笔画图案。请按照本分步指南快速提升您的 PSD 图像。
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中使用 Aspose.PSD 添加描边图案
url: /zh/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD 在 Java 中添加描边图案

## Introduction
如果您需要 **add stroke pattern java**，Aspose.PSD for Java 让它出奇地简单。无论您是在构建图形设计工具、自动化批量编辑，还是仅仅在尝试图层效果，本教程将带您一步步完成——从加载 PSD 到验证新图案。让我们深入了解，看看您多快就能增强图像。

## Quick Answers
- **我需要哪个库？** Aspose.PSD for Java  
- **支持哪个 Java 版本？** JDK 8 或更高  
- **测试是否需要许可证？** 免费试用可用于开发；生产环境需要许可证  
- **实现大约需要多长时间？** 基本图案描边大约 10‑15 分钟  
- **可以在多个图层上复用该图案吗？** 可以，只需将相同的 `PattResource` 分配给其他图层  

## What is add stroke pattern java?
在 Java 中添加描边图案是指将自定义填充（通常是重复的位图）应用于图层的描边效果。这种技术让您能够创建风格化的轮廓——比如虚线、砖块纹理或自定义图形边框——直接在 PSD 文件中，而无需打开 Photoshop。

## Why Use Aspose.PSD for add stroke pattern java?
- **完整的 PSD 保真度** – 所有图层效果、资源和混合模式均被保留。  
- **无需原生 Photoshop** – 在任何装有 JDK 的操作系统上均可运行。  
- **编程控制** – 自动化批处理或集成到服务器端服务中。  
- **丰富的 API** – 在统一的流畅接口中访问全局资源、图案填充和混合模式。

## Prerequisites
- **Java 开发工具包 (JDK)** – 确保已安装 JDK 8 或更高版本。  
- **Aspose.PSD for Java** – 从 [here](https://releases.aspose.com/psd/java/) 下载库并将 JAR 添加到项目的类路径中。  
- **IDE** – IntelliJ IDEA、Eclipse 或您喜欢的任何编辑器。

## Import Packages
First, import the classes you’ll need for handling PSD files, colors, rectangles, and stroke effects.

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

## Step 1: Load the PSD File
Load the source PSD so you can work with its layers and resources.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 2: Prepare New Pattern Data
Create a simple 4 × 4 pixel pattern that will be used for the stroke.

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

## Step 3: Access the Stroke Effect
Locate the stroke effect on the target layer (in this example, the fourth layer).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Step 4: Modify the Stroke Effect
### Update Stroke Effect Properties
Adjust opacity and blend mode to see the visual impact of the new pattern.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Update the Pattern Resource
Replace the existing global pattern resource with the one you just created.

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

## Step 5: Apply the New Pattern
Bind the updated pattern resource to the stroke effect and save the PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Step 6: Verify the Changes
Reload the file and confirm that the new pattern, opacity, and blend mode are correctly applied.

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

## Common Issues and Solutions
| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| 图案未显示 | `PatternId` 引用错误 | 确保在 `PattResource` 上设置的 `PatternId` 与 `PatternFillSettings` 中使用的匹配。 |
| 保存后描边消失 | 不透明度设为 0 或效果被隐藏 | 验证 `setOpacity` 在 0‑255 之间且 `isVisible()` 返回 `true`。 |
| 颜色异常 | 混合模式不匹配 | 使用 `BlendMode.Color`（或其他符合设计意图的模式）。 |

## FAQ's
### Aspose.PSD for Java 是什么？
Aspose.PSD for Java 是一个库，允许开发者以编程方式创建、编辑和转换 PSD（Photoshop 文档）文件。

### 我可以在商业项目中使用 Aspose.PSD for Java 吗？
可以，您可以在商业项目中使用。可从 [here](https://purchase.aspose.com/buy) 购买许可证。

### Aspose.PSD for Java 有免费试用吗？
有，您可以从 [here](https://releases.aspose.com/) 下载免费试用版。

### 如何获取 Aspose.PSD for Java 的支持？
您可以在 Aspose 社区论坛 [here](https://forum.aspose.com/c/psd/34) 获得支持。

### Aspose.PSD for Java 的系统要求是什么？
您需要安装 JDK 并准备一个 IDE 用于开发。该库支持包括 Windows、Linux 和 macOS 在内的多种操作系统。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose