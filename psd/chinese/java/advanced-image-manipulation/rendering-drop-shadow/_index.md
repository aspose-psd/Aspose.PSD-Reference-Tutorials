---
date: 2025-12-04
description: 了解如何使用 Aspose.PSD for Java 将 PSD 保存为 PNG 并应用渲染投影阴影。本指南涵盖如何添加阴影、将 PSD
  转换为 PNG，以及在 Java 中应用投影阴影。
language: zh
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD Java 将 PSD 保存为 PNG 并添加投影阴影
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 PSD 保存为 PNG 并添加投影（Aspose.PSD Java）

## 介绍

如果你在 Java 中处理 Photoshop 文件，**将 PSD 保存为 PNG** 并添加专业外观的投影是常见需求。Aspose.PSD 让此任务变得简单，只需几行代码即可**将 PSD 转换为 PNG**并**在 Java 中应用投影**。本教程将从加载 PSD 文件到导出带有渲染投影效果的最终 PNG，完整演示整个过程。

## 快速回答
- **“将 PSD 保存为 PNG”是什么意思？** 它将分层的 Photoshop 文件转换为平面的 PNG 图像，保留透明度。  
- **转换时可以添加投影吗？** 可以——Aspose.PSD 允许在导出前修改图层效果。  
- **运行代码需要许可证吗？** 免费试用可用于评估；生产环境需要许可证。  
- **支持哪个 Java 版本？** Java 8 或更高。  
- **投影效果可以自定义吗？** 当然——可以调节颜色、透明度、距离、大小、角度等参数。

## 前置条件

在开始之前，请确保你已经具备：

- **Java 开发环境** – 已安装 JDK 8 或更高版本。  
- **Aspose.PSD 库** – 从官方站点[此处](https://releases.aspose.com/psd/java/)下载最新 JAR。  
- **PSD 文件** – 包含至少一个你想添加投影的图层的文件。  

## 如何在 Java 中将 PSD 保存为 PNG 并添加投影？

下面是逐步指南。每一步都有简要说明以及需要复制的完整代码。

### 步骤 1：导入所需的包

我们首先导入提供图像加载、效果处理和 PNG 导出功能的类。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### 步骤 2：定义文档目录

设置源 PSD 和生成的 PNG 所在的文件夹。

```java
String dataDir = "Your Document Directory";
```

### 步骤 3：设置 PSD 与 PNG 文件路径

指定输入 PSD 和输出 PNG 的完整路径。

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### 步骤 4：加载启用效果的 PSD 文件

启用 **loadEffectsResource** 可确保图层效果（如投影）可供操作。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 步骤 5：访问投影效果

这里我们获取第二个图层（索引 1）上应用的第一个效果。随后即可读取或修改投影参数。

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 步骤 6：验证投影属性（可选但有帮助）

检查现有属性有助于决定是否需要更改。下面的断言确认默认值。

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **小贴士：** 如果想要**使用自定义设置添加投影**，在保存之前修改 `shadowEffect` 的属性，例如 `shadowEffect.setColor(Color.getRed());`。

### 步骤 7：将修改后的图像保存为 PNG

最后，我们将带有渲染投影的 PSD 导出为 PNG 文件。`TruecolorWithAlpha` 选项可保留透明度。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

至此，你已经完成了一个完整的 **将 PSD 转换为 PNG** 工作流，同时在单次操作中**在 Java 中应用投影**。

## 为什么选择 Aspose.PSD 来完成此任务？

- **无需本地 Photoshop** – 在任何支持 Java 的平台上均可运行。  
- **完整的 PSD 保真度** – 所有图层信息、蒙版和效果均被保留。  
- **细粒度控制** – 在导出前可调节投影的每个参数。  
- **高性能** – 针对大文件和批处理进行优化。

## 常见问题与故障排除

| 症状 | 可能原因 | 解决办法 |
|------|----------|----------|
| `NullPointerException` 出现在 `shadowEffect` 上 | 目标图层没有效果或索引错误。 | 检查图层索引 (`im.getLayers()[i]`) 并确保存在效果。 |
| 导出的 PNG 为空白 | PNG 选项未正确设置或图像未保存。 | 使用 `PngColorType.TruecolorWithAlpha` 并确认 `im.save()` 路径可写。 |
| 投影颜色不可见 | 投影不透明度为 0 或颜色与背景相同。 | 设置 `shadowEffect.setOpacity(255);` 并选择对比度高的颜色。 |

## 常见问答

**问：可以一次对多个图层添加投影吗？**  
答：可以。遍历 `im.getLayers()` 并根据需要修改每个图层的 `DropShadowEffect`。

**问：“Spread” 参数的作用是什么？**  
答：它控制投影从完全不透明到透明的过渡程度。数值越高，边缘越硬。

**问：Aspose.PSD 是否兼容所有 Photoshop 版本？**  
答：它支持从早期版本到最新 Photoshop CC 文件的广泛 PSD 版本。

**问：如果遇到问题，如何获取帮助？**  
答：访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34) 获取社区支持和官方帮助。

**问：可以在购买前试用 Aspose.PSD 吗？**  
答：当然可以。从 [Aspose 官网](https://releases.aspose.com/) 下载免费试用版。

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**最后更新：** 2025-12-04  
**测试环境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

---