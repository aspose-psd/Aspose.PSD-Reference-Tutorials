---
date: 2026-07-08
description: Java 图像编辑库教程：学习如何使用 Aspose.PSD for Java 裁剪图像、resize、expand canvas，以及将
  PSD 转换为 JPEG。
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: 扩展和裁剪图像
og_description: Java 图像编辑库教程展示如何使用 Aspose.PSD for Java 在几分钟内裁剪、expand canvas 并将 PSD
  转换为 JPEG。
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java 图像编辑库 – 使用 Aspose.PSD 裁剪图像
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java 图像编辑库 – 使用 Aspose.PSD 裁剪图像
url: /zh/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 图像编辑库：使用 Aspose.PSD 在 Java 中裁剪图像

## 介绍

在本教程中，您将学习如何使用 **java image editing library**——具体而言是 Aspose.PSD for Java——来裁剪、扩展并将 PSD 文件转换为 JPEG。无论是为 Web 门户准备资源，还是自动生成缩略图，下面的步骤都提供了可重复、可投入生产的工作流，您可以将其集成到任何 Java 8+ 项目中。

## 快速答复
- **哪个库处理 Java 裁剪图像？** Aspose.PSD for Java。  
- **开发是否需要许可证？** 免费试用可用于测试；生产环境需要商业许可证。  
- **可以在裁剪的同时将 PSD 转换为 JPEG 吗？** 可以，使用 `JpegOptions` 并配合裁剪矩形。  
- **是否支持 Java 8？** Aspose.PSD 支持 Java 8 及更高版本。  
- **实现需要多长时间？** 基本裁剪操作通常在 10 分钟以内完成。

## 什么是 “crop image java”？

crop image java 指的是在源图片中选取一个矩形区域，并丢弃该区域之外的所有内容。使用 Aspose.PSD，您可以创建一个定义该区域的 `Rectangle`，将其应用于 `RasterImage`，然后以 JPEG 等任意受支持的格式保存结果。

## 为什么使用 Aspose.PSD 进行 Java 图像裁剪？

Aspose.PSD 提供了 **java image editing library**，能够原生处理 PSD 文件，支持 100 多个图层功能，并且可以处理高达 10 000 × 10 000 像素的图像，同时内存使用保持在 500 MB 以下。它还内置了 JPEG、PNG、BMP 等格式的转换，无需外部工具。这使得批量处理流水线既快速又可靠，易于维护。

## 前置条件

1. **Java Development Kit (JDK)** – 已安装 Java 8 或更高版本。  
2. **Aspose.PSD for Java** – 从官方站点 **[here](https://releases.aspose.com/psd/java/)** 下载库。  

> **专业提示：** 将 Aspose.PSD JAR 添加到项目的 classpath 或 Maven/Gradle 依赖中，以避免 `ClassNotFoundException`。

## 导入包

在 Java 源文件中添加所需的 import。这些类提供了图像加载、光栅操作、矩形定义以及 JPEG 导出选项的访问。

## 如何使用 Aspose.PSD 在 Java 中裁剪图像？

使用 `RasterImage` 加载源 PSD，定义描述裁剪区域的 `Rectangle`（负坐标可扩展画布），最后使用 `JpegOptions` 保存结果。此三步流程在一次传递中同时完成裁剪和格式转换，省去中间文件的需求。

## 步骤 1：设置文档目录

指定包含源 PSD 文件的文件夹。将占位符替换为您机器上的实际路径。

```
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```
```

## 步骤 2：指定源路径和目标路径

定义读取 PSD 的位置以及写入裁剪后 JPEG 的位置。

```
```java
String dataDir = "Your Document Directory";
```
```

## 步骤 3：加载并缓存图像

`RasterImage` 表示内存中的 PSD 光栅化版本。  
将 PSD 加载到 `RasterImage` 对象中。缓存可提升后续操作（如裁剪）的性能。

```
```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```
```

## 步骤 4：创建裁剪矩形

`Rectangle` 定义裁剪区域的 X、Y 坐标以及宽度/高度。  
创建一个描述您想保留区域的 `Rectangle`。坐标可以为负，以 **扩展** 画布后再裁剪，这在为原始图像添加边框时非常有用。

```
```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```
```

> **为什么使用负坐标？**  
> 负的 X/Y 值会将裁剪区域向左/上移动，实际上在最终裁剪前为原始内容周围添加空白（扩展）空间。

## 步骤 5：保存裁剪后的图像

`JpegOptions` 指定 JPEG 输出的设置，如质量和压缩。  
最后，使用 `JpegOptions` 保存生成的图像。此步骤还演示了在应用裁剪矩形的同时 **convert psd jpeg**。

```
```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```
```

> **结果：** `jpeg_out.jpg` 现在包含一个 300 × 300 像素的图像，该图像在每侧扩展了 200 像素后再裁剪到定义的矩形。

恭喜！您已成功完成 **java image cropping**，扩展了画布，并将 PSD 文件转换为 JPEG——全部只需几行简洁代码。

## 常见使用场景

- **为网页准备资源** – 在上传前裁剪并调整截图或设计稿的尺寸。  
- **生成缩略图** – 从大型 PSD 中提取特定区域用于预览。  
- **自动批处理** – 遍历文件夹中的 PSD 文件，对每个文件应用相同的裁剪矩形。

## 故障排除与技巧

| 问题 | 建议解决方案 |
|-------|----------------|
| 加载大型 PSD 时出现 `OutOfMemoryError` | 提前调用 `rasterImage.cacheData()`，并考虑增大 JVM 堆大小（`-Xmx`）。 |
| 裁剪区域偏离中心 | 检查矩形的 X/Y 偏移；记住负值会扩展画布。 |
| 输出的 JPEG 看起来模糊 | 调整 `JpegOptions` 的质量设置（例如 `new JpegOptions { Quality = 90 }`）。 |

## 常见问答

### Q1: Aspose.PSD 是否兼容不同的 Java 版本？

A1: 是的，Aspose.PSD 支持 Java 8、11、17 以及更高版本，确保在各种开发环境中的广泛兼容性。

### Q2: 我可以在商业项目中使用 Aspose.PSD 吗？

A2: 当然，Aspose.PSD 提供商业许可证，允许在个人和商业应用中使用。

### Q3: 支持的图像文件格式是否有限制？

A3: Aspose.PSD 支持 30 多种图像格式，包括 PSD、JPEG、PNG、BMP、TIFF 等。完整列表请参阅 [documentation](https://reference.aspose.com/psd/java/)。

### Q4: 如何获取 Aspose.PSD 相关的支持？

A4: 访问 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 向社区或 Aspose 支持团队寻求帮助。

### Q5: 是否提供免费试用？

A5: 是的，您可以通过免费试用探索 Aspose.PSD。下载地址在 [here](https://releases.aspose.com/)。

---

**最后更新：** 2026-07-08  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

```
```java
rasterImage.save(destName, new JpegOptions(), destRect);
```
```

## 相关教程

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [How to Rotate Image 270 Degrees with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [How to Adjust Gamma in Java Image Processing with Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}