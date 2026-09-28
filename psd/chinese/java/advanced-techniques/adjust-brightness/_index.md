---
date: 2026-09-28
description: Java 图像处理教程展示了如何使用 Aspose.PSD for Java 调整图像的亮度。请按照逐步代码加载、修改并保存 PSD 或
  TIFF 文件。
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: 调整图像亮度
og_description: Java 图像处理教程展示了如何使用 Aspose.PSD for Java 调整图像的亮度。请按照逐步代码加载、修改并保存 PSD
  或 TIFF 文件。
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: Java 图像处理：使用 Aspose.PSD 调整亮度
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: Java 图像处理：使用 Aspose.PSD 调整亮度
url: /zh/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 调整图像亮度

## 介绍

在本 **java image processing** 教程中，您将学习如何直接通过 Java 代码调整图片的亮度。亮度调节是图形设计师、摄影师以及任何构建图像处理流水线的人经常需要完成的任务。在本 **java image manipulation** 指南中，我们将使用 Aspose.PSD for Java 库，完整演示工作流——加载 PSD/TIFF、应用亮度偏移并保存结果。

## 快速答案

- **哪个库处理亮度？** Aspose.PSD for Java.  
- **哪个方法更改亮度？** `RasterImage.adjustBrightness()`.  
- **我可以使用 PSD 和 TIFF 文件吗？** Yes, the API supports both formats and 10+ additional image types.  
- **生产环境需要许可证吗？** A commercial license is required for non‑evaluation use.  
- **实现需要多长时间？** Typically under 10 minutes for a basic adjustment.

## 什么是 java image processing？

`Java image processing` 指的是一套技术，使您能够使用 Java 以编程方式读取、转换和写入图像数据。调整亮度是核心操作之一，它会改变每个像素的整体亮度，使暗区变亮或亮区变暗。

## 为什么使用 Aspose.PSD for Java？

Aspose.PSD for Java 提供了一个全面的纯 Java 解决方案，支持广泛的光栅和矢量格式，消除本机依赖，并为大文件提供高性能缓存。其丰富的 API 让开发者能够以最少的代码执行复杂的颜色校正和基于图层的编辑，非常适合简单的调节和高级图像处理流水线。

- **支持 10+ 光栅和矢量格式** – PSD、TIFF、JPEG、PNG、BMP、GIF 等。  
- **Pure‑Java 实现** – 无本机 DLL 或外部依赖，可在任何 JVM 上运行。  
- **高性能缓存** – 可缓存光栅数据，使对大文件的重复编辑速度提升至最高 2 倍。  
- **丰富的 API** – 超过 150 个用于颜色校正、图层处理、蒙版和合成的方法。

## 先决条件

在深入教程之前，请确保您具备以下先决条件：

- Aspose.PSD for Java 库：从 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 下载并安装该库。  
- 已在机器上安装 Java Development Kit (JDK) 8 或更高版本。  
- 开发环境（IDE），如 IntelliJ IDEA、Eclipse 或 VS Code。

## 导入包

首先，将必要的包导入到您的 Java 项目中。在本示例中，我们将使用以下代码：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

现在，让我们将图像亮度调整的过程拆分为简单的步骤：

## 如何使用 Aspose.PSD 调整亮度？

加载源图像，应用亮度偏移，配置保存选项，并将结果写入磁盘——全部四个简洁步骤。以下章节提供了清晰的逐步演示，您可以直接复制到自己的项目中。此方法确保每个操作高效执行，并且最终图像在保持原始质量的同时呈现所需的亮度变化。

### 步骤 1：加载图像

`RasterImage` 类表示内存中 PSD 或 TIFF 文件的光栅化版本。它提供对像素的直接访问，以进行颜色校正操作。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

在此步骤中，我们加载目标图像并将其强制转换为 `RasterImage` 以进行后续处理。

### 步骤 2：调整亮度

`adjustBrightness(int value)` 根据指定的整数值改变每个像素的亮度。正数会使图像变亮，负数会使其变暗。该方法就地处理图像，无需创建额外的对象。

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

这里，我们使用 `adjustBrightness` 方法修改图像的亮度。在本例中，我们将亮度降低 50 单位，但您可以根据需求自定义该值。

### 步骤 3：设置 TiffOptions

`TiffOptions` 指定 TIFF 输出的编码参数，例如每个样本的位数和光度解释。它允许您控制生成文件的编码方式。

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

为保存调整后的图像配置 `TiffOptions`。根据具体需求调整 `bitsPerSample` 和 `photometric` 属性。

### 步骤 4：保存结果图像

调用 `save` 使用先前定义的选项将处理后的光栅数据写入文件。此操作是原子性的，确保输出文件为有效的 TIFF 图像。

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

最后，使用指定的 `TiffOptions` 保存修改后的图像。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|--------|----------|
| **`ClassCastException` 在转换 Image 时** | 文件不是光栅图像（例如，矢量 PSD）。 | 验证源文件格式，或在转换前使用 `image instanceof RasterImage`。 |
| **亮度更改无效** | 在调整之前图像未被缓存。 | 如步骤 1 所示，调用 `rasterImage.cacheData()`。 |
| **保存的文件出现损坏** | `TiffOptions` 配置不正确。 | 确保 `bitsPerSample` 与源图像深度匹配（通常为每通道 8 位）。 |

## 常见问答

**Q: 我可以在除 PSD 之外的其他图像格式中调整亮度吗？**  
**A:** 是的，Aspose.PSD for Java 除了支持 PSD 和 TIFF 外，还支持 JPEG、PNG、BMP、GIF 等多种光栅格式。

**Q: 在图像调整过程中如何处理错误？**  
**A:** 将处理代码放在 try‑catch 块中，捕获 `IOException` 或 `ImageProcessingException` 以管理文件访问和光栅操作错误。

**Q: 亮度调整的范围是否有限制？**  
**A:** 该方法接受 –255 到 +255 的整数值；超出此范围的值会被限制到最近的界限。

**Q: 我可以在商业项目中使用 Aspose.PSD for Java 吗？**  
**A:** 可以，生产使用需要商业许可证。请在 [here](https://purchase.aspose.com/buy) 购买许可证。

**Q: 是否提供免费试用？**  
**A:** 是的，您可以从 [here](https://releases.aspose.com/) 获取免费试用以探索该库。

**Q: `adjustBrightness` 方法会影响图层可见性吗？**  
**A:** 该方法作用于光栅化的合成图像，因此在光栅化过程中会忽略隐藏的图层，保留预期的视觉结果。

**Q: 我可以链式调用多个调整（例如，对比度、饱和度）吗？**  
**A:** 完全可以。在调整亮度后，您可以在同一 `RasterImage` 实例上调用 `adjustContrast`、`adjustSaturation` 或其他颜色校正方法。

---

**最后更新：** 2026-09-28  
**测试环境：** Aspose.PSD for Java 24.12 (latest at time of writing)  
**作者：** Aspose

## 相关教程

- [Image Processing Java Library：使用 Aspose.PSD 反转图层](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [使用 Aspose.PSD for Java 将图像转换为灰度](/psd/java/advanced-techniques/grayscale-image/)
- [如何使用 Aspose.PSD for Java 将图像旋转到特定角度](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}