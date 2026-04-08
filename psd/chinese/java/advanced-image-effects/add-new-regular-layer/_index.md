---
date: 2026-04-08
description: 学习如何使用 Aspose.PSD for Java 并通过 Aspose 临时许可证将 PSD 导出为 PNG，以及创建新的 PSD 图层。本分步教程涵盖
  PSD 图像操作和设置图层位置。
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: 向 PSD 添加新普通图层
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 导出 PSD 为 PNG 并添加新普通图层 – Aspose 临时许可证
url: /zh/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 PSD 为 PNG 并使用 Aspose.PSD for Java 添加新常规图层

## 介绍

在本 **aspose psd tutorial** 中，您将了解如何 **export PSD to PNG**，同时在同一文件中 **creating a new regular layer**，并 **using an aspose temporary license** 进行开发。无论是生成适用于网页的缩略图、为设计流水线准备资源，还是仅仅尝试 **psd image manipulation**，Aspose.PSD for Java 都为您提供完整的编程控制。我们将逐步演示每一步——从加载源文件到保存更新后的 PSD 以及 PNG 副本——让您立即开始操作 PSD 图层。

## 快速答案

- **Can I export PSD to PNG with one call?** 是的，添加图层后，您可以使用 `PngOptions` 调用 `save`。
- **Do I need a license for development?** 临时许可证可用于测试；生产环境需要正式许可证。
- **Which Java version is supported?** Aspose.PSD 支持 Java 8 及更高版本。
- **Is layer positioning pixel‑based?** 是的，您使用 **set layer position** 方法以像素设置 left、top、right、bottom 坐标。
- **Will the PNG retain layer transparency?** PNG 将包含所有可见图层的合并结果。

## 为什么使用 aspose 临时许可证？

使用 **aspose temporary license** 可让您在不受功能限制的情况下评估 Aspose.PSD 的完整功能集。它会去除评估水印，解锁所有 API——包括 **create new psd layer** 对象的能力——并让您在类似生产环境中测试代码，随后再购买永久许可证。

## 先决条件

在开始之前，请确保您拥有：

- **Java Development Environment** – 已安装 JDK 8+ 和构建工具（Maven/Gradle）。
- **Aspose.PSD for Java** – 从官方网站 [here](https://releases.aspose.com/psd/java/) 下载最新的 JAR。
- **A sample PSD file** – 示例中我们将使用 `OneLayer.psd`。

## 导入包

在 Java 类中添加所需的导入。这些类提供了 **psd image manipulation** 和图层处理的核心功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 什么是 “set layer position” 并且它为何重要？

当您添加新图层时，需要定义它在画布上的位置。方法 `setLeft`、`setTop`、`setRight` 和 `setBottom` 在像素坐标中 **set layer position**。正确的定位可确保图形准确对齐，这对于合成 UI 资源或准备可打印文件等任务至关重要。

## 分步指南

### 步骤 1：加载 PSD 文件

首先，加载您想要修改的现有 PSD。这将为您提供一个可操作的 `PsdImage` 对象。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### 步骤 2：准备像素数据和矩形

我们将创建两个像素缓冲区（`int[]`），并定义新图层绘制的矩形区域。这是 **creating a new psd layer** 的基础。

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### 步骤 3：初始化图层数据

使用默认的 ARGB 值填充像素缓冲区。数值 `-10000000` 对应于半透明的深色阴影。

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### 步骤 4：添加常规图层（Manipulate PSD Layers）

现在我们 **add regular layers** 到 PSD 图像，并使用 left、top、right、bottom 属性 **set layer position**。这演示了如何以编程方式 **manipulate PSD layers**。

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### 步骤 5：导出 PSD 为 PNG 并保存更新后的 PSD

图层就位后，保存修改后的文档。首先我们将结果导出为 PNG（即 **export psd to png** 步骤），随后保存包含新图层的 PSD。

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** 如果您只需要 PNG，可以跳过 PSD 的 `save` 调用，直接使用 `PngOptions` 调用 `save`。

## 常见问题与故障排除

| 症状 | 可能原因 | 解决办法 |
|---------|--------------|-----|
| PNG 显示为空白 | 图层不可见或完全透明 | 确保设置了非透明像素值或调用 `layer.setVisible(true)`。 |
| `ArrayIndexOutOfBoundsException` | 矩形尺寸与像素数组长度不匹配 | 验证 `rect.width * rect.height == dataArray.length`。 |
| 运行时 LicenseException | 未加载有效许可证 | 在调用任何 API 方法之前加载临时或永久许可证。 |

## 常见问题

**Q: Aspose.PSD 是否兼容 Java 8？**  
A: 是的，Aspose.PSD 支持 Java 8 及更高版本。

**Q: 我可以对添加的图层应用变换（旋转、缩放）吗？**  
A: 当然可以！`Layer` 类提供 `rotate`、`scale`、`translate` 等方法，实现完整的变换控制。

**Q: 我在哪里可以找到更多 Aspose.PSD 文档？**  
A: 详细的 API 文档可在 [here](https://reference.aspose.com/psd/java/) 查看。

**Q: 我如何获取 Aspose.PSD 的临时许可证？**  
A: 请访问临时许可证页面 [here](https://purchase.aspose.com/temporary-license/)。

**Q: 是否有 Aspose.PSD 的社区论坛？**  
A: 有，您可以在 Aspose 论坛 [here](https://forum.aspose.com/c/psd/34) 参与讨论。

## 结论

您现在已经学习了如何使用 Aspose.PSD for Java **export PSD to PNG** 并 **adding new regular layers**，并了解了 **aspose temporary license** 如何让您在无任何限制的情况下尝试此工作流。本教程展示了核心 **psd image manipulation** 能力：加载文件、创建图层、填充像素数据以及导出最终合成。欢迎尝试不同的矩形尺寸、像素颜色或图层效果，以满足项目需求。

---

**最后更新:** 2026-04-08  
**测试环境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}