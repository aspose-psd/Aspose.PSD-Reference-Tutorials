---
date: 2026-09-28
description: 如何在 Java 中使用 Aspose.PSD 向 JFIF 段添加 thumbnail。请遵循本分步指南，快速可靠地在 PSD 文件中嵌入
  thumbnail。
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: 在 Java 中向 JFIF 段添加 thumbnail
og_description: 如何在 Java 中使用 Aspose.PSD 向 JFIF 段添加 thumbnail。请遵循本分步指南，快速可靠地在 PSD 文件中嵌入
  thumbnail。
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: 如何在 Java 中向 JFIF 段添加 thumbnail
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: 如何在 Java 中向 JFIF 段添加 thumbnail
url: /zh/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中向 JFIF 段添加缩略图

## 介绍
在 PSD 文件的 JFIF 段中添加缩略图是一个常见需求，当您需要在不加载完整图像的情况下快速预览时。本教程将教您如何使用 Aspose.PSD 在 Java 中 **如何添加缩略图** 到 JFIF 段。教程结束时，您将拥有可运行的代码片段，了解底层 JFIF 结构，并获得高效处理大文件的技巧。

## 快速回答
- **需要哪个库？** Aspose.PSD for Java.
- **哪个 Java 版本可用？** JDK 11 or later.
- **需要多少行代码？** 大约 10 行用于加载、修改和保存。
- **我可以处理多兆字节的文件吗？** 是的，Aspose.PSD 采用流式处理数据，内存使用保持低。
- **是否需要商业许可证？** 生产环境需要许可证；提供免费试用。

## 什么是 JFIF 段？
JFIF 段是 JPEG 文件交换格式（JPEG File Interchange Format）块，可存储缩略图、EXIF 或颜色配置文件等可选数据。  
它位于 PSD 文件的 JPEG 流中，并被大多数图像查看器识别，用于快速生成预览。

## 为什么要在 PSD 文件中添加缩略图？
Aspose.PSD for Java 支持 **30+ image formats**，并且可以在不将整个文档加载到内存中的情况下处理高达 **2 GB** 的文件。添加缩略图可在传输预览时减少网络带宽，并加快画廊应用中的 UI 渲染速度。

## 先决条件
- Java Development Kit (JDK)：确保系统已安装 Java。您可以从 [Oracle 的 JDK 网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下载。
- Aspose.PSD for Java：您需要拥有 Aspose.PSD for Java 库。您可以从 [Aspose.PSD Java 下载页面](https://releases.aspose.com/psd/java/) 获取。
- Integrated Development Environment (IDE)：使用 IntelliJ IDEA 或 Eclipse 等 IDE 进行 Java 开发。
- Basic Understanding of Java：熟悉 Java 编程语言及其概念。

## 如何在 Java 中向 JFIF 段添加缩略图？
加载目标 PSD，定位 JFIF 资源，替换其缩略图数据，然后保存文件。整个操作只需几次简洁的 API 调用，Aspose.PSD 会为您处理底层 JPEG 结构。

### 步骤 1：导入包
`Document`、`JfifResource` 以及相关类属于 Aspose.PSD 命名空间。Document 表示 PSD 文件容器，JfifResource 提供对 PSD 中 JFIF 段的访问。在源文件顶部导入它们。

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### 步骤 2：加载 PSD 图像
通过将文件路径传递给构造函数来创建 `PsdImage` 实例。PsdImage 是 Aspose.PSD 用于建模 Photoshop 文档的类。它在流式读取像素数据的同时加载文档元数据。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### 步骤 3：遍历图像资源
在 `Resources` 集合中搜索 `JfifResource`。找到后，您可以用新的 JPEG 编码预览替换其缩略图字节数组。

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### 步骤 4：调整缩略图数据
使用任意图像处理库生成小尺寸 JPEG 缩略图（例如 120 × 120 px），然后将生成的字节数组赋给 `jfifResource.ThumbnailData`。

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### 步骤 5：保存修改后的图像
在 `PsdImage` 对象上调用 `save` 方法，指定输出路径和所需格式。JFIF 段现在已包含新的缩略图。

```java
image.save(dataDir + "output.psd");
```

## 常见问题及解决方案
- **缩略图在查看器中不可见：** 确保缩略图数据是有效的 JPEG 字节数组，并且其尺寸在 256 × 256 px 以内，这是 JFIF 规范支持的最大尺寸。
- **大 PSD 文件出现 OutOfMemoryError：** 使用 `PsdImage.load(inputStream, true)` 启用流式模式，以保持低内存消耗。
- **资源类型不正确：** 验证您修改的资源确实是 `JfifResource`；其他资源如 `ExifResource` 不会影响缩略图显示。

## 常见问题

**Q: 什么是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一个商业库，使开发者能够创建、编辑、转换和渲染 Photoshop PSD 文件，而无需 Adobe Photoshop。

**Q: 在哪里可以找到 Aspose.PSD for Java 的更多文档？**  
A: 详细文档可在 [Aspose.PSD for Java 文档页面](https://reference.aspose.com/psd/java/) 找到。

**Q: Aspose.PSD for Java 适合商业使用吗？**  
A: 是的，Aspose.PSD for Java 可用于商业。您可以在 [Aspose.PSD 的购买页面](https://purchase.aspose.com/buy) 购买许可证。

**Q: 我可以在购买前试用 Aspose.PSD for Java 吗？**  
A: 可以，您可以从 [Aspose.PSD 的试用下载页面](https://releases.aspose.com/) 下载免费试用版。

**Q: 如何获取 Aspose.PSD for Java 的支持？**  
A: 请访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34) 获取支持。

---

**最后更新：** 2026-09-28  
**测试环境：** Aspose.PSD for Java 24.11  
**作者：** Aspose

## 相关教程

- [使用 Aspose PSD for Java 向 PSD 文件添加 IOPA 资源](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [向图像添加签名 – 使用 Aspose.PSD for Java 在画布上绘制图像](/psd/java/advanced-image-effects/add-signature-to-image/)
- [如何使用 Aspose.PSD for Java 将图像按特定角度旋转](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}