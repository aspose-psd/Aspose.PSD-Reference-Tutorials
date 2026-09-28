---
date: 2026-09-28
description: 了解如何在 Java 中使用 Aspose.PSD 绘制椭圆，这是领先的 Java 图像处理教程，帮助您创建椭圆和其他形状。
keywords:
- how to draw ellipse
- draw shapes java
- java image processing tutorial
- create ellipse image
- draw ellipses java
lastmod: 2026-09-28
linktitle: 在 Java 中绘制椭圆
og_description: 了解如何在 Java 中使用 Aspose.PSD 绘制椭圆，这是顶级的 Java 图像处理教程，可让您高效创建椭圆、绘制形状并生成位图图像。
og_image_alt: Guide showing how to draw an ellipse in Java with Aspose.PSD
og_title: 如何在 Java 中使用 Aspose.PSD 库绘制椭圆
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to draw ellipse in Java using Aspose.PSD, the leading Java
    image processing tutorial for creating ellipses and other shapes.
  headline: How to draw ellipse in Java using Aspose.PSD library
  type: TechArticle
- questions:
  - answer: Aspose.PSD offers a fully functional trial that lets you evaluate all
      features before purchasing a license.
    question: Can I use Aspose.PSD for free?
  - answer: Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides, API references, and sample projects.
    question: Where can I find more examples and documentation?
  - answer: Temporary licenses are available through the Aspose portal at [Aspose.PSD
      Temporary License](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  - answer: It supports BMP, PNG, JPEG, TIFF, GIF, and native PSD among others.
    question: What image formats can Aspose.PSD export to?
  - answer: Yes, the library is designed for high‑throughput server environments and
      includes features such as multi‑threaded processing and memory‑efficient streaming.
    question: Is Aspose.PSD suitable for enterprise‑level workloads?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw ellipse
- Aspose.PSD
- Java graphics
- image processing
title: 如何在 Java 中使用 Aspose.PSD 库绘制椭圆
url: /zh/java/java-graphics-drawing/drawing-ellipses/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.PSD 库绘制椭圆

## 介绍
在本教程中，您将学习 **如何绘制椭圆**，使用 Aspose.PSD 库在 Java 中。Aspose.PSD for Java 是一个强大的 API，允许您创建、编辑和导出 PSD 文件，而无需 Adobe Photoshop。绘制诸如椭圆之类的形状是任何 Java 图像处理项目的核心技能，本指南将带您逐步完成所有步骤——从项目设置到保存最终位图。

## 快速答案
- **哪个库最适合在 Java 中绘制椭圆？** Aspose.PSD for Java.
- **需要多少行代码？** 大约十行，加上一些设置语句。
- **开发是否需要许可证？** 免费试用可用于测试；生产环境需要商业许可证。
- **我可以输出为 BMP、PNG 或 JPEG 吗？** 是的，Aspose.PSD 支持 BMP、PNG、JPEG 和 PSD。
- **API 是否兼容 Java 8 及更高版本？** 完全支持 Java 8‑21。

## Aspose.PSD for Java 是什么？
Aspose.PSD for Java 是一个纯 Java 库，能够以编程方式创建、操作和转换 Photoshop PSD 文件。它支持超过 100 种图像格式，并且可以处理高达 2 GB 的文件，而无需将整个文档加载到内存中。

## 为什么在绘制椭圆时使用 Aspose.PSD？
Aspose.PSD 提供高性能，能够在几秒钟内处理多页文档，同时支持超过 100 种输入和输出格式，如 BMP、PNG、JPEG 和 PSD。它完全在 Java 中运行，消除了对本地 Photoshop 的需求，使其非常适合 CI/CD 流水线和基于云的服务。

## 先决条件
- 基本的 Java 编程知识。
- 已安装 JDK 8 或更高版本。
- 如 IntelliJ IDEA 或 Eclipse 的 IDE。
- Aspose.PSD for Java 库。您可以从 [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) 下载。

## 导入包
首先，从 Aspose.PSD 命名空间导入所需的类。

## 如何在 Java 中绘制椭圆？
加载 Aspose.PSD 库，创建一个空白的 PsdImage 画布，获取 Graphics 对象，可选地清除背景，然后使用带有所需颜色和样式的 Pen 对象在 Rectangle 边界内绘制椭圆。最后，以 BMP、PNG 或 JPEG 格式保存图像。此过程通常需要少于 15 行代码。

## 步骤 1：设置 Java 项目
在开始编码之前，请确保您的项目将 Aspose.PSD JAR 作为 Maven/Gradle 依赖项或将 JAR 添加到类路径中。

## 步骤 2：创建 PsdImage 实例
PsdImage 表示一个内存中的 Photoshop 文档，并提供用于绘图的画布。

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

## 步骤 3：初始化 graphics 对象
Graphics 提供绘图方法，将形状渲染到图像表面上。

```java
Image image = new PsdImage(100, 100);
```

## 步骤 4：清除 graphics 表面
可选地使用背景颜色清除画布，以确保绘图区域干净。

```java
Graphics graphics = new Graphics(image);
```

## 步骤 5：绘制点状椭圆
Pen 定义绘制形状时使用的轮廓颜色和样式。

```java
graphics.clear(Color.getYellow());
```

## 步骤 6：绘制连续椭圆
使用实心蓝色笔刷的 Pen 为第二个椭圆创建连续的轮廓。

```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```

## 步骤 7：保存图像
BmpOptions 指定用于保存图像的 BMP 格式设置。

```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```

```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## 常见问题及解决方案
- **图像为空白：** 确保在绘制之前调用了带可见颜色的 `graphics.clear()`。
- **椭圆形状失真：** 验证 `Rectangle` 的尺寸与图像的宽高比匹配。
- **大文件出现内存不足错误：** 使用 `PsdImage` 的流式 API 处理文件的部分，而不是加载整个文档。

## 常见问题
**Q: 我可以免费使用 Aspose.PSD 吗？**  
A: Aspose.PSD 提供功能完整的试用版，让您在购买许可证前评估所有功能。

**Q: 我在哪里可以找到更多示例和文档？**  
A: 请访问 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) 获取全面的指南、API 参考和示例项目。

**Q: 我如何获取用于测试的临时许可证？**  
A: 可通过 Aspose 门户在 [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

**Q: Aspose.PSD 可以导出哪些图像格式？**  
A: 它支持 BMP、PNG、JPEG、TIFF、GIF 以及原生 PSD 等格式。

**Q: Aspose.PSD 适合企业级工作负载吗？**  
A: 是的，该库专为高吞吐量服务器环境设计，包含多线程处理和内存高效流式等特性。

## 结论
现在，您已经拥有一个完整的、端到端的示例，展示如何在 Java 中使用 Aspose.PSD **绘制椭圆**。通过设置 `PsdImage`、使用 `Graphics` API 并配置 `Pen` 对象，您可以渲染点状和实线椭圆，并将结果保存为任何受支持的位图格式。将这些步骤集成到您自己的应用程序中，以生成动态图形、缩略图或自定义 UI 元素，而无需依赖外部图形编辑器。

---

**最后更新：** 2026-09-28  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose

## 相关教程
- [在 PSD 中使用 Aspose.PSD for Java 绘制并保存矩形](/psd/java/basic-image-operations/simple-drawing/)
- [使用 Aspose.PSD for Java 调整图像大小 – 绘制形状与基本图像操作](/psd/java/basic-image-operations/)
- [向图像添加签名 – 在画布上使用 Aspose.PSD for Java 绘制图像](/psd/java/advanced-image-effects/add-signature-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}