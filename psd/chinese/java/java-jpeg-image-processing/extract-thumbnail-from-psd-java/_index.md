---
date: 2026-10-03
description: 了解如何使用 Aspose.PSD 在 Java 中提取 PSD 的缩略图。本分步指南涵盖环境设置、代码示例以及将缩略图保存为 JPEG
  图像。
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: 在 Java 中从 PSD 提取缩略图
og_description: 了解如何使用 Aspose.PSD 在 Java 中提取 PSD 缩略图。本指南将带您完成环境设置、加载文件、提取缩略图以及将其保存为
  JPEG 图像的全过程。
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: 使用 Aspose.PSD 在 Java 中提取 PSD 缩略图
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: 在 Java 中从 PSD 提取缩略图
url: /zh/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中提取 PSD 缩略图

## 介绍
从 PSD 文件中提取缩略图让您无需加载完整分辨率图像即可生成快速预览。在 Java 中，Aspose.PSD 使此过程简洁且高效。在本教程中，您将学习如何设置库、定位缩略图资源，并将其保存为 JPEG 文件——只需几行代码。

## 快速答案
- **哪个库处理 PSD 缩略图？** Aspose.PSD for Java.
- **需要多少行代码？** 大约五行即可加载、提取并保存。
- **我可以从大型 PSD 文件中提取缩略图吗？** 是的，Aspose.PSD 可处理高达 500 MB 的文件而无需完整内存加载。
- **开发时需要许可证吗？** 免费试用可用于评估；生产环境需要许可证。
- **支持哪些输出格式？** 提取的缩略图可保存为 JPEG、PNG 或 BMP。

## 什么是从 PSD 提取缩略图？
从 PSD 提取缩略图是读取嵌入在 Photoshop（PSD）文档中的小预览图像的过程。该预览作为资源存储，可独立保存用于目录或显示目的。缩略图通常是低分辨率的表示，供应用程序在不加载完整图像的情况下快速显示视觉摘要。

## 为什么在此任务中使用 Aspose.PSD？
Aspose.PSD 支持 **30+ 图像格式**，并且能够处理高达 **500 MB** 的 PSD 文件，同时保持低内存使用，因为它按需读取资源。该 API 还提供强大的错误处理，使您即使在文件损坏的情况下也能可靠地提取缩略图。

## 先决条件
- 已安装 Java Development Kit (JDK)。
- 从 [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/) 下载 Aspose.PSD for Java 库。
- 熟悉 Java 语法和项目设置的基础知识。

## 如何在 Java 中从 PSD 文件提取缩略图？
使用 `PsdImage` 加载 PSD 文件，定位 `ThumbnailResource`，并将其图像数据保存为 JPEG。Aspose.PSD 抽象了底层解析，您只需调用 `getResources()`，然后对提取的图像调用 `save()`。此方法适用于任何包含缩略图的 PSD，无论文件大小如何。

## 导入包
`Image` 是用于加载图像的基类。`PsdImage` 表示 PSD 文档。`ThumbnailResource` 和 `Thumbnail4Resource` 表示缩略图资源。`JpegOptions` 指定 JPEG 保存选项。

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## 步骤 1：加载 PSD 文件
首先，创建指向 PSD 文件的 `PsdImage` 实例。构造函数仅读取标题和必需的资源，从而将内存使用保持在最低水平。

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

将 `"Your_Document_Directory/"` 替换为 PSD 文件所在的目录路径，将 `"your_file.psd"` 替换为 PSD 文件的名称。

## 步骤 2：遍历图像资源
Aspose.PSD 将缩略图存储为图像资源集合中的 `ThumbnailResource` 对象。遍历该集合，检查资源类型，并捕获遇到的第一个缩略图。

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## 步骤 3：保存提取的缩略图
获取缩略图后，调用其 `save` 方法将其写入磁盘。您可以选择 JPEG、PNG 或 BMP；JPEG 是网页预览中最常用的格式。

## 步骤 4：处理不同的缩略图类型
如果 PSD 包含多个缩略图变体，例如 `Thumbnail4Resource`，请扩展遍历逻辑以检查每种类型。API 为每种资源提供单独的类，允许您选择所需的分辨率。

## 常见问题及解决方案
- **未找到缩略图：** 并非所有 PSD 文件都嵌入预览。请在 Photoshop 的 “File → File Info” 面板中验证源文件。
- **不支持的格式错误：** 确保使用最新的 Aspose.PSD 版本；旧版本可能缺少新型缩略图资源类型。
- **大型文件内存不足：** 使用 `PsdImage.load(..., LoadOptions)` 并调用 `LoadOptions.setLoadResourcesOnly(true)`，在仅需缩略图时避免加载完整图像数据。

## 常见问题

**Q: 什么是 Aspose.PSD？**  
A: Aspose.PSD 是一个 Java 库，能够在不需要 Adobe Photoshop 的情况下，以编程方式创建、操作和转换 PSD 以及其他光栅图像格式。

**Q: 在哪里可以找到 Aspose.PSD for Java 的更多文档？**  
A: 您可以参考 [documentation](https://reference.aspose.com/psd/java/) 获取详细的 API 参考和示例。

**Q: 我可以在购买前免费试用 Aspose.PSD 吗？**  
A: 是的，您可以下载 [free trial](https://releases.aspose.com/) 来评估该库的功能。

**Q: 如何获取 Aspose.PSD 的临时许可证？**  
A: 临时许可证可在 [temporary license](https://purchase.aspose.com/temporary-license/) 页面获取。

**Q: Aspose.PSD 适用于商业使用吗？**  
A: 是的，Aspose.PSD 可根据其许可条款用于个人和商业项目。

---

**最后更新：** 2026-10-03  
**已测试版本：** Aspose.PSD for Java 24.12  
**作者：** Aspose

## 相关教程

- [如何使用 Aspose.PSD for Java 将 PSD 转换为光栅图像格式](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [使用 Aspose.PSD Java 将 PSD 保存为 JPEG 并支持 RGB 颜色](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [使用 Aspose.PSD for Java 调整图像大小 – 绘制形状与基本图像操作](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}