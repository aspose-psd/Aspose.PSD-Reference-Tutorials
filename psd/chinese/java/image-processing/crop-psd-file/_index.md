---
date: 2026-08-17
description: 了解如何使用 Aspose.PSD for Java 在 Java 中裁剪 PSD 文件——一种快速、精确的方式，在您的 Java 应用程序中裁剪
  Photoshop 文档。
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: 裁剪 PSD 文件
og_description: 使用 Aspose.PSD for Java 在 Java 中裁剪 PSD 文件。本指南逐步演示如何高效裁剪 Photoshop 文件，提供无代码解释和最佳实践技巧。
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: 使用 Aspose.PSD 在 Java 中裁剪 PSD 文件——快速图像裁剪
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: 使用 Aspose.PSD 在 Java 中裁剪 PSD 文件
url: /zh/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 裁剪 PSD 文件

## 介绍

如果您需要以编程方式裁剪 Photoshop 文档，**crop psd file java** 是从事图形流水线、资产流水线或自动化设计工作流的 Java 开发人员的常见任务。Aspose.PSD for Java 提供了专用的 API，允许您定义一个矩形并仅用几行代码提取所需区域。在本教程中，您将了解该库为何为高性能裁剪而构建、如何设置环境以及生成 PSD 和 PNG 结果的具体步骤。

## 快速答案
- **什么库处理 Java 中的 PSD 裁剪？** Aspose.PSD for Java.
- **进行基本裁剪需要多少行代码？** 加载图像后调用两次 API。
- **我可以将裁剪区域导出为 PNG 吗？** 是的，使用内置的 PNG 保存选项。
- **生产使用是否需要许可证？** 超过试用期后需要商业许可证。
- **支持哪些 Java 版本？** Java 8 及更高版本，包括 Java 11、17 和 21。

## 什么是 crop psd file java？

Crop psd file java 指的是使用 Java 代码以编程方式从 Photoshop 文档（.psd）中裁剪出矩形区域的过程。借助 Aspose.PSD，您可以在不启动 Photoshop 的情况下完成此操作，非常适合服务器端图像流水线。

## 为什么使用 Aspose.PSD for Java？

Aspose.PSD 支持 **30+ input and output formats**，并且能够在不将整个文档加载到内存中的情况下处理高达 **500 MB** 的 PSD 文件，这归功于其流式架构。该库保留图层、蒙版和颜色配置文件，提供的裁剪结果与 Photoshop 的原生输出相匹配。这种可量化的性能让您能够在普通硬件上以可预测的内存使用量处理批量作业。

## 先决条件

- **Java 开发环境** – 已安装并配置 JDK 8 或更高版本。
- **Aspose.PSD for Java** – 下载最新的 JAR 和文档 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)。
- **示例 PSD 文件** – 将 .psd 文件放置在项目目录中，以便代码能够找到它。

## 如何在 Java 中裁剪 PSD 文件？

加载源文件，定义要保留的矩形区域，执行裁剪，最后以所需格式保存结果。整个工作流仅需五个简明步骤，每个步骤都配有占位符，您可以在其中插入自己的代码。

### 步骤 1：设置文档目录

将 “Your Document Directory” 替换为包含要处理的 PSD 的绝对或相对路径。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### 步骤 2：加载 PSD 文件

`RasterImage` 类是 Aspose.PSD 用于对 PSD 文件进行栅格操作的入口。加载文件会创建一个可供操作的内存表示。

```java
String dataDir = "Your Document Directory";
```

### 步骤 3：定义裁剪区域

`Rectangle` 定义了要保留区域的 X、Y 坐标以及宽度和高度。该类是标准 Java AWT 包的一部分，Aspose.PSD 使用它来指定裁剪边界。

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### 步骤 4：保存裁剪后的 PSD

应用裁剪后，您可以将结果持久化回 PSD 格式。库仅写入裁剪后的像素，保留原始的颜色模式和位深度。

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### 步骤 5：将裁剪后的图像保存为 PNG

如果需要 Web 友好的版本，可将裁剪后的栅格导出为 PNG。Aspose.PSD 提供 PNG 保存选项，允许您控制压缩级别和交错方式。

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## 常见问题及解决方案

- **矩形坐标不正确** – 确保 X/Y 值从左上角的 0 开始；负值会抛出 `ArgumentException`。
- **大文件内存激增** – 当不需要隐藏图层时，使用 `loadOptions.setLoadOnlyVisibleLayers(true)` 选项以降低内存占用。
- **颜色配置文件丢失** – 在裁剪前调用 `image.getColorProfile()` 保存原始 ICC 配置文件，并在操作后重新分配它。

## 常见问题

### Q1：我可以使用 Aspose.PSD for Java 裁剪其他格式的图像吗？

A1: Aspose.PSD 主要面向 PSD 文件，但它也支持 BMP、GIF、JPEG、PNG、TIFF 以及其他多种栅格格式的输入和输出。

### Q2：Aspose.PSD for Java 适合大规模图像处理吗？

A2: 是的。该库的流式架构能够以低于 100 MB 的内存占用处理多百页的 PSD 文件，非常适合批量作业。

### Q3：使用 Aspose.PSD for Java 有哪些许可考虑？

A3: 生产部署需要商业许可证。详细信息请参阅 [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy)。

### Q4：如何获取 Aspose.PSD for Java 相关问题的支持？

A4: 访问 [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) 提问、分享代码片段，并获得社区和产品工程师的帮助。

### Q5：我可以在购买前试用 Aspose.PSD for Java 吗？

A5: 可以，您可以下载功能完整的免费试用版 [Aspose.PSD free trial download](https://releases.aspose.com/)。

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## 相关教程

- [在 Aspose.PSD for Java 中按矩形裁剪图像](/psd/java/image-editing/crop-image-by-rectangle/)
- [在 Aspose.PSD for Java 中按位移裁剪图像](/psd/java/image-editing/crop-image-by-shifts/)
- [如何使用 Aspose.PSD 在 Java 中旋转图像](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}