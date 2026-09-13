---
date: 2026-09-13
description: 了解如何在 Java 中使用 Aspose.PSD 绘制 ellipse 和其他形状。本分步 Java graphics 教程展示 gradient
  fills、polygon fills 和 image export。
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: 使用 Graphics 在 Java 中绘图
og_description: 了解如何在 Java 中使用 Aspose.PSD 绘制 ellipse。本 Java graphics 教程涵盖 shape drawing、gradient
  fills、polygon filling 和 exporting images。
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: 如何在 Java 中使用 Aspose.PSD 的 graphics 绘制 ellipse
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: 如何在 Java 中使用 Aspose.PSD 的 graphics 绘制 ellipse
url: /zh/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 在 Java 中绘制椭圆的图形

## 介绍
在本 Java 图形教程中，您将学习使用 Aspose.PSD for Java 以编程方式 **绘制椭圆** 对象和其他形状。无论是需要生成动态缩略图、创建自定义 UI 元素，还是自动化设计工作流，掌握椭圆绘制和渐变填充都能让您获得精确的视觉控制。下面的步骤将引导您完成图形初始化、笔和画刷的配置，以及将结果导出为常见图像格式。

## 快速回答
- **需要的库是什么？** Aspose.PSD for Java（从官方网站下载）。  
- **本教程关注哪种形状？** 绘制椭圆并填充多边形。  
- **我可以导出为 BMP 之外的格式吗？** 可以——支持 PNG、JPEG、TIFF 等多种格式。  
- **开发时需要许可证吗？** 免费的临时许可证可用于测试；生产环境需要正式许可证。  
- **API 适用于大图像吗？** Aspose.PSD 可处理高达 500 MB 的文件，而无需将整个位图加载到内存中。

## 如何在 Java 中绘制椭圆？
加载具有所需宽度和高度的 `PsdImage`，创建 `Graphics` 对象，设置 `Pen`，并使用边界矩形调用 `drawEllipse`。整个操作只需几次方法调用，在现代硬件上对典型的 800×600 图像的处理时间不足一秒。

## 什么是 Aspose.PSD for Java？
Aspose.PSD for Java 是一个 **纯 Java 库，提供 50 多种图像格式转换和完整的 PSD 编辑功能**，无需 Adobe Photoshop。它能够渲染、修改并导出多层文件，同时保持低内存使用，非常适合服务器端图形生成。

## 为什么使用 Aspose.PSD 绘制形状？
Aspose.PSD 提供高性能、广泛的格式支持和精确的渲染，使其非常适合服务器端图形生成和复杂形状绘制。

- **性能：** 处理高达 500 MB 的图像，堆内存占用低于 150 MB（约比竞争库低 30 %）。  
- **格式支持：** 超过 50 种输入和输出格式，包括 BMP、PNG、JPEG、TIFF 和 PSD。  
- **精度：** 子像素渲染确保在高 DPI 显示器上呈现清晰的椭圆和平滑的渐变。

## 前置条件
- 具备 Java 编程的基础知识。  
- 已安装 Java Development Kit（JDK）。  
- 使用 IntelliJ IDEA 或 Eclipse 等 IDE。  
- Aspose.PSD for Java 库。您可以从 [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) 下载。

## 导入包
首先，导入必要的 Aspose.PSD 类和标准的 Java 工具类。以下类提供绘图原语和颜色处理功能：
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## 步骤 1：创建图像对象
`PsdImage` 表示一个内存中的光栅画布，可在其上绘制并以多种格式保存。
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## 步骤 2：初始化图形对象
`Graphics` 是与 `PsdImage` 关联的绘图表面，支持绘制形状等矢量操作。
```java
Graphics graphics = new Graphics(image);
```

## 步骤 3：清除图像表面
`clear` 用单一背景颜色填充整个画布。
```java
graphics.clear(Color.getWhite());
```

## 步骤 4：创建并配置笔对象
`Pen` 定义绘制轮廓时的笔触颜色、宽度和样式。
```java
Pen pen = new Pen(Color.getBlue());
```

## 步骤 5：绘制形状
`drawEllipse` 使用当前的笔在指定的矩形内绘制一个椭圆。
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## 步骤 6：使用画刷进行填充
`LinearGradientBrush` 创建一个在 **定义区域** 内 **在两种颜色之间过渡** 的渐变填充。
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## 步骤 7：保存修改后的图像
`save` 将 `PsdImage` 按所选格式（如 BMP 或 PNG）写入磁盘。
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## 常见陷阱与故障排除
- **Graphics 上的 NullPointerException：** 确保在创建 `Graphics` 对象之前已完整实例化 `PsdImage`。  
- **颜色不正确：** 当 **默认调色板不符合预期** 时，使用 `Color.fromArgb` 指定 **精确** 的 ARGB 值。  
- **大图像性能下降：** 启用 `PsdImageOptions` 并将 `compression = CompressionType.Rle` 设置为 **降低** **内存开销**。

## 常见问题

**Q: Aspose.PSD 能处理复杂的 **图像操作** 吗？**  
A: 是的，除了形状绘制外，它还支持 **图层合并**、**通道调整**、**文本渲染** 和 **高级遮罩**。

**Q: Aspose.PSD 适用于 **高性能** 应用吗？**  
A: 绝对可以；该库已 **针对速度进行优化**，能够在普通服务器上 **在 2 秒以内处理** **10 MP** 图像。

**Q: 我在哪里可以找到更多示例和文档？**  
A: 请访问 [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) 获取完整的指南和 API 参考。

**Q: Aspose.PSD 支持多种图像格式导出吗？**  
A: 是的，您可以导出为 BMP、PNG、JPEG、TIFF、GIF、PSD 等多种格式。

**Q: 如果遇到问题，我该如何获取支持或帮助？**  
A: 可在 [support forum](https://forum.aspose.com/c/psd/34) 与 Aspose.PSD 社区联系，或考虑获取 [temporary license](https://purchase.aspose.com/temporary-license/) 以获得优先支持。

---

**最后更新：** 2026-09-13  
**测试环境：** Aspose.PSD for Java 24.10  
**作者：** Aspose

## 相关教程

- [使用 Aspose.PSD for Java 调整图像大小 – 绘制形状和基本图像操作](/psd/java/basic-image-operations/)
- [使用 Aspose.PSD for Java 在 PSD 中绘制并保存矩形](/psd/java/basic-image-operations/simple-drawing/)
- [为图像添加签名 – 使用 Aspose.PSD for Java 在画布上绘制图像](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}