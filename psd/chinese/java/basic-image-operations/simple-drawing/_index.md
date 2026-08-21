---
date: 2026-06-13
description: 了解如何使用 Aspose.PSD for Java 在 PSD 文件中绘制矩形。本指南展示了 step‑by‑step 代码、添加 layers、server‑side
  image processing 和 shape drawing。
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: 执行简单绘图
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何在 PSD 中使用 Aspose.PSD for Java 绘制矩形
url: /zh/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 PSD 中使用 Aspose.PSD for Java 绘制矩形

## 介绍

在本教程中，您将学习使用纯 Java 的 Aspose.PSD 库在 Photoshop PSD 文件中 **如何绘制矩形**。无论您是构建服务器端资产流水线、自动化缩略图生成，还是向现有设计添加动态图形，以下步骤都为您提供完整的、可投入生产的解决方案。我们将介绍创建新的 PSD 文档、添加图层、清除背景，最后绘制红色和蓝色矩形——全部无需启动 Photoshop。

## 快速答案
- **创建 PSD 文件的主要类是什么？** `PsdImage`
- **哪个方法用于清除图层的背景颜色？** `Graphics.clear(Color)`
- **如何绘制红色矩形？** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **开发时需要许可证吗？** 免费试用可用于测试；生产环境需要许可证。
- **我可以使用相同的 API 操作已有的 PSD 文件吗？** 是的，Aspose.PSD 支持完整的 PSD 编辑。

## 在 PSD 文件中绘制红色矩形是什么？

绘制红色矩形是指使用 `Graphics` 对象在 PSD 图像的特定图层上渲染一个填充或描边为红色的矩形形状。此操作常用于突出显示区域、创建占位符或以编程方式添加简单图形。

## 为什么使用 Aspose.PSD for Java 来操作 PSD 文件？

Aspose.PSD for Java 支持 **50+ input and output formats**，能够在不将整个文件加载到内存的情况下处理多百页的 PSD 文件，并可在任何支持 Java 8 或更高版本的平台上运行。其服务器端图像处理引擎消除了对 Photoshop 的需求，降低了许可成本，并实现了自动化工作流，能够在普通虚拟机上每小时处理高达 **10 GB** 的图像数据。

## 先决条件

- 已在机器上安装 Java Development Kit (JDK) 8 或更高版本。  
- Aspose.PSD for Java 库。您可以从 [Aspose.PSD for Java 文档](https://reference.aspose.com/psd/java/) 下载。

## 导入包

`import` 语句将所需的类引入作用域，以便您可以处理 PSD 图像、图层、颜色和图形。

`PsdImage` 类是 Aspose.PSD 的顶层对象，表示内存中的单个 PSD 文件。  
`Graphics` 提供绘图原语，如直线、矩形和椭圆。  
`Color` 和 `Pen` 让您指定笔触颜色和粗细。  
`Layer` 类表示 PSD 文档中的单个图像图层。  
`Rectangle` 类定义用于绘图操作的矩形区域的位置和大小。  
`SolidBrush` 类使用纯色填充形状。

## 创建 PSD 文档的第一步是什么？

您通过提供像素单位的画布宽度和高度来实例化 `PsdImage`，从而创建空的 PSD 文件结构。设置好任何初始图层或背景后，调用 `save` 方法并传入文件路径，将文档写入磁盘。这为后续的编辑操作做好准备。

## 步骤 1：创建新文档

首先，使用所需的画布尺寸创建一个全新的 PSD 文档。该文档将承载我们将要绘制的图层。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 如何向 PSD 图像添加一个新的空白图层？

首先，使用与父 `PsdImage` 相同的宽度和高度创建一个新的 `Layer` 实例。然后使用 `add` 方法将此图层添加到图像的 `Layers` 集合中。图层加入图像后，获取其 `Graphics` 对象以执行绘图操作；如果缺少此步骤，绘图将不会显示。

## 步骤 2：添加图层

接下来，添加一个覆盖图像全部宽高的空白图层。图层对于分离绘图操作至关重要。

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## 清除图层背景颜色的目的是什么？

使用特定的 `Color` 调用 `Graphics.clear` 会用该颜色填充整个图层，从而有效地重置所有像素数据。这确保了先前的内容被移除，图层从已知的背景开始，避免在后续在 Photoshop 中打开或编辑 PSD 时出现意外的透明度或颜色混合。

## 步骤 3：绘制形状

我们将使用 `Graphics` 类来操作图层的像素数据。下面是三个示例，演示如何清除背景并使用不同颜色绘制矩形。

### 清除图层颜色（将背景设为黄色）

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### 绘制红色矩形（主要示例）

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 绘制蓝色矩形（附加示例）

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## 如何将编辑后的 PSD 文件保存到磁盘？

在 `PsdImage` 对象上使用 `save` 方法，传入完整的文件路径，并可选地指定所需的图像格式（默认即 PSD）。此操作将所有图层、蒙版和绘图指令写入符合 Photoshop 规范的单个 PSD 文件，从而可以无警告地打开。

## 步骤 4：保存更改

最后，将修改后的 PSD 图像写入磁盘。文件将包含新的图层和绘制的形状。

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## 常见问题及解决方案

- **绘制后图层不可见：** 确保在创建 `Graphics` 对象之前 **before** 将图层添加到图像中。绘图表面必须附加到有效的图层上。
- **颜色显示不正确：** 验证您使用的是 `Color.getRed()`（或 `Color.getBlue()`），而不是构造超出 0‑255 范围的自定义 RGB 值。
- **文件未保存：** 确认 `outputDir` 路径存在且应用程序具有写入权限。在 Linux 上，可能需要调整文件夹所有权或使用 `Files.createDirectories`。
- **大文件性能下降：** 使用 `PsdImage` 的 `setLoadOptions` 仅加载所需通道，降低超过 200 MB 的 PSD 文件的内存消耗。

## 常见问题

**Q1: 我可以使用 Aspose.PSD for Java 来操作已有的 PSD 文件吗？**  
A1: 是的，Aspose.PSD for Java 提供了广泛的功能来编辑和操作现有的 PSD 文件，包括图层重新排序、蒙版调整和矢量绘图。

**Q2: 我在哪里可以找到 Aspose.PSD for Java 的支持？**  
A2: 您可以访问 [Aspose.PSD for Java 论坛](https://forum.aspose.com/c/psd/34) 获取社区驱动的帮助和官方 Aspose 的回复。

**Q3: 是否提供 Aspose.PSD for Java 的免费试用？**  
A3: 是的，您可以在 [此处](https://releases.aspose.com/) 获取免费试用版。试用版包含所有功能，但会在保存的文件中添加水印。

**Q4: 我如何购买 Aspose.PSD for Java 的许可证？**  
A4: 您可以从 [Aspose.PSD 购买页面](https://purchase.aspose.com/buy) 购买许可证。许可选项包括永久授权、订阅和站点授权。

**Q5: 是否提供 Aspose.PSD for Java 的临时许可证？**  
A5: 是的，您可以在 [此处](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

## 其他常见问题

**Q: 我可以绘制除矩形之外的其他形状吗？**  
A: 是的，`Graphics` 类还支持通过 `drawPath` 方法绘制椭圆、直线和自定义路径。

**Q: Aspose.PSD 是否支持绘制形状的透明度？**  
A: 当然；您可以使用带有 ARGB 颜色的 `SolidBrush` 来包含 alpha 透明度，从而实现半透明叠加。

**Q: 是否可以编辑图层的透明度？**  
A: 是的，每个 `Layer` 对象都有 `setOpacity` 方法，接受 0 到 255 的值，以实现对图层透明度的细粒度控制。

**Q: 我如何加载已有的 PSD 文件而不是创建新文件？**  
A: 在操作图层之前，使用 `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` 加载已有的 PSD 文件。加载的图像保留所有原始图层和蒙版。

## 结论

您已经掌握了使用 Aspose.PSD for Java 在 PSD 文件中 **如何绘制矩形** 并操作图层的技巧。通过创建文档、添加图层、清除背景以及使用 `Graphics` API 绘图，您可以在服务器端自动化无数图形设计任务。尝试不同的笔、画刷和图层效果，将此基础扩展为完整的图像生成流水线。

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [如何在 Java 中绘制形状 – 基础图像操作](/psd/java/basic-image-operations/)
- [使用 Aspose.PSD 进行简单缩放 – Java 图像处理库](/psd/java/basic-image-operations/simple-resizing/)
- [在 Aspose.PSD for Java 中按矩形裁剪图像](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**最后更新：** 2026-06-13  
**测试环境：** Aspose.PSD for Java 24.12 (latest at time of writing)  
**作者：** Aspose