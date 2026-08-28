---
date: 2026-08-28
description: 使用 Aspose.PSD 在 Java 中向 layer 添加 pattern。请按照本分步指南应用 stroke layer effect，配置
  pattern resources，并高效保存您的 PSD files。
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: 如何在 Java 中添加 Stroke Layer Pattern
og_description: 使用 Aspose.PSD 在 Java 中向 layer 添加 pattern。请遵循本简明指南应用 stroke layer effect，配置
  pattern resources，并高效保存您的 PSD files。
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: 在 Java 中向 layer 添加 pattern – Aspose.PSD 教程
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
title: 如何在 Java 中向 layer 添加 pattern
url: /zh/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中向图层添加图案

## 介绍
在 Java 中向图层添加图案是一个常见需求，当您需要使用自定义描边效果来丰富 Photoshop PSD 文件时。使用 Aspose.PSD for Java，这项任务变得直观，即使您是库的新手。在本教程中，您将学习如何加载 PSD、创建图案资源、将其附加到描边效果，并保存结果——全部通过清晰的逐步说明。

## 快速答案
- **需要哪个库？** Aspose.PSD for Java。  
- **实现需要多长时间？** 基本图案大约需要 10‑15 分钟。  
- **我需要许可证吗？** 免费试用可用于开发；生产环境需要商业许可证。  
- **支持哪个 Java 版本？** JDK 8 或更高。  
- **我可以在 Web 服务中使用吗？** 可以，API 与平台无关，可在任何 Java 环境中运行。

## 向图层添加图案是什么？
向图层添加图案是指将平铺的位图分配给描边或填充效果，使图形在形状轮廓上重复。此技术广泛用于装饰边框、纹理和品牌叠加，允许设计师在不手动绘制每个元素的情况下创建一致的视觉主题。

## 为什么在此任务中使用 Aspose.PSD？
Aspose.PSD 支持 **30+ 图像格式**，并且能够在不将整个文档加载到内存中的情况下操作高达 **2 GB** 的 PSD 文件，在典型服务器硬件上提供快速性能。其流畅的 API 让您能够以编程方式处理图层效果，消除在自动化流水线中使用 Photoshop 的需求。

## 先决条件
在开始之前，请确保您具备以下条件：
- 已安装 Java Development Kit (JDK) 8 或更高版本。
- Aspose.PSD for Java – 从 **Aspose.PSD for Java 下载页面**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) 下载并将 JAR 添加到项目的类路径中。
- 一个 IDE，例如 IntelliJ IDEA 或 Eclipse，用于编辑和运行示例代码。
- 一个包含您想要修改的形状图层的示例 PSD 文件。

## 导入包
首先，导入提供对 PSD 对象、资源和效果访问的命名空间。

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

## 如何在 Java 中向图层添加图案？

加载目标 PSD，创建图案资源，将其附加到所需图层的描边效果，最后保存文件。此端到端流程仅需几行代码，并适用于任何包含矢量形状图层的标准 PSD。

### 步骤 1：加载 PSD 文件
加载文档后，您可以访问其图层层次结构和效果集合。  
`PsdLoadOptions` 配置 PSD 的读取方式，而 `PsdImage` 表示内存中的已加载文件。

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

通过加载 PSD 文件，您现在可以访问并操作其图层和效果。

### 步骤 2：准备新图案数据
`PatternResource` 保存您想要平铺为描边图案的位图。  
`PatternResource` 是 PSD 的全局资源，用于存储重复的位图图案。`Rectangle` 定义图案的边界，`UUID` 提供唯一标识符。

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

此图案数据将用于创建新的描边效果。

### 步骤 3：访问描边效果
`StrokeEffect` 表示应用于形状图层的描边图层效果。

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

这确保您正在处理正确的图层和效果。

### 步骤 4：修改描边效果
现在更新描边的属性以引用新的图案资源。

#### 更新描边效果属性
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### 更新图案资源
`PattResource` 是 PSD 的全局图层资源，用于存储图案数据。

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

这些代码段将现有图案替换为您提供的图案。

### 步骤 5：应用新图案
`PatternFillSettings` 保存基于图案的描边效果的填充设置。将更改提交到图层并将更新后的 PSD 写回磁盘。

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

这确保新图案正确应用并保存了更改。

### 步骤 6：验证更改
重新加载文件并检查描边，以确认图案如预期出现。

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

此步骤验证图案数据已正确应用到描边效果。

## 常见问题和故障排除
- **图案不可见：** 确保图案图像的 DPI 与 PSD 的分辨率匹配，并且描边的 `Enabled` 标志设置为 `true`。  
- **大型 PSD 文件导致 OutOfMemoryError：** 使用 `PsdImage.load(..., LoadOptions)` 并将 `LoadOptions.setLoadAllLayers(false)` 设置为按需加载图层。  
- **选择了错误的图层：** 在访问其效果之前验证图层索引或名称；您可以枚举 `psdImage.getLayers()` 列出可用图层。

## 常见问题

**Q: 什么是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一个库，使开发人员能够以编程方式创建、编辑和转换 PSD（Photoshop Document）文件。

**Q: 我可以在商业项目中使用 Aspose.PSD for Java 吗？**  
A: 可以，您可以在商业项目中使用它。您可以从 **Aspose 购买页面**([Aspose purchase page](https://purchase.aspose.com/buy)) 购买许可证。

**Q: 是否有 Aspose.PSD for Java 的免费试用版？**  
A: 有，您可以从 **Aspose 发布页面**([Aspose releases page](https://releases.aspose.com/)) 下载免费试用版。

**Q: 我如何获得 Aspose.PSD for Java 的支持？**  
A: 您可以在 Aspose 社区论坛 **此处**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)) 获取支持。

**Q: Aspose.PSD for Java 的系统要求是什么？**  
A: 您需要安装 JDK 并拥有用于开发的 IDE。该库支持 Windows、Linux 和 macOS。

## 结论
您现在已经学习了如何使用 Aspose.PSD 在 Java 中向图层添加图案。通过上述步骤，您可以以编程方式为 PSD 文件添加自定义描边图案，自动化品牌工作流，并将图形处理集成到任何基于 Java 的应用程序中。探索 Aspose.PSD 的其他功能，如图层合并、颜色调整以及导出为 PNG 或 JPEG，以进一步扩展您的图像处理工具箱。

---

**最后更新：** 2026-08-28  
**测试环境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose

## 相关教程

- [渲染图案填充图层 PSD 文件](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [图案叠加 PSD：使用 Aspose.PSD for Java 添加效果](/psd/java/advanced-image-effects/add-pattern-effects/)
- [如何使用 Aspose.PSD 在 Java 中更改描边颜色](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}