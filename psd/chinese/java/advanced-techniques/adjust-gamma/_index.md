---
date: 2026-08-01
description: 在简明教程中学习如何在 Java 图像处理使用 Aspose.PSD 调整 Gamma、将 PSD 转换为 TIFF，并修复褪色的图像。
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: 调整图像的 Gamma
og_description: 了解如何在 Java 图像处理使用 Aspose.PSD 调整 Gamma – 这是一款快速的服务器端库，可在几行代码内纠正褪色的图像并将
  PSD 转换为 TIFF。
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: 如何调整 Gamma – 使用 Aspose.PSD 的 Java 处理
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: 如何在 Java 图像处理中使用 Aspose.PSD 调整 Gamma
url: /zh/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 图像处理 中使用 Aspose.PSD 调整 Gamma

## 介绍

如果您正在进行 **java image processing**，学习 **how to adjust gamma** 是一种基础技术，可在不丢失细节的情况下提升亮度和对比度。在本教程中，我们将演示如何使用 **Aspose.PSD for Java** 对 PSD 文件应用 gamma 校正，**convert PSD to TIFF**，并避免 **washed‑out image**。您将看到这种方法为何快速、可靠，并且非常适合 **server‑side image processing** 流程。

## 快速答案
- **What does gamma correction do?** 它重新映射亮度值，使暗区更亮或亮区更暗，同时保留整体细节。  
- **Which library handles the processing?** Aspose.PSD for Java 提供了专用于栅格图像的 `adjustGamma` 方法。  
- **Can I convert PSD to TIFF in the same flow?** 是的 — 在 gamma 调整后，您可以使用 `TiffOptions` 将图像直接保存为 TIFF。  
- **Do I need a license for development?** 免费试用可用于测试；生产环境需要商业许可证。  
- **What Java version is supported?** Aspose.PSD 支持 Java 8 及更高版本。  

## 什么是 Java Gamma 校正？

Gamma 校正改变了编码像素值与显示亮度之间的非线性关系。通过微调 gamma 曲线，您可以 **fix washed out image** 问题或在不使高光过度曝光的情况下增强阴影细节。它通过对每个像素应用幂律函数来实现，使暗部变亮并压缩高光，从而产生更自然的视觉效果。

## 为什么使用 Aspose.PSD 进行 Gamma 校正？

Aspose.PSD 是一个 **java image processing library**，它抽象了 PSD 格式的复杂性。它支持处理高达 2 GB 的文件，能够处理超过 50 种不同的图像格式，并提供了简洁的 `adjustGamma` 调用，使其非常适合 **java gamma correction** 和 **convert PSD to TIFF** 工作流。

## 先决条件

1. **Java Development Environment** – 已安装 Java 8 或更高版本。  
2. **Aspose.PSD Library** – 下载并将 JAR 添加到项目中。请参阅官方 [documentation](https://reference.aspose.com/psd/java/)。  
3. **Sample Image** – 您想要处理的 PSD 文件（例如 `sample.psd`）。  

## 导入包

在开始之前，导入必要的命名空间，以便访问栅格处理和文件格式选项。

## 步骤 1：加载图像

`RasterImage` 类表示内存中 PSD 图层的栅格像素数据。一次加载图像并进行缓存，可减少后续调整时的内存消耗。

## 步骤 2：调整 Gamma

使用 `new RasterImage("sample.psd")` 加载 PSD 并调用 `rasterImage.adjustGamma(2.0f)` — 这行代码将在所有颜色通道上应用 2.0 的 gamma，提亮阴影且保持高光不变。如果需要对特定通道进行微调，您可以为红、绿、蓝通道分别传入数值。

## 步骤 3：创建 TiffOptions

`TiffOptions` 允许您控制压缩方式、每样本位数以及其他 TIFF 特定设置。设置 8 位样本 (`{8,8,8}`) 可在保持颜色保真度的同时，使 TIFF 文件大小保持在合理范围。

## 步骤 4：保存结果图像

调用 `rasterImage.save("output.tif", tiffOptions)` 将处理后的图像写入磁盘。保存后，您可以将 TIFF 输入到下游系统，例如打印服务或 Web API。

## 常见用例

- **Automated graphics pipelines** – 在生成缩略图之前即时调整 gamma。  
- **Batch conversion tools** – 在归一化亮度的同时，将大型 PSD 档案转换为 TIFF。  
- **Web services** – 暴露一个端点，接收 PSD，应用 gamma 校正，并返回供客户端使用的 TIFF。  

## 常见问题及解决方案

| 问题 | 原因 | 解决方法 |
|-------|----------------|------------|
| **Image appears washed out** | Gamma 值过高（例如 > 2.5） | 将 gamma 系数降低到 1.8 到 2.2 之间的值。 |
| **`rasterImage.isCached()` returns false** | 图像尚未加载到内存 | 在调整 gamma 之前调用 `rasterImage.cacheData()`。 |
| **TIFF file size is large** | 每样本位数设置为 16 位 | 如示例所示，使用 8 位样本 (`{8,8,8}`)。 |

## 常见问题

**Q: 我可以对每个颜色通道应用不同的 gamma 值吗？**  
**A: 可以 — `adjustGamma` 方法接受红、绿、蓝通道的单独 float 值。**

**Q: 是否可以在保存之前链式执行多个图像调整？**  
**A: 完全可以。您可以在同一个 `RasterImage` 实例上顺序执行缩放、裁剪或颜色校正等操作。**

**Q: Aspose.PSD 是否支持多页 PSD 文件？**  
**A: 支持，每个图层都可以单独访问和处理。**

**Q: 除了 TIFF，我还能导出哪些格式？**  
**A: Aspose.PSD 通过相应的选项类支持 PNG、JPEG、BMP 以及许多其他格式。**

**Q: 如何避免 gamma 校正后出现 washed‑out image？**  
**A: 从适中的 gamma（约 2.0）开始并预览结果；如果图像过亮，则降低 gamma。**

## 结论

恭喜！您已成功学习 **how to adjust gamma** 在 **java image processing** 工作流中的使用，完成了 PSD 到 TIFF 的转换，并避免了诸如 **washed‑out image** 等常见问题。此方案让您对亮度和对比度拥有细粒度的控制，非常适合自动化图形流水线、Web 服务或桌面工具。

---

**最后更新：** 2026-08-01  
**测试环境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [Java 图像处理教程 - 使用 Aspose.PSD for Java 调整图像亮度](/psd/java/advanced-techniques/adjust-brightness/)
- [如何将 PSD 转换为 TIFF 并使用 Aspose.PSD for Java 调整对比度](/psd/java/advanced-techniques/adjust-contrast/)
- [在 Java 中将 PSD 转换为图像 – 使用 Aspose.PSD 应用调整图层](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

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

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```