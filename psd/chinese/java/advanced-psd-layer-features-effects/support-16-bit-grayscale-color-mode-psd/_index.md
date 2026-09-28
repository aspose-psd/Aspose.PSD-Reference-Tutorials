---
date: 2026-09-28
description: 了解如何使用 Aspose.PSD for Java 将 PSD 导出为 PNG，并将 PSD 颜色模式设置为 16 位灰度。提供带代码示例的分步指南。
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: 导出 PSD 为 PNG – 16 位灰度 – Java
og_description: 使用 Aspose.PSD for Java 将 PSD 导出为 PNG 并采用 16 位灰度。按照此分步教程可保留 65,536
  种灰度色阶。
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: 在 Java 中使用 16 位灰度将 PSD 导出为 PNG – Aspose.PSD 指南
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: 如何在 Java 中将 PSD 导出为 PNG 并使用 16 位灰度颜色模式
url: /zh/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中将 PSD 导出为 PNG（16‑bit 灰度色彩模式）

## 介绍
将 PSD 导出为 PNG 并保持 16‑bit 灰度色彩模式，可让您获得专业照片的细腻层次，同时拥有 PNG 的通用兼容性。在本指南中，您将学习如何 **将 PSD 色彩模式设置为 16‑bit 灰度**，随后使用 Aspose.PSD for Java **将 PSD 导出为 PNG**。教程涵盖从前置条件到故障排除的全部内容，帮助您将此工作流集成到任何基于 Java 的图像管道中。

## 快速答案
- **“将 PSD 导出为 PNG” 包含哪些步骤？** 加载 PSD，必要时更改其色彩模式，然后保存为 PNG 文件。  
- **哪个 Aspose 类负责转换？** `PsdImage` 用于加载 PSD，`PngOptions` 定义 PNG 输出设置。  
- **生产环境是否需要许可证？** 是的——试用版可用于测试，但商业使用必须购买付费许可证。  
- **PNG 能保留 16‑bit 深度吗？** 完全可以，使用 `PngColorType.GrayscaleWithAlpha` 即可。  
- **支持哪些 IDE？** 任意 Java IDE——IntelliJ IDEA、Eclipse、VS Code 或 NetBeans。

## 什么是将 PSD 导出为 PNG？
将 PSD 导出为 PNG 是指将 Adobe Photoshop 文档（PSD）转换为可移植网络图形（PNG）文件的过程，同时保留图像的像素数据和色彩深度。此转换常用于在网页上共享高质量灰度资源，而不会丢失色调细节。

## 为什么要以 16‑bit 灰度导出 PSD 为 PNG？
以 PNG 导出并保持 16‑bit 灰度可保留 65 536 种灰度层次，远比 8‑bit 图像的 256 种层次提供更丰富的色调。PNG 的通用支持确保文件可在浏览器、移动应用和桌面编辑器中无损显示，而 Aspose.PSD 的无损压缩则保证不会产生伪影。

## 前置条件
在开始之前，请确保已准备好以下项目：

1. **Java Development Kit (JDK)** – 从 [Oracle 的站点](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下载并安装最新 JDK。  
2. **Aspose.PSD for Java 库** – 从 [Aspose 下载页面](https://releases.aspose.com/psd/java/) 获取 JAR 包。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 Visual Studio Code 任意一种均可。  
4. **基本的 Java 知识** – 您应熟悉创建类、处理异常以及使用文件路径。  
5. **示例 PSD 文件** – 在 Adobe Photoshop 中创建或在线获取免费样本。

## 如何一步步将 PSD 导出为 PNG

## 如何将 PSD 色彩模式设置为 16‑bit 灰度？
`PsdImage` 是 Aspose.PSD 用于加载并在内存中表示 PSD 文件的类。  
`ColorMode` 是一个枚举，定义 PSD 图像的色彩模式。

使用 `PsdImage` 加载 PSD，利用 `ColorMode` 属性更改其色彩模式，然后保存修改后的文件。此操作完全在内存中完成，省去中间文件，确保转换快速高效。

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

这些导入语句为您提供了操作 PSD 文件、设置色彩模式以及导出 PNG 所需的功能。

## 如何定义源目录和输出目录？
`File` 是 java.io 包中的类，表示文件系统中的文件或目录路径。

您需要告诉程序从哪里读取原始 PSD，以及将转换后的 PNG 写入何处。使用绝对路径或相对路径均可，但请在不同环境中保持一致，以避免路径解析错误。

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

将占位符字符串替换为您机器上的实际路径。

## 如何在可重用方法中封装转换逻辑？
`convertPsdToPng` 是自定义方法，用于封装将 PSD 文件转换为 PNG（可选设置）的所有步骤。

创建专用方法可让您对多个文件或不同设置重复使用相同的转换步骤。通过传入源路径、目标文件夹以及可选的压缩级别等参数，使工作流灵活且易于维护。

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

此方法让您 **设置 PSD 色彩模式**，随后 **将 PSD 导出为 PNG**，实现一次性完成。

## 如何加载 PSD 并应用 16‑bit 灰度模式？
`PsdImage` 是 Aspose.PSD 用于将 PSD 文件加载到内存的类。  
`ColorMode.GRAYSCALE_16` 是一个枚举值，用于将图像设置为 16‑bit 灰度。  
`channelBitsCount` 是一个属性，指定每个通道的位数。

在转换方法内部，构建完整文件路径，实例化 `PsdImage`，并将其 `ColorMode` 更改为 `ColorMode.GRAYSCALE_16`。`channelBitsCount` 必须设为 16，以保持高位深，确保图像保留所有色调信息。

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` 用于帮助您追踪每个导出文件所使用的设置。

## 如何在图像上绘制细微边框（可选步骤）？
`Graphics` 是一个类，提供在 `PsdImage` 画布上绘图的能力。

您可以选择在图像周围绘制一个灰色矩形，以便在测试期间更清晰地看到输出。此步骤演示了如何使用图层和图形对象，矩形会根据图像尺寸动态计算，始终保持居中。

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

矩形会根据图像尺寸动态计算，始终保持居中。

## 如何使用新色彩模式保存修改后的 PSD？
`PsdOptions` 是一个类，用于控制 PSD 文件的保存方式，包括色彩模式和位深设置。

在绘制（或跳过）步骤后，调用 `PsdImage` 实例的 `save` 方法，并传入一个保留 16‑bit 灰度配置的 `PsdOptions` 对象。这样可确保保存的 PSD 保持所需的色彩模式且不丢失数据。

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## 如何在保留 16‑bit 深度的同时将 PSD 转换为 PNG？
`PngOptions` 是一个类，定义 PNG 输出设置，如色彩类型和压缩级别。  
`PngColorType.GrayscaleWithAlpha` 是一个枚举值，用于以带 Alpha 通道的方式存储 16‑bit 灰度数据。

加载新保存的 PSD，使用 `PngColorType.GrayscaleWithAlpha` 配置 `PngOptions`，然后调用 `save`。这会在 PNG 文件中保留 16‑bit 灰度数据，提供无损的高质量图像，适合后续处理或分发。

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

现在您已成功 **将 PSD 导出为 PNG**，并保持高质量的 16‑bit 灰度数据。

## 常见问题及解决方案
| 问题 | 产生原因 | 解决办法 |
|------|----------|----------|
| **“Unsupported color type” 异常** | 尝试以不受支持的通道配置保存 PSD。 | 确保 `channelBitsCount` 与实际位深（16）匹配，且 `channelsCount` 对于灰度图像为 1。 |
| **文件未找到** | 源目录路径不正确。 | 仔细检查 `sourceDir` 字符串，并确认 PSD 文件确实位于该位置。 |
| **输出 PNG 显示为全黑** | PNG 保存时未正确处理 Alpha 通道。 | 如上所示使用 `PngColorType.GrayscaleWithAlpha`。 |
| **大尺寸 PSD 导致内存溢出** | 将整个文件加载到内存。 | 通过 `PsdImage.load(inputStream, new LoadOptions())` 启用流式模式，以高效处理大文件。 |

## 常见问答

**问：什么是 16‑bit 灰度色彩模式？**  
答：它提供 65 536 种灰度层次，远比标准的 8‑bit（256 层次）呈现出更丰富的色调细节。

**问：我可以使用 Aspose.PSD 处理非灰度图像吗？**  
答：当然可以！Aspose.PSD 支持 RGB、CMYK、Lab、Indexed 等多种色彩模式。

**问：Aspose.PSD 有试用版吗？**  
答：有，您可以免费试用 Aspose.PSD。只需前往 [Aspose 下载页面](https://releases.aspose.com/)。

**问：在哪里可以找到更多 Aspose.PSD 示例？**  
答：请查看官方 [文档](https://reference.aspose.com/psd/java/)，其中包含深入教程、API 参考和示例项目。

**问：如何购买 Aspose.PSD 的许可证？**  
答：访问 [Aspose 购买页面](https://purchase.aspose.com/buy) 进行购买。

---

**最后更新：** 2026-09-28  
**测试环境：** Aspose.PSD for Java 24.12（撰写时的最新版本）  
**作者：** Aspose

## 相关教程

- [使用 Aspose.PSD for Java 指定位深将 PSD 转换为 PNG](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [使用 Aspose.PSD for Java 导出带图层效果的 PSD 为 PNG](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [使用 Aspose.PSD Java 将 PSD 保存为 JPEG 并支持 RGB 色彩](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}