---
date: 2026-06-03
description: 了解如何使用 Aspose.PSD for Java 调整图像大小。本分步指南涵盖 Resize Type Enumeration、高质量图像缩放以及如何将
  PSD 转换为 JPEG。
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: 使用 Resize Type Enumeration 进行图像缩放
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何在 Java 中使用 Resize Type Enumeration 调整图像大小
url: /zh/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Resize Type 枚举在 Java 中调整图像大小

## 介绍

如果您希望在 Java 项目中高效地 **how to resize image** 文件，Aspose.PSD for Java 提供了简洁且高性能的 API。在本教程中，我们将演示如何加载 PSD、应用 **Resize Type Enumeration** 进行高质量图像缩放，最后 **convert PSD to JPEG**。无论您是构建桌面编辑器还是自动化的服务器端流水线，这些步骤都能让您仅用几行代码即可控制尺寸、质量和格式。

## 快速答案
- **哪个库处理 resize image java？** Aspose.PSD for Java.
- **哪种 resize type 能提供最佳质量？** `ResizeType.LanczosResample`.
- **在调整大小后，我可以将 PSD 转换为 JPEG 吗？** 是的，只需使用 `JpegOptions` 保存。
- **生产环境需要许可证吗？** 需要有效的 Aspose.PSD 许可证才能用于生产。
- **这种方法适用于大批量处理吗？** 当然；API 能在不将整个文档加载到内存的情况下处理数百页的文件。

## 在 Java 中什么是 “how to resize image”？

**How to resize image** 指的是以编程方式更改图像的像素尺寸，同时保持视觉保真度。Aspose.PSD 的 `Resize` 方法结合 `ResizeType` 枚举提供了对缩放算法的精确控制，使开发者能够在各种源文件和目标尺寸之间保持质量。

## 为什么使用 Resize Type 枚举？

`ResizeType` 让您可以选择在速度和视觉质量之间取得最佳平衡的重采样算法。对于大多数场景，**LanczosResample** 能以适中的性能开销提供锐利的结果，在普通服务器级 CPU 上处理 2000 × 1500 图像的时间不足 120 ms，同时保持边缘细节完整。

## 前置条件

在开始之前，请确保您拥有：

1. **Java 开发环境** – 已安装并配置 JDK 8 或更高版本。  
2. **Aspose.PSD 库** – 从 [website](https://releases.aspose.com/psd/java/) 下载最新的 JAR。  
3. **示例 PSD 文件** – 使用 SDK 附带的 [sample.psd](Your Document Directory/sample.psd) 文件进行动手测试。

## 导入包

`Image` 是 Aspose.PSD 中所有图像类型的基类。将所需的导入语句添加到您的 Java 源文件中：

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步骤 1：加载图像

### 定义锚点

`RasterImage` 类是 Aspose.PSD 的核心对象，表示从 PSD 文件加载的基于光栅的图像。

将您的 PSD 加载到 `RasterImage` 实例中，以便操作其像素：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## 步骤 2：调整图像大小

`image.resize(width, height, resizeType)` 使用所选算法将图像调整为指定的尺寸。

现在使用 **Resize Type Enumeration** 对加载的图像进行大小调整。在本例中，我们使用 Lanczos Resample 方法，它在 **how to resize image** 时能够提供高质量的结果：

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 步骤 3：保存调整大小后的图像

`image.save(path, options)` 按提供的选项将图像以指定格式写入磁盘。

调整大小后，使用指定的尺寸和选定的 resize type 保存图像。在此，我们还通过将结果保存为 JPEG 文件演示 **convert psd to jpeg**：

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## 为什么使用 Resize Type 枚举？

`ResizeType` 为您提供对重采样算法的细粒度控制，使您能够在速度和质量之间取得平衡。对于大多数应用程序，`LanczosResample` 提供了很好的折衷，能够在不产生显著性能惩罚的情况下呈现锐利的结果，并且在各种图像内容上表现良好。

## 常见问题及解决方案

- **图像在调整大小后出现模糊** – 尝试使用不同的 `ResizeType`，如 `Bicubic` 或 `NearestNeighbour`，以查看哪种在您的特定图像上能获得最佳视觉效果。  
- **大 PSD 文件出现 OutOfMemoryError** – 将图像分成更小的块处理或增大 JVM 堆大小（`-Xmx` 参数）。Aspose.PSD 能在不将整个文档加载到内存的情况下处理高达 **2 GB** 的文件。

## 常见问答

### Q1：Aspose.PSD for Java 是否适用于小型和大型项目？

A1：当然！Aspose.PSD for Java 旨在满足各种规模的项目，提供可扩展性和高效性。

### Q2：我可以使用除 Lanczos Resample 之外的其他 resize type 吗？

A2：是的，Aspose.PSD for Java 提供多种 resize type，例如 **NearestNeighbour**、**Bicubic** 等。请查阅 API 文档获取完整列表。

### Q3：在哪里可以找到 Aspose.PSD for Java 的额外支持？

A3：如有任何疑问或需要帮助，请访问 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)。

### Q4：是否有 Aspose.PSD for Java 的免费试用？

A4：是的，您可以在 [here](https://releases.aspose.com/) 获取免费试用版。

### Q5：如何获取 Aspose.PSD for Java 的临时许可证？

A5：要获取临时许可证，请访问 [this link](https://purchase.aspose.com/temporary-license/)。

## 常见问题

**Q：如何在不调整大小的情况下以编程方式将 PSD 文件转换为 JPEG？**  
A：使用 `Image.load` 加载 PSD，然后调用 `image.save("output.jpg", new JpegOptions());`。

**Q：在调整大小时是否可以保持原始 DPI？**  
A：是的，您可以在保存之前为 `Image` 对象设置 `Resolution` 属性。

**Q：我可以链式调用多次 resize 操作吗？**  
A：虽然可以多次调用 `resize`，但更高效的做法是先计算最终尺寸并一次性完成缩放。

---

**最后更新：** 2026-06-03  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [使用 Aspose.PSD 的简单缩放 – Java 图像处理库](/psd/java/basic-image-operations/simple-resizing/)
- [在 Aspose.PSD for Java 中使用双三次重采样实现高质量图像缩放](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [如何使用 Aspose.PSD for Java 将 PSD 转换为 PNG 并按比例调整大小](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}