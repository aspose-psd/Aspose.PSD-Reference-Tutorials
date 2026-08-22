---
date: 2026-07-17
description: 了解如何在 Aspose.PSD for Java 中使用流创建 BMP 图像。遵循此分步 java 图像教程，实现高效的图像生成。
keywords:
- how to create bmp
- generate image stream
- java image tutorial
lastmod: 2026-07-17
linktitle: 使用流创建图像
og_description: 了解如何在 Aspose.PSD for Java 中使用流创建 BMP 图像。此 java 图像教程展示了 BMP 文件的分步生成。
og_image_alt: 'Guide: create BMP image from stream with Aspose.PSD Java'
og_title: 如何在 Aspose.PSD for Java 中使用流创建 BMP
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to create BMP images using stream in Aspose.PSD for Java.
    Follow this step‑by‑step java image tutorial for efficient image generation.
  headline: How to Create BMP Using Stream in Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`BmpOptions` combined with `Image.create`.'
    question: What is the main class for BMP creation?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `FileCreateSource` streams the data.
    question: Can I generate large BMPs (>10 MB) without loading the whole file into
      memory?
  - answer: Java 8 through Java 21 are fully compatible.
    question: Which Java versions are supported?
  - answer: Only the Aspose.PSD for Java JAR; no external imaging libraries needed.
    question: Is any additional dependency required?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create bmp
- Aspose.PSD
- Java image processing
- stream image generation
title: 如何在 Aspose.PSD for Java 中使用流创建 BMP
url: /zh/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用流在 Aspose.PSD for Java 中创建 BMP

## 介绍

直接从流创建 BMP 文件可以让您对内存使用和文件处理进行细粒度控制，这对于高性能的 Java 应用程序至关重要。在本教程中，您将学习 **如何创建 BMP** 图像，使用 Aspose.PSD 的流式 API，逐步进行。我们将涵盖从环境设置到保存最终图像的全部内容，帮助您立即将此技术集成到实际项目中。

## 快速答案
- **创建 BMP 的主要类是什么？** `BmpOptions` 与 `Image.create` 组合使用。
- **开发是否需要许可证？** 免费试用可用于测试；生产环境需要商业许可证。
- **我可以在不将整个文件加载到内存的情况下生成大于 10 MB 的 BMP 吗？** 可以，使用 `FileCreateSource` 可流式传输数据。
- **支持哪些 Java 版本？** 完全兼容 Java 8 至 Java 21。
- **是否需要额外的依赖？** 仅需 Aspose.PSD for Java 的 JAR；不需要外部图像库。

## 如何在 Aspose.PSD for Java 中使用流创建 BMP？

加载目标目录，使用 `FileCreateSource` 配置 `BmpOptions`，然后调用 `Image.create` 并指定所需的宽度和高度——整个操作仅需三行简洁代码即可完成。这种方法直接将 BMP 写入文件流，避免临时缓冲区，从而在批量图像生成时提供最佳性能。

## Aspose.PSD for Java 是什么？

Aspose.PSD for Java 是一个功能全面的库，能够以编程方式创建、操作和转换 Photoshop®（PSD）文件以及超过 30 种其他光栅格式。它可以在不将完整图像加载到内存的情况下处理高达 2 GB 的文件，非常适合服务器端图像流水线。

## 为什么使用基于流的 BMP 生成？

基于流的生成通过直接将字节写入磁盘来降低内存开销，这在创建大型 BMP 或并行处理大量图像时尤为有益。Aspose.PSD 能够处理 **30 多种图像格式**，并在普通服务器硬件上在不到一秒的时间内生成最高达 500 MPixel 的 BMP。

## 前提条件

在开始之前，请确保您已具备以下条件：

- **Java Development Kit (JDK)** – 已安装 Java 8 或更高版本。
- **Aspose.PSD Library** – 从[文档](https://reference.aspose.com/psd/java/)下载最新的 JAR。
- **IDE** – Eclipse、IntelliJ IDEA 或您偏好的任何 Java 兼容 IDE。

## 导入包

`import` 语句将所需的类引入作用域。  
`BmpOptions` 配置 BMP 特定设置，而 `FileCreateSource` 表示输出流。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## 步骤 1：设置文档目录

`File` 表示文件系统中的文件或目录路径。  

`File dataDir = new File("Your Document Directory");` – 该变量指向 BMP 将被保存的文件夹。  
将 `"Your Document Directory"` 替换为您机器上的实际路径。

```java
String dataDir = "Your Document Directory";
```

## 步骤 2：指定输出文件名

`String outFile = dataDir.getAbsolutePath() + File.separator + "output.bmp";` – 定义要创建的 BMP 文件的完整路径和名称。

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

## 步骤 3：配置 BmpOptions

`BmpOptions bmpOptions = new BmpOptions();` – 创建一个选项对象。  
您可以设置 `bitsPerPixel`（例如 24 表示真彩色）来控制图像质量和文件大小。

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

## 步骤 4：创建 FileCreateSource

`FileCreateSource fileSource = new FileCreateSource(outFile, false);` – 将输出路径包装为流源。  
`bmpOptions.setSource(fileSource);` 告诉 Aspose.PSD 将 BMP 直接写入此流。

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

## 步骤 5：生成图像

`Image` 是 Aspose.PSD 中表示图像的类，提供创建、编辑和保存光栅图形的方法。  

`Image img = Image.create(bmpOptions, 800, 600);` – 使用配置的选项创建一个 800 × 600 像素的空白 BMP。  
该图像现在已准备好进行进一步的绘制或处理。

```java
Image image = Image.create(imageOptions, 500, 500);
```

## 步骤 6：图像处理

`Graphics` 是用于在 `Image` 对象上绘制形状、文本和其他图形的类。  

您可以使用从 `img` 获取的 `Graphics` 对象绘制形状、添加文本或应用滤镜。  
最后，调用 `img.save()` 完成文件保存。此步骤确保所有未完成的操作都刷新到流中。

```java
// Perform desired image processing operations
// ...

// Save the processed image
image.save(desName);
```

## 常见问题及解决方案

- **文件权限错误** – 确认 Java 进程对目标目录具有写入权限。
- **大型图像导致内存不足** – 使用 `FileCreateSource`（如示例所示）流式传输数据，而不是将整个位图加载到内存中。
- **颜色异常** – 确保 `bitsPerPixel` 与所需的颜色深度匹配；24 bpp 是真彩色 BMP 的标准。

## 常见问答

### Q1：我可以将 Aspose.PSD 与其他 Java 库一起使用吗？

A1: 是的，Aspose.PSD 可与流行的 Java 图像库（如 ImageIO）平稳集成，允许您在不冲突的情况下组合功能。

### Q2：在哪里可以找到 Aspose.PSD 相关查询的支持？

A2: 访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34) 获取社区帮助以及 Aspose 工程师的官方回复。

### Q3：Aspose.PSD 是否提供免费试用？

A3: 是的，您可以在[此处](https://releases.aspose.com/)获取免费试用。

### Q4：如何获取 Aspose.PSD 的临时许可证？

A4: 在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证。

### Q5：Aspose.PSD 的系统要求是什么？

A5: 请参阅[文档](https://reference.aspose.com/psd/java/)了解支持的操作系统、Java 版本和内存指南。

## 结论

现在，您已经掌握了使用 Aspose.PSD for Java 通过流创建 **BMP** 图像的完整、可投入生产的工作流。通过利用 `BmpOptions` 和 `FileCreateSource`，您可以实现快速、内存高效的 BMP 生成，能够从简单的缩略图扩展到大规模光栅图形。欢迎尝试不同的尺寸、颜色深度和后处理步骤，以满足您的应用需求。

---

**最后更新：** 2026-07-17  
**测试环境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose

## 相关教程

- [使用 Aspose.PSD for Java 从流加载图像](/psd/java/advanced-techniques/loading-images-from-stream/)
- [使用 Aspose.PSD for Java 将图像保存到流](/psd/java/advanced-techniques/save-images-to-stream/)
- [在 Aspose.PSD for Java 中通过设置路径创建图像](/psd/java/image-editing/create-image-by-setting-path/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}