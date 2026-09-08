---
date: 2026-09-08
description: 学习如何使用 Aspose.PSD for Java 在图像上绘制矩形，涵盖位图创建、背景颜色设置以及 Java 图像处理的图形初始化。
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: 在 Java 中绘制矩形
og_description: 学习如何使用 Aspose.PSD for Java 在图像上绘制矩形。本指南涵盖位图创建、设置背景颜色以及在 Java 中初始化图形。
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: 如何使用 Aspose.PSD for Java 在图像上绘制矩形
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: 如何使用 Aspose.PSD for Java 在图像上绘制矩形
url: /zh/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 在图像上绘制矩形

## 简介
如果您需要以编程方式在图像上 **how to draw rectangle**，Aspose.PSD for Java 为您提供干净、高性能的 API。在本教程中，您将看到如何创建位图、设置背景颜色，以及 **initialize graphics java** 对象，以便渲染任意大小和颜色的矩形。步骤简单，代码简洁，最终生成的 BMP 文件可在任何基于 Java 的工作流中使用。

## 快速答案
- **哪个库处理矩形绘制？** Aspose.PSD for Java.
- **需要多少行代码？** 大约六行代码即可创建图像、设置背景并绘制两个矩形。
- **支持导出哪些图像格式？** BMP、PNG、JPEG、TIFF、GIF 等。
- **开发是否需要许可证？** 免费试用可用于测试；生产环境需要许可证。
- **我可以更改边框粗细吗？** 可以——在绘制前调整 `Pen` 的 thickness 属性。

## 在图像上绘制矩形是什么？
在图像上绘制矩形是指使用图形上下文在位图上渲染填充或轮廓形状。Aspose.PSD 的 `Graphics` 类提供的方法可以让您一次调用即可指定颜色、位置和尺寸。

## 为什么在矩形绘制中使用 Aspose.PSD for Java？
Aspose.PSD 支持 **50+ 图像格式**，并且可以在不将整个文档加载到内存的情况下处理高达 **2 GB** 的文件。其 `Graphics` API 的运行速度比原生 Java AWT 快 **3 倍**，非常适合高吞吐量的服务器端图像处理。

## 前提条件
在开始之前，请确保您已拥有：

- **Java Development Kit (JDK) 8 或更高版本** 已安装。
- **Aspose.PSD for Java** 库已从 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) 下载并添加到项目的 classpath 中。

### 导入包
`import` 语句让您能够访问位图创建和绘图所需的类。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
这些导入将使您能够访问在图像上绘制矩形所需的类和方法。

## 如何在 Java 中绘制图像上的矩形？
加载一个新的 `PsdImage`，使用背景颜色清除其表面，创建一个 `Graphics` 对象，然后使用所需的笔和刷调用 `drawRectangle`。整个过程只需几次方法调用，即可生成可直接保存的位图。  
`PsdImage` 表示一个可在内存中编辑并保存的位图。  
`Graphics` 提供了在图像上渲染形状的绘图表面。

### 步骤 1：创建新图像
`PsdImage` 类表示一个内存中的位图。初始化它同时会分配像素缓冲区。

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
在此步骤中，`PsdImage` 被初始化为宽度和高度均为 **100 px**，为演示提供了一个小画布。

### 步骤 2：初始化 graphics java 对象
`Graphics` 实例是与您刚创建的图像关联的绘图表面。

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
此 `Graphics` 对象将用于执行绘图操作，例如填充形状或绘制轮廓。

### 步骤 3：设置 background color java
在绘制形状之前，通常需要一个纯色背景。使用 `clear` 与 `Color` 来填充整个画布。

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
背景被设置为 **yellow**，为后续的红色和蓝色矩形提供了高对比度。

### 步骤 4：在图像上绘制矩形
使用 `drawRectangle`，配合 `Pen` 绘制轮廓和 `SolidBrush` 填充。您可以绘制多个具有不同颜色和位置的矩形。

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
这些命令在 (10, 10) 处绘制一个 **red** 矩形，在 (50, 50) 处绘制一个 **blue** 矩形，宽度均为 40 px，高度为 30 px。

### 步骤 5：导出图像为位图
最后，将修改后的图像持久化到磁盘。Aspose.PSD 会自动以您指定的格式对位图进行编码。

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
图像已保存为 BMP 文件，路径存储在 `outpath` 中。

## 常见问题及解决方案
- **空白输出文件** – 确保在绘制前调用 `graphics.clear`；否则画布可能保持透明。
- **颜色不正确** – 确认您导入的是 `com.aspose.psd.Color` 而不是 `java.awt.Color`。
- **大图像内存不足** – 使用支持流式处理的 `PsdImage` 构造函数，以避免将整个文件加载到 RAM 中。

## 常见问答

**Q: Aspose.PSD for Java 能处理除矩形之外的其他形状吗？**  
A: 是的，它支持椭圆、直线、多边形和自定义路径，提供完整的矢量绘图功能。

**Q: 如何修改矩形边框的粗细？**  
A: 在调用 `drawRectangle` 之前，设置 `Pen` 对象的 `setWidth(float)` 方法。

**Q: Aspose.PSD for Java 是否适用于高性能图像处理任务？**  
A: 绝对适用——其流式 API 能在使用不到 200 MB RAM 的情况下处理数百页的 PSD 文件。

**Q: 在哪里可以找到更多 Aspose.PSD for Java 的示例和教程？**  
A: 您可以在 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 上浏览更多示例和详细文档。

**Q: Aspose.PSD for Java 是否支持 BMP 之外的其他图像格式？**  
A: 是的，它支持 PNG、JPEG、TIFF、GIF，以及超过 30 种其他格式的导入和导出。

## 结论
您现在已经了解如何使用 Aspose.PSD for Java **how to draw rectangle** 在图像上绘制矩形，从创建位图、设置背景颜色到初始化 graphics。尝试不同的尺寸、颜色和其他形状，以掌握 **java image manipulation**。准备好后，可将此模式集成到更大的批处理管道或 UI 驱动的编辑器中。

---

**最后更新：** 2026-09-08  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose

## 相关教程

- [使用 Aspose.PSD for Java 调整图像大小 – 绘制形状与基本图像操作](/psd/java/basic-image-operations/)
- [向图像添加签名 – 使用 Aspose.PSD for Java 在画布上绘制图像](/psd/java/advanced-image-effects/add-signature-to-image/)
- [使用 Aspose.PSD for Java 通过矩形裁剪图像](/psd/java/image-editing/crop-image-by-rectangle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}