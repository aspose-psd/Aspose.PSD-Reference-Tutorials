---
date: 2025-12-21
description: 了解如何使用 Aspose.PSD 通过调整图像伽马值进行 Java 图像处理。一步步指南，教您将 PSD 转换为 TIFF 并应用伽马校正。
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java 图像处理 – 使用 Aspose.PSD 调整伽马
url: /zh/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 图像处理 – 使用 Aspose.PSD 调整 Gamma

## 介绍

如果您正在进行 **java image processing**，对图片的 Gamma 进行调整是一种基础技术，可在不丢失细节的情况下提升亮度和对比度。在本教程中，我们将演示如何使用 **Aspose.PSD for Java** 对 PSD 文件进行 Gamma 校正，然后将结果导出为 TIFF 图像。您将看到这种方法为何快速、可靠，并且非常适合服务器端图像流水线。

## 快速答案
- **Gamma 校正的作用是什么？** 它重新映射亮度值，使暗部变亮或亮部变暗，同时保留整体细节。  
- **哪个库负责处理？** Aspose.PSD for Java 提供了专用的 `adjustGamma` 方法用于光栅图像。  
- **可以在同一流程中将 PSD 转为 TIFF 吗？** 可以——在 Gamma 调整后，直接使用 `TiffOptions` 将图像保存为 TIFF。  
- **开发时需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。  
- **支持的 Java 版本是什么？** Aspose.PSD 支持 Java 8 及更高版本。

## 什么是 java 图像处理？

Java 图像处理是指使用 Java 库对视觉数据进行操作、分析和转换的过程。任务包括调整大小、滤镜、颜色校正和格式转换——所有这些都可以在桌面或 Web 应用程序中实现自动化。

## 为什么使用 Aspose.PSD 进行 Gamma 校正？

Aspose.PSD 提供了高级 API，抽象了 PSD 格式的复杂性，让您专注于实际的图像调整。它处理缓存、颜色配置文件，并提供简洁的 `adjustGamma` 调用，使其成为 **图像 Gamma 校正** 和 **convert psd to tiff** 工作流的理想选择。

## 前提条件

在开始教程之前，请确保已完成以下准备工作：

1. **Java 开发环境** – 确保系统已安装 Java 开发环境。  
2. **Aspose.PSD 库** – 下载并将 Aspose.PSD 库集成到您的 Java 项目中。您可以在 [documentation](https://reference.aspose.com/psd/java/) 中找到所需资源。  
3. **示例图像** – 准备一张用于 Gamma 调整的示例 PSD 图像。

## 导入包

要启动此过程，请在 Java 项目中导入所需的包。这为无缝使用 Aspose.PSD 功能奠定基础。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 步骤 1：加载图像

首先将示例 PSD 图像加载到 `RasterImage` 类的实例中。这是后续 Gamma 调整的基础。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## 步骤 2：调整 Gamma

现在，使用 `adjustGamma` 方法对已加载的图像进行 Gamma 调整。根据需求微调 Gamma 值。

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 步骤 3：创建 TiffOptions

为生成的图像创建 `TiffOptions` 实例。设置各种属性，如每样本位数和光度选项，以满足您的输出规格。

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 步骤 4：保存结果图像

使用前面定义的 `TiffOptions` 将处理后的图像保存为 TIFF 格式。

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 常见问题及解决方案

| 问题 | 产生原因 | 解决方法 |
|------|----------|----------|
| **图像出现漂白现象** | Gamma 值过高（例如 > 2.5） | 将 Gamma 系数降低到 1.8 到 2.2 之间的值。 |
| **`rasterImage.isCached()` 返回 false** | 图像尚未加载到内存 | 在调整 Gamma 之前调用 `rasterImage.cacheData()`。 |
| **TIFF 文件大小过大** | 每样本位数设置为 16 位 | 如示例所示使用 8 位样本 (`{8,8,8}`)。 |

## 常见问答

**Q: 能否为每个颜色通道应用不同的 Gamma 值？**  
A: 可以——`adjustGamma` 方法接受红、绿、蓝通道的独立 float 值。

**Q: 是否可以在保存之前链式执行多个图像调整？**  
A: 完全可以。您可以在同一个 `RasterImage` 实例上依次进行缩放、裁剪或颜色校正等操作。

**Q: Aspose.PSD 是否支持多页 PSD 文件？**  
A: 支持，每个图层都可以单独访问和处理。

**Q: 除了 TIFF，我还能导出哪些格式？**  
A: Aspose.PSD 通过相应的选项类支持 PNG、JPEG、BMP 等多种格式。

## 结论

恭喜！您已成功通过 Aspose.PSD for Java 调整 PSD 文件的 Gamma 并将其导出为 TIFF 图像，实现了 **java image processing**。此工作流为图像亮度和对比度提供了细粒度控制，非常适合自动化图形流水线、Web 服务或桌面工具。

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## 常见问题

### Q1: 在哪里可以找到 Aspose.PSD 文档？

A1: 您可以在 [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/) 访问文档。

### Q2: 如何下载 Aspose.PSD for Java？

A2: 从 [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/) 下载库。

### Q3: 在哪里可以购买 Aspose.PSD？

A3: 访问 [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) 进行购买。

### Q4: 是否提供免费试用？

A4: 是的，您可以在 [https://releases.aspose.com/](https://releases.aspose.com/) 体验免费试用。

### Q5: 在哪里可以获取 Aspose.PSD 的支持？

A5: 请前往 Aspose.PSD 论坛 [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34) 获取支持。