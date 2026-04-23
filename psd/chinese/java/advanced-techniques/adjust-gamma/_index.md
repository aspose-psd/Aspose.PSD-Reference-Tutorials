---
date: 2026-02-27
description: 学习如何在 Java 图像处理中使用 Aspose.PSD 调整伽马、将 PSD 转换为 TIFF，并在简明教程中修复褪色的图像。
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: 如何在 Java 图像处理使用 Aspose.PSD 调整伽马
url: /zh/java/advanced-techniques/adjust-gamma/
weight: 23
---

 in Java Image Processing with Aspose.PSD" translate to Chinese: "# 如何使用 Aspose.PSD 在 Java 图像处理 中调整伽马"

Similarly other headings.

Proceed.

Translate paragraphs.

Make sure to keep bullet points etc.

Let's craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD 在 Java 图像处理 中调整伽马

## 介绍

如果您正在进行 **java 图像处理**，学习 **如何调整伽马** 是一种基础技术，可在不丢失细节的情况下提升亮度和对比度。在本教程中，我们将演示如何使用 **Aspose.PSD for Java** 对 PSD 文件进行伽马校正、**将 PSD 转换为 TIFF**，并避免出现 **颜色褪色的图像**。您将了解为何这种方法快速、可靠，且非常适合服务器端图像流水线。

## 快速回答
- **伽马校正的作用是什么？** 它会重新映射亮度值，使暗部更亮或亮部更暗，同时保留整体细节。  
- **哪个库负责处理？** Aspose.PSD for Java 提供了专门的 `adjustGamma` 方法用于光栅图像。  
- **可以在同一流程中将 PSD 转换为 TIFF 吗？** 可以——在伽马调整后，直接使用 `TiffOptions` 将图像保存为 TIFF。  
- **开发时需要许可证吗？** 免费试用版可用于测试；生产环境需要商业许可证。  
- **支持哪个 Java 版本？** Aspose.PSD 支持 Java 8 及更高版本。

## 如何在 Java 图像处理 中调整伽马
调整伽马是任何 **java 图像处理教程** 中处理亮度或对比度的核心部分。下面我们将分步骤说明每行代码的意义，并展示如何将该过程集成到现有代码库中。

## 什么是 Java 伽马校正？
伽马校正改变了编码像素值与显示亮度之间的非线性关系。通过微调伽马曲线，您可以 **修复颜色褪色的图像** 问题，或在不导致高光过曝的情况下增强阴影细节。

## 为什么使用 Aspose.PSD 进行伽马校正？
Aspose.PSD 是一个强大的 **java 图像处理库**，它抽象了 PSD 格式的复杂性。它处理颜色配置文件、缓存，并提供简洁的 `adjustGamma` 调用，使其非常适合 **java 伽马校正** 和 **将 PSD 转换为 TIFF** 的工作流。

## 前置条件

1. **Java 开发环境** – 已安装 Java 8 或更高版本。  
2. **Aspose.PSD 库** – 下载并将 JAR 添加到项目中。参见官方 [documentation](https://reference.aspose.com/psd/java/)。  
3. **示例图像** – 您想要处理的 PSD 文件（例如 `sample.psd`）。  

## 导入包

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 步骤 1：加载图像

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

**小贴士：** 将光栅数据缓存一次，可在连续进行多次调整时减少内存波动。

## 步骤 2：调整伽马

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

如果需要对各通道进行特定调整，可为红、绿、蓝通道传入不同的值。

## 步骤 3：创建 TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

设置 8 位样本 (`{8,8,8}`) 可在保持颜色保真度的同时，使 TIFF 文件大小保持在合理范围。

## 步骤 4：保存结果图像

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

保存后，您可以将 TIFF 输入到下游系统，如打印服务或 Web API。

## 常见使用场景

- **自动化图形流水线** – 在生成缩略图前实时调整伽马。  
- **批量转换工具** – 将大型 PSD 档案批量转换为 TIFF，同时归一化亮度。  
- **Web 服务** – 提供一个端点，接收 PSD、进行伽马校正并返回 TIFF 供客户端使用。

## 常见问题及解决方案

| 问题 | 产生原因 | 解决办法 |
|------|----------|----------|
| **图像出现颜色褪色** | 伽马值过高（例如 > 2.5） | 将伽马因子降低到 1.8~2.2 之间。 |
| **`rasterImage.isCached()` 返回 false** | 图像尚未加载到内存 | 在调整伽马前调用 `rasterImage.cacheData()`。 |
| **TIFF 文件大小过大** | 每样本位数设置为 16 位 | 如示例所示使用 8 位样本 (`{8,8,8}`)。 |

## 常见问答

**问：可以为每个颜色通道设置不同的伽马值吗？**  
答：可以——`adjustGamma` 方法接受红、绿、蓝通道的独立 float 值。

**问：是否可以在保存前链式调用多个图像调整？**  
答：完全可以。您可以在同一个 `RasterImage` 实例上依次执行缩放、裁剪或颜色校正等操作。

**问：Aspose.PSD 是否支持多页 PSD 文件？**  
答：支持，每个图层都可以单独访问和处理。

**问：除了 TIFF，我还能导出哪些格式？**  
答：Aspose.PSD 通过相应的选项类支持 PNG、JPEG、BMP 等多种格式。

**问：如何避免伽马校正后出现颜色褪色的图像？**  
答：从适中的伽马值（约 2.0）开始预览结果；如果图像过亮，则适当降低伽马。

## 结论

恭喜！您已经成功学习了在 **java 图像处理** 工作流中 **如何调整伽马**，并实现了 PSD 到 TIFF 的转换，同时规避了常见的 **颜色褪色的图像** 问题。此模式为您提供了对亮度和对比度的细粒度控制，非常适合自动化图形流水线、Web 服务或桌面工具。

---

**最后更新：** 2026-02-27  
**测试版本：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}