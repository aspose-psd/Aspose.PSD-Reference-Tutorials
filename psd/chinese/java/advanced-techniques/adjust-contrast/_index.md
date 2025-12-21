---
date: 2025-12-21
description: 学习如何使用 Aspose.PSD for Java（领先的 Java 图像处理库）调整图像对比度，并高效地将 PSD 转换为 TIFF。
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 调整图像对比度
url: /zh/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 调整图像对比度

## 介绍

如果你正在寻找 **如何在 Java 项目中调整对比度**，这里就是正确的地方。Aspose.PSD for Java 是一个强大的 **java 图像处理库**，可以让你微调图像属性，如对比度、亮度等。在本教程中，我们将逐步演示如何提升 PSD 文件的对比度，然后 **将 PSD 转换为 TIFF** 以供后续工作流使用。

## 快速答案
- **“调整对比度”是什么意思？** 它改变最暗像素和最亮像素之间的差异，使细节更加突出。
- **哪个库负责此功能？** Aspose.PSD for Java —— 完整的图像处理工具包。
- **需要许可证吗？** 临时许可证可用于测试；生产环境需要正式许可证。
- **可以将结果保存为 TIFF 吗？** 可以，我们将使用 `TiffOptions` 导出处理后的图像。
- **代码运行时间多久？** 对于标准大小的 PSD 文件，通常在一秒以内。

## 什么是对比度调整？
对比度调整会修改图像的色调范围，放大明暗区域之间的区别。这在扫描后图像显得平淡或在为印刷准备图形时尤为有用。

## 为什么选择 Aspose.PSD for Java？
- **丰富的格式支持** – 打开、编辑并保存 PSD、TIFF、PNG、JPEG 等多种格式。
- **高性能** – 缓存和光栅图像优化降低内存开销。
- **简洁的 API** – 像 `adjustContrast` 这样的单方法调用让代码易读。

## 前置条件

在开始之前，请确保你已经具备：

- 基本的 Java 编程知识。
- 已安装 Aspose.PSD for Java 库。你可以在此处下载 [here](https://releases.aspose.com/psd/java/)。

## 导入包

在你的 Java 类中添加所需的导入：

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
```

我们将源 PSD 文件（`sample.psd`）加载到 `Image` 对象中，这个对象是后续所有处理的入口。

## 步骤 2：转换为 RasterImage 并缓存数据

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

将对象强制转换为 `RasterImage` 可以让我们进行像素级操作。缓存可以提升性能，尤其是处理大文件时。

## 如何调整图像对比度

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 方法接受一个表示百分比变化的整数。在本例中，我们将对比度提升 **50 %**。

## 使用 Aspose.PSD 将 PSD 转换为 TIFF

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

这里我们配置 `TiffOptions`（每样本位数、光度解释），并将增强对比度后的图像写入 TIFF 文件。

## 常见问题及解决方案
- **图像未缓存：** 对于大型 PSD，请始终调用 `cacheData()`，以避免 `OutOfMemoryError`。
- **颜色意外偏移：** 确认 `setPhotometric` 与目标色彩空间（RGB 与 CMYK）匹配。
- **文件未找到：** 确保 `dataDir` 指向正确的文件夹，并且文件名拼写无误。

## 常见问答

### Q1: Aspose.PSD 是否兼容不同的图像格式？

A1: 是的，Aspose.PSD 支持多种图像格式，为你的项目提供灵活性。

### Q2: 如何获取 Aspose.PSD 的临时许可证？

A2: 你可以在此处获取临时许可证 [here](https://purchase.aspose.com/temporary-license/)。

### Q3: 在哪里可以找到 Aspose.PSD 文档？

A3: 文档可在此处查看 [here](https://reference.aspose.com/psd/java/)。

### Q4: Aspose.PSD 提供哪些支持选项？

A4: 如需支持，请访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)。

### Q5: 我可以购买 Aspose.PSD 吗？

A5: 可以，你可以在此处购买 [here](https://purchase.aspose.com/buy)。

## 结论

现在你已经了解 **如何使用 Aspose.PSD for Java 调整 PSD 图像的对比度**，以及 **如何将 PSD 转换为 TIFF** 以进行后续处理。这些步骤让你能够细粒度地控制图像质量，同时保持代码简洁易维护。欢迎尝试其他图像调整方法，如 `adjustBrightness` 或 `adjustGamma`，以满足你的特定需求。

---

**最后更新：** 2025-12-21  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}