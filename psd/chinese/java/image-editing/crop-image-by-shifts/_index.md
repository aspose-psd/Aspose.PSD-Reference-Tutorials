---
date: 2026-07-03
description: 了解如何使用 Aspose.PSD for Java 裁剪 Java 图像。本分步图像裁剪教程涵盖加载 PSD 文件、设置位移值以及保存结果。
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: 按位移裁剪图像
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD 按位移裁剪 Java 图像
url: /zh/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 按位移裁剪 Java 图像

## 介绍

在 Java 图像处理领域，**crop image java** 是准备图形、缩略图或 UI 资源的常见需求。Aspose.PSD for Java 通过提供一个简单的 `crop` 方法，使此任务变得直截了当，该方法适用于任何受支持的光栅格式。在本教程中，您将学习如何加载 PSD 文件，定义左右上下的位移值，应用裁剪并保存结果——全部无需编写自定义像素操作代码。

## 快速答疑
- **哪个库负责裁剪？** Aspose.PSD for Java 提供内置的 `crop` 方法。  
- **我需要许可证吗？** 临时许可证可用于评估；生产环境需要正式许可证。  
- **支持哪些格式？** 超过 30 种光栅格式，包括 PSD、JPEG、PNG、BMP 和 TIFF。  
- **最大文件大小？** 可处理高达 2 GB 的文件，而无需将整个图像加载到内存中。  
- **代码行数多少？** 仅需五个逻辑步骤——加载、缓存、定义位移、裁剪和保存。

## 什么是 crop image java？

`crop image java` 指在 Java 应用程序中修剪位图的操作。使用 Aspose.PSD 时，该操作由 `crop` 方法执行，该方法接受图像每一侧的位移值并返回一个新的图像实例。

## 为什么在图像裁剪中使用 Aspose.PSD？

Aspose.PSD 支持 **30+** 图像格式，并且能够在使用不到 150 MB RAM 的情况下处理多百页的 PSD 文件，这归功于其惰性加载架构。该库还保证像素级精确结果，保留图层、蒙版和色彩配置文件——这是许多通用图像库无法保证的。

## 先决条件

### Java 开发工具包 (JDK)

确保在系统上安装了最新版本的 JDK。您可以从 [here](https://www.oracle.com/java/technologies/javase-downloads.html) 下载。

### Aspose.PSD for Java 库

首先，您需要获取 Aspose.PSD for Java 库。前往 [download page](https://releases.aspose.com/psd/java/) 并获取最新版本。

### 集成开发环境 (IDE)

选择您喜欢的 Java IDE，例如 Eclipse 或 IntelliJ，以获得流畅的编码体验。

## 如何裁剪 crop image java？

加载源文件，为每一侧定义像素位移，然后调用 `crop` 方法——整个工作流可以用五行简洁的代码实现。`crop` 操作会创建一个仅包含您指定区域的新图像，原始文件保持不变。

### 步骤 1：加载图像

`Image` 是 Aspose.PSD 中所有图像类型的基类。  
`RasterImage` 表示光栅图像并提供裁剪功能。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 步骤 2：缓存图像数据

`cacheData()` 将图像数据加载到内存中，以加快处理速度。  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### 步骤 3：定义位移值

以像素为单位指定图像四侧（左、上、右、下）的位移值。  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### 步骤 4：应用裁剪

`crop(left, right, top, bottom)` 按每侧指定的像素位移裁剪图像。  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### 步骤 5：保存结果

`JpegOptions` 定义 JPEG 编码设置，例如质量和色彩配置文件。  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

恭喜！您已成功使用 Aspose.PSD for Java 裁剪图像。

## 常见问题与解决方案

- **图像未改变：** 验证位移值为正且未超过原始尺寸。  
- **大文件出现 OutOfMemoryError：** 如步骤 2 所示启用缓存；这会强制 Aspose.PSD 使用临时文件而不是将整个图像保存在 RAM 中。  
- **裁剪后颜色偏移：** 如需精确的颜色保真度，请通过调用 `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` 来确保保留色彩配置文件。

## 常见问答

**Q: Aspose.PSD 是否兼容所有图像格式？**  
A: 是的，Aspose.PSD 支持超过 30 种光栅格式，包括 PSD、JPEG、PNG、BMP、TIFF 和 GIF，确保广泛的兼容性。

**Q: 我可以对同一图像执行多次裁剪操作吗？**  
A: 当然可以。在每次调用 `crop` 后，您会得到一个新的图像对象，您可以根据需要再次裁剪。

**Q: 是否有 Aspose.PSD 的社区论坛？**  
A: 有，您可以在 [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) 获取支持并与社区互动。

**Q: 如何获取 Aspose.PSD 的临时许可证？**  
A: 请访问 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

**Q: 是否有展示 Aspose.PSD 功能的示例项目？**  
A: 请在 [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/) 中查阅文档和示例。

---

**最后更新:** 2026-07-03  
**已测试于:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## 相关教程

- [在 Aspose.PSD for Java 中按矩形裁剪图像](/psd/java/image-editing/crop-image-by-rectangle/)
- [Java 图像裁剪 - 使用 Aspose.PSD for Java 扩展和裁剪图像](/psd/java/image-editing/expand-and-crop-images/)
- [Java 图像缩放 - 在 Aspose.PSD for Java 中使用 Resize Type 枚举](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}