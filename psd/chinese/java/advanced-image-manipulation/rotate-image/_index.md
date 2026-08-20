---
date: 2026-05-19
description: 了解如何使用 Aspose.PSD for Java 将 PSD 转换为 JPEG 并将图像旋转 270 度。本指南展示了如何旋转 PSD
  文件、翻转图像以及将 PSD 转换为 JPEG。
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: 旋转图像 270 度
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 将 PSD 转换为 JPEG 并旋转 270°
url: /zh/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 PSD 转换为 JPEG 并将图像旋转 270 度，使用 Aspose.PSD for Java

## 介绍

在本 **Java 图像处理教程** 中，您将学习如何 **将 PSD 转换为 JPEG** 并使用 Aspose.PSD for Java 将图像旋转 270 度。无论您是在构建批处理管道、基于 Web 的编辑器，还是桌面实用程序，该库都允许您在无需 Photoshop 的情况下操作 PSD 图层。我们还将介绍可选的翻转，并展示从加载 PSD 文件到保存 JPEG 的完整端到端流程。

## 快速答案
- **哪个库负责旋转？** Aspose.PSD for Java  
- **示例使用的旋转角度是多少？** 270 度  
- **我还能翻转图像吗？** 是的 – 使用 `RotateFlipType` 选项，如 `Rotate90FlipX`  
- **如何保存结果？** 示例中我们使用 `JpegOptions` 将其保存为 JPEG  
- **生产环境需要许可证吗？** 商业使用需要有效的 Aspose.PSD 许可证  

## 什么是“将图像旋转 270 度”？

将图像旋转 270 度意味着顺时针旋转整圆的四分之三（或逆时针旋转 90 度）。这种方向通常在先前的变换后恢复原始的纵向布局，并且在图像最初以横向模式拍摄但需要以纵向显示时常被使用。结果是一个方向正确且不失真的视觉图像。

## 为什么在此任务中使用 Aspose.PSD？

Aspose.PSD 支持 **50+ 输入和输出格式**——包括 PSD、JPEG、PNG、BMP、GIF 和 TIFF，并且能够在不将整个文档加载到内存的情况下处理高达 **2 GB** 的文件。该 API 可在任何 Java 运行时（JDK 8+）上运行，无需本地 Photoshop 安装，并提供一次性调用 `rotateFlip`，即可在一步完成旋转和翻转。

## 前提条件

在开始之前，请确保您已具备：

- 已安装 **Aspose.PSD for Java** 库。您可以在[此处](https://reference.aspose.com/psd/java/)下载并查看完整的 API 参考。  
- Java 开发环境（JDK 8 或更高）。  
- 您想要旋转的示例 PSD 文件。请在代码中将 `sourceFile` 变量更新为指向您文件的正确路径。

## 导入包

`Image`、`RotateFlipType` 和 `JpegOptions` 类是加载、转换和保存文件所必需的。  
`Image` 是表示内存中 PSD 文档的核心类。  
`RotateFlipType` 枚举了支持的旋转和翻转操作。  
`JpegOptions` 配置 JPEG 输出设置，例如质量。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 如何在旋转后将 PSD 转换为 JPEG？

加载源 PSD，应用 270 度旋转，然后立即将其保存为 JPEG。对于典型的 10 MP 图像，此三步流程在现代 CPU 上可在不到一秒的时间内完成，非常适合高吞吐量的批处理作业。仅处理必要的图像数据可保持低内存消耗，且生成的 JPEG 在降低文件大小的同时保持视觉保真度。

### 步骤 1：加载 PSD 文件

`Image` 是 Aspose.PSD 的核心类，表示内存中的单个 PSD 文档。实例化它时仅读取头部信息，从而保持低内存使用。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### 步骤 2：将图像旋转 270 度

`rotateFlip` 对图像执行指定的旋转和可选的翻转。`RotateFlipType.Rotate270FlipNone` 将画布顺时针旋转 270 度，同时保持图像方向不变。

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **专业提示：** 如果您还需要水平或垂直翻转图像，请选择其他 `RotateFlipType`，例如 `Rotate90FlipX` 或 `Rotate180FlipY`。

### 步骤 3：将 PSD 转换为 JPEG 并保存

`JpegOptions` 定义 JPEG 特定的参数，如压缩质量。`save` 方法将转换后的图像以所需格式写入磁盘。

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

文件 `RotatedImage_out.jpg` 现在包含已旋转 270 度并保存为 JPEG 的原始 PSD 内容。

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **图像显示颠倒** | 确认您使用了 `Rotate270FlipNone`。若需顺时针旋转 90 度，请使用 `Rotate90FlipNone`。 |
| **输出文件损坏** | 确保目标文件夹存在且您拥有写入权限。 |
| **许可证异常** | 在生产环境加载图像前，安装临时或永久的 Aspose.PSD 许可证。 |

## 常见问答

**Q: Aspose.PSD 是否兼容不同的图像格式？**  
A: 是的，Aspose.PSD 支持 PSD、JPEG、PNG、BMP、GIF、TIFF 以及许多其他光栅格式。

**Q: 我可以应用自定义旋转，而不仅仅是预定义的翻转吗？**  
A: 当然可以！虽然 `RotateFlipType` 提供常用角度，您仍可以链式调用或使用变换矩阵实现任意角度的旋转。

**Q: 如何将旋转后的 PSD 转换为其他格式，例如 PNG？**  
A: 在 `save` 方法中将 `JpegOptions` 替换为 `PngOptions`（或相应的选项类）。

**Q: 在哪里可以找到更多支持或帮助？**  
A: 社区帮助请访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)。

**Q: 是否提供免费试用？**  
A: 是的，您可以通过 [免费试用](https://releases.aspose.com/) 体验 Aspose.PSD。

**Q: 如何获取临时许可证？**  
A: 如果您需要临时许可证，可在[此处](https://purchase.aspose.com/temporary-license/)获取。

---

**最后更新：** 2026-05-19  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [使用 Aspose.PSD for Java 将 PSD 转换为光栅图像格式](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [使用 Java 将 PSD 转换为 PNG 并旋转 PSD 文件中的图层](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [如何使用 Aspose.PSD 在 Java 中旋转图像](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}